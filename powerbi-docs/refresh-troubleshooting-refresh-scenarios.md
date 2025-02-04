---
title: Problemen met vernieuwingsscenario's oplossen
description: Problemen met vernieuwingsscenario's oplossen
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 11/28/2018
ms.author: davidi
LocalizationGroup: Data refresh
ms.openlocfilehash: 8535787cb66ad2dc897ff3a3e4ecaccddfaa80f0
ms.sourcegitcommit: c8c126c1b2ab4527a16a4fb8f5208e0f7fa5ff5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2019
ms.locfileid: "54285111"
---
# <a name="troubleshooting-refresh-scenarios"></a>Problemen met vernieuwingsscenario's oplossen
Hier vindt u informatie over de verschillende scenario's die zich kunnen voordoen bij het vernieuwen van gegevens in de Power BI-service.

> [!NOTE]
> Als u een situatie tegenkomt die hieronder niet wordt vermeld en die problemen veroorzaakt, kunt u om hulp vragen op de [site van de community](http://community.powerbi.com/) of een [ondersteuningsticket](https://powerbi.microsoft.com/support/) aanmaken.
> 
> 

## <a name="refresh-using-web-connector-doesnt-work-properly"></a>Vernieuwen via web-connector werkt niet goed
Als u een script voor een web-connector hebt dat gebruikmaakt van de functie [**Web.Page**](https://msdn.microsoft.com/library/mt260924.aspx), en u de gegevensset of het rapport hebt bijgewerkt na 18 november 2016, moet u een gateway gebruiken om vernieuwing goed te laten werken.

## <a name="unsupported-data-source-for-refresh"></a>Gegevensbron waarvoor vernieuwen niet wordt ondersteund
Bij het configureren van een gegevensset kan er een foutbericht worden weergegeven met de melding dat de gegevensset een niet-ondersteunde gegevensbron gebruikt voor het vernieuwen. Zie [Troubleshooting unsupported data source for refresh](service-admin-troubleshoot-unsupported-data-source-for-refresh.md) (Probleem met niet-ondersteunde gegevensbron oplossen) voor meer informatie.

## <a name="dashboard-doesnt-reflect-changes-after-refresh"></a>Dashboard bevat geen wijzigingen na vernieuwen
Wacht ongeveer 10-15 minuten totdat de vernieuwde gegevens zijn doorgevoerd in de dashboardtegels.  Als de wijzigingen dan nog steeds niet zichtbaar zijn, maakt u de visualisatie opnieuw vast aan het dashboard.

## <a name="gatewaynotreachable-when-setting-credentials"></a>Foutbericht GatewayNotReachable bij instellen van referenties
Het foutbericht GatewayNotReachable kan worden weergegeven als u referenties instelt voor een gegevensbron. Dit kan het gevolg zijn van een verouderde gateway.  Installeer de nieuwste versie van de gateway en probeer het opnieuw.

## <a name="processing-error-the-following-system-error-occurred-type-mismatch"></a>Verwerkingsfout: De volgende systeemfout is opgetreden: Type komt niet overeen
Dit kan een probleem zijn met uw M-script in het Power BI Desktop-bestand of de Excel-werkmap.  De fout kan ook worden veroorzaakt door een verouderde versie van Power BI Desktop.

## <a name="tile-refresh-errors"></a>Fouten bij vernieuwen van tegels
Zie [Troubleshooting tile errors](refresh-troubleshooting-tile-errors.md) (Problemen met tegelfouten oplossen) voor een lijst van fouten die kunnen optreden met dashboardtegels, plus een beschrijving.

## <a name="refresh-fails-when-updating-data-from-sources-that-use-aad-oauth"></a>Vernieuwing mislukt bij het bijwerken van gegevens uit bronnen die OAuth AAD gebruiken
Het OAuth-token van Azure Active Director (**AAD**), dat wordt gebruikt door veel verschillende gegevensbronnen, verloopt over ongeveer één uur. Er zijn situaties mogelijk waarin het laden van gegevens langer duurt dan de geldigheidsduur van het token (meer dan één uur), omdat de Power BI-service maximaal twee uur wacht bij het laden van gegevens. In dit geval kan het laden van de gegevens mislukken met een fout.

**Microsoft Dynamics CRM Online** en **SharePoint Online** (SPO) zijn voorbeelden van gegevensbronnen die AAD OAuth gebruiken. Als u verbinding maakt met deze gegevensbronnen en het laden van gegevens langer duurt dan een uur, kan dit de reden zijn.

Microsoft werkt aan een oplossing waarmee het token tijdens het laden van de gegevens kan worden vernieuwd. Als uw exemplaar van Dynamics CRM Online of SharePoint Online (of een andere gegevensbron die AAD OAuth gebruikt) echter zo groot is dat deze de drempelwaarde van twee uur kan overschrijden, kan er ook een time-out optreden voor het laden van gegevens vanuit de Power BI-service.

Als u verbinding maakt met een gegevensbron van **SharePoint Online** met behulp van AAD OAuth, is een andere vereiste dat u het account gebruikt waarmee u zich aanmeldt bij de **Power BI-service**.

## <a name="uncompressed-data-limits-for-refresh"></a>Limieten voor niet-gecomprimeerde gegevens bij vernieuwen
De maximale grootte voor gegevenssets die worden geïmporteerd in de **Power BI-service** is 1 GB. Deze gegevenssets zijn sterk gecomprimeerd om goede prestaties te garanderen. Bij gedeelde capaciteit is het bovendien zo dat de service een limiet van 10 GB plaatst op de hoeveelheid niet-gecomprimeerde gegevens die tijdens het vernieuwen wordt verwerkt. Bij deze limiet wordt rekening gehouden met de compressie en is daarom veel hoger dan 1 GB. Gegevenssets in Power BI Premium vallen niet onder deze limiet. Als vernieuwing in Power BI-service om deze reden mislukt, verkleint u de hoeveelheid gegevens die worden geïmporteerd in Power BI en probeert u het opnieuw.

## <a name="scheduled-refresh-timeout"></a>Time-out bij geplande vernieuwing
Er wordt een time-out van twee uur gehanteerd voor de geplande vernieuwing van geïmporteerde gegevenssets. Deze time-out is vijf uur voor gegevenssets in **Premium**-werkruimten. Als deze limiet wordt bereikt, kunt u proberen om de gegevensset kleiner of minder complex te maken. Een andere optie is om de gegevensset op te splitsen in kleinere delen.

## <a name="access-to-the-resource-is-forbidden"></a>Toegang tot de resource is verboden  
Deze fout kan optreden vanwege verlopen referenties in het cachegeheugen. Meld u aan bij Power BI en ga naar https://app.powerbi.com?alwaysPromptForContentProviderCreds=true om de cache van uw internetbrowser te wissen. Hierdoor dwingt u een update van uw referenties af. 
    
    
## <a name="data-refresh-failure-because-of-password-change-or-expired-credentials"></a>Fout bij gegevens vernieuwen vanwege gewijzigd wachtwoord of verlopen referenties 
Gegevens vernieuwen kan ook mislukken vanwege verlopen referenties in het cachegeheugen. Meld u aan bij Power BI en ga naar https://app.powerbi.com?alwaysPromptForContentProviderCreds=true om de cache van uw internetbrowser te wissen. Hierdoor dwingt u een update van uw referenties af.


## <a name="next-steps"></a>Volgende stappen
[Gegevens vernieuwen](refresh-data.md)  
[Problemen met de on-premises gegevensgateway oplossen](service-gateway-onprem-tshoot.md)  
[Problemen met Power BI Gateway - Personal oplossen](service-admin-troubleshooting-power-bi-personal-gateway.md)  

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

