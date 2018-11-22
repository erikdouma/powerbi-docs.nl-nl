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
ms.openlocfilehash: 0449d7953b5cefb4c76d89f05ec5b3fa70e9c0da
ms.sourcegitcommit: a739a99e1006834a0f56e387c0bd9d945fb8a76b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/15/2018
ms.locfileid: "51679349"
---
# <a name="power-bi-premium-support-for-large-datasets"></a>Power BI Premium-ondersteuning voor grotere gegevenssets

Power BI Premium ondersteunt uploads met Power BI Desktop-bestanden (pbix) die maximaal 10 GB groot zijn. Een gegevensset kan, na te zijn geüpload, worden vernieuwd tot een grootte van 12 GB. Als u een grote gegevensset wilt gebruiken, publiceert u deze naar een werkruimte die is toegewezen aan Premium capaciteit.
 
## <a name="best-practices"></a>Aanbevolen procedures

In deze sectie worden aanbevolen procedures beschreven voor het werken met grote gegevenssets.

**Grote modellen kunnen een zware belasting vormen voor de resources** in uw capaciteit. Er wordt ten minste een P1 SKU aangeraden voor alle modellen die groter zijn dan 1 GB. Hoewel het mogelijk is om grote modellen te publiceren naar werkruimten die worden ondersteund door A-SKU's tot A3, kunt u de modellen niet vernieuwen.

In de volgende tabel zijn de aanbevolen SKU's voor verschillende pbix-grootten weergegeven:

   |SKU  |Grootte van pbix-bestand   |
   |---------|---------|
   |P1    | < 3 GB        |
   |P2    | < 6 GB        |
   |P3, P4, P5    | tot 10 GB   |

De Power BI Embedded A4-SKU is gelijk aan de P1-SKU, A5 = P2 en A6 = P3. Wanneer u grote modellen publiceert naar A- en EM-SKU's, worden mogelijk fouten geretourneerd die niet specifiek zijn voor de beperking van de modelgrootte in de gedeelde capaciteit. Het vernieuwen van fouten voor grote modellen in A- en EM-SKU's verwijst mogelijk naar time-outs. We werken eraan om de foutmeldingen voor dergelijke scenario's te verbeteren.

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
