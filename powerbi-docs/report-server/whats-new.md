---
title: Wat is er nieuw in Power BI Report Server
description: Meer informatie over wat er nieuw is in Power BI Report Server. Dit onderwerp bestrijkt de primaire functiegebieden. Het wordt bijgewerkt wanneer nieuwe items worden uitgebracht.
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
ms.date: 10/31/2017
ms.author: maghan
ms.openlocfilehash: 433581f77cfeaa002cffeecd927ba8751fc46617
ms.sourcegitcommit: eec6b47970bf69ed30638d1a20051f961ba792f2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/06/2018
---
# <a name="whats-new-in-power-bi-report-server"></a>Wat is er nieuw in Power BI Report Server
Meer informatie over wat er nieuw is in Power BI Report Server. Dit onderwerp bestrijkt de primaire functiegebieden. Het wordt bijgewerkt wanneer nieuwe items worden uitgebracht.

Ga naar [On-premises rapportage met de Power BI Report Server](https://powerbi.microsoft.com/report-server/) om Power BI Report Server en de geoptimaliseerde versie van Power BI Desktop voor Power BI Report Server te downloaden.

![tip](media/whats-new/fyi-tip.png "tip") Zie [Power BI Report Server - release-opmerkingen](release-notes.md) voor de huidige release-opmerkingen.

Zie de volgende onderwerpen voor verwante informatie over nieuwe functies en mogelijkheden:

* [Wat is er nieuw in de Power BI-service](../service-whats-new.md)
* [Wat is er nieuw in Power BI Desktop](../desktop-latest-update.md)
* [Wat is er nieuw in de mobiele apps voor Power BI](../mobile-whats-new-in-the-mobile-apps.md)
* [Power BI-teamblog](https://powerbi.microsoft.com/blog/)

## <a name="october-2017-release"></a>Release van oktober 2017
### <a name="power-bi-report-data-sources"></a>Power BI-rapportgegevensbronnen
Voor Power BI-rapporten in Power BI Report Server kan verbinding worden gemaakt met een groot aantal verschillende gegevensbronnen. U kunt gegevens importeren en vernieuwing van gegevens plannen, of rechtstreeks met DirectQuery of een liveverbinding met SQL Server Analysis Services een query op de gegevens uitvoeren. Zie de lijst met gegevensbronnen die geplande vernieuwing ondersteunen en bronnen die DirectQuery ondersteunen in 'Power BI-rapportgegevensbronnen in Power BI Report Server'.

### <a name="scheduled-data-refresh-for-imported-data"></a>Geplande gegevensvernieuwing voor geïmporteerde gegevens
In Power BI Report Server kunt u geplande gegevensvernieuwing instellen om gegevens up-to-date te houden in Power BI-rapporten met een ingesloten model in plaats van met een liveverbinding of DirectQuery. Met een ingesloten model importeert u de gegevens, zodat deze worden losgekoppeld van de oorspronkelijke gegevensbron. Het model moet worden bijgewerkt om de gegevens actueel te houden. Geplande vernieuwing is de aangewezen manier om dat te doen. Lees meer over geplande vernieuwing voor Power BI-rapporten in Power BI Report Server.

### <a name="editing-power-bi-reports-from-the-server"></a>Power BI-rapporten bewerken vanaf de server
U kunt Power BI-rapportbestanden (.pbix) openen en bewerken vanaf de server, maar u krijgt het oorspronkelijke bestand terug dat u hebt geüpload.  Dit betekent **dat de gegevens niet worden bijgewerkt wanneer u het bestand voor het eerst opent als de gegevens zijn vernieuwd door de server**. U moet ze lokaal handmatig vernieuwen om de wijziging te zien.

### <a name="large-file-uploaddownload"></a>Grote bestanden uploaden/downloaden
U kunt bestanden van maximaal 2 GB uploaden, hoewel deze limiet standaard is ingesteld op 1 GB in de Report Server-instellingen in SQL Server Management Studio (SSMS).  Deze bestanden worden opgeslagen in de database, net als voor SharePoint. Er is geen speciale configuratie vereist voor de SQL Server-catalogus.  

### <a name="accessing-shared-datasets-as-odata-feeds"></a>Toegang tot gedeelde gegevenssets als OData-feeds
Met een OData-feed hebt u toegang tot gedeelde gegevenssets van Power BI Desktop. Zie [Gedeelde gegevenssets openen als OData-feeds in Power BI Report Server](access-dataset-odata.md)voor meer informatie.

### <a name="scale-out"></a>Uitschalen
Deze versie biedt ondersteuning voor uitschalen. Gebruik voor de beste ervaring een load balancer en stel serveraffiniteit in. Denk erom dat het scenario nog niet is geoptimaliseerd voor uitschalen, waardoor modellen mogelijk op meerdere knooppunten worden gerepliceerd. Het scenario werkt zonder de Network Load Balancer en tijdelijke sessies. U ziet echter niet alleen een overmatig gebruik van geheugen op knooppunten wanneer het model N keer wordt geladen, maar de prestaties tussen verbindingen worden trager wanneer het model wordt gestreamd en een nieuw knooppunt treft tussen aanvragen.  

### <a name="administrator-settings"></a>Beheerdersinstellingen
Beheerders kunnen de volgende eigenschappen instellen in geavanceerde SSMS-eigenschappen voor de serverfarm:

* EnableCustomVisuals: True/False
* EnablePowerBIReportEmbeddedModels: True/False
* EnablePowerBIReportEmbeddedModels: True/False
* MaxFileSizeMb: standaard is nu 1000
* ModelCleanupCycleMinutes: hoe vaak er wordt gecontroleerd om modellen uit het geheugen te verwijderen
* ModelExpirationMinutes: hoe lang het duurt tot het model is verlopen en wordt verwijderd, op basis van de laatste keer dat het is gebruikt
* ScheduleRefreshTimeoutMinutes: hoe lang het vernieuwen van gegevens kan duren voor een model. Dit is standaard twee uur.  Er is geen vaste bovengrens.

**Configuratiebestand rsreportserver.config**

```
<Configuration>
  <Service>
    <PollingInterval>10</PollingInterval>
    <IsDataModelRefreshService>false</IsDataModelRefreshService>
    <MaxQueueThreads>0</MaxQueueThreads>
  </Service>
</Configuration>
```

### <a name="developer-api"></a>API voor ontwikkelaars
De API voor ontwikkelaars (REST API) die is geïntroduceerd voor SSRS 2017, is uitgebreid voor Power BI Report Server voor gebruik met zowel Excel-bestanden als .pbix-bestanden. Een mogelijk gebruiksvoorbeeld is het via programmacode downloaden van bestanden, het vernieuwen ervan en het vervolgens opnieuw publiceren. Dit is bijvoorbeeld de enige manier waarop Excel-werkmappen met PowerPivot-modellen kunnen worden vernieuwd.

Merk op dat er een nieuwe afzonderlijke API is voor grote bestanden, die wordt bijgewerkt in de Power BI Report Server-versie van Swagger. 

### <a name="sql-server-analysis-services-ssas-and-the-power-bi-report-server-memory-footprint"></a>SQL Server Analysis Services (SSAS) en het geheugengebruik van Power BI Report Server
Power BI Report Server fungeert intern nu als host voor SQL Server Analysis Services (SSAS). Dit is niet specifiek voor geplande vernieuwing. Door SSAS te hosten, kunt u het geheugengebruik van de rapportserver aanzienlijk uitbreiden. Het configuratiebestand AS.ini is beschikbaar op de serverknooppunten. Als u bekend bent met SSAS, kunt u dus de instellingen bijwerken, inclusief de maximale geheugenlimiet en schijfopslag in de cache enzovoort. Zie [Servereigenschappen in Analysis Services](https://docs.microsoft.com/sql/analysis-services/server-properties/server-properties-in-analysis-services) voor meer informatie.

### <a name="viewing-and-interacting-with-excel-workbooks"></a>Excel-werkmappen weergeven en ermee werken
Excel en Power BI bevatten een portfolio met hulpprogramma's die uniek is in de branche. Dankzij deze twee programma’s kunnen bedrijfsanalisten eenvoudiger hun gegevens verzamelen, vormgeven, analyseren en op een visuele manier verkennen. Zakelijke gebruikers kunnen nu niet alleen Power BI-rapporten weergeven in de webportal, maar ook hetzelfde doen met Excel-werkmappen in Power BI Report Server. Zo hebben ze één locatie waar ze hun selfservice Microsoft BI-inhoud kunnen publiceren en weergeven.

We hebben een [overzicht gepubliceerd hoe u Office Online Server (OOS) toevoegt aan de voorbeeldomgeving van uw Power BI Report Server](excel-oos.md). Klanten met een Volumelicentie-account kunnen OOS kosteloos downloaden uit het Volume License Servicing Center. Ze beschikken dan over alleen-lezenfunctionaliteit. Als de functionaliteit eenmaal is geconfigureerd, kunnen gebruikers Excel-werkmappen weergeven en werken met werkmappen die:

* Geen afhankelijkheden van de externe gegevensbron hebben
* Een liveverbinding hebben met een externe SQL Server Analysis Services-gegevensbron
* Een PowerPivot-gegevensmodel hebben

### <a name="support-for-new-table-and-matrix-visuals"></a>Ondersteuning voor nieuwe visuele tabel- of matrixelementen
Power BI Report Server ondersteunt nu de nieuwe visuele Power BI-tabel en -matrixelementen. Als u rapporten wilt maken met deze visuele elementen, hebt u een bijgewerkte versie van Power BI Desktop nodig voor de release van oktober 2017. Deze functie kan niet worden geïnstalleerd naast de Power BI Desktop-release (juni 2017). Selecteer op de [downloadpagina van Power BI Report Server](https://powerbi.microsoft.com/report-server/) **Geavanceerde downloadinstellingen** voor de meest recente versie van Power BI Desktop.

## <a name="june-2017"></a>Juni 2017
* Power BI Report Server algemeen beschikbaar gesteld (GA).

## <a name="may-2017"></a>Mei 2017
* Voorbeeld van Power BI Report Server beschikbaar gesteld
* Mogelijkheid om Power BI-rapporten on-premises te publiceren
  * Ondersteuning voor aangepaste visuele elementen
  * Alleen ondersteuning voor liveverbindingen voor Analysis Services, er volgen meer gegevensbronnen.
  * App Power BI - Mobiel bijgewerkt om Power BI-rapporten weer te geven die worden gehost in Power BI Report Server
* Verbeterde samenwerking in rapporten met opmerkingen

## <a name="next-steps"></a>Volgende stappen
[Releaseopmerkingen bij Power BI Report Server](release-notes.md)  
[Gebruikershandboek](user-handbook-overview.md)  
[Beheerdershandboek](admin-handbook-overview.md)  
[Snelstartgids: Power BI Report Server installeren](quickstart-install-report-server.md)  
[Report Builder installeren](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder)  
[SQL Server Data Tools (SSDT) downloaden](http://go.microsoft.com/fwlink/?LinkID=616714)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](https://community.powerbi.com/)

