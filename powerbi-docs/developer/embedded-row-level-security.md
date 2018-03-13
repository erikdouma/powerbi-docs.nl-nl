---
title: Beveiliging op rijniveau met ingesloten Power BI-inhoud
description: Meer informatie over de stappen die u moet uitvoeren voor het insluiten van Power BI-inhoud in uw toepassing.
services: powerbi
documentationcenter: 
author: markingmyname
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 02/22/2018
ms.author: maghan
ms.openlocfilehash: 2dde59bba1c5d9ded1c82cf2dd1086be14f19304
ms.sourcegitcommit: d6e013eb6291ae832970e220830d9862a697d1be
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/23/2018
---
# <a name="use-row-level-security-with-power-bi-embedded-content"></a>Beveiliging op rijniveau met ingesloten Power BI-inhoud
Beveiliging op rijniveau (RLS) kan worden gebruikt om de gebruikerstoegang tot gegevens in dashboards, tegels, rapporten en gegevenssets te beperken. Meerdere gebruikers kunnen werken met dezelfde artefacten, terwijl ze allemaal verschillende gegevens zien. Het insluiten van inhoud biedt ondersteuning voor RLS.

Als u inhoud wilt insluiten voor niet-Power BI-gebruikers (app is eigenaar van de gegevens), een typisch ISV-scenario, is dit artikel van belang voor u. U moet het insluittoken zo configureren dat rekening wordt gehouden met de gebruiker en rol. Lees verder voor meer informatie over hoe u dit doet.

Als u inhoud wilt insluiten voor Power BI-gebruikers (gebruiker is eigenaar van de gegevens), werkt RLS hetzelfde als bij het rechtstreeks insluiten van inhoud in de Power BI-service. U hoeft verder niets te doen in uw toepassing. Zie [Beveiliging op rijniveau (RLS) met Power BI](../service-admin-rls.md) voor meer informatie.

![Items die betrokken zijn bij beveiliging op rijniveau.](media/embedded-row-level-security/powerbi-embedded-rls-components.png)

Om te kunnen profiteren van RLS, is het belangrijk dat u de drie hoofdbegrippen kent: gebruikers, rollen en regels. Laten we deze items eens nader bekijken:

**Gebruikers**: eindgebruikers die het artefact weergeven (dashboard, tegel, rapport of gegevensset). In Power BI Embedded worden gebruikers geïdentificeerd op basis van de eigenschap username (gebruikersnaam) in een insluittoken.

**Rollen**: gebruikers behoren tot rollen. Rollen zijn containers voor regels en kunnen namen hebben als *Verkoopmanager* of *Verkoper*. U maakt rollen in Power BI Desktop. Zie [Beveiliging op rijniveau (RLS) met Power BI Desktop](../desktop-rls.md) voor meer informatie.

**Regels**: rollen bevatten regels, en deze regels zijn de werkelijke filters die op de gegevens worden toegepast. Deze kunnen zo eenvoudig zijn als "Land = Nederland", maar ook veel ingewikkelder.
In de rest van dit artikel gebruiken we een voorbeeld van het ontwerp en gebruik van RLS binnen een ingesloten toepassing. Voor dit voorbeeld gebruiken we het PBIX-bestand [Voorbeeld van een retailanalyse](http://go.microsoft.com/fwlink/?LinkID=780547).

![Voorbeeldrapport](media/embedded-row-level-security/powerbi-embedded-report-example.png)

## <a name="adding-roles-with-power-bi-desktop"></a>Rollen toevoegen met Power BI Desktop
In het voorbeeld van een retailanalyse worden de verkoopcijfers voor alle winkels van een winkelketen weergegeven. Zonder RLS zou elke regiomanager die zich aanmeldt en het rapport weergeeft dezelfde gegevens zien. Het senior management heeft besloten dat elke regiomanager alleen de verkoopcijfers mag zien voor de winkels die ze beheren. Hiervoor kunnen we RLS gebruiken.

RLS is geschreven in Power BI Desktop. Na het openen van de gegevensset en het rapport kunnen we overschakelen naar de diagramweergave van het schema:

![Diagramweergave in Power BI Desktop](media/embedded-row-level-security/powerbi-embedded-schema.png)

We noemen enkele dingen die opvallen in dit schema:

* Alle metingen, zoals **Totale verkoop**, worden opgeslagen in de feitentabel **Verkoop**.
* Er zijn vier extra gerelateerde dimensietabellen: **Artikel**, **Tijd**, **Winkel** en **Regio**.
* Met de pijlen op de relatielijnen wordt aangegeven in welke richting filters van de ene naar de andere tabel kunnen stromen. Als er bijvoorbeeld een filter op **Tijd[Datum]** wordt toegepast in het huidige schema, worden alleen de waarden in de tabel **Verkoop** gefilterd. Andere tabellen worden niet beïnvloed door dit filter omdat alle pijlen op de relatielijnen naar de tabel Verkoop toe wijzen, en niet ervandaan.
* In de tabel **Regio** wordt de manager van elke regio aangegeven:
  
    ![Rijen in de tabel Regio](media/embedded-row-level-security/powerbi-embedded-district-table.png)

Als we in dit schema een filter toepassen op de kolom **Regiomanager** in de tabel **Regio**, en als dat filter overeenkomt met de gebruiker die het rapport weergeeft, worden in de tabellen **Winkel** en **Verkoop** alleen de gegevens voor die regiomanager weergegeven.

U doet dit als volgt:

1. Op het tabblad **Modellering** selecteert u **Rollen beheren**.
   
    ![Tabblad Modellering in Power BI Desktop](media/embedded-row-level-security/powerbi-embedded-manage-roles.png)
2. Maak een nieuwe rol met de naam **Manager**.
   
    ![Nieuwe rol maken](media/embedded-row-level-security/powerbi-embedded-new-role.png)
3. Voer in de tabel **Regio** de volgende DAX-expressie in: **[Regiomanager] = USERNAME()**.
   
    ![DAX-instructie voor RLS-regel](media/embedded-row-level-security/powerbi-embedded-new-role-dax.png)
4. Om te controleren of de regels correct functioneren, selecteert u op het tabblad **Modellering** **Als rollen weergeven**. Selecteer vervolgens de rol **Manager** die u zojuist hebt gemaakt, plus de rol **Andere gebruiker**. Voer **Andrew Ma** in als gebruiker.
   
    ![Dialoogvenster Als rollen weergeven](media/embedded-row-level-security/powerbi-embedded-new-role-view.png)
   
    In de rapporten worden de gegevens weergegeven alsof u bent aangemeld als **Andrew Ma**.

Door het filter toe te passen zoals we hier hebben gedaan, worden alle records in de tabellen **Regio**, **Winkel** en **Verkoop** gefilterd. Echter, vanwege de filterrichting van de relaties tussen **Verkoop** en **Tijd**, worden de tabellen **Verkoop** en **Artikel**, en **Artikel** en **Tijd** niet gefilterd. Download voor meer informatie over kruisfiltering in twee richtingen het technische document over [Kruisfiltering in twee richtingen in SQL Server Analysis Services 2016 en Power BI Desktop](http://download.microsoft.com/download/2/7/8/2782DF95-3E0D-40CD-BFC8-749A2882E109/Bidirectional%20cross-filtering%20in%20Analysis%20Services%202016%20and%20Power%20BI.docx).

## <a name="applying-user-and-role-to-an-embed-token"></a>Gebruiker en rol toepassen op een insluittoken
Nu de rollen in Power BI Desktop zijn geconfigureerd, moet u nog enig werk in de toepassing verrichten om van de rollen te kunnen profiteren.

Gebruikers worden geverifieerd en geautoriseerd door de toepassing, en insluittokens worden gebruikt om de betreffende gebruiker toegang te verlenen tot een specifiek Power BI Embedded-rapport. Power BI Embedded bevat geen specifieke informatie over de identiteit van de gebruiker. Voor de juiste werking van RLS moet u aanvullende contextgegevens bij insluittokens doorgeven in de vorm van identiteiten. Dit wordt gedaan met behulp van de API [GenerateToken](https://msdn.microsoft.com/library/mt784614.aspx).

De API [GenerateToken](https://msdn.microsoft.com/library/mt784614.aspx) accepteert een lijst identiteiten met vermelding van de relevante gegevenssets. Voor de juiste werking van RLS moet u het volgende doorgeven als onderdeel van de identiteit.

* **gebruikersnaam (verplicht)**: een tekenreeks die kan worden gebruikt om de identiteit van de gebruiker vast te stellen bij het toepassen van RLS-regels. Er kan slechts één gebruiker worden opgegeven.
* **rollen (verplicht)**: een tekenreeks met de rollen die kunnen worden geselecteerd bij het toepassen van de regels voor beveiliging op rijniveau. Als u meerdere rollen wilt doorgeven, moeten deze worden doorgegeven als een tekenreeksmatrix.
* **gegevensset (verplicht)**: de toepasselijke gegevensset voor het artefact dat u wilt insluiten. 

U kunt het insluittoken maken met behulp van de methode **GenerateTokenInGroup** in **PowerBIClient.Reports**. 

U kunt bijvoorbeeld het voorbeeld [PowerBIEmbedded_AppOwnsData](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/App%20Owns%20Data) wijzigen. *Home\HomeController.cs regel 76 en 77* kunnen worden gewijzigd van:

```
// Generate Embed Token.
var generateTokenRequestParameters = new GenerateTokenRequest(accessLevel: "view");

var tokenResponse = await client.Reports.GenerateTokenInGroupAsync(GroupId, report.Id, generateTokenRequestParameters);
```

in

```
var generateTokenRequestParameters = new GenerateTokenRequest("View", null, identities: new List<EffectiveIdentity> { new EffectiveIdentity(username: "username", roles: new List<string> { "roleA", "roleB" }, datasets: new List<string> { "datasetId" }) });

var tokenResponse = await client.Reports.GenerateTokenInGroupAsync("groupId", "reportId", generateTokenRequestParameters);
```

Als u de REST-API aanroept, accepteert de bijgewerkte API nu een extra JSON-matrix met de naam **identities** (identiteiten), met een gebruikersnaam, een tekenreeks met de lijst met rollen en een tekenreeks met de lijst met gegevenssets, bijvoorbeeld:

```
{
    "accessLevel": "View",
    "identities": [
        {
            "username": "EffectiveIdentity",
            "roles": [ "Role1", "Role2" ],
            "datasets": [ "fe0a1aeb-f6a4-4b27-a2d3-b5df3bb28bdc" ]
        }
    ]
}
```

Nu zijn alle benodigde onderdelen aanwezig. Als een gebruiker zich bij uw toepassing aanmeldt om dit artefact weer te geven, ziet deze alleen de gegevens die hij of zij mag zien, zoals gedefinieerd in de beveiliging op rijniveau.

## <a name="working-with-analysis-services-live-connections"></a>Werken met liveverbindingen van Analysis Services
Beveiliging op rijniveau kan worden gebruikt voor liveverbindingen van Analysis Services met on-premises servers. Als u dit type verbinding wilt gebruiken, moet u een aantal concepten goed kennen.

De effectieve identiteit die wordt opgegeven voor de eigenschap voor de gebruikersnaam, moet een Windows-gebruiker zijn met machtigingen voor de Analysis Services-server.

**Configuratie van on-premises gegevensgateway**

Voor liveverbindingen van Analysis Services wordt een [on-premises gegevensgateway](../service-gateway-onprem.md) gebruikt. Bij het genereren van een insluittoken, met een opgegeven identiteit, moet het hoofdaccount zijn opgegeven als beheerder van de gateway. Als het hoofdaccount niet is opgegeven, wordt de beveiliging op rijniveau niet correct toegepast op de gegevens. Een niet-beheerder van de gateway kan rollen opgeven, maar moet zijn eigen gebruikersnaam als effectieve identiteit opgeven.

**Gebruik van rollen**

Rollen kunnen worden opgegeven met de identiteit in een insluittoken. Als er geen rol wordt opgegeven, wordt de rollen herleid op basis van de opgegeven gebruikersnaam.

**De functie CustomData gebruiken**

Met de functie CustomData kunt u vrije tekst (tekenreeks) doorgeven met behulp van de eigenschap van de CustomData-verbindingsreeks, een waarde die via de functie CUSTOMDATA() door AS moet worden gebruikt.
U kunt de functie gebruiken als alternatieve manier voor het aanpassen van het gegevensverbruik.
De functie kan binnen de DAX-query voor rollen worden gebruikt en de functie kan zonder rol in de DAX-query voor metingen worden gebruikt.
De functie CustomData maakt deel uit van de functionaliteit voor het genereren van tokens voor de artefacten Dashboard, Rapport en Tegel. Dashboards kunnen over meerdere CustomData-identiteiten (één per tegel/model) beschikken.

> [!NOTE]
> De functie CustomData werkt alleen voor modellen die zich in Azure Analysis Services bevinden. Bovendien werkt de functie alleen in de livemodus. In tegenstelling tot gebruikers en rollen, kan de functie voor aangepaste gegevens niet in een PBIX-bestand worden ingesteld. Tijdens het genereren van een token met de functie voor aangepaste gegevens moet u over een gebruikersnaam beschikken.
>
>

**CustomData SDK - toevoegingen**

De eigenschap van de CustomData-tekenreeks is toegevoegd aan de effectieve identiteit in het scenario voor het genereren van tokens.
        
        [JsonProperty(PropertyName = "customData")]
        public string CustomData { get; set; }

Met behulp van de volgende aanroep kan de identiteit kan worden gemaakt met aangepaste gegevens:

        public EffectiveIdentity(string username, IList<string> datasets, IList<string> roles = null, string customData = null);

**CustomData SDK - gebruik**

Als u REST API aanroept, kunt u binnen elke identiteit aangepaste gegevens toevoegen, bijvoorbeeld:

```
{
    "accessLevel": "View",
    "identities": [
        {
            "username": "EffectiveIdentity",
            "roles": [ "Role1", "Role2" ],
            "customData": "MyCustomData",
            "datasets": [ "fe0a1aeb-f6a4-4b27-a2d3-b5df3bb28bdc" ]
        }
    ]
}
```

## <a name="considerations-and-limitations"></a>Overwegingen en beperkingen
* De toewijzing van gebruikers aan rollen in de Power BI-service heeft geen invloed op de beveiliging op rijniveau bij gebruik van een insluittoken.
* Wanneer u een identiteit met een insluittoken opgeeft, worden RLS-instellingen in de Power BI-service niet toegepast op beheerders of leden met machtigingen voor bewerken, maar op de gegevens.
* Liveverbindingen van Analysis Services worden ondersteund voor on-premises servers.
* Live verbindingen van Azure Analysis Services bieden ondersteuning voor het filteren op rollen, maar niet voor dynamische filteren op gebruikersnaam.
* Als RLS niet vereist is voor de onderliggende gegevensset, mag de GenerateToken-aanvraag **geen** effectieve identiteit bevatten.
* Als de onderliggende gegevensset een cloudmodel is (model in de cache of DirectQuery), moet de effectieve identiteit ten minste één rol bevatten. Anders wordt roltoewijzing niet uitgevoerd.
* Een lijst met identiteiten kan meerdere identiteitstokens insluiten in het dashboard. Voor alle andere artefacten bevat de lijst één identiteit.

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](https://community.powerbi.com/)