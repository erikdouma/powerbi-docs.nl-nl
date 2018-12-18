---
title: De interactie tussen visuals in een rapport begrijpen
description: Documentatie voor Power BI-eindgebruikers waarin wordt uitgelegd hoe visuals op een rapportpagina werken.
author: mihart
manager: kvivek
ms.custom: seodec18
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 12/06/2018
ms.author: mihart
LocalizationGroup: Reports
ms.openlocfilehash: 406f1f6428d5ce26401720220eaffe32314a9bbd
ms.sourcegitcommit: cd85d88fba0d9cc3c7a4dc03d2f35d2bd096759b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/12/2018
ms.locfileid: "53280415"
---
# <a name="how-visuals-cross-filter-each-other-in-a-power-bi-report"></a>Hoe visuele elementen elkaar kruislings filteren in een Power BI-rapport
Een van de geweldige functies van Power BI is de manier waarop alle visuals op een rapportpagina onderling zijn verbonden. Als u een gegevenspunt in een van deze visuals selecteert, worden alle andere visuals op de pagina die deze gegevens bevatten, gewijzigd op basis van deze selectie. 

![video van hoe visuals onderling werken](media/end-user-interactions/interactions.gif)

Visualisaties op een rapportpagina kunnen standaard worden gebruikt voor het kruislings filteren, kruislings markeren, en zoomen van de andere visualisaties op de pagina. Als u bijvoorbeeld een staat op een kaartvisualisatie selecteert, kan de kolomdiagram zo worden gemarkeerd en de lijndiagram zo gefilterd dat alleen de gegevens worden weergegeven die van toepassing zijn op deze staat.

Zie [Over filteren en markeren](../power-bi-reports-filters-and-highlighting.md). En als u een visualisatie hebt die ondersteuning biedt voor [analyseren](../power-bi-visualization-drill-down.md), heeft het analyseren van één visualisatie standaard geen invloed op de andere visualisaties op de rapportpagina. 

Hoe de visuals op een pagina precies samenwerken, wordt ingesteld door de *rapportontwerper*. Ontwerpers kunnen visuele interacties in- en uitschakelen, en de standaardinstellingen voor kruislings filteren, kruislings markeren en zoomen wijzigen.
  
> [!NOTE]
> De termen *kruislings filteren* en *kruislings markeren* worden gebruikt om de hier beschreven werking te onderscheiden van wat er gebeurt wanneer u het venster **Filters** gebruikt en visualisaties markeert.  

### <a name="next-steps"></a>Volgende stappen
[How to use report filters](../power-bi-how-to-report-filter.md) (Rapportfilters gebruiken)
