---
title: Typen inzichten die door Power BI worden ondersteund
description: Snelle inzichten en inzichten weergeven met Power BI.
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
ms.date: 12/20/2017
ms.author: mihart
ms.openlocfilehash: 53e5e67da9bacd9fc9dcbb770747823647aa3a3c
ms.sourcegitcommit: 6ea8291cbfcb7847a8d7bc4e2b6abce7eddcd0ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/21/2017
---
# <a name="types-of-insights-supported-by-power-bi"></a>Typen inzichten die door Power BI worden ondersteund
## <a name="how-does-insights-work"></a>Hoe werkt Inzichten?
Power BI doorzoekt snel verschillende subsets van uw gegevensset terwijl er tegelijkertijd een geavanceerde algoritmen worden toegepast om potentieel interessante inzichten te detecteren. Power BI probeert binnen de toegewezen hoeveelheid tijd zo veel mogelijk van een gegevensset te scannen.

U kunt inzichten uitvoeren op basis van een gegevensset of dashboardtegel.   

## <a name="what-types-of-insights-can-we-find"></a>Wat voor typen inzichten kunnen er worden gezocht?
Hier volgen enkel van de algoritmen die we gebruiken:

## <a name="category-outliers-topbottom"></a>Categorie-uitbijters (boven/onder)
Markeert gevallen, voor een meting in het model, waarbij een of twee leden van een dimensie veel hogere waarden hebben dan andere leden van de dimensie.  

![](media/service-insight-types/pbi_auto_insight_types_category_outliers.png)

## <a name="change-points-in-a-time-series"></a>Punten wijzigen in een tijdreeks
Geeft aan wanneer er belangrijke wijzigingen in trends in een tijdreeks van gegevens plaatsvinden.

![](media/service-insight-types/pbi_auto_insight_types_changepoint.png)

## <a name="correlation"></a>Correlatie
Detecteert gevallen waarbij meerdere metingen een correlatie tussen elkaar laten zien wanneer ze worden afgezet tegen een dimensie in de gegevensset.

![](media/service-insight-types/pbi_auto_insight_types_correlation.png)

## <a name="low-variance"></a>Lage afwijking
Detecteert gevallen waarbij de gegevenspunten niet ver van het gemiddelde liggen.

![](media/service-insight-types/power-bi-low-variance.png)

## <a name="majority-major-factors"></a>Meerderheid (belangrijke factoren)
Wanneer een meerderheid van de totale waarde kan worden toegeschreven aan één factor wanneer de waarde wordt onderverdeeld op basis van een andere dimensie.  

![](media/service-insight-types/pbi_auto_insight_types_majority.png)

## <a name="overall-trends-in-time-series"></a>Algemene trends in Time Series
Detecteren van opwaartse of neerwaartse trends in Time Series-gegevens.

![](media/service-insight-types/pbi_auto_insight_types_trend.png)

## <a name="seasonality-in-time-series"></a>Seizoensgebondenheid in Time Series
Hiermee worden periodieke patronen in Time Series-gegevens gedetecteerd, zoals wekelijkse, maandelijkse of jaarlijkse seizoensgebondenheid.

![](media/service-insight-types/pbi_auto_insight_types_seasonality_new.png)

## <a name="steady-share"></a>Onveranderlijk deel
Markeert gevallen waarbij voor een continue variabele er een correlatie bestaat tussen het aandeel van de waarde van een onderliggend item in relatie tot de totale waarde van een bovenliggend item.

![](media/service-insight-types/pbi_auto_insight_types_steadyshare.png)

## <a name="time-series-outliers"></a>Time Series-uitbijters
Detecteert of er specifieke datums of tijden voor verschillende tijdreeksen zijn met waarden die aanzienlijk afwijken van de andere datum-/tijdwaarden.

![](media/service-insight-types/pbi_auto_insight_types_time_series_outliers.png)

## <a name="next-steps"></a>Volgende stappen
[Power BI-inzichten](service-insights.md)

Als u de eigenaar van een gegevensset bent, kunt u deze [optimaliseren voor inzichten](service-insights-optimize.md)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

