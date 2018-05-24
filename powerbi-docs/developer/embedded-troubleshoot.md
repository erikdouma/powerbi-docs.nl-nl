---
title: Problemen oplossen met uw ingesloten toepassing
description: In dit artikel worden enkele veelvoorkomende problemen besproken die kunnen optreden tijdens het insluiten van inhoud uit Power BI.
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-developer
ms.topic: conceptual
ms.date: 04/23/2018
ms.author: maghan
ms.openlocfilehash: 2108d8fc290a5af568a3e06ae5986e82413b680b
ms.sourcegitcommit: 638de55f996d177063561b36d95c8c71ea7af3ed
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/17/2018
---
# <a name="troubleshooting-your-embedded-application"></a>Problemen oplossen met uw ingesloten toepassing

In dit artikel worden enkele veelvoorkomende problemen besproken die kunnen optreden tijdens het insluiten van inhoud uit Power BI.

## <a name="tools-for-troubleshooting"></a>Hulpprogramma's voor het oplossen van problemen

### <a name="fiddler-trace"></a>Traceren met Fiddler

[Fiddler](http://www.telerik.com/fiddler) is een gratis hulpprogramma van Telerik waarmee u het HTTP-verkeer kunt controleren.  U kunt hiermee het verkeer tussen de Power BI API's en de clientcomputer bekijken. Het programma kan fouten en verwante informatie weergeven.

![Traceren met Fiddler](../includes/media/gateway-onprem-tshoot-tools-include/fiddler.png)

### <a name="f12-in-browser-for-front-end-debugging"></a>F12 in de browser voor front-endfoutopsporing

Met F12 wordt het ontwikkelvenster in uw browser weergegeven. Hier kunt u onder andere informatie over het netwerkverkeer bekijken.

![Fouten opsporen in de browser met F12](media/embedded-troubleshoot/browser-f12.png)

### <a name="extracting-error-details-from-power-bi-response"></a>Foutdetails extraheren uit het Power BI-antwoord

Dit codefragment laat zien hoe u de foutdetails van de HTTP-uitzondering kunt extraheren:

```
public static string GetExceptionText(this HttpOperationException exc)
{
    var errorText = string.Format("Request: {0}\r\nStatus: {1} ({2})\r\nResponse: {3}",
    exc.Request.Content, exc.Response.StatusCode, (int)exc.Response.StatusCode, exc.Response.Content);
    if (exc.Response.Headers.ContainsKey("RequestId"))
    {
        var requestId = exc.Response.Headers["RequestId"].FirstOrDefault();
        errorText += string.Format("\r\nRequestId: {0}", requestId);
    }

    return errorText;
}
```
Het is raadzaam om de aanvraag-id's (en foutdetails voor probleemoplossing) in een logboek te registreren.
Geef de aanvraag-id op als u contact opneemt met Microsoft Ondersteuning.

## <a name="app-registration"></a>App-registratie

**App-registratiefout**

Er wordt in de foutberichten in Azure Portal of op de Power BI-pagina voor het registreren van apps aangegeven dat u over onvoldoende bevoegdheden beschikt. Als u een toepassing wilt registreren, moet u een beheerder van de Azure AD-tenant zijn of moet de functie voor toepassingsregistraties door niet-beheerders zijn ingeschakeld.

**De Power BI-service wordt weergegeven in Azure Portal tijdens het registreren van een nieuwe app**

Er moet ten minste één gebruiker zijn aangemeld voor Power BI. Als de **Power BI-service** niet in de API-lijst wordt vermeld, is er geen gebruiker aangemeld voor Power BI.

## <a name="rest-api"></a>REST API

**De API-aanroep retourneert fout 401**

Mogelijk is er een Fiddler-opname nodig om het probleem nader te onderzoeken. Het vereiste machtigingsbereik voor de geregistreerde toepassing ontbreekt mogelijk in Azure AD. Controleer of het vereiste bereik aanwezig is in de app-registratie voor Azure AD in Azure Portal.

**De API-aanroep retourneert fout 403**

Mogelijk is er een Fiddler-opname nodig om het probleem nader te onderzoeken. Er kunnen verschillende reden zijn voor een 403-fout.

* De gebruiker heeft de hoeveelheid insluittokens overschreden die voor een gedeelde capaciteit kan worden gemaakt. U moet Azure-capaciteit aanschaffen als u insluittokens wilt genereren, en de werkruimte vervolgens aan die capaciteit toewijzen. Zie [Create Power BI Embedded capacity in the Azure portal](https://docs.microsoft.com/en-us/azure/power-bi-embedded/create-capacity) (Power BI Embedded-capaciteit maken in Azure Portal).
* Het Azure AD-verificatietoken is verlopen.
* De geverifieerde gebruiker is geen lid van de groep (app-werkruimte).
* De geverifieerde gebruiker is geen beheerder van de groep (app-werkruimte).
* De autorisatie-header wordt mogelijk niet correct vermeld. Controleer deze op spelfouten.

De back-end van de toepassing moet het verificatietoken mogelijk vernieuwen voordat GenerateToken wordt aangeroepen.

```
    GET https://wabi-us-north-central-redirect.analysis.windows.net/metadata/cluster HTTP/1.1
    Host: wabi-us-north-central-redirect.analysis.windows.net
    ...
    Authorization: Bearer eyJ0eXAiOi...
    ...
 
    HTTP/1.1 403 Forbidden
    ...
     
    {"error":{"code":"TokenExpired","message":"Access token has expired, resubmit with a new access token"}}
```

**Het token wordt niet gegeneerd wanneer de effectieve identiteit wordt opgegeven**

GenerateToken kan om enkele verschillende redenen mislukken wanneer de effectieve identiteit wordt opgegeven.

* De gegevensset ondersteunt de effectieve identiteit niet.
* De gebruikersnaam is niet opgegeven.
* Er is geen rol niet opgegeven.
* DatasetId is niet opgegeven.
* Gebruiker beschikt niet over de juiste machtigingen.

Probeer het volgende om te controleren wat de reden is.

* Voer de [gegevensset](https://msdn.microsoft.com/library/mt784653.aspx) uit. Staat de eigenschap IsEffectiveIdentityRequired in gesteld op true (waar)?
* Voor elke EffectiveIdentity moet een gebruikersnaam worden opgegeven.
* Staat IsEffectiveIdentityRolesRequired in gestel op true (waar) en er dus een rol is vereist.
* DatasetId is verplicht voor elke EffectiveIdentity.
* Voor Analysis Services moet de hoofdgebruiker een gatewaybeheerder zijn.

## <a name="data-sources"></a>Gegevensbronnen

**De ISV wil andere referenties voor dezelfde gegevensbron hebben**

Een gegevensbron kan één set referenties voor één hoofdgebruiker hebben. Als u andere referenties moet gebruiken, maakt u aanvullende hoofdgebruikers. Vervolgens wijst u de andere referenties voor elk van de hoofdgebruikers toe en sluit u ze in met het Azure AD-token van de desbetreffende gebruiker.

## <a name="content-rendering"></a>Inhoud weergeven

**De ingesloten inhoud kan niet worden weergegeven of er treedt een time-out op** 

Controleer of het insluitingstoken is verlopen. Controleer de vervaldatum van het insluitingstoken en vernieuw het token. Zie [Refresh token using JavaScript SDK](https://github.com/Microsoft/PowerBI-JavaScript/wiki/Refresh-token-using-JavaScript-SDK-example) (Token vernieuwen met de JavaScript-SDK) voor meer informatie.

**Het rapport of het dashboard wordt niet geladen**

Als de gebruiker het rapport of het dashboard niet ziet, controleert u of het rapport of het dashboard correct wordt geladen in powerbi.com. Het rapport of het dashboard werkt niet in uw toepassing als het niet worden geladen in powerbi.com.

**Het rapport of het dashboard presteert traag**

Open het bestand vanuit Power BI Desktop, of in powerbi.com, om te controleren of de prestaties acceptabel zijn. Zodoende kunt u problemen met uw toepassing of de API voor insluiten uitsluiten.

Zie [Veelgestelde vragen over Power BI Embedded](embedded-faq.md) voor meer informatie.

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)