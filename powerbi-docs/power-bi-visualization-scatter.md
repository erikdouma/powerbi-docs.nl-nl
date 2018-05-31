---
title: Spreidingsdiagrammen in Power BI
description: Spreidingsdiagrammen in Power BI
services: powerbi
documentationcenter: ''
author: mihart
manager: kfile
backup: ''
editor: ''
tags: ''
featuredvideoid: PVcfPoVE3Ys
qualityfocus: identified
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 02/28/2018
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: a3befe1e32aa86113433a4f891ddd46a253c8062
ms.sourcegitcommit: 493f160d04ed411ff4741c599adc63ba1f65230f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2018
ms.locfileid: "33813111"
---
# <a name="scatter-charts-and-bubble-charts-in-power-bi"></a>Spreidingsdiagrammen en bellendiagrammen in Power BI
Een spreidingsdiagram heeft altijd twee waardeassen, waarbij een reeks numerieke gegevens op een horizontale as en een andere reeks numerieke waarden op de verticale as wordt weergegeven. In het diagram worden punten weergegeven op het snijpunt van een numerieke x- en y-waarde, waarbij deze waarden in één gegevenspunt worden gecombineerd. Deze gegevenspunten kunnen, afhankelijk van de gegevens, gelijkmatig of ongelijkmatig over de horizontale as zijn verdeeld.

Bij een bellendiagram worden de gegevenspunten vervangen door bellen. De *grootte* van de bellen geven de gegevens een extra dimensie.

![](media/power-bi-visualization-scatter/power-bi-bubble-chart.png)

U kunt het aantal gegevenspunten instellen  

## <a name="when-to-use-a-scatter-chart-or-bubble-chart"></a>Wanneer u een spreidingsdiagram of bellendiagram gebruikt
### <a name="scatter-charts-are-a-great-choice"></a>In de volgende gevallen komen spreidingsdiagrammen goed van pas:
* om relaties weer te geven van tussen de 2 (spreiding) of 3 (bellen) **numerieke** waarden.
* om twee groepen getallen als een reeks xy-coördinaten te tekenen.
* in plaats van een lijndiagram als u de schaal van de horizontale as wilt wijzigen    
* om de horizontale as om te zetten in een logaritmische schaal.
* om werkbladgegevens met paren of gegroepeerde sets waarden weer te geven. In een spreidingsdiagram kunt u de onafhankelijke schalen van de assen aanpassen voor meer informatie over de gegroepeerde waarden.
* om patronen weer te geven in grote gegevenssets, bijvoorbeeld door lineaire of niet-lineaire trends, clusters en uitschieters weer te geven.
* om grote aantallen gegevenspunten te vergelijken zonder rekening te houden met tijd.  Hoe meer gegevens u opneemt in een spreidingsdiagram, des te beter zijn de vergelijkingen die u kunt maken.

### <a name="bubble-charts-are-a-great-choice"></a>In de volgende gevallen komen bellendiagrammen goed van pas:
* als uw gegevens 3 gegevensreeksen bevatten met elk een set waarden.
* om financiële gegevens weer te geven.  Verschillende belgrootten zijn handig om specifieke waarden visueel te benadrukken.
* om te gebruiken met kwadranten.

## <a name="create-a-scatter-chart"></a>Een spreidingsdiagram maken
Bekijk deze video voor informatie over de optie Een spreidingsdiagram maken en volg daarna de onderstaande stappen om zelf een spreidingsdiagram te maken.

<iframe width="560" height="315" src="https://www.youtube.com/embed/PVcfPoVE3Ys?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>


In deze instructies wordt het voorbeeld van een retailanalyse gebruikt. Om mee te lezen kunt u het [voorbeeld downloaden](sample-datasets.md) voor de Power BI-service (app.powerbi.com) of voor Power BI Desktop.   

1. Selecteer het gele pictogram met het plusteken om een [lege rapportpagina ](power-bi-report-add-page.md) te maken.
 
2. Selecteer de volgende velden in het deelvenster Velden:
   - **Verkoop** > **Verkoop per vierkante meter**
   - **Verkoop** > **Afwijkingspercentage totale verkoop**
   - **District** > **District**

    ![](media/power-bi-visualization-scatter/power-bi-bar-chart.png)

    Als u de Power BI-service gebruikt, moet u het rapport openen in de [bewerkweergave](service-interact-with-a-report-in-editing-view.md).

3. Converteer naar een spreidingsdiagram. Selecteer het pictogram voor spreidingsdiagrammen in het deelvenster Visualisaties.

   ![](media/power-bi-visualization-scatter/pbi_scatter_chart_icon.png).

4. Sleep **District** van **Details** naar **Legenda**. We hebben nu een spreidingsdiagram die **Afwijking van totale verkoop in %** op de y-as afzet tegen de **verkoop per vierkante meter op de x-as**. De kleuren van de gegevenspunten vertegenwoordigen de districten:

    ![](media/power-bi-visualization-scatter/power-bi-scatter.png)

Nu gaan we een derde dimensie toevoegen.

## <a name="create-a-bubble-chart"></a>Een bellendiagram maken

1. Sleep **Verkoop** > **Omzet van dit jaar** > **Waarde** vanuit het deelvenster **Velden** naar het gebied **Grootte**. De gegevenspunten worden uitgevouwen naar volumes die evenredig zijn met de verkoopwaarde.
   
   ![](media/power-bi-visualization-scatter/power-bi-bubble.png)

2. Beweeg de muisaanwijzer over een bel. De grootte van de bel geeft de waarde van **Omzet van dit jaar** weer.
   
    ![](media/power-bi-visualization-scatter/pbi_scatter_chart_hover.png)

3. Wanneer u het aantal gegevenspunten zo wilt instellen dat deze in uw bellengrafiek worden weergegeven, vouwt u in de sectie **Indeling** van het deelvenster **Visualisaties** de kaart **Algemeen** uit en past u het **gegevensvolume** aan. U kunt het maximale gegevensvolume instellen op een willekeurige waarde tot 10.000 (de standaardwaarde is 3500).

    ![Gegevensvolume](media/power-bi-visualization-scatter/pbi_scatter_data_volume.png) 

   > [!NOTE]
   > Omdat meer gegevenspunten kan leiden tot een langere laadtijd, kunt u beter uw rapporten op internet en op mobiel uittesten en ervoor zorgen dat de prestaties overeenkomen met de verwachtingen van uw gebruikers als u toch besluit om rapporten te publiceren met beperkingen aan de bovengrens van de schaal. Om goede prestaties te kunnen garanderen, moet u voor grotere aantallen gegevenspunten de resultaten op verschillende formulierfactoren testen.

4. U kunt [de kleuren, labels, titels, achtergrond en meer van de visual wijzigen](service-getting-started-with-color-formatting-and-axis-properties.md). Voor een [betere toegankelijkheid](desktop-accessibility.md) kunt u markeringsvormen aan elke regel toevoegen. Als u voor elke lijn een andere markeringsvorm gebruikt, is het makkelijker voor gebruikers om verschillende lijnen (of vlakken) van elkaar te onderscheiden. Als u de markeringsvorm wilt selecteren, vouwt u de kaart **Vormen** uit en selecteert u vervolgens een markeringsvorm.

      ![Vorm van markering](media/power-bi-visualization-scatter/pbi_scatter_marker.png)

   U kunt ook de markeringsvorm wijzigen in een ruit, driehoek of vierkant:

   ![Vierkante markering](media/power-bi-visualization-scatter/pbi_scatter_chart_hover_square.png)


## <a name="considerations-and-troubleshooting"></a>Aandachtspunten en probleemoplossing

### <a name="your-scatter-chart-has-only-one-data-point"></a>**Uw spreidingsdiagram heeft slechts één gegevenspunt**
Hebt u een spreidingsdiagram gemaakt en wordt daarin slechts één gegevenspunt weergegeven waarin alle waarden op de x- en y-as worden samengevoegd?  Of worden in het diagram alle waarden langs een horizontale of verticale lijn weergegeven?

![](media/power-bi-visualization-scatter/pbi_scatter_tshoot1.png)

Voeg een veld toe aan het gebied **Details** om aan te geven hoe de waarden moeten worden gegroepeerd. Het veld moet uniek zijn voor elk punt dat moet worden weergegeven.  
Zoals een eenvoudig rijnummer of ID-veld:

![](media/power-bi-visualization-scatter/pbi_scatter_tshoot.png)

Als uw gegevens dit niet bevatten, maakt u een veld waarin uw x- en y-waarden samen worden gevoegd in iets unieks per punt:

![](media/power-bi-visualization-scatter/pbi_scatter_tshoot2.png)

[Gebruik van de Query Editor van Power BI Desktop om een indexkolom toe te voegen](desktop-add-custom-column.md) aan uw gegevensset om een nieuw veld te maken.  Voeg deze kolom toe aan het gebied **Details** van uw visualisatie.

## <a name="next-steps"></a>Volgende stappen
 [Typen visualisaties in Power BI](power-bi-visualization-types-for-reports-and-q-and-a.md)

[Probeer het uit, het is gratis.](https://powerbi.com/)  

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

