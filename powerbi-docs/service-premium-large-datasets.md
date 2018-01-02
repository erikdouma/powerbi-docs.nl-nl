---
title: Power BI Premium-ondersteuning voor grotere gegevenssets
description: Power BI Premium ondersteunt nu gegevenssets tot 10 GB.
services: powerbi
documentationcenter: 
author: MarkMcGeeAtAquent
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
ms.date: 12/11/2017
ms.author: v-mamcge
ms.openlocfilehash: 82ac4382fe80d83b60705f135b50738718f28876
ms.sourcegitcommit: 7eb15c813a0d14322cb1316bb7aab23cbc13aae6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/11/2017
---
# <a name="power-bi-premium-support-for-large-datasets"></a>Power BI Premium-ondersteuning voor grotere gegevenssets

Power BI Premium ondersteunt uploads met Power BI Desktop-bestanden (pbix) die maximaal 10 GB groot zijn. Als u een grote gegevensset wilt gebruiken, publiceert u deze naar een werkruimte die is toegewezen aan Premium capaciteit.
 
## <a name="best-practices"></a>Aanbevolen procedures

In deze sectie worden aanbevolen procedures beschreven voor het werken met grote gegevenssets.

**Grote modellen kunnen een aanzienlijke belasting op uw resource-capaciteit vormen**; het wordt aangeraden voor modellen groter dan 1 GB minimaal een P1 SKU te gebruiken. In de volgende tabel zijn de aanbevolen SKU's voor verschillende pbix-grootten weergegeven:


   |SKU  |Grootte van pbix-bestand   |
   |---------|---------|
   |P1    | < 3 GB        |
   |P2    | < 6 GB        |
   |P3    | tot 10 GB   |



**Uw pbix-bestanden bevatten gegevens in een sterk gecomprimeerde toestand**. De gegevens breiden waarschijnlijk meerdere keren uit wanneer ze in het geheugen worden geladen. Van daaruit breiden ze mogelijk meerdere keren uit tijdens het vernieuwen van gegevens.

**Geplande vernieuwing van grote gegevenssets kan erg lang duren** en een zware belasting voor uw resources vormen. Plan het vernieuwen van gegevens daarom niet te veel gelijktijdig. U ziet ook dat de time-out voor geplande vernieuwingstaken voor alle gegevenssets in deze capaciteit is verdubbeld tot vier uur.

**Het voor de eerste keer laden van een rapport voor grote gegevenssets kan erg lang duren** als het al enige tijd geleden is dat de gegevensset is gebruikt, omdat het model in het geheugen van de uw Premium-capaciteit wordt geladen. Voor rapporten waarvoor het laden langer duurt, wordt de laadvoortgang via een voortgangsbalk weergegeven.

**Als u de werkruimte uit de Premium-capaciteit verwijdert**, werken het model en alle gekoppelde rapporten en dashboards niet meer.

**Omdat de beperkingen van geheugen en tijd per query veel hoger zijn in Premium capaciteit**, is het raadzaam filters en slicers te gebruiken om van visuals alleen de benodigde informatie weer te geven.

## <a name="next-steps"></a>Volgende stappen
[Power BI Premium - wat is het?](service-premium.md)  
[Releaseopmerkingen bij Power BI Premium](service-premium-release-notes.md)  
[Technisch document over Microsoft Power BI Premium](https://aka.ms/pbipremiumwhitepaper)  
[Een technisch document over een Power BI-implementatie voor de onderneming plannen](https://aka.ms/pbienterprisedeploy)  
[De verlengde Pro-proefversie activeren](service-extended-pro-trial.md)  

Nog vragen? [Misschien dat de Power Bi-community het antwoord weet](https://community.powerbi.com/)
