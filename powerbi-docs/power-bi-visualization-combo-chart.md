---
title: Combinatiegrafieken in Power BI (zelfstudie)
description: Deze documentatie is een zelfstudie (met video) waarin wordt uitgelegd waarom en hoe u een combinatiegrafiek maakt in Power BI.
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: lnv66cTZ5ho
qualityfocus: monitoring
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/27/2017
ms.author: mihart
ms.openlocfilehash: c00ba74501a411743036c4514750bccbbae3eb00
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2017
---
# <a name="combo-chart-in-power--tutorial"></a>Combinatiegrafieken in Power BI (zelfstudie)
Een combinatiegrafiek in Power BI is een visualisatie waarin een lijndiagram wordt gecombineerd met een kolomdiagram. Als u deze twee diagrammen combineert, kunt u de gegevens sneller vergelijken.

Combinatiegrafieken kunnen één of twee Y-assen bevatten.

## <a name="when-to-use-a-combo-chart"></a>Wanneer gebruikt u een combinatiegrafiek?
In de volgende gevallen komen combinatiegrafieken goed van pas:

* Als u hebt een lijndiagram en een kolomdiagram met dezelfde X-as hebt.
* Als u meerdere metingen met verschillende waardebereiken wilt vergelijken.
* Als u het verband tussen twee metingen wilt illustreren in één visualisatie.
* Als u wilt controleren of één meting voldoet aan het doel dat is gedefinieerd door een andere meting.
* Als u ruimte op het canvas wilt besparen.

## <a name="create-a-basic-single-axis-combo-chart"></a>Een eenvoudige combinatiegrafiek met één as maken
Kijk hoe Will een combinatiegrafiek maakt op basis van het voorbeeld van verkoop en marketing.

<iframe width="560" height="315" src="https://www.youtube.com/embed/lnv66cTZ5ho?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>


Als u uw eigen combinatiegrafiek wilt maken, meldt u zich aan bij Power BI en selecteert u **Gegevens ophalen\> Voorbeelden \> Voorbeeld van een retailanalyse**. 

1. Selecteer op het dashboard Voorbeeld van een retailanalyse de tegel **Totaal aantal winkels** om het rapport Voorbeeld van een retailanalyse te openen.
2. Selecteer **Rapport bewerken** om het rapport in de bewerkingsweergave te openen.
3. [Voeg een nieuwe rapportpagina toe](power-bi-report-add-page.md).
4. Maak een kolomdiagram waarin de omzet voor dit jaar en de brutomarge marge per maand wordt weergegeven.
   
    a.  Selecteer in het deelvenster Velden achtereenvolgens **Verkoop** \> **Omzet dit jaar** > **Waarde**.
   
    b.  Sleep **Verkoop** \> **Brutomarge dit jaar** naar de bron **Waarde**.
   
    c.  Selecteer **Tijd** \> **FiscalMonth** om deze waarde toe te voegen aan de bron **As**. 
   
    ![](media/power-bi-visualization-combo-chart/combotutorial1new.png)
5. Selecteer de weglatingstekens (...) in de rechterbovenhoek van de visualisatie en selecteer **Sorteren op FiscalMonth**.
6. Converteer de kolomdiagram naar een combinatiegrafiek. Selecteer de kolomdiagram en selecteer vervolgens in het deelvenster **Visualisaties** de optie **Lijndiagram en gegroepeerd kolomdiagram**.
   
    ![](media/power-bi-visualization-combo-chart/converttocombo_new2.png)
7. Ga naar het deelvenster **Velden** en sleep **Verkoop** \> **Omzet van afgelopen jaar** naar de bucket **Regelwaarden**.
   
   ![](media/power-bi-visualization-combo-chart/linevaluebucket.png)
   
   Uw combinatiegrafiek moet er ongeveer als volgt uitzien:
   
   ![](media/power-bi-visualization-combo-chart/combochartdone-new.png)

## <a name="create-a-combo-chart-with-two-axes"></a>Een combinatiegrafiek met twee assen maken
In deze taak vergelijken we de brutomarge en de omzet.

1. Maak een nieuw lijndiagram waarin de procentuele brutomarge van het vorige jaar per maand wordt bijgehouden.  In januari was de brutomarge 35%, in april nemen we een piek (45%) waar, in juli daalde het brutomargepercentage en in augustus was er opnieuw een daling. Krijgen we een soortgelijk patroon voor afgelopen jaar en dit jaar te zien?
   
   ![](media/power-bi-visualization-combo-chart/combo1_new.png)
2. Voeg **Omzet van dit jaar > Waarde** en **Omzet van afgelopen jaar** aan het lijndiagram toe. De schaal van **BM % vorig jaar** is veel kleiner is dan de schaal van **Verkoop**, waardoor het lastig is om de waarden te vergelijken.      
   
   ![](media/power-bi-visualization-combo-chart/flatline_new.png)
3. Converteer het lijndiagram naar een lijndiagram en gestapeld kolomdiagram, zodat de visual eenvoudiger te lezen en te interpreteren is.
   
   ![](media/power-bi-visualization-combo-chart/converttocombo_new.png)
4. Sleep **Brutomarge % vorig jaar** van **Kolomwaarden** naar **Regelwaarden**. In Power BI worden twee assen gemaakt, zodat de gegevenssets verschillend kunnen worden geschaald. Aan de linkerkant in dollars en aan de rechterkant in percentages.
   
   ![](media/power-bi-visualization-combo-chart/power-bi-combochart.png)    

## <a name="add-titles-to-the-axes"></a>Titels toevoegen aan de assen
1. Selecteer het pictogram met de verfroller ![](media/power-bi-visualization-combo-chart/power-bi-paintroller.png) om het opmaakvenster te openen.
2. Selecteer de pijl-omlaag om de **Y-as** uit te breiden.
3. Stel voor de **Y-as (kolom)** de **Positie** in op **Links**, stel **Titel** in op **Aan**, stel **Stijl** in op **Alleen titel weergeven** en stel voor **Weergeven** de optie **Miljoenen** in.
   
   ![](media/power-bi-visualization-combo-chart/power-bi-y-axis-column.png)
4. Zorg er bij **Y-as (kolom)** ook voor dat **Secundaire weergeven** is ingesteld op **Aan**. Hiermee geeft u de opties weer om het regeldiagramgedeelte van de combinatiegrafiek op te maken.
   
   ![](media/power-bi-visualization-combo-chart/power-bi-show-secondary.png)
5. Voor **Y-as (regel)** laat u **Positie** ingesteld staan op **Rechts**, stelt u **Titel** in op **Aan** en stelt u voor **Stijl** de optie **Alleen titel weergeven** in.
   
   Uw combinatiegrafiek bevat nu twee assen, beide met titels.
   
   ![](media/power-bi-visualization-combo-chart/power-bi-titles-on.png)

U kunt nu het volgende doen:

* [De combinatiegrafiek toevoegen als dashboardtegel](service-dashboard-tiles.md).
* [Het rapport opslaan](service-report-save.md).

## <a name="highlighting-and-cross-filtering"></a>Markeren en kruislings filteren
Zie [Een filter aan een rapport toevoegen](power-bi-report-add-filter.md) voor meer informatie over het gebruik van het deelvenster Filters.

Wanneer u een kolom of regel in een combinatiegrafiek markeert, worden de andere filters op de rapportpagina kruislings gefilterd en omgekeerd.

## <a name="next-steps"></a>Volgende stappen
[Een visualisatie toevoegen aan een rapport](power-bi-report-add-visualizations-i.md)

[Visualisaties in Power BI Reports](power-bi-report-visualizations.md)

[Typen visualisaties in Power BI](power-bi-visualization-types-for-reports-and-q-and-a.md)

[Power BI - basisconcepten](service-basic-concepts.md)

[Probeer het uit, het is gratis.](https://powerbi.com/)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/).

