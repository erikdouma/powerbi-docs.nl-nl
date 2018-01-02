---
title: Sjablooninhoudspakketten ontwerpen in Power BI
description: Sjablooninhoudspakket ontwerpen
services: powerbi
documentationcenter: 
author: guyinacube
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
ms.date: 10/09/2017
ms.author: asaxton
ms.openlocfilehash: 332b8eb7087bbf70559a1e63b0736c9cb9289349
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/15/2017
---
# <a name="author-template-content-packs-in-power-bi"></a>Sjablooninhoudspakketten ontwerpen in Power BI
Bij het ontwerpen van een sjablooninhoudspakket maakt u gebruik van Power BI Desktop en PowerBI.com. Uw inhoudspakket bestaat uit vier onderdelen:

* Met query’s kunt u [verbinding](../desktop-connect-to-data.md)maken met de gegevens en deze [transformeren](../desktop-query-overview.md), en [parameters](https://powerbi.microsoft.com/blog/deep-dive-into-query-parameters-and-power-bi-templates/) definiëren  
* Gegevensmodel voor het maken van [relaties](../desktop-create-and-manage-relationships.md), [metingen](../desktop-measures.md) en Q&A-verbeteringen  
* Rapport[pagina's](../desktop-report-view.md) bevatten visuele elementen en filters waarmee u inzicht kunt krijgen in uw gegevens  
* [Dashboard](../service-dashboards.md) en [tegels](../service-dashboard-create.md) bieden een overzicht van de inzichten die zijn opgenomen  

U kent deze onderdelen mogelijk al als bestaande functies van Power BI. Bij het maken van een inhoudspakket moet u voor elk aspect rekening houden met extra dingen. Zie de onderstaande secties voor meer informatie.

<a name="queries"></a>

## <a name="queries"></a>Query's
In sjablooninhoudspakketten worden in Power BI Desktop ontwikkelde query’s gebruikt om verbinding maken met uw gegevensbron en gegevens te importeren. Deze query's zijn vereist om een consistent schema te retourneren, en worden ondersteund voor de geplande gegevensvernieuwing (directe query wordt niet ondersteund).

Sjablooninhoudspakketten ondersteunen maar één gegevensbron per inhoudspakket; definieer uw query’s dus zorgvuldig. Eén gegevensbron wordt gedefinieerd als een bron die de dezelfde verificatie vereist. U kunt meerdere API-aanroepen doen in verschillende query's, als alle aanroepen naar hetzelfde API-eindpunt gaan en de dezelfde verificatie gebruiken. Power BI-inhoudspakketten bieden geen ondersteuning voor meerdere bronnen waarvoor verschillende verificaties nodig zijn.

### <a name="connect-to-your-api"></a>Verbinding maken met uw API
Voordat u kunt beginnen met het samenstellen van query’s, moet u vanuit Power BI Desktop verbinding maken met uw API.

U kunt gebruikmaken van de gegevensconnectors die standaard in Power BI Desktop beschikbaar zijn om verbinding te maken met uw API. U kunt de webgegevensconnector (Gegevens ophalen -> Web) gebruiken om verbinding te maken met uw REST API of de OData-verbinding (Gegevens ophalen -> OData-feed) om verbinding te maken met de OData-feed. Houd er rekening mee dat deze connectors standaard alleen werken als uw API ondersteuning biedt voor basisverificatie.

> [!NOTE]
> Als uw API gebruikmaakt van andere verificatietypen, zoals OAuth 2.0 of Web-API-sleutel, moet u uw eigen gegevensconnector ontwikkelen zodat Power BI Desktop verbinding kan maken met uw API en kan worden geverifieerd. Raadpleeg voor meer informatie over het ontwikkelen van een eigen gegevensconnector voor uw inhoudspakket [deze](https://aka.ms/DataConnectors) documentatie over gegevensconnectors. 
> 
> 

### <a name="consider-the-source"></a>Houd rekening met de bron
De query's definiëren de gegevens die worden opgenomen in het gegevensmodel. Afhankelijk van de grootte van uw systeem, moeten deze query's ook filters bevatten om ervoor te zorgen dat uw klanten een handelbare hoeveelheid gegevens krijgen die past in uw bedrijfsscenario.

Power BI-inhoudspakketten kunnen meerdere query's parallel en voor meerdere gebruikers tegelijk uitvoeren.  Plan uw strategie voor bandbreedtebeperking en gelijktijdigheid vooruit, en vraag ons hoe u uw inhoudspakket fouttolerant kunt maken.

### <a name="schema-enforcement"></a>Schema afdwingen
Zorg ervoor dat uw query’s bestand zijn tegen veranderingen in uw systeem. Wijzigingen in het schema bij vernieuwen kunnen het model breken. Als de bron een null- of ontbrekend schemaresultaat kan retourneren voor sommige query's, kunt u overwegen een lege tabel te retourneren of een aangepaste foutmelding weer te geven die zinvol is voor uw gebruiker.

### <a name="parameters"></a>Parameters
[Parameters](https://powerbi.microsoft.com/blog/deep-dive-into-query-parameters-and-power-bi-templates/) in Power BI Desktop maken het uw gebruikers mogelijk invoerwaarden op te geven waarmee de gebruiker de opgehaalde waarden kan aanpassen. Bedenk van tevoren welke parameters u nodig hebt, om te voorkomen dat u dingen over moet doen nadat u al tijd hebt gestoken in het opbouwen van gedetailleerde query’s of rapporten.

> [!NOTE]
> Sjablooninhoudspakketten ondersteunen momenteel alleen tekstparameters. Er kunnen andere parametertypen worden gebruikt tijdens de ontwikkeling, maar tijdens het [test](template-content-pack-testing.md#templates)gedeelte zijn alle waarden die door gebruikers worden opgegeven letterlijke waarden.
> 
> 

### <a name="additional-query-tips"></a>Meer querytips
* Zorg ervoor dat alle kolommen het juiste gegevenstype hebben  
* Kolommen hebben een informatieve naam (zie Q&A)  
* Overweeg het gebruik van functies of query's voor gedeelde logica  
* Privacyniveaus worden momenteel niet ondersteund in de service - als u een prompt krijgt over privacyniveaus, moet u de query mogelijk zo herschrijven dat relatieve paden worden gebruikt  

## <a name="data-model"></a>Gegevensmodel
Een goed gedefinieerd gegevensmodel zorgt ervoor dat uw klanten gemakkelijk en intuïtief met het inhoudspakket kunnen communiceren. Maak het gegevensmodel in Power BI Desktop.

> [!NOTE]
> Een groot deel van de basismodellering (typen, kolomnamen) moet worden uitgevoerd in de [query's](#queries).
> 
> 

### <a name="qa"></a>Q&A
De modellering is ook van invloed op hoe goed de Q&A-resultaten voor uw klanten zijn. Zorg ervoor dat u synoniemen toevoegt voor veelgebruikte kolommen, en dat uw kolommen de juiste namen hebben in de [query's](#queries).

### <a name="additional-data-model-tips"></a>Meer tips voor gegevensmodellen
* Op alle waardekolommen wordt opmaak toegepast
    >[!NOTE]
    >Typen moeten worden toegepast in de query.  
* Op alle metingen wordt opmaak toegepast  
* Standaardsamenvatting is ingesteld. Met name 'Niet samenvatten', indien van toepassing (bijvoorbeeld voor unieke waarden)  
* Gegevenscategorie is ingesteld, indien van toepassing  
* Relaties zijn ingesteld waar nodig  

## <a name="reports"></a>Rapporten
De rapportpagina's bieden meer inzicht in de gegevens die zijn opgenomen in uw inhoudspakket. Gebruik de pagina's van de rapporten om de belangrijkste zakelijke vragen te beantwoorden waarvoor uw inhoudspakket is bedoeld. Maak het rapport met behulp van Power BI Desktop.

> [!NOTE]
> Er kan maar één rapport worden opgenomen in een inhoudspakket. Maak gebruik van de verschillende pagina’s om bepaalde secties van uw scenario te belichten.
> 
> 

### <a name="additional-report-tips"></a>Meer rapporttips
* Gebruik meer dan één visualisatie per pagina voor kruislings filteren  
* Lijn de visuele elementen zorgvuldig uit (geen overlapping)  
* Pagina is ingesteld op'4:3'- of '16:9'-modus voor lay-out  
* Alle gepresenteerde aggregaties zijn zinnige getallen (gemiddelden, unieke waarden)  
* Segmentering produceert rationele resultaten  
* Logo is aanwezig op ten minste het bovenste rapport  
* Elementen zijn zoveel mogelijk in het kleurenschema van de client  

<a name="dashboard"></a>

## <a name="dashboard"></a>Dashboard
Het dashboard is voor uw klanten het belangrijkste interactiepunt met uw inhoudspakket. Het moet een overzicht bevatten van de opgenomen inhoud, met name van de belangrijke metrische gegevens voor uw bedrijfsscenario.

Voor het maken van een dashboard voor uw sjablooninhoudspakket uploadt u uw PBIX via Gegevens ophalen > Bestanden of publiceert u rechtstreeks vanuit Power BI Desktop.

> [!NOTE]
> Voor sjablooninhoudspakketten is momenteel één rapport en gegevensset per inhoudspakket vereist. Maak geen inhoud van meerdere rapporten of gegevenssets vast aan het dashboard dat in het inhoudspakket wordt gebruikt.
> 
> 

### <a name="additional-dashboard-tips"></a>Meer dashboardtips
* Behoud hetzelfde thema bij het vastmaken, zodat de tegels op uw dashboard consistent zijn  
* Maak een logo vast aan het thema, zodat gebruikers weten waar het pakket van afkomstig is  
* De voorgestelde indeling die werkt met de meeste schermresoluties is 5 tot 6 kleine tegels breed  
* Alle dashboardtegels moeten geschikte titels/ondertitels hebben  
* Overweeg verticale of horizontale groeperingen te maken in het dashboard voor verschillende scenario’s  

<a name="restrictions"></a>

## <a name="summary-of-restrictions"></a>Overzicht van beperkingen
Zoals vermeld in de bovenstaande secties, hebben sjablooninhoudspakketten momenteel een aantal beperkingen:  

| Ondersteund | *Niet ondersteund* |
| --- | --- |
| Gegevenssets die zijn gemaakt in PBI Desktop |*Gegevenssets uit andere inhoudspakketten of invoer zoals Excel-bestanden* |
| Gegevensbron ondersteund voor via de cloud geplande gegevensvernieuwing |*Directe query of on-premises connectiviteit wordt niet ondersteund* |
| Query's retourneren een consistent schema of fouten indien van toepassing |*Dynamische of aangepaste schema's* |
| Eén gegevensbron per gegevensset |*Meerdere gegevensbronnen zoals mashups of URL's die worden gedetecteerd als meerdere gegevensbronnen* |
| Parameters van het type tekst |*Andere parametertypen (zoals datum) of 'lijst met toegestane waarden'* |
| Eén dashboard, rapport en gegevensset |*Meerdere dashboards, rapporten of gegevenssets* |

## <a name="next-step"></a>Volgende stap
[Inhoudspakket testen en verzenden](template-content-pack-testing.md)

