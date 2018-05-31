---
title: Eenvoudig vlakdiagram
description: Eenvoudig vlakdiagram.
services: powerbi
documentationcenter: ''
author: mihart
manager: kfile
backup: ''
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 01/20/2018
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: 62d518b923d541ee937f485da946ae08b20fa386
ms.sourcegitcommit: 493f160d04ed411ff4741c599adc63ba1f65230f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2018
ms.locfileid: "33811800"
---
# <a name="basic-area-chart"></a>Eenvoudig vlakdiagram
Het eenvoudige vlakdiagram (ook wel gelaagd vlakdiagram genoemd) is gebaseerd op het lijndiagram. Het gebied tussen as en lijn wordt gevuld met kleuren om het volume aan te geven. 

Vlakdiagrammen benadrukken de mate van wijzigingen in de loop van de tijd en kunnen worden gebruikt om de aandacht te vestigen op de totale waarde voor een trend. Gegevens die bijvoorbeeld de winst in de loop van de tijd voorstellen, kunnen worden afgezet in een vlakdiagram om de totale winst te benadrukken.

![](media/power-bi-visualization-basic-area-chart/powerbi-area-chartnew.png)

## <a name="when-to-use-a-basic-area-chart"></a>Wanneer wordt een eenvoudig vlakdiagram gebruikt?
In de volgende gevallen komen eenvoudige vlakdiagrammen goed van pas:

* om de volumetrend in een tijdreeks te bekijken en te vergelijken 
* voor afzonderlijke reeksen die een fysiek telbare verzameling voorstellen

### <a name="prerequisites"></a>Vereisten
 - Power BI-service
 - Voorbeeld van een retailanalyse

Meld u aan bij Power BI als u mee wilt doen en selecteer achtereenvolgens **Gegevens ophalen\> Voorbeelden \> Voorbeeld van een retailanalyse > Verbinding maken** en kies **Naar dashboard gaan**. 

## <a name="create-a-basic-area-chart"></a>Een eenvoudig vlakdiagram maken
 

1. Selecteer op het dashboard Voorbeeld van een retailanalyse de tegel **Totaal aantal winkels** om het rapport Voorbeeld van een retailanalyse te openen.
2. Selecteer **Rapport bewerken** om het rapport in de bewerkingsweergave te openen.
3. Voeg een nieuwe pagina toe door onder aan het rapport het gele pluspictogram (+) te selecteren.
4. Maak een vlakdiagram waarin de omzet van dit jaar en die van vorig jaar per maand worden weergegeven.
   
   a. Selecteer in het deelvenster VELDEN achtereenvolgens **Verkoop \> Omzet vorig jaar** en **Omzet dit jaar > Waarde**.

   ![](media/power-bi-visualization-basic-area-chart/power-bi-bar-chart.png)

   b.  Converteer het diagram naar een elementair vlakdiagram door het pictogram Vlakdiagram te selecteren in het deelvenster VISUALISATIES.

   ![](media/power-bi-visualization-basic-area-chart/convertchart.png)
   
   c.  Selecteer **Tijd\> Maand** om deze waarde toe te voegen aan de bron **As**.   
   ![](media/power-bi-visualization-basic-area-chart/powerbi-area-chartnew.png)
   
   d.  Selecteer het beletselteken (rechtsboven in het visuele element) en kies **Sorteren op maand** om de waarden in de grafiek per maand weer te geven.

## <a name="highlighting-and-cross-filtering"></a>Markeren en kruislings filteren
Zie [Een filter aan een rapport toevoegen](power-bi-report-add-filter.md) voor informatie over het gebruik van het deelvenster FILTERS.

Selecteer een bepaald gebied of de bovenrand ervan in uw diagram als u dat gebied wilt markeren.  Als er zich in tegenstelling tot andere visualisatietypen andere visualisaties op dezelfde pagina bevinden, worden andere visualisaties op de rapportpagina niet kruislings gefilterd wanneer er een eenvoudige vlakdiagrammen worden gemarkeerd. Vlakdiagrammen zijn echter wel een doel voor kruislings filteren dat door andere visualisaties op de rapportpagina wordt geactiveerd. Zie [Interacties van visuals in rapporten](service-reports-visual-interactions.md) voor meer informatie.

## <a name="considerations-and-troubleshooting"></a>Aandachtspunten en probleemoplossing
* Met eenvoudige vlakdiagrammen kunnen waarden die het gevolg zijn van bedekking op de gelaagde vlakken niet effectief worden vergeleken. Power BI maakt gebruik van transparantie om de overlapping van gebieden aan te geven. Dit werkt echter alleen goed met twee of drie verschillende vlakken. Als u trends voor drie of meer metingen wilt vergelijken, kunt u lijndiagrammen gebruiken. Als u volumes voor drie of meer metingen wilt vergelijken, kunt u treemapgrafieken gebruiken.

## <a name="next-steps"></a>Volgende stappen
[Rapporten in Power BI](service-reports.md)  
[Visualisaties in Power BI-rapporten](power-bi-report-visualizations.md)  
[Power BI - basisconcepten](service-basic-concepts.md)  
Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

