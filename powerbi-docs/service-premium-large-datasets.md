---
title: Power BI Premium-ondersteuning voor grotere gegevenssets
description: Power BI Premium ondersteunt nu gegevenssets tot 10 GB.
author: jocaplan
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-admin
ms.topic: conceptual
ms.date: 10/18/2018
ms.author: jocaplan
LocalizationGroup: Premium
ms.openlocfilehash: 416f022ee3c413c69650e6f1736cc94edcd58f13
ms.sourcegitcommit: a764e4b9d06b50d9b6173d0fbb7555e3babe6351
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/22/2018
ms.locfileid: "49641247"
---
# <a name="power-bi-premium-support-for-large-datasets"></a>Power BI Premium-ondersteuning voor grotere gegevenssets

Power BI Premium ondersteunt uploads met Power BI Desktop-bestanden (pbix) die maximaal 10 GB groot zijn. Een gegevensset kan, na te zijn geüpload, worden vernieuwd tot een grootte van 12 GB. Als u een grote gegevensset wilt gebruiken, publiceert u deze naar een werkruimte die is toegewezen aan Premium capaciteit. Dit artikel bevat overwegingen en best practices voor het werken met grote gegevenssets.

**Grote modellen kunnen een zware belasting vormen voor de resources** in uw capaciteit. Er wordt ten minste een P1 SKU aangeraden voor alle modellen die groter zijn dan 1 GB. In de volgende tabel zijn de aanbevolen SKU's voor verschillende pbix-grootten weergegeven:

   |SKU  |Grootte van pbix-bestand   |
   |---------|---------|
   |P1    | < 3 GB        |
   |P2    | < 6 GB        |
   |P3, P4, P5    | tot 10 GB |

**Uw pbix-bestanden bevatten gegevens in een sterk gecomprimeerde toestand**. De gegevens breiden waarschijnlijk meerdere keren uit wanneer ze in het geheugen worden geladen. Van daaruit breiden ze mogelijk meerdere keren uit tijdens het vernieuwen van gegevens.

**Geplande vernieuwing van grote gegevenssets kan erg lang duren** en een zware belasting voor uw resources vormen. Plan het vernieuwen van gegevens daarom niet te veel gelijktijdig. U ziet ook dat de time-out voor geplande vernieuwingstaken voor alle gegevenssets in deze capaciteit is verdubbeld tot vier uur. Het is raadzaam [incrementeel vernieuwen](service-premium-incremental-refresh.md) te gebruiken omdat dit sneller en betrouwbaarder is en hiermee minder resources worden verbruikt.

**Het voor de eerste keer laden van een rapport voor grote gegevenssets kan erg lang duren** als het al enige tijd geleden is dat de gegevensset is gebruikt, omdat het model in het geheugen van de uw Premium-capaciteit wordt geladen. Voor rapporten waarvoor het laden langer duurt, wordt de laadvoortgang via een voortgangsbalk weergegeven.

**Als u de werkruimte uit de Premium-capaciteit verwijdert**, werken het model en alle gekoppelde rapporten en dashboards niet meer.

**Omdat de beperkingen van geheugen en tijd per query veel hoger zijn in Premium-capaciteit**, is het zeer aan te bevelen om filters en slicers te gebruiken om alleen de benodigde informatie van visuals weer te geven.

**Volgende stappen**

[Wat is Power BI Premium?](service-premium.md)
[Releaseopmerkingen bij Power BI Premium](service-premium-release-notes.md)
[Technisch document over Microsoft Power BI Premium](https://aka.ms/pbipremiumwhitepaper)
[Technisch document over het plannen van een Power BI Enterprise-implementatie](https://aka.ms/pbienterprisedeploy)

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](https://community.powerbi.com/)
