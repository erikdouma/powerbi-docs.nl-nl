---
title: Typen inzichten die door Power BI worden ondersteund
description: Snelle inzichten en inzichten weergeven met Power BI.
author: mihart
manager: kvivek
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: powerbi-consumer
ms.topic: conceptual
ms.date: 12/06/2018
ms.author: mihart
LocalizationGroup: Dashboards
ms.openlocfilehash: 216c58644ee13cc6015878fc31d83e47e5673398
ms.sourcegitcommit: a054782370dec56d49bb205ee10b7e2018f22693
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/22/2019
ms.locfileid: "56662061"
---
# <a name="types-of-insights-supported-by-power-bi"></a>Typen inzichten die door Power BI worden ondersteund
## <a name="how-does-insights-work"></a>Hoe werkt Inzichten?
Power BI doorzoekt snel verschillende subsets van uw gegevensset terwijl er tegelijkertijd een geavanceerde algoritmen worden toegepast om potentieel interessante inzichten te detecteren. Power BI probeert binnen de toegewezen hoeveelheid tijd zo veel mogelijk van een gegevensset te scannen.

U kunt inzichten uitvoeren op basis van een gegevensset of dashboardtegel.   

## <a name="what-types-of-insights-can-we-find"></a>Wat voor typen inzichten kunnen er worden gezocht?
Hier volgen enkel van de algoritmen die we gebruiken:

## <a name="category-outliers-topbottom"></a>Categorie-uitbijters (boven/onder)
Markeert gevallen, voor een meting in het model, waarbij een of twee leden van een dimensie veel hogere waarden hebben dan andere leden van de dimensie.  

![Voorbeeld van categorie-uitbijters](./media/end-user-insight-types/pbi_auto_insight_types_category_outliers.png)

## <a name="change-points-in-a-time-series"></a>Punten wijzigen in een tijdreeks
Geeft aan wanneer er belangrijke wijzigingen in trends in een tijdreeks van gegevens plaatsvinden.

![Voorbeeld van het wijzigen van punten in een tijdreeks](./media/end-user-insight-types/pbi_auto_insight_types_changepoint.png)

## <a name="correlation"></a>Correlatie
Detecteert gevallen waarbij meerdere metingen een correlatie tussen elkaar laten zien wanneer ze worden afgezet tegen een dimensie in de gegevensset.

![Voorbeeld van correlatie](./media/end-user-insight-types/pbi_auto_insight_types_correlation.png)

## <a name="low-variance"></a>Lage afwijking
Detecteert gevallen waarbij de gegevenspunten niet ver van het gemiddelde liggen.

![Voorbeeld van lage afwijking](./media/end-user-insight-types/power-bi-low-variance.png)

## <a name="majority-major-factors"></a>Meerderheid (belangrijke factoren)
Wanneer een meerderheid van de totale waarde kan worden toegeschreven aan één factor wanneer de waarde wordt onderverdeeld op basis van een andere dimensie.  

![Voorbeeld van belangrijke factoren](./media/end-user-insight-types/pbi_auto_insight_types_majority.png)

## <a name="overall-trends-in-time-series"></a>Algemene trends in Time Series
Detecteren van opwaartse of neerwaartse trends in Time Series-gegevens.

![Voorbeeld van algemene trends in Time Series](./media/end-user-insight-types/pbi_auto_insight_types_trend.png)

## <a name="seasonality-in-time-series"></a>Seizoensgebondenheid in Time Series
Hiermee worden periodieke patronen in Time Series-gegevens gedetecteerd, zoals wekelijkse, maandelijkse of jaarlijkse seizoensgebondenheid.

![Voorbeeld van seizoensgebondenheid](./media/end-user-insight-types/pbi_auto_insight_types_seasonality_new.png)

## <a name="steady-share"></a>Onveranderlijk deel
Markeert gevallen waarbij voor een continue variabele er een correlatie bestaat tussen het aandeel van de waarde van een onderliggend item in relatie tot de totale waarde van een bovenliggend item.

![Voorbeeld van onveranderlijk deel](./media/end-user-insight-types/pbi_auto_insight_types_steadyshare.png)

## <a name="time-series-outliers"></a>Time Series-uitbijters
Detecteert of er specifieke datums of tijden voor verschillende tijdreeksen zijn met waarden die aanzienlijk afwijken van de andere datum-/tijdwaarden.

![Voorbeeld van Time Series-uitbijters](./media/end-user-insight-types/pbi_auto_insight_types_time_series_outliers.png)

## <a name="next-steps"></a>Volgende stappen
[Power BI-inzichten](end-user-insights.md)

Als u de eigenaar van een gegevensset bent, kunt u deze [optimaliseren voor inzichten](../service-insights-optimize.md)

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

