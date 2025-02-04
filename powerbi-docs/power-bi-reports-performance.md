---
title: Aanbevolen procedures voor de prestaties van Power BI
description: Dit artikel bevat informatie voor het snel maken van betrouwbare rapporten in Power BI
author: MarkMcGeeAtAquent
ms.author: kfile
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 05/18/2018
LocalizationGroup: Reports
ms.openlocfilehash: f603a733c6c604a89b0b9608904acdf13b66b713
ms.sourcegitcommit: c8c126c1b2ab4527a16a4fb8f5208e0f7fa5ff5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2019
ms.locfileid: "54287779"
---
# <a name="power-bi-performance-best-practices"></a>Aanbevolen procedures voor de prestaties van Power BI

Dit artikel biedt informatie voor het snel maken van betrouwbare rapporten in Power BI.  

## <a name="use-filters-to-limit-report-visuals-to-display-only-whats-needed"></a>Filters gebruiken om in rapporten alleen de benodigde visuals weer te geven 

Hoe meer gegevens via een visual moeten worden weergeven, hoe langzamer de visual wordt geladen. Hoewel dit principe duidelijk lijkt, wordt dit gemakkelijk vergeten. Voorbeeld: stel u eens voor dat u een grote gegevensset hebt. Hierop maakt u een rapport met een tabel van de tabel. Eindgebruikers gebruiken slicers op de pagina om de gewenste rijen weer te geven. Doorgaans zijn ze slechts in enkele tientallen rijen geïnteresseerd.

Vaak wordt de fout gemaakt dat de standaardweergave van de tabel niet wordt gefilterd, waardoor alle 100M+-rijen worden weergegeven. De gegevens voor deze rijen moeten in het geheugen worden geladen en bij elke vernieuwing worden gedecomprimeerd. Dit is een grote belasting op het geheugen. De oplossing: verklein het maximale aantal items dat in de tabel wordt weergegeven met behulp van het filter Top N. Het maximale aantal items kan vele malen groter zijn dan wat gebruikers nodig hebben, bijvoorbeeld 10.000. Als gevolg hiervan wordt de ervaring voor de eindgebruiker niet gewijzigd, maar wordt het geheugengebruik van het rapport vele malen verminderd en worden de prestaties aanzienlijk verbeterd.

Een soortgelijke benadering als hierboven beschreven, wordt aangeraden voor alle visuals in uw rapporten. Stel uzelf de vraag of alle gegevens in deze visual nodig zijn. Zijn er manieren om de hoeveelheid gegevens die worden weergegeven in de visual te filteren met minimale gevolgen voor de eindgebruiker? Houd er rekening mee dat met name tabellen kostbaar kunnen zijn.

## <a name="limit-visuals-on-report-pages"></a>Visuals op rapportpagina's beperken

Het bovenstaande principe is evenzeer van toepassing op het aantal visuals in een bepaald rapport. Het wordt ten zeerste aangeraden het aantal visuals in een bepaald rapport te beperken tot hetgeen noodzakelijk is. Drillthrough-pagina's vormen een uitstekende manier om meer informatie te bieden zonder nog meer visuals in het rapport te persen.  

## <a name="optimize-your-model"></a>Het model optimaliseren

Een aantal aanbevolen procedures:

- Tabellen of kolommen die niet worden gebruikt, moeten indien mogelijk worden verwijderd. 
- Vermijd afzonderlijke tellingen in velden met hoge kardinaliteit, dat wil zeggen met miljoenen afzonderlijke waarden.  
- Zorg ervoor dat u velden met onnodige details en hoge kardinaliteit vermijdt. U kunt bijvoorbeeld unieke waarden voor datum/tijd splitsen in afzonderlijke kolommen, bijvoorbeeld dag, maand, jaar enzovoort. Of gebruik, indien mogelijk, afronding voor velden met een hoge nauwkeurigheid om de kardinaliteit te verlagen (bijvoorbeeld 13,29889 -> 13,3).
- Gebruik waar mogelijk gehele getallen in plaats van tekenreeksen.
- Maak zo min mogelijk gebruik van DAX-functies die elke rij in een tabel moeten testen, zoals RANKX. In het ergste geval kunnen deze functies de runtime en geheugenvereisten exponentieel laten toenemen door de lineaire toename van de tabelgrootte.
- Bij het verbinden met gegevensbronnen via DirectQuery kunt u kolommen indexeren die vaak worden gefilterd of weer worden gesliced. Hierdoor neemt de reactiesnelheid van het rapport aanzienlijk toe.  

Zie [DirectQuery in SQL Server 2016 Analysis Services](https://blogs.msdn.microsoft.com/analysisservices/2017/04/06/directquery-in-sql-server-2016-analysis-services-whitepaper/) voor meer instructies voor het optimaliseren van gegevensbronnen voor DirectQuery.

## <a name="directquery-and-live-connection-understand-underlying-data-source-performance"></a>DirectQuery en Live-verbinding: inzicht in prestaties van onderliggende gegevensbronnen

Wanneer gebruikers in combinatie met DirectQuery of een liveverbinding een Power BI-rapport bekijken, stuurt Power BI in realtime query's naar de onderliggende gegevensbron. Het rapport wordt opgebouwd als de gegevensbron de querygegevens retourneert. Hierdoor zijn de rapportprestaties in dergelijke gevallen grotendeels afhankelijk van de prestaties van de onderliggende gegevensbron.

In deze gevallen is het belangrijk om inzicht te hebben in de prestaties van de onderliggende gegevensbron. Verschillende gegevensbronnen hebben verschillende hulpprogramma's voor inzicht in queryprestaties. SQL Server en Azure SQL bieden bijvoorbeeld de Query Store, waarin een geschiedenis van query's en hun runtime-statistieken worden vastgelegd.

Als vuistregel geldt dat u bij het implementeren van Power BI-rapporten die zijn gebaseerd op DirectQuery en live-verbindingen, moet proberen wat uw eindgebruikers in Power BI Desktop doen. Als het rapport langzaam wordt geladen in Power BI Desktop, zal het vrijwel zeker ook langzaam worden geladen in de service voor uw eindgebruikers. 

## <a name="directquery-best-practices"></a>Aanbevolen procedures voor DirectQuery

Het volgende gedeelte bevat algemene aanbevelingen voor het maken van een verbinding via DirectQuery.
  
### <a name="db-design-guidance"></a>Ontwerprichtlijnen voor DB

- Breng berekende kolommen en metingen waar mogelijk dichter naar de bron. Hoe dichter bij de bron, hoe hoger de kans op prestaties.
- Optimaliseer. Krijg inzicht in de uitvoering van voor uw query's, voeg indexen toe voor vaak gefilterde kolommen, enzovoort.

### <a name="modeling-guidance"></a>Richtlijnen voor modellering

- Start in Power BI Desktop.
- Vermijd complexe query's in Query-Editor.
- Gebruik geen relatieve datumfiltering in de Query-Editor.  
- Houd metingen in eerste instantie eenvoudig en voeg geleidelijk complexiteit toe.
- Vermijd relaties in berekende kolommen en kolommen met unieke id’s.
- Stel 'Uitgaan van referentiële integriteit' in voor relaties. Dit leidt in veel gevallen tot aanzienlijke verbeteringen in de queryprestaties.  

### <a name="general"></a>Algemeen

- Pas eerst filters toe.
- Overweeg het uitschakelen van interactie tussen visuals. Hierdoor wordt de querybelasting verminderd wanneer gebruikers kruislingse markeringen gebruiken.
- Beperk het aantal visuals en de gegevens per visual, zoals hierboven is beschreven.
- Als u beveiliging op rijniveau inschakelt, kan dit leiden tot belangrijke wijzigingen in de prestaties. Zorg ervoor dat u tests uitvoert voor de verschillende beveiligingsrollen op rijniveau die uw gebruikers krijgen.
- Houd er rekening mee dat er op queryniveau time-outs worden afgedwongen door de service om ervoor te zorgen dat langlopende query's niet alle beschikbare systeemresources in beslag nemen. Voor query's die langer duren dan 225 seconden, treedt een time-out op. Deze query’s resulteren in een fout op het niveau van de visual.

## <a name="understand-dashboards-and-query-caches"></a>Dashboards en querycaches begrijpen

Visuals die zijn vastgemaakt aan dashboards, worden afgehandeld door de querycache wanneer het dashboard wordt geladen. Wanneer u daarentegen een rapport opent, worden de query's direct uitgevoerd op de gegevensbron: ofwel Power BI-service (in het geval van importeren) of de door u opgegeven gegevensbron (in het geval van DirectQuery of live-verbinding).  

> [!NOTE]
> Wanneer u live-rapporttegels vastmaakt aan een dashboard, worden ze niet afgehandeld uit de cache. In plaats daarvan gedragen ze zich als rapporten en worden query's rechtstreeks uitgevoerd op back-endkernen.

Zoals de naam al aangeeft, zorgt het ophalen van de gegevens uit de querycache voor betere en consistentere prestaties dan wanneer u vertrouwt op de gegevensbron. Een manier om te profiteren van deze functionaliteit is door dashboards in te stellen als startpagina voor uw gebruikers. Maak veelgebruikte en vaak opgevraagde visuals vast aan de dashboards. Op deze manier worden dashboards een waardevolle 'eerste verdedigingslinie' die consistente prestaties bieden met minder belasting van de capaciteit. Gebruikers kunnen nog steeds doorklikken naar het rapport om zich te verdiepen in de details.  
 

Voor DirectQuery en liveverbindingen wordt deze querycache periodiek bijgewerkt door het uitvoeren van een query op de gegevensbron. Dit gebeurt standaard elk uur, maar dit kan worden geconfigureerd in de instellingen van de gegevensset. Via elke update van de querycache worden query's naar de onderliggende gegevensbron verzonden om de cache bij te werken. Het aantal query's dat wordt gegenereerd, is afhankelijk van het aantal visuals dat is vastgemaakt aan dashboards die afhankelijk zijn van deze gegevensbron. U ziet dat als beveiliging op rijniveau is ingeschakeld, er query's worden gegenereerd voor elke andere beveiligingscontext. Als uw gebruikers bijvoorbeeld twee verschillende soorten rollen gebruiken, met twee verschillende weergaven van de gegevens, worden tijdens het vernieuwen van querycache twee sets met query's gegenereerd. 

## <a name="understand-custom-visual-performance"></a>Prestaties van aangepaste visuals begrijpen 

Zorg ervoor dat u voor elke aangepaste visual de juiste stappen uitvoert om hoge prestaties te garanderen. Onvoldoende geoptimaliseerde aangepaste visuals kunnen de prestaties van het volledige rapport negatief beïnvloeden. 

## <a name="deep-dive-into-query-performance-with-sql-profiler-and-power-bi-desktop"></a>Verdiepen in queryprestaties met SQL Profiler en Power BI Desktop

Voor meer informatie over welke visuals de meeste tijd en resources gebruiken, kunt u SQL Profiler verbinden met Power BI Desktop voor een volledige weergave van de prestaties van query's.

> [!NOTE]
> Power BI Desktop ondersteunt verbindingen met een poort voor diagnostische gegevens. Via de poort voor diagnostische gegevens kunt u verbinding maken met andere hulpprogramma's en traceringen uitvoeren voor diagnostische doeleinden. *Het aanbrengen van wijzigingen in het model wordt niet ondersteund. Wijzigingen in het model kunnen leiden tot beschadiging en verlies van gegevens.*

Ga hiervoor als volgt te werk:
  
1. **Installeer SQL Server Profiler en voer Power BI Desktop uit**

   SQL Server Profiler is beschikbaar als onderdeel van SQL Server Management Studio.

2. **Bepaal de poort die wordt gebruikt door Power BI Desktop**

   Voer de opdrachtprompt of PowerShell uit met administratorbevoegdheden en gebruik netstat om de poort te vinden die door Power BI Desktop wordt gebruikt voor analyse:

   `> netstat -b -n`

   In de uitvoer wordt een lijst met toepassingen en hun open poorten weergegeven, bijvoorbeeld:  

   `TCP    [::1]:55786            [::1]:55830            ESTABLISHED`

   [msmdsrv.exe]

   Zoek de poort die wordt gebruikt door msmdsrv.exe en noteer deze voor later gebruik. In dit geval kunt u poort 55786 gebruiken.
3. **Stel de verbinding in tussen SQL Server Profiler en Power BI Desktop**

   - Start SQL Server Profiler via het menu **Start**
   - **Bestand** > **Nieuwe tracering**
   - Servertype: Analysis Services
   - Servernaam: localhost:[poortnummer zoals eerder gevonden]
   - Selecteer in het volgende scherm de optie **Uitvoeren**
   - SQL-Profiler is nu live en profileert actief de query's die worden verzonden door Power BI Desktop. 
   - Terwijl query's worden uitgevoerd, ziet u de respectieve duur en CPU-tijden. Met deze informatie kunt u bepalen welke query's een knelpunt vormen.  

Via SQL Profiler kunt u de query's identificeren die de meeste CPU-tijd in beslag nemen. Dit zijn waarschijnlijk de knelpunten. De visuals waarmee die query's worden uitgevoerd, moet u vervolgens in de gaten houden voor doorlopende optimalisatie.

## <a name="gateway-best-practices"></a>Aanbevolen procedures voor Gateway

De On-premises gegevensgateway is een uitstekend hulpprogramma om de Power BI-service te verbinden met uw on-premises gegevens. Met een slechte planning kan het echter tevens een knelpunt vormen voor de rapportprestaties. Dit geldt met name voor DirectQuery-/live-verbindinggegevenssets, waarbij alle query's en reacties op query's via de gateway verlopen. Hier volgen enkele aanbevolen procedures voor optimaal presterende gateways: 

- **Gebruik de ondernemingsmodus** in plaats van de persoonlijke modus.
- **Aanbevolen hardwarespecificaties voor de gateway**: 8 CPU-kernen, 16 GB RAM-geheugen.
- **Stel bewaking in**: stel bewaking in van de prestaties op de gatewaycomputer om te controleren of de gateway overbelast raakt en een knelpunt begint te vormen. Zie [Problemen voor de On-premises gegevensgateway oplossen](service-gateway-onprem-tshoot.md) voor meer informatie.
- **Schaal omhoog of schaal uit**: als de gateway inderdaad een knelpunt wordt, kunt u omhoog schalen (de gateway naar een krachtigere computer met meer CPU en RAM-geheugen verplaatsen) of uitschalen (bijvoorbeeld gegevenssets splitsen naar andere gateways). 
- **Afzonderlijke import versus DirectQuery**: als u wilt uitschalen, wordt aanbevolen de gateways voor de import te scheiden van de gateways voor DirectQuery.

## <a name="network-latency"></a>Netwerklatentie

Netwerklatentie kan invloed hebben op rapportprestaties doordat de tijd toeneemt die nodig is voor aanvragen de Power BI-service bereiken en voor antwoorden worden geleverd. Aan tenants in Power BI wordt een specifiek gebied toegewezen. U kunt de thuisregio van uw tenant weergeven door te navigeren naar powerbi.com. Selecteer dan ?** in de rechterbovenhoek en vervolgens **Over Power BI**. Wanneer gebruikers van een tenant de Power BI-service openen, worden hun aanvragen altijd doorgestuurd naar deze regio. Zodra de aanvragen de Power BI-service bereiken, kan de service aanvullende aanvragen verzenden, bijvoorbeeld naar de onderliggende gegevensbron of de gateway. Ook hierop is netwerklatentie van toepassing.

Hulpprogramma's zoals [Azure-snelheidstest](http://azurespeedtest.azurewebsites.net/) bieden een indicatie van de netwerklatentie tussen de client en de Azure-regio. Probeer in het algemeen om gegevensbronnen, gateways en uw Power BI-cluster zo dicht mogelijk bij te houden om de impact van de netwerklatentie te beperken. Als netwerklatentie een probleem vormt, kunt u gateways en gegevensbronnen zoeken die zich dichter bij uw Power BI-cluster bevinden door ze op virtuele machines te plaatsen.

Voor het verder verbeteren van netwerklatentie, kunt u [Azure ExpressRoute](https://azure.microsoft.com/services/expressroute/) gebruiken. Hiermee kunt u snellere en betrouwbaardere netwerkverbindingen maken tussen uw clients en de Azure-datacenters.

## <a name="next-steps"></a>Volgende stappen

- [Een implementatie met Power BI Enterprise plannen](https://aka.ms/pbienterprisedeploy), met allesomvattende richtlijnen voor grootschalige implementaties van Power BI
- [DirectQuery in SQL Server 2016 Analysis Services](https://blogs.msdn.microsoft.com/analysisservices/2017/04/06/directquery-in-sql-server-2016-analysis-services-whitepaper/)
- [[YouTube] Snel betrouwbare rapporten maken in Power BI](https://www.youtube.com/watch?v=GhiJABR7XX0)
- [[YouTube] Power BI Enterprise-implementaties](https://www.youtube.com/watch?v=K-zEWICvICM)