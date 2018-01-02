---
title: "Labels voor inlinehiërarchie gebruiken in Power BI Desktop"
description: "Labels voor inlinehiërarchie gebruiken in Power BI Desktop"
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
ms.date: 09/06/2017
ms.author: davidi
ms.openlocfilehash: 470b25af4ee59542d010d3e649d25da7305319ad
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/15/2017
---
# <a name="use-inline-hierarchy-labels-in-power-bi-desktop"></a>Labels voor inlinehiërarchie gebruiken in Power BI Desktop
**Power BI Desktop** ondersteunt het gebruik van **labels voor inlinehiërarchie**, de eerste van twee functies waarmee het hiërarchisch analyseren wordt verbeterd. De tweede functie, die nog in ontwikkeling is, maakt het gebruik van geneste hiërarchielabels mogelijk (houd dit in de gaten, onze updates verschijnen regelmatig).   

## <a name="how-inline-hierarchy-labels-work"></a>Hoe labels voor inlinehiërarchie werken
Met labels voor inlinehiërarchie kunt u hiërarchielabels zien terwijl u visuele elementen uitvouwt met de functie **Alles uitvouwen**. Een groot voordeel van deze hiërarchielabels is dat u ook op deze verschillende hiërarchielabels kunt **sorteren** terwijl u uw hiërarchische gegevens uitvouwt.

### <a name="using-the-built-in-expand-all-feature-without-sorting-by-hierarchy-labels"></a>De ingebouwde functie Alles uitvouwen gebruiken (zonder sorteren op hiërarchielabels)
Voordat we labels voor inlinehiërarchie in actie gaan bekijken, kijken we eerst nog eens hoe de standaardfunctie **Alles uitvouwen** zich gedraagt. Daardoor kunnen we beter begrijpen (en waarderen) hoe handig labels voor inlinehiërarchie kunnen zijn.

In de volgende afbeelding ziet u een staafdiagram met de verkoopcijfers per jaar. Als u er met de rechtermuisknop op klikt, kunt u **Alles uitvouwen** kiezen.

![](media/desktop-inline-hierarchy-labels/inlinehierarchy_4.png)

Als **Alles uitvouwen** is geselecteerd, wordt de datumhiërarchie uitgevouwen van *Jaar* naar *Kwartaal*, zoals u in de volgende afbeelding kunt zien.

![](media/desktop-inline-hierarchy-labels/inlinehierarchy_5.png)

Merk op dat de labels *Jaar* en *Maand* samen inline worden getoond. Dit labelschema gaat op deze manier verder als u **Alles uitvouwen** ook toepast tot onder aan de hiërarchie.

![](media/desktop-inline-hierarchy-labels/inlinehierarchy_6.png)

Dit is dus het gedrag van de ingebouwde *Datumhiërarchie*, gekoppeld aan velden met het gegevenstype *datum/tijd*. We gaan verder naar de volgende sectie, waar we de verschillen zien van de nieuwe functie voor labels voor inlinehiërarchie.

### <a name="using-inline-hierarchy-labels"></a>Werken met labels voor inlinehiërarchie
We kijken nu naar een ander diagram en gebruiken gegevens met informele hiërarchieën. In het volgende visuele element zien we een staafdiagram met **Verkoopbedrag**, waarbij *Kleur* als as wordt gebruikt. In deze gegevens vormen *Kleur* en *Klasse* een informele hiërarchie. Hier kunt u opnieuw *Alles uitvouwen* selecteren om in de hiërarchie in te zoomen.

![](media/desktop-inline-hierarchy-labels/inlinehierarchy_7.png)

Als u **Alles uitvouwen** selecteert, wordt het volgende niveau getoond, met een weergave van de labels voor inlinehiërarchie. Standaard worden inlinehiërarchieën gesorteerd op de meetwaarde, in dit geval **Verkoopbedrag**. Als labels voor inlinehiërarchie zijn ingeschakeld, kunt u deze gegevens ook sorteren op hiërarchie door het beletselteken (**...**) in de rechterbovenhoek te selecteren en vervolgens **Sorteren op > Kleurklasse**, zoals u in de volgende afbeelding kunt zien.

![](media/desktop-inline-hierarchy-labels/inlinehierarchy_8.png)

Als u **Kleurklasse** hebt geselecteerd, worden de gegevens gesorteerd op basis van de geselecteerde informele hiërarchie, zoals in het onderstaande voorbeeld is te zien.

![](media/desktop-inline-hierarchy-labels/inlinehierarchy_9.png)

> [!NOTE]
> Met de functie voor labels voor inlinehiërarchie kunt u de ingebouwde tijdhiërarchie nog niet op waarde sorteren, maar nog slechts op volgorde van hiërarchie.
> 
> 

## <a name="troubleshooting"></a>Problemen oplossen
Het kan voorkomen dat de visuele elementen vast komen te zitten in de uitgevouwen toestand van een inlinehiërarchieniveau. In sommige gevallen ziet u dat sommige visuele elementen vastzitten in de modus waarin ze werden uitgevouwen. Uitzoomen heeft dan geen zin. Dit kan optreden als u de volgende stappen hebt uitgevoerd (u vindt de oplossing hiervoor *onder* deze stappen):

Stappen waardoor visuele elementen mogelijk in een uitgevouwen toestand vast komen te zitten:

1. Schakel de functie **labels voor inlinehiërarchie** in
2. Maak een paar visuele elementen met hiërarchieën
3. Pas **Alles uitvouwen** toe en sla uw bestand op
4. Schakel de functie *labels voor inlinehiërarchie* **uit** en start Power BI Desktop opnieuw
5. Open vervolgens het bestand opnieuw

Als u deze stappen hebt uitgevoerd en uw visuele elementen vastzitten in de uitgevouwen modus, kunt u dit als volgt oplossen:

1. Schakel de functie **labels voor inlinehiërarchie** opnieuw in en start Power BI Desktop opnieuw
2. Open het bestand opnieuw en zoom opnieuw uit tot u de bovenkant van de betreffende visuele elementen ziet
3. Sla uw bestand op
4. Schakel de functie **labels voor inlinehiërarchie** uit en start Power BI Desktop opnieuw
5. Open het bestand opnieuw

U kunt het visuele element ook verwijderen en opnieuw maken.

