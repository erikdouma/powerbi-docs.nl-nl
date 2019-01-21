---
title: Over filters en markeren in Power BI-rapporten
description: Over filters en markeren in Power BI-rapporten
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 09/28/2018
ms.author: maggies
LocalizationGroup: Reports
ms.openlocfilehash: ace392570dbabc65d128941fc735231622f2c008
ms.sourcegitcommit: c8c126c1b2ab4527a16a4fb8f5208e0f7fa5ff5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2019
ms.locfileid: "54285318"
---
# <a name="about-filters-and-highlighting-in-power-bi-reports"></a>Over filters en markeren in Power BI-rapporten
 In dit artikel wordt beschreven hoe u filters en markeringen toepast in de Power BI-service. De ervaring is echter nagenoeg hetzelfde als in Power BI Desktop. ***Filters*** zorgen ervoor dat alleen die gegevens worden weergegeven waarop u zich wilt concentreren. ***Markeren*** is geen vorm van filteren. Hiermee worden geen gegevens verwijderd, maar wordt een subset van de zichtbare gegevens gemarkeerd. De niet-gemarkeerde gegevens blijven zichtbaar maar zijn lichter van kleur.

Er zijn veel verschillende manieren om rapporten in Power BI te filteren en te markeren. Wanneer al deze informatie in één artikel zou worden gepresenteerd, zou dit alleen maar tot verwarring leiden. Daarom hebben we deze in de volgende secties opgesplitst:

* Inleiding tot filters en markeren (het artikel dat u nu leest)
* De manieren waarop u in rapporten [filters kunt maken en gebruiken in de bewerkingsweergave](power-bi-report-add-filter.md). Wanneer u over bewerkingsmachtigingen beschikt voor een rapport, kunt u filters in rapporten maken, wijzigen en verwijderen.
* De manieren waarop u in de leesweergave van rapporten [filters en markeringen kunt gebruiken in rapporten die met u zijn gedeeld](consumer/end-user-reading-view.md). De mogelijkheden zijn beperkter, maar u beschikt nog altijd over tal van filter- en markeeropties.  
* Een gedetailleerd overzicht van de [besturingselementen voor filteren en markeren die beschikbaar zijn in de bewerkingsweergave](consumer/end-user-report-filter.md), inclusief uitgebreide informatie over de typen filters (bijvoorbeeld datum en tijd, numerieke tekst) en het verschil tussen de basisopties en geavanceerde opties.
* Nu u weet hoe de standaardfilter- en markeeropties werken, vindt u hier meer informatie over het [wijzigen van de manier waarop visualisaties op een pagina elkaar filteren en markeren](consumer/end-user-interactions.md)

## <a name="intro-to-the-filters-pane"></a>Inleiding tot het deelvenster Filters

U kunt filters toepassen in het deelvenster **Filters** of door rechtstreeks in het rapport [selecties te maken in slicers](visuals/power-bi-visualization-slicers.md). Het deelvenster Filters bevat de tabellen en velden die in het rapport worden gebruikt en de filters die zijn toegepast, indien van toepassing. 

![](media/power-bi-reports-filters-and-highlighting/power-bi-add-filter-reading-view.png)

Er zijn vier soorten filters.

- **Paginafilter** wordt toegepast op alle visuals op een rapportpagina     
- **Visualfilter** wordt toegepast op één visual op een rapportpagina. U ziet filters op het niveau van visuals alleen als u een visual op het rapportcanvas hebt geselecteerd.    
- **Rapportfilter** wordt toegepast op alle pagina's in een rapport    
- **Gedetailleerde filter** wordt toegepast op één item in een rapport    

U kunt zowel in de lees- als de bewerkingsweergave zoeken in pagina-, visual- en rapportfilters, om de gewenste waarde te zoeken en te selecteren. 

![Zoeken in een filter](media/power-bi-reports-filters-and-highlighting/power-bi-search-filter.png)

Als naast het filter het woord **All** staat, betekent dit dat alle waarden in het veld zijn opgenomen in het filter.  Zo betekent **Chain (All)** (Keten (Alle)) in onderstaande schermopname dat deze rapportpagina gegevens bevat over alle winkelketens.  Het filter op rapportniveau **FiscalYear is 2013 or 2014** (Boekjaar is 2013 of 2014) betekent daarentegen dat het rapport alleen gegevens voor de boekjaren 2013 en 2014 bevat.

## <a name="filters-in-reading-or-editing-view"></a>Filters in lees- of bewerkingsweergave
U kunt in twee modi met rapporten werken: in de [leesweergave](consumer/end-user-reading-view.md) en de bewerkingsweergave. De beschikbare filtermogelijkheden zijn afhankelijk van de modus waarin u werkt.

* In de bewerkingsweergave kunt u filters voor rapporten, pagina’s, visuals en drillthrough toevoegen. Wanneer u het rapport opslaat, worden de filters samen met het rapport opgeslagen, zelfs als u het rapport in een mobiele app opent. Personen die het rapport in de leesweergave bekijken, kunnen de filters gebruiken die u hebt toegevoegd, maar kunnen geen nieuwe filters toevoegen.
* In de leesweergave kunt u de filters gebruiken die al beschikbaar zijn in het rapport. Daarnaast kunt u de door u aangebrachte selecties opslaan. U kunt geen nieuwe filters toevoegen.

### <a name="filters-in-reading-view"></a>Filters in leesweergave
Als u alleen in de leesweergave toegang hebt tot een rapport, ziet het deelvenster Filters er ongeveer als volgt uit:

![](media/power-bi-reports-filters-and-highlighting/power-bi-filter-reading-view.png)

Deze pagina van het rapport bevat dus zes filters op paginaniveau en één filter op rapportniveau.

Elke visual kan filters hebben voor alle velden in de visual, en de auteur van het rapport kan meer filters toevoegen. In de onderstaande afbeelding ziet u een bellendiagram waarop zes filters zijn toegepast.

![](media/power-bi-reports-filters-and-highlighting/power-bi-filter-visual-level.png)

Verken de gegevens in de leesweergave door de bestaande filters te wijzigen. De wijzigingen die u aanbrengt, worden samen met het rapport opgeslagen, zelfs als u het rapport in een mobiele app opent. Tijdens een [rondleiding door het deelvenster Filters van het rapport](consumer/end-user-report-filter.md) leert u hoe u dit doet.

Wanneer u het rapport afsluit, worden uw filters opgeslagen. Als u uw filters ongedaan wilt maken en wilt terugkeren naar de standaardfilters, slicers, zoomwaarden en sorteervolgorde die door de auteur van het rapport zijn ingesteld, selecteert u **Standaardinstelling herstellen** in de bovenste menubalk.

![](media/power-bi-reports-filters-and-highlighting/power-bi-reset-to-default.png)

### <a name="filters-in-editing-view"></a>Filters in de bewerkingsweergave
Wanneer u over eigenaarsmachtigingen voor een rapport beschikt en het rapport opent in de leesweergave, ziet u dat **Filters** slechts een van de vele beschikbare deelvensters is.

![](media/power-bi-reports-filters-and-highlighting/power-bi-add-filter-editing-view.png)

Net als in de leesweergave ziet u dat deze pagina van het rapport zes filters op paginaniveau en één filter op rapportniveau heeft. En als u het bellendiagram selecteert, ziet u dat er zes filters op visualniveau zijn toegepast.

In de leesweergave kunt u meer doen met filters en markeringen. U kunt voornamelijk nieuwe filters toevoegen. Meer informatie over [Een filter toevoegen aan een rapport](power-bi-report-add-filter.md) en nog veel meer.

## <a name="ad-hoc-highlighting"></a>Ad-hoc-markeringen
Selecteer een veld op het rapportcanvas om de andere visuals op de pagina te markeren. Selecteer een lege ruimte in hetzelfde visuele element om deze te verwijderen. Dit type markeringen is een leuke manier om snel de impact van gegevens te verkennen. Zie [Interacties tussen visuals](consumer/end-user-interactions.md) als u de werking wilt verfijnen van dit type kruislings toegepaste markeringen.

![](media/power-bi-reports-filters-and-highlighting/power-bi-adhoc-filter.gif)


## <a name="next-steps"></a>Volgende stappen
[Een filter toevoegen aan een rapport (in de bewerkingsweergave)](power-bi-report-add-filter.md)

[Een overzicht van de rapportfilters](consumer/end-user-report-filter.md)

[Wijzigen hoe visuele rapportelementen elkaar kruislings filteren en markeren](consumer/end-user-interactions.md)

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

