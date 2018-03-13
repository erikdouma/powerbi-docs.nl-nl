---
title: Gegevens en records weergeven in visuele elementen in Power BI Desktop
description: De functies Gegevens weergeven en Records weergeven in Power BI Desktop gebruiken om in te zoomen op details
services: powerbi
documentationcenter: 
author: davidiseminger
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
ms.date: 02/22/2018
ms.author: davidi
LocalizationGroup: Learn more
ms.openlocfilehash: c44a5140fe40217aac170abb0b351197803b6299
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/24/2018
---
# <a name="use-see-data-and-see-records-in-power-bi-desktop"></a>Gegevens weergeven en Records weergeven gebruiken in Power BI Desktop
In **Power BI Desktop** kunt u inzoomen op de gegevens van een visueel element en ziet u een tekstweergave van de gegevens of afzonderlijke gegevenselementen voor een geselecteerd visueel element. Deze functies worden soms aangeduid met *doorklikken* of *analyse* of *detailanalyse*.

Gebruik **Records weergeven** om de onderliggende rijen te bekijken voor een geselecteerd gegevenselement van een visueel element; gebruik **Gegevens weergeven** om een tekstversie te bekijken van de waarden in dat visuele element. Voor het gebruik van **Gegevens weergeven** en **Records weergeven** gelden beperkingen, zoals besproken aan het eind van dit artikel.

![](media/desktop-see-data-see-records/see-data-see-records_1.png)

## <a name="using-see-data-in-power-bi-desktop"></a>Gegevens weergeven gebruiken in Power BI Desktop
De knop **Gegevens weergeven** bevindt zich op het tabblad **Gegevens/analyseren** in de sectie **Visual Tools** van het lint.

![](media/desktop-see-data-see-records/see-data-see-records_2.png)

U kunt ook **gegevens weergeven** door met de rechtermuisknop op een visueel element te klikken en **Gegevens weergeven** te selecteren in het menu dat wordt weergegeven.

![](media/desktop-see-data-see-records/see-data-see-records_3.png)

> [!NOTE]
> Houd de muisaanwijzer boven een gegevenspunt in het visuele element, zodat het snelmenu zichtbaar wordt.
> 
> 

Als u **Gegevens weergeven** selecteert, wordt er door **Power BI Desktop** gefocust op het visuele element en de gegevens die u hebt geselecteerd en wordt er ruimte op het canvas vrijgemaakt voor het weergeven van het visuele element en de tekstweergave van de gegevens. Het visuele element wordt weergegeven op het bovenste gedeelte van het canvas; de gegevens wordt weergegeven op de onderste helft, zoals weergegeven in de volgende afbeelding. Dit is de *horizontale* weergave.

![](media/desktop-see-data-see-records/see-data-see-records_4.png)

U kunt ook overschakelen naar de *verticale weergave* (of terug naar de *horizontale weergave*) door het pictogram in de rechterbovenhoek te selecteren.

![](media/desktop-see-data-see-records/see-data-see-records_5.png)

Als u terug wilt gaan naar het rapport, selecteert u **< Terug naar rapport** in de linkerbovenhoek van het canvas.

![](media/desktop-see-data-see-records/see-data-see-records_6.png)

## <a name="using-see-records-in-power-bi-desktop"></a>Records weergeven gebruiken in Power BI Desktop
U kunt zich ook focussen op één gegevenselement in een visueel element en inzoomen op de achterliggende gegevens. Zodra een visueel element is geselecteerd, zijn er twee manieren om **Records weergeven** te gebruiken: u kunt op het lint **Gegevens/analyseren** de wisselknop **Records weergeven** inschakelen en vervolgens op een gegevenselement klikken. U kunt ook met de rechtermuisknop op een gegevenselement klikken en **Records weergeven** selecteren in het menu dat verschijnt.

![](media/desktop-see-data-see-records/see-data-see-records_7.png)

> [!NOTE]
> Als het geselecteerde visuele element geen ondersteuning biedt voor **Records weergeven**, dan wordt de knop op het lint grijs weergegeven.
> 
> 

Zodra **Records weergeven** is geselecteerd, wordt er door **Power BI Desktop** gefocust op dat afzonderlijke gegevenselement en worden op het canvas de gegevens voor dat element weergegeven, zoals weergegeven in de volgende afbeelding.

![](media/desktop-see-data-see-records/see-data-see-records_8.png)

> [!NOTE]
> U kunt wijzigingen in gegevens die worden bekeken in de weergave **Records weergeven** (of door gebruikers worden gewijzigd), niet in een rapport opslaan.

Als u terug wilt gaan naar het rapport, selecteert u de knop **Terug naar rapport** in de linkerbovenhoek van het canvas.

## <a name="limitations"></a>Beperkingen
Er zijn enkele beperkingen waar u rekening mee moet houden bij het gebruik van **Gegevens weergeven** of **Records weergeven**:

* Alleen de volgende visuele typen worden ondersteund:
  * **Balk**
  * **Kolom**
  * **Kaart**
  * **Structuurkaart**
  * **Choropletenkaart**
  * **Cirkeldiagram**
  * **Ringdiagram**
  * **Trechterdiagram**
* U kunt **Records weergeven** niet gebruiken als voor het visuele element een berekende meting wordt gebruikt
* U kunt **Records weergeven** niet gebruiken als u bent verbonden met een live, multidimensionaal model (MD)

## <a name="next-steps"></a>Volgende stappen
**Power BI Desktop** bevat diverse functies voor gegevensbeheer en het opmaken van rapporten. Bekijk de volgende bronnen voor enkele voorbeelden:

* [Use grouping and binning in Power BI Desktop](desktop-grouping-and-binning.md) (Groeperen en binning in Power BI Desktop gebruiken)
* [Use gridlines, snap-to-grid, z-order, alignment and distribution in Power BI Desktop reports](desktop-gridlines-snap-to-grid.md) (Rasterlijnen, Uitlijnen op raster, Z-volgorde, Uitlijnen en Verdelen gebruiken in Power BI Desktop-rapporten)

