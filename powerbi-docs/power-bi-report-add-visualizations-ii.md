---
title: Deel 2, visualisaties toevoegen aan een Power BI-rapport (zelfstudie)
description: 'Zelfstudie: Deel 2, visualisaties toevoegen aan een Power BI-rapport'
services: powerbi
documentationcenter: 
author: mihart
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
ms.date: 10/28/2017
ms.author: mihart
ms.openlocfilehash: 2b3f25c772a049d10bc03941db677c67c844da8b
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2017
---
# <a name="part-2-add-visualizations-to-a-power-bi-report-tutorial"></a>Deel 2, visualisaties toevoegen aan een Power BI-rapport (zelfstudie)
In [Deel 1](power-bi-report-add-visualizations-ii.md) hebt u een eenvoudige visualisatie gemaakt door selectievakjes naast de veldnamen te selecteren.  In deel 2 leert u hoe u slepen-en-neerzetten kunt gebruiken, en hoe u gebruik kunt maken van de volledige functionaliteit van de deelvensters **Velden** en **Visualisaties** om visualisaties te maken en te wijzigen.

## <a name="create-a-new-visualization"></a>Een nieuwe visualisatie maken
In deze zelfstudie verdiepen we ons in de gegevensset voor retailanalyse en maken we een aantal belangrijke visualisaties.

### <a name="open-a-report-and-add-a-new-blank-page"></a>Open een rapport en voeg een nieuwe lege pagina toe.
1. Open de werkruimte waarin u het voorbeeld van een retailanalyse hebt opgeslagen. Selecteer **Voorbeeld van een retailanalyse** om het rapport te openen in de leesweergave.
   
   ![](media/power-bi-report-add-visualizations-ii/power-bi-open-report.png)
2. Selecteer **Rapport bewerken** om het rapport te openen in de bewerkingsweergave.
   
   ![](media/power-bi-report-add-visualizations-ii/editreport1.png)
3. [Voeg een nieuwe pagina toe](power-bi-report-add-page.md) door onder aan het tekenpapier het gele pluspictogram te selecteren.
   
   ![](media/power-bi-report-add-visualizations-ii/pbi_addreportpage.png)

### <a name="add-a-visualization-that-looks-at-this-years-sales-compared-to-last-year"></a>Voeg een visualisatie toe die een beeld geeft van de jaaromzet vergeleken met vorig jaar.
1. Selecteer in de tabel **Sales** (Omzet): **This Year Sales** (Omzet dit jaar)  > **Value** (Waarde) en **Last Year Sales** (Omzet vorig jaar). In Power BI wordt een kolomdiagram gemaakt.  Dit is interessant en u wilt graag meer details weten. Hoe ziet de omzet eruit per maand?  
   
   ![](media/power-bi-report-add-visualizations-ii/pbi_part2_4bnew.png)
2. Sleep **Month** (Maand) in de tabel Time (Tijd) naar het gebied **Axis** (As).  
   ![](media/power-bi-report-add-visualizations-ii/pbi_part2_5newnew.png)
3. [Wijzig de visualisatie](power-bi-report-change-visualization-type.md) in een vlakdiagram.  Er zijn veel visualisatietypen waaruit u kunt kiezen. Bekijk [de beschrijvingen van de typen, tips voor aanbevolen procedures en zelfstudies](power-bi-visualization-types-for-reports-and-q-and-a.md) voor hulp bij het bepalen welk type u het beste kunt gebruiken. Selecteer het vlakpictogram in het deelvenster Visualisaties.
4. Sorteer de visualisatie door het beletselteken te selecteren en **Sort by Month** (Sorteren op maand) te kiezen.
5. [Wijzig het formaat van de visualisatie](power-bi-visualization-move-and-resize.md) door de visualisatie te selecteren, en een van de cirkelomtrekken te pakken en te slepen. Maak deze groot genoeg om de schuifbalk te laten verdwijnen en klein genoeg zodat er voldoende ruimte is om nog een visualisatie toe te voegen.
   
   ![](media/power-bi-report-add-visualizations-ii/pbi_part2_7b.png)
6. [Sla het rapport op](service-report-save.md).

### <a name="add-a-map-visualization-that-looks-at-sales-by-location"></a>Een kaartvisualisatie toevoegen die de omzet per locatie weergeeft
1. Selecteer **Territory** (Territorium) in de tabel **Store** (Winkel). In Power BI wordt herkend dat Territory (Territorium) een locatie is en wordt een kaartvisualisatie gemaakt.  
   ![](media/power-bi-report-add-visualizations-ii/pbi_part2_8newnew.png)
2. Sleep **Total Stores** (Total aantal winkels) naar het gebied Size (Grootte).  
   ![](media/power-bi-report-add-visualizations-ii/power-bi-add-visual-to-a-reportnew.png)
3. Voeg een legenda toe.  Sleep **Chain** (Keten) naar het gebied Legend (Legenda) om de gegevens te bekijken per winkelnaam.  
   ![](media/power-bi-report-add-visualizations-ii/power-bi-add-visual-to-a-report-3new.png)

## <a name="next-steps"></a>Volgende stappen
* Ga naar [The report editor... take a tour](service-the-report-editor-take-a-tour.md) (De rapporteditor... een rondleiding) voor meer informatie over het deelvenster Velden.   
* Zie [Filters and highlighting in Power BI reports](power-bi-reports-filters-and-highlighting.md) (Filters en markeren in Power BI-rapporten) voor meer informatie over het filteren en markeren van visualisaties.  
* Zie [Aggregates in reports](service-aggregates.md) (Statistische functies in rapporten) voor meer informatie over het gebruiken en wijzigen van statistische functies.  
* Meer informatie over [Visualisaties in Power BI-rapporten](power-bi-report-visualizations.md).  
* Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/).

