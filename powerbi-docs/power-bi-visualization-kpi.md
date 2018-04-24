---
title: Visuele KPI-elementen (zelfstudie)
description: KPI maken in de Power BI-service en Power BI Desktop
services: powerbi
documentationcenter: ''
author: mihart
manager: kfile
backup: ''
editor: ''
tags: ''
featuredvideoid: xmja6EpqaO0
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 03/21/2018
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: 4d6af52f10f16d973dc97ed0da1ed74bf63ec2cc
ms.sourcegitcommit: 312390f18b99de1123bf7a7674c6dffa8088529f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2018
---
# <a name="kpi-visuals-tutorial"></a>Visuele KPI-elementen (zelfstudie)
Een Key Performance Indicator (KPI) is een visuele aanwijzing waarmee de voortgang naar een meetbaar doel wordt aangegeven. Zie [Microsoft Developer Network](https://msdn.microsoft.com/library/hh272050) voor meer informatie over KPI's.

## <a name="when-to-use-a-kpi"></a>Een KPI gebruiken
KPI's zijn een prima keuze:

* voor het meten van voortgang (waarmee loop ik voor of achter?)
* voor het meten van de afstand tot een doel (hoe ver loop ik voor of achter?)   

## <a name="kpi-visual-requirements"></a>Vereisten voor Visuele KPI-elementen
Een Key Performance Indicator (KPI) is gebaseerd op een specifieke meting en is ontworpen voor het evalueren van de huidige waarde en status van een metrieke waarde tegen een gedefinieerd doel. Daarom zijn voor een visueel KPI-element een *basismeting* vereist, waarmee een waarde en een *doelmeting* of doelwaarde worden bepaald, en een drempelwaarde of doelstelling.

> [!NOTE]
> Momenteel moet een KPI-gegevensset doelstellingswaarden voor een KPI bevatten. Als uw gegevensset geen doelstellingswaarde bevat, kunt u doelstellingen maken door een Excel-werkblad met doelstellingen aan uw gegevensmodel of PBIX-bestand toe te voegen.
> 
> 

## <a name="how-to-create-a-kpi"></a>KPI's maken
Meld u aan bij de Power BI-service als u mee wilt doen en selecteer **Gegevens ophalen > Voorbeelden > Voorbeeld van een retailanalyse**. We maken een KPI die de voortgang meet die we hebben gemaakt bij een verkoopdoel.

Of kijk naar Will die laat zien hoe u eenvoudige metrische visuele elementen maakt: meters, kaarten en KPI's.

<iframe width="560" height="315" src="https://www.youtube.com/embed/xmja6EpqaO0?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>

1. Open het rapport in de [bewerkweergave](service-reading-view-and-editing-view.md) en [voeg een nieuwe pagina toe](power-bi-report-add-page.md).    
2. Selecteer **Verkopen > Totaal aantal eenheden dit jaar**.  Dit wordt de indicator.
3. Voeg **Tijd > Maand** toe.  Dit stelt de trend voor.
4. BELANGRIJK: sorteer de kaart op **Maand**. Als u de visualisatie naar een KPI hebt omgezet, is er geen optie meer om te sorteren.

    ![](media/power-bi-visualization-kpi/power-bi-sort-by-month.png)
5. Zet het visuele element om naar een KPI door het KPI-pictogram in het deelvenster Visualisatie te selecteren.
   
    ![](media/power-bi-visualization-kpi/power-bi-kpi-icon.png)
6. Voeg een doelstelling toe. Voeg de verkopen van vorig jaar als doelstelling toe. Sleep **Totaal aantal eenheden vorig jaar** naar het veld **Doelstellingen**.
   
    ![](media/power-bi-visualization-kpi/power-bi-kpi.png)
7. U kunt eventueel de KPI opmaken door het verfrollerpictogram te selecteren om het deelvenster Opmaak te openen.
   
   * **Indicator**: hiermee worden de weergave-eenheden en het aantal decimalen bepaald.
   * **Trendas**: als deze is ingesteld op **Aan** wordt de trendas weergegeven als achtergrond van het visuele KPI-element.  
   * **Doelstellingen**: als deze is ingesteld op **Aan** worden de doelstelling en de weg naar het doel als een percentage op het visuele element weergegeven.
   * **Kleurcodering > Richting**: sommige KPI's worden bij hogere waarden als *beter* beschouwd en sommige worden bij lagere waarden als *beter* beschouwd. Bijvoorbeeld omzet versus wachttijd. Meestal is een hogere waarde voor omzet beter versus een hogere waarde voor wachttijd. Selecteer **hoog is beter** en wijzig desgewenst de kleurinstellingen.

1. Als u de KPI's naar wens hebt ingesteld, [maakt u ze aan een dashboard vast](service-dashboard-pin-tile-from-report.md).

KPI's zijn ook op uw mobiele apparaten beschikbaar, zodat u altijd een vinger aan de pols van uw bedrijf hebt.

## <a name="considerations-and-troubleshooting"></a>Aandachtspunten en probleemoplossing
* Als uw KPI niet lijkt op de hierboven afgebeelde KPI, kan dat komen omdat u op maand dient te sorteren. Omdat KPI's geen sorteeroptie hebben, moet u op maand sorteren *voordat* u uw visualisatie naar een KPI omzet.

## <a name="next-steps"></a>Volgende stappen

[Visualisaties in Power BI-rapporten](power-bi-report-visualizations.md)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

