---
title: Een Power BI-dashboard maken op basis van een rapport
description: Een Power BI-dashboard maken op basis van een rapport
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: 
qualityfocus: 
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 05/09/2017
ms.author: mihart
ms.openlocfilehash: 67cc9508d71fa29303d09e8901294a2d6b7f8a56
ms.sourcegitcommit: 804ee18b4c892b7dcbd7d7d5d987b16ef16fc2bb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/09/2018
---
# <a name="create-a-power-bi-dashboard-from-a-report"></a>Een Power BI-dashboard maken op basis van een rapport
U hebt [Dashboards in Power BI](service-dashboards.md) gelezen en u wilt nu uw eigen dashboard maken. Er zijn veel verschillende manieren om een dashboard te maken: op basis van een rapport, helemaal vanaf het begin, op basis van een gegevensset, door een bestaand dashboard te dupliceren, en meer.  In dit onderwerp en deze video ziet u hoe u een nieuw dashboard kunt maken door visualisaties van een bestaand rapport vast te maken.

> **OPMERKING**: Dashboards zijn een functie van Power BI-service, niet van Power BI Desktop. Dashboards kunnen niet worden gemaakt in Power BI - Mobiel, maar wel worden [bekeken en gedeeld](mobile-apps-view-dashboard.md).
> 
> 

![](media/service-dashboard-create/power-bi-completed-dashboard-small.png)

## <a name="video-create-a-dashboard-by-pinning-visuals-and-images-from-a-report"></a>Video: Een dashboard maken door visualisaties en afbeeldingen van een rapport vast te maken
Kijk hoe Amanda een nieuw dashboard maakt door visualisaties van een rapport vast te maken. Probeer het vervolgens zelf uit met behulp van het voorbeeld van een inkoopanalyse door de stappen onder de video te volgen.

<iframe width="560" height="315" src="https://www.youtube.com/embed/lJKgWnvl6bQ" frameborder="0" allowfullscreen></iframe>

## <a name="import-a-dataset-with-a-report"></a>Een gegevensset met een rapport importeren
We gaan een van de Power BI-voorbeeldgegevenssets importeren en gebruiken om ons nieuwe dashboard te maken. Het voorbeeld dat we gebruiken is een Excel-werkmap met twee PowerView-bladen. Als de werkmap wordt geïmporteerd in Power BI, wordt er een gegevensset en een rapport toegevoegd aan uw werkruimte.  Het rapport wordt automatisch gemaakt op basis van de PowerView-werkbladen.

1. [Selecteer deze koppeling](http://go.microsoft.com/fwlink/?LinkId=529784) om het Excel-bestand met het voorbeeld van een inkoopanalyse te downloaden en op te slaan. We raden u aan het op te slaan in uw OneDrive voor bedrijven.
2. Open de Power BI-service (app.powerbi.com) in uw browser en meld u aan.
3. Selecteer een bestaande werkruimte of maak een nieuwe app-werkruimte.
4. Selecteer in de linker navigatie **Gegevens ophalen**.
   
    ![](media/service-dashboard-create/power-bi-get-data3.png)
5. Selecteer **Bestanden**.
   
   ![](media/service-dashboard-create/power-bi-select-files.png)
6. Navigeer naar de locatie waar u het Excel-bestand met het voorbeeld van een inkoopanalyse hebt opgeslagen. Selecteer het en kies **Verbinding maken**.
   
   ![](media/service-dashboard-create/power-bi-connectnew.png)
7. Selecteer voor deze oefening **Importeren**.
   
    ![](media/service-dashboard-create/power-bi-import.png)
8. Wanneer het bericht wordt weergegeven dat het importeren is voltooid, selecteert u de **x** om het bericht te sluiten.
   
   ![](media/service-dashboard-create/power-bi-view-datasetnew.png)

### <a name="open-the-report-and-pin-some-tiles-to-a-dashboard"></a>Open het rapport en maak enkele tegels vast aan een dashboard
1. Blijf in dezelfde werkruimte en selecteer het tabblad **Rapporten**. Het zojuist geïmporteerde rapport wordt weergegeven met een geel sterretje. Selecteer de naam van het rapport om het te openen.
   
    ![](media/service-dashboard-create/power-bi-reports.png)
2. Het rapport wordt geopend in de [Leesweergave](service-reading-view-and-editing-view.md). Let op de twee tabbladen aan de onderkant: Discount Analysis (Kortingsanalyse) en Spend Overview (Uitgavenoverzicht). Elk tabblad vertegenwoordigt een pagina van het rapport.
   
    ![](media/service-dashboard-create/power-bi-reading-view.png)
3. Wijs een visualisatie aan om de beschikbare opties zichtbaar te maken. Als u een visualisatie aan een dashboard wilt toevoegen, selecteert u het punaisepictogram ![](media/service-dashboard-create/power-bi-pin-icon.png).
   
    ![](media/service-dashboard-create/power-bi-hover.png)
4. Omdat we een nieuw dashboard maken, selecteert u de optie **Nieuw dashboard** en geeft u het een naam. 
   
   ![](media/service-dashboard-create/power-bi-pin-tile.png)
5. Wanneer u **Vastmaken** selecteert, wordt het nieuwe dashboard in de huidige werkruimte gemaakt. Wanneer het bericht **Aan dashboard vastgemaakt** wordt weergegeven, selecteert u **Naar dashboard gaan**. Als u wordt gevraagd of u het rapport wilt opslaan, kiest u **Opslaan**.
   
     ![](media/service-dashboard-create/power-bi-pin-success.png)
6. Het nieuwe dashboard wordt geopend in Power BI en het bevat één tegel - de visualisatie die we zojuist hebben vastgemaakt. 
   
   ![](media/service-dashboard-create/power-bi-pinned.png)
7. Selecteer de tegel om terug te gaan naar het rapport. Maak nog een paar tegels vast aan het nieuwe dashboard. Wanneer het venster **Aan dashboard vastmaken** verschijnt, selecteert u deze keer **Bestaand dashboard**.  
   
   ![](media/service-dashboard-create/power-bi-existing-dashboard.png)

Gefeliciteerd, u hebt uw eerste dashboard gemaakt! Nu u een dashboard hebt, kunt u er nog veel meer mee doen.  Probeer een van de voorgestelde **Volgende stappen** hieronder, of ga er zelf mee spelen en verkennen.   

## <a name="next-steps"></a>Volgende stappen
* [Het formaat van tegels bewerken en ze verplaatsen](service-dashboard-edit-tile.md)
* [Alles over dashboardtegels](service-dashboard-tiles.md)
* [Uw dashboard delen door een app te maken](service-create-distribute-apps.md)
* [Power BI - basisconcepten](service-basic-concepts.md)
* [Dashboards in Power BI](service-dashboards.md)
* [Tips voor het ontwerpen van een geweldig dashboard](service-dashboards-design-tips.md)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

