---
title: Ringdiagrammen in Power BI (zelfstudie)
description: 'Zelfstudie: Ringdiagrammen in Power BI'
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
ms.date: 09/27/2017
ms.author: mihart
ms.openlocfilehash: 2f428095eb57c5358770f1d6d8572316d2b84c37
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2017
---
# <a name="doughnut-charts-in-power-bi-tutorial"></a>Ringdiagrammen in Power BI (zelfstudie)
Een ringdiagram lijkt sterk op een cirkeldiagram omdat ook hierin de relatie van de delen ten opzichte van het geheel wordt getoond. Het enige verschil is dat het midden leeg is, waardoor er ruimte is voor een label of pictogram.

## <a name="create-a-doughnut-chart"></a>Een ringdiagram maken
Meld u aan bij Power BI als u mee wilt doen. Selecteer achtereenvolgens **Gegevens ophalen** \> **Voorbeelden** \> **Voorbeeld van een retailanalyse** \> **Verbinding maken**. 

1. Selecteer op het dashboard de tegel **Totaal aantal winkels** om het rapport Voorbeeld van een retailanalyse te openen.
2. Selecteer **Rapport bewerken** om het rapport in de bewerkweergave te openen.
3. [Voeg een nieuwe rapportpagina toe](power-bi-report-add-page.md).
4. Maak een ringdiagram waarin de omzet van dit jaar per categorie wordt weergegeven.
   
   * Selecteer in het deelvenster **Velden** de opties **Verkoop** \> **Omzet van afgelopen jaar**.
   * Converteer naar een ringdiagram. Als Omzet van afgelopen jaar niet voorkomt in het gebied **Waarden**, sleept u het erheen.
     
       ![](media/power-bi-visualization-doughnut-charts/convertdonut.png)
   * Selecteer **Artikel** \> **Categorie** om deze toe te voegen aan het gebied **Legenda**. 
     
       ![](media/power-bi-visualization-doughnut-charts/doughnuttutorial.png)

## <a name="considerations-and-troubleshooting"></a>Overwegingen en probleemoplossing
* De som van de waarden in het ringdiagram moet 100% zijn.
* Te veel categorieën zorgen er voor dat het diagram moeilijk te interpreteren is.
* Ringdiagrammen kunnen het best worden gebruikt om een bepaalde sectie met het totaal te vergelijken en niet om de afzonderlijke secties onderling te vergelijken. 

## <a name="next-steps"></a>Volgende stappen
[Reports in Power BI](service-reports.md) (Rapporten in Power BI)

[Visualization types in Power BI](power-bi-visualization-types-for-reports-and-q-and-a.md) (Typen visualisaties in Power BI)

[Visualizations in Power BI reports](power-bi-report-visualizations.md) (Visualisaties in Power BI-rapporten)

[Power BI - Basic Concepts](service-basic-concepts.md) (Power BI - basisconcepten)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

