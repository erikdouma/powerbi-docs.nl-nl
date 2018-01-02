---
title: Rasterlijnen en Uitlijnen op raster gebruiken in Power BI Desktop-rapporten
description: Rasterlijnen, Uitlijnen op raster, Z-volgorde, Uitlijnen en Verdelen gebruiken in Power BI Desktop-rapporten
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
ms.date: 12/06/2017
ms.author: davidi
ms.openlocfilehash: 7dc805f8e791a839bc6b69eb07a71496b64844a2
ms.sourcegitcommit: d91436de68a0e833ecff18d976de9d9431bc4121
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/06/2017
---
# <a name="use-gridlines-and-snap-to-grid-in-power-bi-desktop-reports"></a>Rasterlijnen en Uitlijnen op raster gebruiken in Power BI Desktop-rapporten
Op het canvas van het **Power BI Desktop**-rapport vindt u rasterlijnen waarmee u visuele elementen netjes op een rapportpagina kunt uitlijnen. Het bevat ook de functie Uitlijnen op raster, waarmee u de visuele elementen in uw rapporten op gelijkmatige afstand kunt zetten en ze een professioneel en uitgelijnd uiterlijk geven.

In **Power BI Desktop** kunt u ook de z-volgorde van objecten in een rapport wijzigen (naar voren of naar achteren). En u kunt geselecteerde visuele elementen op het canvas uitlijnen of gelijkmatig verdelen.

![](media/desktop-gridlines-snap-to-grid/snap-to-grid_0.png)

### <a name="enabling-gridlines-and-snap-to-grid"></a>Rasterlijnen en Uitlijnen op raster inschakelen
Als u Rasterlijnen en Uitlijnen op raster wilt inschakelen, selecteert u het lint **Weergave** en schakelt u de selectievakjes in bij **Rasterlijnen weergeven** en **Objecten uitlijnen op raster**.  U kunt één vakje of beide vakjes inschakelen. Ze werken onafhankelijk van elkaar.

![](media/desktop-gridlines-snap-to-grid/snap-to-grid_1.png)

> [!NOTE]
> Als **Rasterlijnen weergeven** en **Objecten uitlijnen op raster** zijn uitgeschakeld, kunt u ze weer inschakelen door verbinding te maken met een gegevensbron.
> 
> 

### <a name="using-gridlines"></a>Rasterlijnen gebruiken
Rasterlijnen zijn visuele hulplijnen waarmee u kunt zien of twee of meer visuele elementen goed zijn uitgelijnd. Wanneer u wilt bepalen of twee (of meer) visuele elementen horizontaal of verticaal zijn uitgelijnd, gebruikt u de rasterlijnen om visueel vast te stellen of de randen zijn uitgelijnd.

Met *Ctrl+klik* kunt u meerdere visuele elementen tegelijk selecteren. Hiermee worden alle geselecteerde randen van de elementen weergegeven, zodat u eenvoudig kunt zien of de visuele elementen goed zijn uitgelijnd.

![](media/desktop-gridlines-snap-to-grid/snap-to-grid_2.png)

#### <a name="using-gridlines-inside-visuals"></a>Rasterlijnen binnen visuele elementen gebruiken
In Power BI zijn ook rasterlijnen binnen visuele elementen aanwezig, waarmee u over visuele hulplijnen beschikt voor het vergelijken van gegevenspunten en waarden. Sinds de release van **Power BI Desktop** in september 2017 kunt u rasterlijnen binnen visuele elementen beheren met behulp van de kaarten **X-as** of **Y-as** (te gebruiken afhankelijk van het type visuele element). Deze vindt u in de sectie **Indeling** van het deelvenster **Visualisaties**. U kunt de volgende elementen van rasterlijnen binnen een visueel element beheren:

* Rasterlijnen in- of uitschakelen
* De kleur van rasterlijnen wijzigen
* De streek (breedte) van rasterlijnen aanpassen
* De lijnstijl van de rasterlijnen in het visuele element selecteren, bijvoorbeeld ononderbroken, onderbroken of gestippeld

Het wijzigen van bepaalde elementen van rasterlijnen kan met name handig zijn in rapporten waar een donkere achtergrond voor visuele elementen wordt gebruikt. De volgende afbeelding toont de sectie *Rasterlijnen* in de kaart **X-as**.

![](media/desktop-gridlines-snap-to-grid/snap-to-grid_9.png)

### <a name="using-snap-to-grid"></a>Uitlijnen op raster gebruiken
Wanneer u **Objecten uitlijnen op raster** inschakelt, worden alle visuele elementen op het **Power BI Desktop**-canvas die u verplaatst (of van grootte verandert) automatisch uitgelijnd met de meest nabije rasteras. Hierdoor kunt u veel makkelijker zien of twee of meer visuele elementen zijn uitgelijnd met dezelfde horizontale of verticale locatie (of grootte).

![](media/desktop-gridlines-snap-to-grid/snap-to-grid_3.png)

Meer hebt u niet nodig als u **Rasterlijnen** en **Objecten uitlijnen op raster** wilt gebruiken om ervoor te zorgen dat de visuele elementen in uw rapporten netjes zijn uitgelijnd.

### <a name="using-z-order-align-and-distribute"></a>Z-volgorde, Uitlijnen en Verdelen gebruiken
U kunt ook de volgorde beheren waarin visuele elementen van voor naar achteren in een rapport worden weergegeven. Dit wordt de *Z-volgorde* van de elementen genoemd. Hiermee kunt u visuele elementen elkaar in een willekeurige volgorde laten overlappen, waarna u de volgorde van voor naar achteren kunt aanpassen. Het ordenen wordt uitgevoerd via de knoppen **Naar voren** en **Naar achteren**. Deze bevinden zich in de sectie **Schikken** van het lint **Indeling**. Het lint verschijnt zodra u een of meer visuele elementen op de pagina selecteert.

![](media/desktop-gridlines-snap-to-grid/snap-to-grid_4.png)

Via het lint **Indeling** kunt u ook de visuele elementen op diverse manieren uitlijnen. U kunt de visuele elementen dus uitlijnen op een manier die voor u het best past.

![](media/desktop-gridlines-snap-to-grid/snap-to-grid_5.png)

Als u één visueel element hebt geselecteerd, kunt u het met de knop **Uitlijnen** uitlijnen met de rand (of het midden) van het rapportcanvas, zoals weergegeven in de volgende afbeelding.

![](media/desktop-gridlines-snap-to-grid/snap-to-grid_6.png)

Als u twee of meer visuele elementen hebt geselecteerd, worden ze samen uitgelijnd en wordt de bestaande, uitgelijnde grens van de visuele elementen voor het uitlijnen gebruikt. Als u bijvoorbeeld twee visuele elementen hebt geselecteerd en hiervoor de knop *Links uitlijnen* selecteert, worden de visuele elementen uitgelijnd met de meest linkse begrenzing van alle geselecteerde visuele elementen.

![](media/desktop-gridlines-snap-to-grid/snap-to-grid_7.png)

U kunt uw visuele elementen ook gelijkmatig over het rapportcanvas verdelen, zowel verticaal als horizontaal. Gebruik hiervoor de knop **Verdelen** op het lint **Indeling**.

![](media/desktop-gridlines-snap-to-grid/snap-to-grid_8.png)

met behulp van slechts enkele selecties van deze hulpmiddelen kunt u uw rapporten er naar eigen wens laten uitzien.

