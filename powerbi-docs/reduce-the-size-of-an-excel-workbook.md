---
title: De grootte van een Excel-werkmap reduceren voor weergave in Power BI
description: De grootte van een Excel-werkmap reduceren voor weergave in Power BI
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
ms.openlocfilehash: 9ee4dba473cf757f23a757c44d5c3ebdd887fdfc
ms.sourcegitcommit: d91436de68a0e833ecff18d976de9d9431bc4121
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/06/2017
---
# <a name="reduce-the-size-of-an-excel-workbook-to-view-it-in-power-bi"></a>De grootte van een Excel-werkmap reduceren voor weergave in Power BI
U kunt een Excel-werkmap kleiner dan 1 GB uploaden naar Power BI. Een Excel-werkmap kan uit twee delen bestaan: een gegevensmodel en de rest van het rapport, de kerninhoud van het werkblad. Als het rapport voldoet aan de volgende maximumgrootte, kunt u het opslaan in **OneDrive voor bedrijven**, verbinding ermee maken vanuit Power BI en weergeven in Excel Online:

* De werkmap in zijn geheel mag niet groter dan 1 GB zijn.
* De kerninhoud van het werkblad mag niet groter dan 10 MB zijn.

## <a name="what-makes-core-worksheet-contents-larger-than-10-mb"></a>Wat maakt de kerninhoud van het werkblad groter dan 10 MB
Hier volgen enkele elementen waardoor de kerninhoud van het werkblad groter wordt dan 10 MB:

* Afbeeldingen.
* Gearceerde cellen. [Verwijderen van een opmaak met gearceerde cellen](https://support.office.com/article/Add-or-change-the-background-color-of-cells-ac10f131-b847-428f-b656-d65375fb815e).
* Gekleurde werkbladen. [Verwijderen van de achtergrond van een werkblad](https://support.office.com/en-US/article/add-or-remove-a-sheet-background-3577a762-8450-4556-96a2-cc265abc00a8).
* Tekstvakken.
* Illustraties.

Houd, indien mogelijk, ermee rekening dat u deze elementen moet verwijderen. 

Als het rapport over een gegevensmodel geschikt, hebt u een aantal andere opties: 

* Verwijder gegevens uit de Excel-werkbladen en bewaar deze in plaats daarvan in het gegevensmodel. Zie 'Gegevens verwijderen uit werkbladen' hieronder voor meer informatie. 
* [Een geheugen-efficiënt gegevensmodel maken](https://support.office.com/article/Create-a-memory-efficient-Data-Model-using-Excel-2013-and-the-Power-Pivot-add-in-951c73a9-21c4-46ab-9f5e-14a2833b6a70) om de totale grootte van het rapport te beperken.

Als u een van deze wijzigingen moet aanbrengen, moet u de werkmap in Excel bewerken.

Meer informatie over [maximale bestandsgrootte voor Excel-werkmappen in SharePoint Online](https://support.office.com/article/File-size-limits-for-workbooks-in-SharePoint-Online-9e5bc6f8-018f-415a-b890-5452687b325e).

## <a name="remove-data-from-worksheets"></a>Gegevens van werkbladen verwijderen
Als u gegevens in Excel importeert vanuit het Power Query-tabblad of het Excel Data-tabblad, heeft de werkmap wellicht dezelfde gegevens in een Excel-tabel en in het gegevensmodel. Grote tabellen in Excel-werkbladen kunnen ervoor zorgen dat de kerninhoud van het werkblad meer dan 10 MB wordt. Wanneer u de tabel in Excel verwijdert en de gegevens in het gegevensmodel bewaart, kunt u de kerninhoud van het werkblad van het rapport aanzienlijk verminderen. 

Volg, wanneer u gegevens in Excel importeert, deze tips op:

* **In Power Query**: Wis het vak **Laden naar werkblad**.
  
  De gegevens worden alleen in het gegevensmodel geïmporteerd, zonder gegevens in Excel-werkbladen te importeren.
* Wanneer u **op het Excel Data-tabblad** eerder **Tabel** hebt aangevinkt in de wizard Importeren: Ga naar **Bestaande verbindingen** \> Klik op de verbinding \> **Alleen verbinding maken**. Verwijder de oorspronkelijke tabel of tabellen die tijdens het eerste importproces is/zijn gemaakt.
* **Op het Excel Data- tabblad**: vink niet **Tabel** aan in het vak **Importgegevens**.

## <a name="workbook-size-optimizer"></a>Optimalisatie van de werkmapgrootte
Als uw werkmap een gegevensmodel bevat, kunt u de werkmapgrootte optimaliseren om de grootte van uw werkmap te verminderen. [Optimalisatie van werkmapgrootte downloaden](https://www.microsoft.com/en-us/download/details.aspx?id=38793).

## <a name="related-info"></a>Verwante informatie
[Een geheugen-efficiënt gegevensmodel maken](https://support.office.com/article/Create-a-memory-efficient-Data-Model-using-Excel-2013-and-the-Power-Pivot-add-in-951c73a9-21c4-46ab-9f5e-14a2833b6a70)

[Koppelingen van OneDrive voor Bedrijven gebruiken in Power BI Desktop](desktop-use-onedrive-business-links.md)

