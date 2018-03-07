---
title: Slicers in Power BI (zelfstudie)
description: 'Zelfstudie: Slicers in Power BI'
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: zIZPA0UrJyA
qualityfocus: monitoring
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 05/30/2017
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: 619f694e6e3ed167a14262994c1c978d5b4ea2e0
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/24/2018
---
# <a name="slicers-in-power-bi-service-tutorial"></a>Slicers in Power BI-service (zelfstudie)
Uw adjunct-directeur van Verkoop wil een aantal metrische gegevens kunnen inzien, voor de gehele afdeling en voor elke afzonderlijke District Manager. Ze kon voor elke manager een aparte rapportpagina maken, of ze kon een slicer gebruiken. Een slicer beperkt het gedeelte van de gegevensset die wordt weergegeven in de andere visualisaties op de pagina.  Slicers bieden een alternatieve manier voor filteren.

![](media/power-bi-visualization-slicers/slicer2.gif)

## <a name="when-to-use-a-slicer"></a>Een slicer gebruiken
Slicers zijn een goede keuze in de volgende situaties.

* Als u veelgebruikte of belangrijke filters op het rapportcanvas voor een eenvoudigere toegang wilt weergeven.
* Als u de huidige gefilterde status gemakkelijker wilt bekijken zonder dat u een vervolgkeuzelijst hoeft te openen om de gefilterde informatie te vinden.
* Als u kolommen die u niet nodig hebt, wilt verbergen maar nog wel wilt kunnen gebruiken voor het filteren - dit zorgt voor smallere en schonere tabellen.
* Als u meer gerichte rapporten wilt maken - aangezien slicers zwevende objecten zijn, kunt u ze naast het interessante deel van het rapport plaatsen waarop uw wilt dat gebruikers zich concentreren.

## <a name="create-a-slicer"></a>Een slicer maken
<iframe width="560" height="315" src="https://www.youtube.com/embed/zIZPA0UrJyA" frameborder="0" allowfullscreen></iframe>


1. Open het [Voorbeeld van een retailanalyse](sample-retail-analysis.md) in [Bewerkweergave](service-interact-with-a-report-in-editing-view.md) en [voeg een nieuwe rapportpagina toe](power-bi-report-add-page.md).
2. Selecteer in het deelvenster Velden **District > District Manager**.
   
    ![](media/power-bi-visualization-slicers/pbi_slicer_chartfirst.png)
3. De visualisatie naar een slicer converteren. Selecteer het slicerpictogram in het deelvenster Visualisaties.
   
    ![](media/power-bi-visualization-slicers/pbi_slicer_select.png)

## <a name="format-the-slicer"></a>De slicer opmaken
1. Met de slicer geselecteerd in het deelvenster Visualisaties, selecteert u het pictogram van de verfroller ![](media/power-bi-visualization-slicers/power-bi-paintroller.png) om de opmaakopties weer te geven.
2. Selecteer **Algemeen > Kleur van omtrek** en kies donkerblauw en verander het **gewicht** in **6**.
   
    ![](media/power-bi-visualization-slicers/pbi_slicer_outline2.png)
3. Onder **Selectiebesturingselementen**, staat standaard **Alles selecteren** op **Uit** en staat **Eén selecteren** op **Aan**. Dit betekent dat ik de CTRL-toets moet gebruiken om meerdere namen tegelijk te selecteren. Zet **Alles selecteren** op **Aan** en **Eén selecteren** op **Uit**.
   
    ![](media/power-bi-visualization-slicers/pbi_slicer_selectioncontrols2.png)
   
   * U ziet dat de slicer nu een optie **Alles selecteren** bovenaan de lijst heeft. Schakel **Alles selecteren** in/uit om alle namen of geen van de namen te selecteren.
   * En u kunt nu meer dan één naam selecteren zonder de CTRL-toets te gebruiken.
4. Onder **Items** kunt u de tekengrootte vergroten naar 14 pt.  We willen er zeker van zijn dat onze collega's deze slicer opmerken.
5. Ten slotte, stel de **Tekstkleur** in op donkerrood.  Dit zal de geselecteerde namen onderscheiden van de niet-geselecteerde namen in onze slicer.
   
    ![](media/power-bi-visualization-slicers/pbi_slicer_font2.png)
6. Veel plezier met het verkennen van de andere beschikbare opties voor slicers.

## <a name="use-the-slicer-in-a-report"></a>De slicer in een rapport gebruiken
1. Voeg een aantal extra visualisaties toe aan de rapportpagina of open het [Voorbeeldrapport van een retailanalyse](sample-retail-analysis.md) en selecteer het tabblad **Regionale maandelijkse verkoop**.
   
    ![](media/power-bi-visualization-slicers/power-bi-retail-sample.png)
2. Segmenteer de rapportagepagina voor Carlos. U ziet hoe de andere visualisaties worden bijgewerkt om deze selecties weer te geven.
   
    ![](media/power-bi-visualization-slicers/slicer2.gif)
3. Sorteer de slicer alfabetisch op de achternaam van de District Manager.  Selecteer de weglatingstekens (...) in de rechterbovenhoek van de slicer en kies **District Manager**.
   
    ![](media/power-bi-visualization-slicers/pbi_slicer_sort2.png)
   
    ![](media/power-bi-visualization-slicers/pbi_slicer_sorted.png)

## <a name="control-what-effect-the-slicer-has-on-other-visuals-on-the-page"></a>Bepalen welk effect de slicer heeft op andere visuele elementen op de pagina
Wilt u dat de slicer alleen een aantal visuele elementen op de rapportpagina filtert?  Gebruik het besturingselement **Visuele interacties** om deze functie in te stellen.

**Opmerking**: als er geen **Visuele interacties** zijn, zoek dan naar het bijbehorende pictogram![](media/power-bi-visualization-slicers/power-bi-slicer-visual-interactions.png). Als u geen van beiden ziet, controleer dan of u in de [bewerkingsweergave](service-reading-view-and-editing-view.md) van een rapport bent.

1. Selecteer de slicer om deze te activeren en kies in de menubalk **Visuele interacties**.
   
    ![](media/power-bi-visualization-slicers/pbi-slicer-interactions.png)
2. Filterbesturingselementen verschijnen boven alle andere visuele elementen op de pagina. Als de slicer een visueel element moet filteren, selecteert u het **Filterpictogram**.  Als de slicer geen invloed mag hebben op het visuele element, selecteert u het pictogram **Geen**.
   
    ![](media/power-bi-visualization-slicers/filter-controls.png)

Zie [Visuele interacties in een Power BI-rapport](service-reports-visual-interactions.md) voor meer informatie.

## <a name="considerations-and-troubleshooting-slicers-in-power-bi"></a>Overwegingen en probleemoplossing bij slicers in Power BI
Er zijn enkele beperkingen bij het gebruik van slicers in Power BI, namelijk de volgende:

1. Slicers bieden geen ondersteuning voor invoervelden.
2. Een enkele slicer kan niet worden gebruikt binnen een volledig rapport. Een slicer geldt alleen voor de huidige pagina.
3. Slicers kunnen niet worden vastgemaakt aan een dashboard.
4. Detailweergave wordt niet ondersteund voor slicers.    
5. Slicers bieden geen ondersteuning voor filters op niveau van visuele elementen.

Hebt u ideeën voor het verbeteren van Power BI? [Een idee verzenden](https://ideas.powerbi.com/forums/265200-power-bi-ideas).

## <a name="next-steps"></a>Volgende stappen
 [Een visualisatie toevoegen aan een rapport](power-bi-report-add-visualizations-i.md)

 [Typen visualisaties in Power BI](power-bi-visualization-types-for-reports-and-q-and-a.md)

 [Power BI - basisconcepten](service-basic-concepts.md)

[Probeer het uit, het is gratis.](https://powerbi.com/)

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

