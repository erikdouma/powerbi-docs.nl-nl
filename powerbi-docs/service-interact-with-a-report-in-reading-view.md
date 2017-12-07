---
title: Interactie met een rapport in de leesweergave in Power BI
description: Interactie met een rapport in de leesweergave in Power BI
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: monitoring
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 08/15/2017
ms.author: mihart
ms.openlocfilehash: 54de712e0743801b3e8c565ca997bbc56e254c69
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2017
---
# <a name="interact-with-a-report-in-reading-view-in-power-bi"></a>Interactie met een rapport in de leesweergave in Power BI
## <a name="reading-view"></a>Leesweergave
De leesweergave is niet zo interactief als de [bewerkweergave](service-interact-with-a-report-in-editing-view.md), maar toch hebt u hier veel mogelijkheden om uw gegevens te verkennen. Dit is handig als u rapporten weergeeft [die met u zijn gedeeld](service-share-dashboards.md) en die alleen kunnen worden geopend in de leesweergave.

Leesweergave is een plezierige en veilige manier om te oefenen en om inzicht in uw gegevens te krijgen. In de leesweergave kunt u visuals op een pagina kruislings markeren en filteren.  U hoeft alleen maar een waarde in de ene visual te markeren of selecteren en u ziet meteen de gevolgen hiervan voor de andere visuals. Gebruik het filtervenster om op een rapportpagina filters toe te voegen of te wijzigen en wijzig de manier waarop waarden in een visualisatie zijn gesorteerd. Het filteren en markeren wordt niet opgeslagen met het rapport.

## <a name="cross-highlight-the-related-visualizations-on-a-page"></a>De verwante visualisaties op een pagina kruislings markeren
De visualisaties op één rapportpagina zijn allemaal met elkaar 'verbonden'.  Dit betekent dat als u een of meer waarden in een visualisatie selecteert, andere visualisaties die gebruikmaken van dezelfde waarde op basis van die selectie worden gewijzigd.

![](media/service-interact-with-a-report-in-reading-view/pagefilter3b.gif)

> [!NOTE]
> Selecteer meer dan een element in een visualisatie door de CTRL-toets ingedrukt te houden.
> 
> 

## <a name="hover-over-visual-elements-to-see-the-details"></a>De muisaanwijzer over visuele elementen bewegen om meer informatie weer te geven
![](media/service-interact-with-a-report-in-reading-view/amarillachart.png)

## <a name="sort-the-data-in-a-visualization"></a>De gegevens in een visualisatie sorteren
Selecteer het beletselteken (...) om **Sorteren op** te openen. Selecteer de pijl om te kiezen op welk veld moet worden geselecteerd of selecteer het pictogram AZ om te schakelen tussen oplopende en aflopende volgorde. 

![](media/service-interact-with-a-report-in-reading-view/pbi_changechartsort.gif) 

## <a name="interact-with-filters"></a>Interactie met filters
Als de auteur van het rapport filters aan een pagina in een rapport heeft toegevoegd, kunt u deze gebruiken in de leesweergave. De wijzigingen die u aanbrengt, worden niet met het rapport opgeslagen.

1. Selecteer het filterpictogram in de rechterbovenhoek.
   
   ![](media/service-interact-with-a-report-in-reading-view/filters.png)  
2. Hierop worden alle filters weergegeven die zijn toegepast op de visual die u hebt geselecteerd (Filters op niveau van visuele elementen), op de hele rapportpagina (Filters op paginaniveau) en binnen het hele rapport (Filters op rapportniveau).
   
   ![](media/service-interact-with-a-report-in-reading-view/power-bi-reading-filters.png)
3. Beweeg de muisaanwijzer over een filter en vouw het filter uit door de pijl-omlaag te selecteren.
   
   ![](media/service-interact-with-a-report-in-reading-view/power-bi-expan-filter.png)
4. Breng wijzigingen aan de filters aan en controleer hoe de visuals worden beïnvloed.  
   
   * In dit voorbeeld is er sprake van een filter op paginaniveau voor **Chain**. Wijzig dit in **Fashions Direct** in plaats van **Lindseys** door het vinkje bij het ene item te verwijderen en aan het andere toe te voegen.
     
     ![](media/service-interact-with-a-report-in-reading-view/power-bi-filter-chain.png)
   * Of verwijder het filteren op **Chain** helemaal door het gumpictogram ![](media/service-interact-with-a-report-in-reading-view/power-bi-eraser-icon.png) te selecteren of door beide winkelketens te selecteren.
   * Selecteer het filter op paginaniveau **District** en schakel over naar **Geavanceerd filteren**. Filter om alleen districten weer te geven die beginnen met **FD** en die niet het getal 4 bevatten.
     
     ![](media/service-interact-with-a-report-in-reading-view/power-bi-advanced-filter.png)

Zie [Een filter toevoegen aan een rapport](power-bi-report-add-filter.md) en [Over filters en markeren in rapporten](power-bi-reports-filters-and-highlighting.md) voor meer informatie.

## <a name="zoom-in-on-individual-visuals"></a>Inzoomen op afzonderlijke visuals
Beweeg de muisaanwijzer over een visual en selecteer het pictogram **Focusmodus** ![](media/service-interact-with-a-report-in-reading-view/pbi_popouticon.jpg). Wanneer u een visualisatie in de focusmodus bekijkt, wordt deze uitgebreid om het volledige rapportcanvas te vullen zoals hieronder wordt weergegeven.

![](media/service-interact-with-a-report-in-reading-view/powerbi-focus-mode.png)

Als u dezelfde visualisatie zonder de afleiding van menubalken, het filtervenster en dergelijke wilt zien, selecteert u het pictogram **Volledig scherm** op de bovenste menubalk  ![](media/service-interact-with-a-report-in-reading-view/power-bi-focus-icon.png)  .

![](media/service-interact-with-a-report-in-reading-view/power-bi-full-screen.png)

Zie [Focusmodus voor rapporten](service-focus-mode.md) en [Modus Volledig scherm voor rapporten](service-fullscreen-mode.md) voor meer informatie.

## <a name="adjust-the-display-dimensions"></a>De afmetingen van de weergave aanpassen
Rapporten kunnen op verschillende apparaten met verschillende schermgrootten en hoogte-breedteverhoudingen worden weergegeven.  De standaardweergave is mogelijk niet wat u op uw apparaat wilt zien.  Als u de weergave wilt aanpassen, selecteert u **Weergave** en kiest u:

* Passend op pagina: de inhoud zo schalen dat deze het beste op de pagina past
* Aan breedte aanpassen: de inhoud zo schalen dat deze het beste bij de breedte van de pagina past
* Ware grootte: de inhoud op volledige grootte weergeven  

![](media/service-interact-with-a-report-in-reading-view/power-bi-view.png)

  De weergaveoptie die u in de leesweergave selecteert, is tijdelijk. Wanneer u het rapport sluit, wordt deze niet opgeslagen.

  Zie [Zelfstudie: weergave-instellingen wijzigen in een rapport](power-bi-change-report-display-settings.md) voor meer informatie.

## <a name="next-steps"></a>Volgende stappen
[Rapporten in Power BI](service-reports.md)

[De bewerkingsweergave openen](service-reading-view-and-editing-view.md)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

