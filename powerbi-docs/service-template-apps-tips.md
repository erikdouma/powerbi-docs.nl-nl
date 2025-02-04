---
title: Tips voor het ontwerpen van sjabloon-apps in Power BI (preview-versie)
description: Tips over het opstellen van query's, gegevensmodellen, rapporten en dashboards voor goede sjabloon-apps
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 02/05/2019
ms.author: maggies
ms.openlocfilehash: 282638c7c1c8a60ee93292602766d63fd0fe436e
ms.sourcegitcommit: 8207c9269363f0945d8d0332b81f1e78dc2414b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/14/2019
ms.locfileid: "56249679"
---
# <a name="tips-for-authoring-template-apps-in-power-bi-preview"></a>Tips voor het ontwerpen van sjabloon-apps in Power BI (preview-versie)

Wanneer u [uw sjabloon-app ontwerpt](service-template-apps-create.md) in Power BI, maakt en test u de werkruimte en brengt u deze in productie. Een ander belangrijk onderdeel is het ontwerpen van het rapport en het dashboard. Het ontwerpproces kan in vier hoofdonderdelen worden opgesplitst. Voor de beste sjabloon-app werkt u de volgende onderdelen af:

* Met **query's** kunt u [verbinding maken](desktop-connect-to-data.md) met de gegevens en deze [transformeren](desktop-query-overview.md), en [parameters](https://powerbi.microsoft.com/blog/deep-dive-into-query-parameters-and-power-bi-templates/) definiëren. 
* In het **gegevensmodel** maakt u [relaties](desktop-create-and-manage-relationships.md), [metingen](desktop-measures.md) en Q&A-verbeteringen.  
* **[Rapportpagina's](desktop-report-view.md)** bevatten visuals en filters waarmee u inzicht kunt krijgen in uw gegevens.  
* **[Dashboards](consumer/end-user-dashboards.md)** en [tegels](service-dashboard-create.md) bieden een overzicht van de inzichten die zijn opgenomen.  

U kent deze onderdelen mogelijk al als bestaande functies van Power BI. Bij het maken van een sjabloon-app moet u rekening houden met een aantal extra zaken. Zie de onderstaande secties voor meer informatie.

<a name="queries"></a>

## <a name="queries"></a>Query's
In sjabloon-apps worden in Power BI Desktop ontwikkelde query's gebruikt om verbinding te maken met uw gegevensbron en gegevens te importeren. Deze query's zijn vereist om een consistent schema te retourneren en worden ondersteund voor de geplande gegevensvernieuwing (DirectQuery wordt niet ondersteund).

### <a name="connect-to-your-api"></a>Verbinding maken met uw API
Voordat u kunt beginnen met het samenstellen van query's, moet u vanuit Power BI Desktop verbinding maken met uw API.

U kunt gebruikmaken van de gegevensconnectors die standaard in Power BI Desktop beschikbaar zijn om verbinding te maken met uw API. U kunt de webgegevensconnector (Gegevens ophalen -> Web) gebruiken om verbinding te maken met uw REST API of de OData-verbinding (Gegevens ophalen -> OData-feed) om verbinding te maken met de OData-feed. Deze connectors werken standaard alleen als uw API ondersteuning biedt voor basisverificatie.

> [!NOTE]
> Als uw API gebruikmaakt van andere verificatietypen, zoals OAuth 2.0 of Web-API-sleutel, moet u uw eigen gegevensconnector ontwikkelen zodat Power BI Desktop verbinding kan maken met uw API en kan worden geverifieerd. Raadpleeg de [documentatie over gegevensconnectors](https://aka.ms/DataConnectors) voor meer informatie over het ontwikkelen van een eigen gegevensconnector voor uw sjabloon-app. 
>
>

### <a name="consider-the-source"></a>Houd rekening met de bron
De query's definiëren de gegevens die zijn opgenomen in het gegevensmodel. Afhankelijk van de grootte van uw systeem, moeten deze query's ook filters bevatten om ervoor te zorgen dat uw klanten een handelbare hoeveelheid gegevens krijgen die past in uw bedrijfsscenario.

Power BI-sjabloon-apps kunnen meerdere query's parallel en voor meerdere gebruikers tegelijk uitvoeren.  Plan uw strategie voor bandbreedtebeperking en gelijktijdigheid vooruit, en vraag ons hoe u uw sjabloon-app fouttolerant kunt maken.

### <a name="schema-enforcement"></a>Schema afdwingen
Zorg ervoor dat uw query’s bestand zijn tegen veranderingen in uw systeem. Wijzigingen in het schema bij vernieuwen kunnen het model breken. Als de bron een null- of ontbrekend schemaresultaat kan retourneren voor sommige query's, kunt u overwegen een lege tabel te retourneren of een zinvolle aangepaste foutmelding weer te geven.

### <a name="parameters"></a>Parameters
[Parameters](https://powerbi.microsoft.com/blog/deep-dive-into-query-parameters-and-power-bi-templates/) in Power BI Desktop maken het uw gebruikers mogelijk invoerwaarden op te geven waarmee de gebruiker de opgehaalde waarden kan aanpassen. Bedenk van tevoren welke parameters u nodig hebt, om te voorkomen dat u dingen over moet doen nadat u al tijd hebt gestoken in het opbouwen van gedetailleerde query's of rapporten.

> [!NOTE]
> Sjabloon-apps ondersteunen alle parameters met uitzondering van Any en Binary.
>

### <a name="additional-query-tips"></a>Meer querytips

* Zorg ervoor dat de namen van kolommen juist zijn getypt.
* Kolommen hebben een informatieve naam (zie [Q&A](#qa)).  
* Overweeg het gebruik van functies of query's voor gedeelde logica.  
* Privacyniveaus worden momenteel niet ondersteund in de service. Als u een prompt krijgt over privacyniveaus, moet u de query mogelijk zo herschrijven dat relatieve paden worden gebruikt.  

## <a name="data-models"></a>Gegevensmodellen

Een goed gedefinieerd gegevensmodel zorgt ervoor dat uw klanten gemakkelijk en intuïtief met de sjabloon-app kunnen communiceren. Maak het gegevensmodel in Power BI Desktop.

> [!NOTE]
> Een groot deel van de basismodellering (typen, kolomnamen) moet worden uitgevoerd in de [query's](#queries).
>


### <a name="qa"></a>Q&A
De modellering is ook van invloed op hoe goed de Q&A-resultaten voor uw klanten zijn. Zorg ervoor dat u synoniemen toevoegt voor veelgebruikte kolommen, en dat uw kolommen de juiste namen hebben in de [query's](#queries).

### <a name="additional-data-model-tips"></a>Meer tips voor gegevensmodellen

Zorg ervoor dat u:
* Op alle waardekolommen opmaak hebt toegepast. Typen in de query hebt toegepast.  
* Op alle metingen opmaak hebt toegepast. 
* Een standaardsamenvatting hebt ingesteld. Met name 'Niet samenvatten', indien van toepassing (bijvoorbeeld voor unieke waarden).  
* De gegevenscategorie hebt ingesteld, indien van toepassing.  
* Relaties hebt ingesteld waar nodig.  

## <a name="reports"></a>Rapporten
De rapportpagina's bieden meer inzicht in de gegevens die zijn opgenomen in uw sjabloon-app. Gebruik de pagina's van de rapporten om de belangrijkste zakelijke vragen te beantwoorden waarvoor uw sjabloon-app is bedoeld. Maak het rapport met behulp van Power BI Desktop.

> [!NOTE]
> U kunt maar één rapport opnemen in een sjabloon-app. Maak gebruik van de verschillende pagina's om bepaalde secties van uw scenario te belichten.
>
>

### <a name="additional-report-tips"></a>Meer rapporttips

* Gebruik meer dan één visual per pagina voor kruislings filteren.  
* Lijn de visuals zorgvuldig uit (geen overlapping).  
* Pagina is ingesteld op '4:3'- of '16:9'-modus voor lay-out.  
* Alle gepresenteerde aggregaties zijn zinnige getallen (gemiddelden, unieke waarden).  
* Segmentering produceert rationele resultaten.  
* Logo is ten minste op het bovenste rapport aanwezig.  
* Elementen zijn zoveel mogelijk in het kleurenschema van de client.  

<a name="dashboard"></a>

## <a name="dashboards"></a>Dashboards
Het dashboard is voor uw klanten het belangrijkste interactiepunt met uw sjabloon-app. Het moet een overzicht bevatten van de opgenomen inhoud, met name van de belangrijke metrische gegevens voor uw bedrijfsscenario.

Voor het maken van een dashboard voor uw sjabloon-app uploadt u uw PBIX via Gegevens ophalen > Bestanden of publiceert u rechtstreeks vanuit Power BI Desktop.

> [!NOTE]
> Voor sjabloon-apps is momenteel één rapport en gegevensset per sjabloon-app vereist. Maak geen inhoud van meerdere rapporten of gegevenssets vast aan het dashboard dat in de sjabloon-app wordt gebruikt.
>
>

### <a name="additional-dashboard-tips"></a>Meer dashboardtips

* Behoud hetzelfde thema bij het vastmaken, zodat de tegels op uw dashboard consistent zijn.  
* Maak een logo vast aan het thema, zodat gebruikers weten waar het pakket van afkomstig is.  
* De voorgestelde indeling die werkt met de meeste schermresoluties is 5 tot 6 kleine tegels breed.  
* Alle dashboardtegels moeten geschikte titels/ondertitels hebben.  
* Overweeg verticale of horizontale groeperingen te maken in het dashboard voor verschillende scenario's.  

## <a name="known-limitations"></a>Bekende beperkingen

| Functie | Bekende beperking |
|---------|---------|
|Inhoud:  Gegevenssets   | Er moet exact één gegevensset aanwezig zijn. Alleen de gegevenssets die zijn ingebouwd in Power BI Desktop (.pbix-bestanden) zijn toegestaan. <br>Niet ondersteund: Gegevenssets uit andere sjabloon-apps, gegevenssets voor meerdere werkruimten, gepagineerde rapporten (.rdl-bestanden), Excel-werkmappen |
|Inhoud: Rapporten     | Maximaal één rapport    |
| Inhoud: Dashboards | Maximaal één niet-lege-dashboard <br>Niet ondersteund: Realtimetegels (met andere woorden, geen ondersteuning voor PushDataset of pubnub) |
| Inhoud: Gegevensstromen | Niet ondersteund: Gegevensstromen |
| Inhoud van bestanden | Alleen .pbix-bestanden worden ondersteund. <br>Niet ondersteund: .rdl-bestanden (gepagineerde rapporten), Excel-werkmappen   |
| Gegevensbronnen | Gegevensbronnen die worden ondersteund voor via de cloud geplande gegevensvernieuwing zijn toegestaan. <br>Niet ondersteund: <br>DirectQuery <br>Liveverbindingen (geen Azure AS) <br>On-premises gegevensbronnen (persoonlijke gateways en bedrijfsgateways worden niet ondersteund) <br>Realtime (geen ondersteuning voor PushDataset) <br>Samengestelde modellen |
| Gegevensset: voor meerdere werkruimten | Gegevenssets voor meerdere werkruimten zijn niet toegestaan  |
| Inhoud: Dashboards | Realtimetegels zijn niet toegestaan (met andere woorden, geen ondersteuning voor PushDataset of pubnub) |
| Queryparameters | Niet ondersteund: Parameters van het type Any of Binary blokkeren het vernieuwen van de gegevensset |
| Aangepaste visuals | Alleen de openbaar beschikbare aangepaste visuals worden ondersteund. [Aangepaste organisatievisuals](power-bi-custom-visuals-organization.md) niet ondersteund |

## <a name="next-steps"></a>Volgende stappen

[Wat zijn Power BI-sjabloon-apps? (preview-versie)](service-template-apps-overview.md)
