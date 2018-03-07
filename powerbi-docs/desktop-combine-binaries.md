---
title: Binaire bestanden combineren in Power BI Desktop
description: Eenvoudig binaire gegevensbestanden combineren in Power BI Desktop
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
LocalizationGroup: Transform and shape data
ms.openlocfilehash: 395562dfecba4657ffa906494f81532febb6a11f
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/24/2018
---
# <a name="combine-binaries-in-power-bi-desktop"></a>Binaire bestanden combineren in Power BI Desktop
Een krachtige aanpak voor het importeren van gegevens in **Power BI Desktop** bestaat uit het combineren van meerdere bestanden, die hetzelfde schema hebben, tot één logische tabel. Met de release van **Power BI Desktop** van november 2016 (en volgende releases) is deze aanpak nog eenvoudiger en uitgebreider gemaakt, zoals in dit artikel is beschreven.

Selecteer **Gegevens ophalen > Bestand > Map** om het proces van het combineren van binaire bestanden vanuit dezelfde map te starten.

![](media/desktop-combine-binaries/combine-binaries_1.png)

## <a name="previous-combine-binaries-behavior"></a>Gedrag van het vorige combinatieproces
Vóór de release van **Power BI Desktop** van november 2016 kon u bepaalde bestandstypen combineren met de transformatie **Binaire bestanden combineren**. Dit had echter zijn beperkingen:

* De transformaties werden niet voor elk afzonderlijk bestand in overweging genomen voordat de bestanden tot één tabel werden gecombineerd. Daarom moesten bestanden vaak worden gecombineerd om vervolgens de *koptekstwaarden* eruit te filteren door rijen te filteren als onderdeel van het bewerkingsproces.
* De transformatie **Binaire bestanden combineren** werkte alleen voor *tekstbestanden* of *CSV-bestanden* en niet voor andere ondersteunde bestandsindelingen, zoals Excel-werkmappen, JSON-bestanden en andere.

Klanten vroegen om een meer intuïtieve benadering van de bewerking **Binaire bestanden combineren**. Dus hebben we de transformatie uitgebreid.

## <a name="current-combine-binaries-behavior"></a>Gedrag van het huidige combinatieproces
**Power BI Desktop** gaat nu efficiënter om met **Binaire bestanden combineren**. Eerst selecteert u **Binaire bestanden combineren** op het linttablad **Start** in **Query Editor**, of in de kolom zelf.

![](media/desktop-combine-binaries/combine-binaries_2a.png)

De transformatie **Binaire bestanden combineren** werkt nu als volgt:

* De transformatie **Binaire bestanden combineren** analyseert elk invoerbestand en bepaalt de juiste bestandsindeling, bijvoorbeeld *tekstbestand*, *Excel-werkmap* of *JSON-bestand*.
* Met de transformatie kunt u uit het eerste bestand een specifiek object selecteren, bijvoorbeeld om een *Excel-werkmap* te extraheren.
  
  ![](media/desktop-combine-binaries/combine-binaries_3.png)
* **Binaire bestanden combineren** gaat dan automatisch als volgt te werk:
  
  * Er wordt een voorbeeldquery gemaakt waarmee alle vereiste extractiestappen in één bestand worden uitgevoerd.
  * Er wordt een *functiequery* gemaakt waarmee de (binaire) bestandsinvoer in parameters wordt uitgedrukt voor de *voorbeeldquery*. De voorbeeldquery en de functiequery worden gekoppeld, zodat de wijzigingen aan de voorbeeldquery in de functiequery worden weerspiegeld.
  * De *functiequery* wordt toegepast op de oorspronkelijke query met binaire invoerbestanden (bijvoorbeeld de query *Map*). De functiequery wordt dus op elke rij toegepast voor binaire invoer. Vervolgens wordt de resulterende gegevensextractie als kolommen op het bovenste niveau uitgevouwen.
    
    ![](media/desktop-combine-binaries/combine-binaries_4.png)

Dankzij het nieuwe gedrag van **Binaire bestanden combineren** kunt u eenvoudig alle binaire bestanden in een bepaalde map combineren, zolang ze hetzelfde bestandstype en dezelfde structuur hebben (dat wil zeggen dezelfde kolommen).

Bovendien kunt u eenvoudig aanvullende transformaties of extractiestappen toepassen door de automatisch gemaakte *voorbeeldquery* te wijzigen, zonder dat u zich zorgen hoeft te maken over het wijzigen of maken van aanvullende stappen voor een *functiequery*. Wijzigingen aan de *voorbeeldquery* worden automatisch in de gekoppelde *functiequery* gegenereerd.

## <a name="next-steps"></a>Volgende stappen
Met Power BI Desktop kunt u verbinding maken met allerlei andere gegevens. Bekijk de volgende bronnen voor meer informatie over gegevensbronnen:

* [Getting Started with Power BI Desktop](desktop-getting-started.md) (Aan de slag met Power BI Desktop)
* [Data Sources in Power BI Desktop](desktop-data-sources.md) (Gegevensbronnen in Power BI Desktop)
* [Shape and Combine Data with Power BI Desktop](desktop-shape-and-combine-data.md) (Gegevens vormgeven en combineren met Power BI Desktop)
* [Connect to CSV files in Power BI Desktop](desktop-connect-csv.md) (Verbinding met CSV-bestanden maken in Power BI Desktop)   
* [Enter data directly into Power BI Desktop](desktop-enter-data-directly-into-desktop.md) (Rechtstreeks gegevens in Power BI Desktop invoeren)   

