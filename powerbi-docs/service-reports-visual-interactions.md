---
title: De interactie van visuals in een rapport wijzigen
description: Documentatie voor het instellen van interacties van visuals in een Microsoft Power BI-rapport.
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: N_xYsCbyHPw
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 09/25/2017
ms.author: mihart
ms.openlocfilehash: 126bd40e98a88138a2732155f9792d65666e52c7
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2017
---
# <a name="visualization-interactions-in-a-power-bi-report"></a>Visualisatie-interacties in een Power BI-rapport
Visualisaties op een rapportpagina kunnen standaard worden gebruikt voor het kruislings filteren en markeren van de andere visualisaties op de pagina.
Als u bijvoorbeeld een staat op een kaartvisualisatie selecteert, wordt de kolomdiagram gemarkeerd en wordt het lijndiagram zo gefilterd dat alleen de gegevens worden weergegeven die van toepassing zijn voor die staat.
Zie [Over filteren en markeren](power-bi-reports-filters-and-highlighting.md).

U kunt deze standaardwerking wijzigen met het besturingselement **Visuele interactie**. Visuele interacties is alleen beschikbaar in de [bewerkweergave](service-interact-with-a-report-in-editing-view.md). Als een rapport met u is gedeeld, hebt u geen toegang tot Visuele interacties.

> [!NOTE]
> De termen *kruislings filteren* en *kruislings markeren* worden gebruikt om de hier beschreven werking te onderscheiden van wat er gebeurt wanneer u het venster **Filters** gebruikt en visualisaties markeert.  
> 
> 

<iframe width="560" height="315" src="https://www.youtube.com/embed/N_xYsCbyHPw?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>

1. Selecteer een visualisatie om deze actief te maken.  
2. Schakel **Visuele interacties** in door de optie te selecteren op de bovenste menubalk. Zoals u ziet, worden er een filter- en markeerpictogram weergegeven wanneer u de muisaanwijzer over de andere visualisaties op de rapportpagina beweegt.
   
    ![](media/service-reports-visual-interactions/pbi-visual-interaction-icon.png)
3. Bepaal welke impact de geselecteerde visualisatie op de andere moet hebben.  
   
   * Als de andere visualisatie kruislings moet worden gefilterd, selecteert u het **filterpictogram** ![](media/service-reports-visual-interactions/pbi-filter-icon-outlined.png).
   * Als de visualisatie echter kruislings moet worden gemarkeerd, selecteert u het **markeerpictogram** ![](media/service-reports-visual-interactions/pbi-highlight-icon-outlined.png).
   * Als er niets hoeft te gebeuren, selecteert u het pictogram voor **geen impact** ![](media/service-reports-visual-interactions/pbi-noimpact-icon-outlined.png).
4. Herhaal dit eventueel voor alle andere visualisaties op de rapportpagina.

### <a name="next-steps"></a>Volgende stappen
[Rapportfilters gebruiken](power-bi-how-to-report-filter.md)

[Filters en markeren in rapporten](power-bi-reports-filters-and-highlighting.md)

[Power BI - basisconcepten](service-basic-concepts.md)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

