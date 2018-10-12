---
title: Ringdiagrammen in Power BI
description: Ringdiagrammen in Power BI
author: mihart
manager: kvivek
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 09/24/2018
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: ab292964bb1b6b1f4218d41c46eb2c28c82a034c
ms.sourcegitcommit: ce8332a71d4d205a1f005b703da4a390d79c98b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2018
ms.locfileid: "47416746"
---
# <a name="doughnut-charts-in-power-bi"></a>Ringdiagrammen in Power BI
Een ringdiagram lijkt sterk op een cirkeldiagram omdat ook hierin de relatie van de delen ten opzichte van het geheel wordt getoond. Het enige verschil is dat het midden leeg is, waardoor er ruimte is voor een label of pictogram.

## <a name="create-a-doughnut-chart"></a>Een ringdiagram maken
In deze instructies wordt het Voorbeeld van een retailanalyse gebruikt om een ringdiagram te maken waarin de verkoop van dit jaar op categorie wordt weergegeven. Om mee te lezen kunt u het [voorbeeld downloaden](../sample-datasets.md) voor de Power BI-service of voor Power BI Desktop.

1. Begin op een [nieuwe, lege rapportpagina](../power-bi-report-add-page.md). Als u de Power BI-service gebruikt, moet u het rapport openen in de [bewerkweergave](../service-interact-with-a-report-in-editing-view.md).

2. Selecteer **Verkoop** \> **Omzet van afgelopen jaar** in het deelvenster Velden.  
   
3. Selecteer in het deelvenster Visualisaties het pictogram voor het ringdiagram ![pictogram voor ringdiagram](media/power-bi-visualization-doughnut-charts/power-bi-icon.png) om uw staafdiagram te converteren naar een ringdiagram. Als **Omzet van afgelopen jaar** niet voorkomt in het gebied **Waarden**, sleept u het erheen.
     
   ![Visualisatiedeelvenster met ringdiagram geselecteerd](media/power-bi-visualization-doughnut-charts/power-bi-doughnut-chart.png)

4. Selecteer **Artikel** \> **Categorie** om deze toe te voegen aan het gebied **Legenda**. 
     
    ![ringdiagram naast het deelvenster Velden](media/power-bi-visualization-doughnut-charts/power-bi-doughnut-done.png)

5. U kunt desgewenst [de grootte en de kleur van de tekst van de grafiek aanpassen](power-bi-visualization-customize-title-background-and-legend.md). 

## <a name="considerations-and-troubleshooting"></a>Aandachtspunten en probleemoplossing
* De som van de waarden in het ringdiagram moet 100% zijn.
* Te veel categorieën zorgen er voor dat het diagram moeilijk te interpreteren is.
* Ringdiagrammen kunnen het best worden gebruikt om een bepaalde sectie met het totaal te vergelijken en niet om de afzonderlijke secties onderling te vergelijken. 

## <a name="next-steps"></a>Volgende stappen
[Trechterdiagrammen in Power BI](power-bi-visualization-funnel-charts.md)

[Visualization types in Power BI](power-bi-visualization-types-for-reports-and-q-and-a.md) (Typen visualisaties in Power BI)


