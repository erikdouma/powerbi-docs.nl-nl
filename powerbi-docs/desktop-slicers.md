---
title: Slicers gebruiken in Power BI Desktop
description: In Power BI Desktop kunt u slicers gebruiken om rapporten te filteren, markeren en aan te passen
services: powerbi
documentationcenter: ''
author: davidiseminger
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
ms.date: 05/08/2018
ms.author: davidi
LocalizationGroup: Create reports
ms.openlocfilehash: 734ee85977dbde709f6e78eda72e9a0d3658adb4
ms.sourcegitcommit: 509be8852ba7595b9441c9479224f9dca298b26d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/09/2018
---
# <a name="using-slicers-power-bi-desktop"></a>Slicers gebruiken in Power BI Desktop

U kunt een **slicer** gebruiken in **Power BI Desktop** om de resultaten van visuals op uw rapportpagina te filteren. En met slicers kunt u het filter dat door interactie met de slicer zelf wordt toegepast, gemakkelijk aanpassen. U kunt ook opties opgeven voor hoe uw slicer wordt weergegeven en hoe u er interactie mee hebt. De volgende afbeelding toont een slicer waarbij de vervolgkeuzelijst met *typen* zichtbaar is. 

![slicers in Desktop](media/desktop-slicers/desktop-slicers_01.png)

Een slicer kan worden weergegeven door middel van verschillende typen weergaven:

* Lijst
* Vervolgkeuzelijst
* Tussen
* Kleiner dan of gelijk aan
* Groter dan of gelijk aan

U kunt een slicer aan een rapport toevoegen door op de **slicer**-visual te klikken in het deelvenster **Visualisaties**.

![het visuele type slicer](media/desktop-slicers/desktop-slicers_02.png)

Slicers gedragen zich op dezelfde manier in **Power BI Desktop** en **Power BI-service**. Voor een artikel over het gebruik van slicers raadpleegt u [Slicers in de Power BI-service](power-bi-visualization-slicers.md).

## <a name="synchronize-slicers-across-report-pages"></a>Slicers synchroniseren op meerdere rapportpagina's

In **Power BI Desktop** kunt u slicers synchroniseren op meerdere rapportpagina's. Selecteer **Slicers synchroniseren** in het deelvenster **Weergave** op het lint om slicers te synchroniseren. Als u slicers synchroniseert, verschijnt het deelvenster **Slicers synchroniseren** zoals dat in de volgende afbeelding wordt weergegeven.

![het deelvenster Slicers synchroniseren weergeven](media/desktop-slicers/desktop-slicers_03.png)

In het deelvenster **Slicers synchroniseren** kunt u opgeven hoe de slicer op meerdere rapportpagina's moet worden gesynchroniseerd. U kunt opgeven of elke slicer op elke afzonderlijke rapportpagina moet worden **toegepast** en of de slicer op elke afzonderlijke rapportpagina **zichtbaar** moet zijn.

U kunt bijvoorbeeld een slicer plaatsen op **pagina 2** van uw rapport, zoals dat in de volgende afbeelding wordt weergegeven. Vervolgens kunt u selecteren of die slicer *van toepassing* moet zijn op alle geselecteerde pagina's en of die slicer *zichtbaar* moet zijn op alle geselecteerde pagina's in het rapport. Voor elke slicer kunt u alle mogelijke combinaties van deze opties kiezen. 

![slicers synchroniseren](media/desktop-slicers/desktop-slicers_04.png)

Met de koppeling **Aan alles toevoegen** in het deelvenster kunt u de geselecteerde slicer toepassen op alle pagina's in het rapport.


Houd er rekening mee dat de selecties in het deelvenster **Slicers synchroniseren** alleen op de *geselecteerde slicer* van toepassing zijn. U kunt meerdere slicers op verschillende pagina's toepassen en het deelvenster gebruiken om voor elke slicer afzonderlijk te bepalen hoe die wordt toegepast op de verschillende pagina's in uw rapport. 

Hoewel uw selectie van slicers kan worden gesynchroniseerd, kunnen andere instellingen zoals vormgeving, bewerken en verwijderen *niet* worden gesynchroniseerd. 

## <a name="advanced-options-for-slicers"></a>Geavanceerde opties voor slicers

U kunt ook een **groepsnaam** toepassen op een verzameling slicers in de sectie **Geavanceerde opties** van het deelvenster **Slicers synchroniseren** en slicers die dezelfde groep delen op meerdere pagina’s laten synchroniseren. 

![groepsnaam voor slicers](media/desktop-slicers/desktop-slicers_05.png)

Met deze functie kunt u een aangepaste groep slicers maken om deze synchroon te houden. Er wordt een standaardnaam opgegeven, maar u kunt elke gewenste naam gebruiken. 

De groepsnaam biedt extra flexibiliteit met slicers. U kunt afzonderlijke groepen maken om slicers die hetzelfde veld gebruiken te synchroniseren of slicers die verschillende velden gebruiken in dezelfde groep plaatsen. 


## <a name="next-steps"></a>Volgende stappen

Wellicht bent u ook geïnteresseerd in de volgende artikelen:

* [Slicers in de Power BI-service](power-bi-visualization-slicers.md)
* [De slicer voor numeriek bereik in Power BI Desktop gebruiken](desktop-slicer-numeric-range.md)
* [Een relatieve datumslicer en -filter in Power BI Desktop gebruiken](desktop-slicer-filter-date-range.md)

