---
title: Rapporten verkennen in de mobiele Power BI-apps
description: 'Meer informatie over het weergeven en gebruiken van rapporten in de mobiele Power BI-app op uw telefoon of tablet. U maakt rapporten in de Power BI-service of Power BI Desktop en kunt ze vervolgens gebruiken de mobiele apps. '
services: powerbi
documentationcenter: 
author: maggiesMSFT
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
ms.date: 01/23/2018
ms.author: maggies
ms.openlocfilehash: 610234a221c5ab1de976f9d554292395760efa0f
ms.sourcegitcommit: 1a5446c3136dc0787f2a1d5b8cad1113704301ba
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/24/2018
---
# <a name="explore-reports-in-the-power-bi-mobile-apps"></a>Rapporten verkennen in de mobiele Power BI-apps
Van toepassing op:

| ![iPhone](media/mobile-reports-in-the-mobile-apps/ios-logo-40-px.png) | ![iPad](media/mobile-reports-in-the-mobile-apps/ios-logo-40-px.png) | ![Android-telefoon](media/mobile-reports-in-the-mobile-apps/android-logo-40-px.png) | ![Android-tablet](media/mobile-reports-in-the-mobile-apps/android-logo-40-px.png) | ![Windows 10-apparaten](media/mobile-reports-in-the-mobile-apps/win-10-logo-40-px.png) |
|:--- |:--- |:--- |:--- |:--- |
| iPhones |iPads |Android-telefoons |Android-tablets |Windows 10-apparaten |

Een Power BI-rapport is een interactieve weergave van uw gegevens met visuele elementen die verschillende bevindingen en inzichten van die gegevens vertegenwoordigen. Rapporten weergeven in de mobiele Power BI-apps is de derde stap in een proces dat uit drie stappen bestaat.

1. [Rapporten maken in Power BI Desktop](desktop-report-view.md). U kunt zelfs [een rapport optimaliseren voor telefoons](mobile-apps-view-phone-report.md) in Power BI Desktop. 
2. Deze rapporten publiceren naar de Power BI-service [(https://powerbi.com)](https://powerbi.com) of [Power BI-rapportserver](report-server/get-started.md).  
3. Vervolgens kunt u de rapporten gebruiken in de mobiele Power BI-apps.

## <a name="open-a-power-bi-report-in-the-mobile-app"></a>Een Power BI-rapport openen in de mobiele app
Power BI-rapporten worden opgeslagen op verschillende plaatsen in de mobiele app, afhankelijk van waar hoe u eraan bent gekomen. Ze kunnen worden opgeslagen in Apps, Gedeeld met mij, werkruimten (met inbegrip van Mijn werkruimte) of op een rapportserver. Soms doorloopt u een gerelateerd dashboard om bij een rapport te komen en soms worden ze in een lijst weergegeven.

* Tik op de drie puntjes (...) in de rechterbovenhoek van een tegel > **Rapport openen**.
  
  ![Rapport openen](media/mobile-reports-in-the-mobile-apps/power-bi-android-open-report-tile.png)
  
  Niet alle tegels hebt de optie om een rapport te openen. Tegels die zijn gemaakt door een vraag te stellen in vak Q&A, openen bijvoorbeeld geen rapporten wanneer u erop tikt. 
  
  Op een telefoon wordt het rapport geopend in de liggende modus, tenzij het rapport is [geoptimaliseerd voor weergave op een telefoon](mobile-reports-in-the-mobile-apps.md#view-reports-optimized-for-phones).
  
  ![Telefoonrapport in de liggende modus](media/mobile-reports-in-the-mobile-apps/power-bi-iphone-report-landscape.png)

## <a name="view-reports-optimized-for-phones"></a>Rapporten weergeven die zijn geoptimaliseerd voor telefoons
Makers van Power BI-rapporten kunnen een rapportindeling maken die speciaal is geoptimaliseerd voor telefoons. Rapportpagina's die zijn geoptimaliseerd voor telefoons beschikken over een extra functionaliteit: u kunt bijvoorbeeld inzoomen op visuals en deze sorteren in de focusmodus, en u krijgt toegang tot de [filters die de auteur van het rapport heeft toegevoegd aan de rapportpagina](mobile-apps-view-phone-report.md#filter-the-report-page-on-a-phone). In een rapportenlijst bevat een geoptimaliseerd rapport een speciaal pictogram ![het telefoonrapport-pictogram](media/mobile-reports-in-the-mobile-apps/power-bi-phone-report-icon.png):

![Telefoonrapport openen](media/mobile-reports-in-the-mobile-apps/power-bi-android-phone-report.png)

Wanneer u een rapport op een telefoon bekijkt, wordt dit geopend in de staande weergave.

![Rapport in de staande weergave](media/mobile-reports-in-the-mobile-apps/07-power-bi-phone-report-portrait.png)

 Een rapport kan bestaan uit een combinatie van pagina's die wel en niet zijn geoptimaliseerd voor telefoons. Wanneer u in dat geval door het rapport bladert, schakelt de weergave voor elke pagina zo nodig van liggend naar staand of omgekeerd.

Lees meer over [rapporten die zijn geoptimaliseerd voor weergave op een telefoon](mobile-apps-view-phone-report.md).

## <a name="use-slicers-to-filter-a-report-page"></a>Slicers gebruiken om een rapportpagina te filteren
Wanneer u een rapport ontwerpt in de Power BI-service [(https://powerbi.com)](https://powerbi.com), dient u er rekening mee te houden dat u op een telefoon het deelvenster Filters niet ziet, maar u kunt wel [slicers op een rapportpagina zien](power-bi-visualization-slicers.md). Voeg slicers toe aan een rapport, zodat u en uw collega's de slicers kunnen gebruiken om de pagina op een telefoon te filteren.

* Wanneer u een waarde selecteert in een slicer op de rapportpagina, worden de andere visuele elementen op de pagina gefilterd.
  
  ![Rapportslicer](media/mobile-reports-in-the-mobile-apps/power-bi-android-tablet-report-slicer.png)
  
  In deze afbeelding filtert de slicer het kolomdiagram zodat alleen de waarden voor juli worden weergegeven.

## <a name="cross-filter-and-highlight-a-power-bi-report-page"></a>Een Power BI-rapportpagina kruisfilteren en markeren
Wanneer u een waarde in een visueel element selecteert, worden de andere visuele elementen niet gefilterd. Wel worden de gerelateerde waarden in de andere visuele elementen gemarkeerd.

* Tik op een waarde in een visueel element.
  
  ![Een pagina kruisfilteren](media/mobile-reports-in-the-mobile-apps/power-bi-android-tablet-report-highlight.png)
  
  Als u tikt op de kolom Large in het ene visuele element, worden de gerelateerde waarden in de andere visuele elementen gemarkeerd. 

## <a name="sort-a-visual-on-an-ipad-or-a-tablet"></a>Een visueel element sorteren op een iPad of tablet
* Tik op het diagram, tik op de drie puntjes (**...** ) en tik op de veldnaam.
  
   ![Een visueel element sorteren](media/mobile-reports-in-the-mobile-apps/power-bi-android-tablet-report-sort.png)
* Als u de sorteervolgorde wilt omkeren, tikt u nogmaals op de drie puntjes (**...** ) en tikt u nogmaals op dezelfde veldnaam.

## <a name="drill-down-and-up-in-a-visual-on-an-ipad-or-a-tablet"></a>In- en uitzoomen op een visueel element op een iPad of een tablet
Als de maker van een rapport deze mogelijkheid heeft toegevoegd aan een visueel element, kunt u op een iPad of tablet inzoomen op een visueel element om de waarden te bekijken waaruit één onderdeel ervan bestaat. U kunt [inzoomen op een visueel element toevoegen](power-bi-visualization-drill-down.md) in Power BI Desktop of de Power BI-service. 

> [!NOTE]
> Inzoomen werkt momenteel niet voor kaarten toewijzingen op de iPad of een tablet.
> 
> 

* Tik op een visueel element. Als er pijlen omhoog en omlaag worden weergegeven in de bovenste hoeken ![Pictogrammen voor inzoomen en uitzoomen](media/mobile-reports-in-the-mobile-apps/power-bi-mobile-drill-up-down.png), kunt u inzoomen. Als u wilt inzoomen op één waarde, tikt u op de pijl in de rechterbovenhoek en tikt u op een waarde in het visuele element, in dit geval de donkerblauw bel FD-04.
  
  ![Inzoomen op een visueel element](media/mobile-reports-in-the-mobile-apps/power-bi-mobile-drill-down-one.png)
* Als u weer wilt uitzoomen, tikt u op de pijl-omhoog in de linkerbovenhoek.
  
  ![Uitzoomen](media/mobile-reports-in-the-mobile-apps/power-bi-mobile-drill-up.png)

## <a name="go-back-to-my-workspace"></a>Teruggaan naar Mijn werkruimte
* Tik op de pijl naast de rapportnaam > tik op **Mijn werkruimte**.
  
  ![Teruggaan](media/mobile-reports-in-the-mobile-apps/power-bi-iphone-report-back.png)

## <a name="next-steps"></a>Volgende stappen
* [Voor uw telefoon geoptimaliseerde Power BI-rapporten weergeven en gebruiken](mobile-apps-view-phone-report.md)
* [Een versie van een rapport maken die is geoptimaliseerd voor telefoons](desktop-create-phone-report.md)
* Vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

