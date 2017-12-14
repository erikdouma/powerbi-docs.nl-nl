---
title: 'Een nieuw rapport maken van een gegevensset '
description: Maak een nieuw Power BI-rapport van een gegevensset.
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: monitoring
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/28/2017
ms.author: mihart
ms.openlocfilehash: f4afb1eaa1b3012fdbdb0eff35e9eff695cc32e4
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2017
---
# <a name="create-a-new-power-bi-report-by-importing-a-dataset"></a>Een nieuw Power BI-rapport maken door een gegevensset te importeren
U hebt [Rapporten in Power BI](service-reports.md) gelezen en u wilt nu uw eigen rapport maken. Er zijn veel verschillende manieren om een rapport te maken. In dit artikel beginnen we met het maken van een zeer eenvoudig rapport vanuit een Excel-gegevensset. Als u de basisbeginselen van het maken van een rapport onder de knie hebt, kunt u met de **Volgende stappen** onderaan verder naar meer geavanceerde onderwerpen over rapporten.  

> **TIP**: zie [Een rapport kopiëren](power-bi-report-copy.md) voor informatie over het maken van een rapport op basis van een bestaand rapport.
> 
> 

## <a name="import-the-dataset"></a>De gegevensset importeren
Bij deze methode om een rapport te maken begint u met een gegevensset en een leeg rapportcanvas. Volg ons en [download de Excel-gegevensset Voorbeeld van een retailanalyse](http://go.microsoft.com/fwlink/?LinkId=529778) en sla deze op onder OneDrive voor bedrijven (voorkeur) of lokaal.

1. We maken het rapport in een Power BI-servicewerkruimte. Selecteer daarom een bestaande werkruimte of maak een nieuwe.
   
   ![](media/service-report-create-new/power-bi-workspaces2.png)
2. Selecteer **Gegevens ophalen** links onderin de navigatiebalk.
   
   ![](media/service-report-create-new/power-bi-get-data3.png)
3. Selecteer **Bestanden** en navigeer naar de locatie waar u het voorbeeld van een retailanalyse hebt opgeslagen.
   
    ![](media/service-report-create-new/power-bi-select-files.png)
4. Selecteer voor deze oefening **Importeren**.
   
   ![](media/service-report-create-new/power-bi-import.png)
5. Als de gegevensset is geïmporteerd, selecteert u **Gegevensset weergeven**.
   
   ![](media/service-report-create-new/power-bi-view-dataset.png)
6. Als u een gegevensset bekijkt, wordt de rapporteditor geopend.  U ziet een leeg canvas en de bewerkingshulpmiddelen voor het rapport.
   
   ![](media/service-report-create-new/power-bi-blank-report.png)

> **TIP**: als u niet weet hoe u een rapportcanvas moet bewerken of als u uw kennis wilt opfrissen, kunt u [een rondleiding van de rapporteditor volgen ](service-the-report-editor-take-a-tour.md) voordat u doorgaat.
> 
> 

## <a name="add-a-radial-gauge-to-the-report"></a>Een radiale meter toevoegen aan het rapport
Nu onze gegevensset is geïmporteerd, kunnen we vragen beantwoorden.  Onze Chief Marketing Officer (CMO) wil weten hoe dicht we de verkoopdoelstellingen voor dit jaar zijn genaderd. Een meter is een [goede visualisatiekeuze](power-bi-report-visualizations.md) om dit soort informatie weer te geven.

1. Selecteer **Verkoop** > **Omzet van dit jaar** > **Waarde** in het deelvenster Velden.
   
    ![](media/service-report-create-new/power-bi-report-step1.png)
2. Converteer het visuele element naar een meter door het metersjabloon te selecteren ![](media/service-report-create-new/powerbi-gauge-icon.png) in het deelvenster **Visualisaties**.
   
    ![](media/service-report-create-new/power-bi-report-step2.png)
3. Sleep **Verkoop** > **Omzet van dit jaar** > **Doel** naar de bron **Doelwaarde**. Het lijkt erop dat we heel dicht bij ons doel zijn.
   
    ![](media/service-report-create-new/power-bi-report-step3.png)
4. Dit is een goed moment om [uw rapport op te slaan](service-report-save.md).
   
   ![](media/service-report-create-new/powerbi-save.png)

## <a name="add-an-area-chart-and-slicer-to-the-report"></a>Een vlakdiagram en slicer toevoegen aan het rapport
Onze CMO heeft nog een paar vragen voor ons. Ze wil graag weten hoe de omzet dit jaar zich verhoudt tot de omzet van vorig jaar. En ze wil graag de resultaten per district zien.

1. Laten we eerst wat ruimte maken op ons canvas. Selecteer de meter en verplaats deze naar de rechterbovenhoek. Pak en sleep een van de hoeken om het vlak kleiner te maken.
2. Hef de selectie van de meter op. Selecteer **Verkoop** > **Omzet van dit jaar** > **Waarde** in het deelvenster Velden en selecteer **Verkoop**  >  **Omzet van vorig jaar**.
   
    ![](media/service-report-create-new/power-bi-report-step4.png)
3. Converteer het visuele element naar een vlakdiagram door het vlakdiagramsjabloon te selecteren ![](media/service-report-create-new/power-bi-areachart-icon.png) in het deelvenster **Visualisaties**.
4. Selecteer **Tijd** > **Periode** om deze toe te voegen aan de bron **As**.
   
    ![](media/service-report-create-new/power-bi-report-step5.png)
5. Als u de visualisatie wilt sorteren, selecteert u de weglatingstekens en kiest u **Sorteren op periode**.
6. Nu gaan we de slicer toevoegen. Selecteer een leeg gebied op het canvas en kies het slicersjabloon ![](media/service-report-create-new/power-bi-slicer-icon.png). Hiermee wordt een lege slicer aan het canvas toegevoegd.
   
    ![](media/service-report-create-new/power-bi-report-step6.png)    
7. Selecteer **District** > **District** in het deelvenster Velden. Verplaats de slicer en verander het formaat ervan.
   
    ![](media/service-report-create-new/power-bi-report-step7.png)  
8. Ga met de slicer zoeken naar patronen en inzichten per district.
   
   ![](media/service-report-create-new/power-bi-slicer-video2.gif)  
9. U kunt steeds opnieuw visualisaties toevoegen.

## <a name="next-steps"></a>Volgende stappen
* [Een kopie van een rapport maken](power-bi-report-copy.md)
* [Het rapport opslaan](service-report-save.md)    
* [Een nieuwe pagina aan het rapport toevoegen](power-bi-report-add-page.md)  
* Meer informatie over [visualisaties aan een dashboard vastmaken](service-dashboard-pin-tile-from-report.md)    
* Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

