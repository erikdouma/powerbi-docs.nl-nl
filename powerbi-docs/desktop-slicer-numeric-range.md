---
title: De slicer voor numeriek bereik in Power BI Desktop gebruiken
description: Informatie over het gebruik van een slicer voor het beperken van numerieke bereiken in Power BI Desktop
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
ms.date: 02/05/2018
ms.author: davidi
ms.openlocfilehash: 6d63236254906619f7244db9f57af162a19a70d6
ms.sourcegitcommit: db37f5cef31808e7882bbb1e9157adb973c2cdbc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/09/2018
---
# <a name="use-the-numeric-range-slicer-in-power-bi-desktop"></a>De slicer voor numeriek bereik in Power BI Desktop gebruiken
Met de **slicer voor numeriek bereik**, kunt u allerlei filters toepassen op een van de numerieke kolommen in het gegevensmodel. U kunt ervoor kiezen om te filteren **tussen** getallen, **kleiner dan of gelijk aan** een getal of **groter dan of gelijk aan** een getal. Hoewel dit eenvoudig klinkt, is het een zeer krachtige manier om uw gegevens te filteren.

![](media/desktop-slicer-numeric-range/slicer-numeric-range_2.png)

## <a name="using-the-numeric-range-slicer"></a>De slicer voor numeriek bereik gebruiken
U kunt de slicer voor numeriek bereik net als elke andere slicer gebruiken. Maak eenvoudig een visueel **slicer**-element voor uw rapport en selecteer vervolgens een numerieke waarde voor de waarde **Veld**. Op de volgende afbeelding is *UnitPrice* geselecteerd.

![](media/desktop-slicer-numeric-range/slicer-numeric-range_3.png)

Selecteer het dakje in de rechterbovenhoek van de **slicer voor numeriek bereik**. Er wordt dan een menu weergegeven.

![](media/desktop-slicer-numeric-range/slicer-numeric-range_4.png)

Voor het numerieke bereik kunt u een keuze maken uit de volgende drie opties:

* Tussen
* Kleiner dan of gelijk aan
* Groter dan of gelijk aan

Wanneer u **Tussen** selecteert in het menu, wordt een schuifregelaar weergegeven en kunt u filteren op numerieke waarden die tussen de getallen liggen. Naast het gebruik van de schuifregelaar zelf, kunt u ook in een vak klikken en de waarden typen. Dit is handig wanneer u wilt segmenteren op specifieke gehele getallen, maar het vanwege de gedetailleerdheid van de balk moeilijk is om precies op dat getal te komen.

Op de volgende afbeelding wordt de rapportpagina gefilterd voor *UnitPrice*-waarden die variëren tussen 500 en 1500.

![](media/desktop-slicer-numeric-range/slicer-numeric-range_5.png)

Wanneer we **Kleiner dan of gelijk aan** selecteren, verdwijnt het besturingselement links (lagere waarde) van de schuifregelaar en kan alleen de bovengrens van de schuifregelaar worden aangepast. Op de volgende afbeelding stellen we de schuifregelaar in op 497.17.

![](media/desktop-slicer-numeric-range/slicer-numeric-range_6.png)

Ten slotte, als we **Groter dan of gelijk aan** selecteren, verdwijnt het besturingselement rechts van de schuifregelaar en kunnen we de lagere waarde aanpassen, zoals op de volgende afbeelding te zien is. Nu worden alleen items met een *UnitPrice* groter dan of gelijk aan 750.56 weergegeven in de visuele elementen op de rapportpagina.

![](media/desktop-slicer-numeric-range/slicer-numeric-range_7.png)

## <a name="snap-to-whole-numbers-with-the-numeric-range-slicer-preview"></a>Uitlijnen op gehele getallen met de slicer voor numeriek bereik (Preview)

Vanaf de versie van **Power BI Desktop** van februari 2018 lijnt uw slicer voor numeriek bereik uit op gehele getallen. Hierdoor kan uw slicer foutloos uitlijnen op gehele getallen. Uitlijning op gehele getallen geldt niet voor decimale filters.


## <a name="limitations-and-considerations"></a>Beperkingen en overwegingen
De volgende beperkingen en overwegingen zijn momenteel van toepassing op de **slicer voor numeriek bereik**

* De **slicer voor numeriek bereik** filtert momenteel elke onderliggende rij in de gegevens, geen statische waarden. Als bijvoorbeeld een veld *Verkoopbedrag* wordt gebruikt, wordt elke transactie op basis van *Verkoopbedrag* gefilterd, niet de som van *Verkoopbedrag* voor elk gegevenspunt van een visueel element.
* Deze slicer werkt momenteel niet met metingen
* Op dit moment is de **slicer voor numeriek bereik** alleen beschikbaar in **Power BI Desktop**. Als een rapport dat gebruikmaakt van de **slicer voor numeriek bereik** wordt gepubliceerd naar de **Power BI-service**, wordt het filter nog wel toegepast, maar wordt dit weergegeven als een slicer voor lijsten.

