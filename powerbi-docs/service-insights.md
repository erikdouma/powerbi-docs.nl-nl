---
title: Automatisch gegevensinzichten genereren met Power BI
description: Meer informatie over het verkrijgen van inzicht in uw gegevenssets en dashboardtegels.
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: et_MLSL2sA8
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 12/06/2017
ms.author: mihart
ms.openlocfilehash: fb498f2b3320b96958467a9db851f119dba20ce7
ms.sourcegitcommit: 54da95f184dd0f7bb59bb0bc8775a1d93129b195
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/08/2017
---
# <a name="automatically-generate-data-insights-with-power-bi"></a>Automatisch gegevensinzichten genereren met Power BI
Hebt u een nieuwe gegevensset en weet niet precies waar u moet beginnen?  Moet u snel een dashboard bouwen?  Wilt u snel inzichten zoeken die u hebt gemist?

Voer Snelle inzichten uit om interessante interactieve visualisaties op basis van uw gegevens te genereren. Snelle inzichten kan worden uitgevoerd op een volledige gegevensset (Snelle inzichten) of op een specifieke dashboardtegel (Scoped inzichten). U kunt inzichten zelfs uitvoeren op een inzicht.

> **Opmerking**: inzichten werken niet met DirectQuery. Ze werken alleen met gegevens die zijn geüpload naar Power BI.
> 
> 

De functie voor inzichten is gebouwd op een groeiende [set geavanceerde analytische algoritmen](service-insight-types.md) die zijn ontwikkeld samen met Microsoft Research. We blijven Microsoft Research gebruiken om ervoor te zorgen dat meer mensen op nieuwe en intuïtieve manieren inzichten in hun gegevens kunnen vinden.

## <a name="run-quick-insights-on-a-dataset"></a>Snelle inzichten uitvoeren op een gegevensset
Kijk hoe Amanda snelle inzichten uitvoert op een gegevensset, een inzicht opent in de focusmodus, een van de inzichten vastmaakt aan haar dashboard en vervolgens inzichten verkrijgt voor haar dashboardtegel.

<iframe width="560" height="315" src="https://www.youtube.com/embed/et_MLSL2sA8" frameborder="0" allowfullscreen></iframe>


Nu is het uw beurt. Verken inzichten door gebruik te maken van het de [voorbeeld van kwaliteitsanalyse van leveranciers](sample-supplier-quality.md).

1. Selecteer op het tabblad **Gegevenssets** het beletselteken (...) en kies **Inzichten verkrijgen**.
   
    ![](media/service-insights/power-bi-ellipses.png)
   
    ![](media/service-insights/power-bi-tab.png)
2. Er worden [verschillende algoritmen](service-insight-types.md) in Power BI gebruikt om trends in uw gegevensset te zoeken.
   
    ![](media/service-insights/pbi_autoinsightssearching.png)
3. Uw inzichten zijn binnen enkele seconden klaar.  Selecteer **Inzichten weergeven** om visualisaties weer te geven.
   
    ![](media/service-insights/pbi_autoinsightsuccess.png)
   
   > **Opmerking**: met sommige gegevenssets kunt u geen inzichten genereren, omdat de gegevens niet statistisch significant zijn.  Zie [Uw gegevens optimaliseren voor inzichten](service-insights-optimize.md) voor meer informatie.
   > 
   > 
1. De visualisaties worden weergeven op een speciaal canvas voor **Snelle inzichten** met maximaal 32 afzonderlijke kaarten met inzichten. Elke kaart bevat een grafiek of diagram plus een korte beschrijving.
   
    ![](media/service-insights/power-bi-insights.png)

## <a name="interact-with-the-insight-cards"></a>Interactie met de kaarten met inzichten
  ![](media/service-insights/pbi_hover.png)

1. Beweeg de muisaanwijzer over de kaart en selecteer het speldpictogram om de visualisatie toe te voegen aan een dashboard.
2. Beweeg de muisaanwijzer over een kaart, selecteer het beletselteken (...) en kies **Inzichten weergeven**. Hiermee opent u het inzicht in een volledig scherm.
   
    ![](media/service-insights/power-bi-insight-focus.png)
3. In de focusmodus kunt u het volgende:
   
   * De visualisaties [filteren](service-interact-with-a-report-in-reading-view.md).  Selecteer de pijl in de rechterbovenhoek van het deelvenster Filters om de filters weer te geven.
     
        ![](media/service-insights/power-bi-insights-filter-new.png)
   * Maak de kaar met inzichten vast aan een dashboard door het speldpictogram ![](media/service-insights/power-bi-pin-icon.png) of **Visueel element vastmaken** te selecteren.
   * Voer inzichten uit op de kaart zelf. Dit wordt vaak aangeduid als **scoped inzichten**. Selecteer in de rechterbovenhoek het gloeilamppictogram ![](media/service-insights/power-bi-bulb-icon.png) of selecteer **Inzichten verkrijgen**.
     
       ![](media/service-insights/pbi-autoinsights-tile.png)
     
     Het inzicht wordt aan de linkerkant weergegeven en de nieuwe kaarten, die uitsluitend zijn gebaseerd op dit ene inzicht, worden aan de rechterkant weergegeven.
     
       ![](media/service-insights/power-bi-insights-on-insights-new.png)
4. Selecteer in de linkerbovenhoek **Focusmodus sluiten** om terug te keren naar het oorspronkelijk canvas inzichten.

## <a name="run-insights-on-a-dashboard-tile"></a>Inzichten uitvoeren op een dashboardtegel
In plaats dat u inzichten zoekt in een complete gegevensset, kunt u uw zoekopdracht afbakenen tot de gegevens die zijn gebruikt om een dashboardtegel te maken. Ook dit wordt vaak aangeduid als **scoped inzichten**.

1. Open een dashboard.
2. Beweeg de muisaanwijzer over een tegel. Selecteer het beletselteken (...) en kies **Inzichten verkrijgen**. De tegel wordt geopend in de [focusmodus](service-focus-mode.md) met de kaarten voor inzichten weergegeven aan de rechterkant.    
   
    ![](media/service-insights/pbi-insights-tile.png)    
4. Wekt een bepaald inzicht uw interesse? Selecteer deze kaart om dieper te graven. Het geselecteerde inzicht wordt aan de linkerkant weergegeven en de nieuwe kaarten met inzichten, die uitsluitend zijn gebaseerd op dit ene inzicht, worden aan de rechterkant weergegeven.    
6. Blijf in uw gegevens spitten, en wanneer u een interessant inzicht hebt gevonden, kunt u dit vastmaken aan uw dashboard door in de rechterbovenhoek **Visueel element vastmaken** te selecteren.

## <a name="next-steps"></a>Volgende stappen
Als u de eigenaar van een gegevensset bent, kunt u deze [optimaliseren voor Snelle inzichten](service-insights-optimize.md)

Meer informatie over de [typen Snelle inzichten die beschikbaar zijn](service-insight-types.md)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

