---
title: Power BI-API's die gebruikmaken van automatisch bewaarbeleid voor realtime-gegevens
description: Meer informatie over het automatisch bewaarbeleid in de Power BI-service
author: markingmyname
manager: kfile
ms.author: maghan
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 06/08/2018
ms.openlocfilehash: 9b5923c7bd92b1fe53ebb7ab9416aca8cece3cfa
ms.sourcegitcommit: c8c126c1b2ab4527a16a4fb8f5208e0f7fa5ff5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2019
ms.locfileid: "54294375"
---
# <a name="automatic-retention-policy-for-real-time-data"></a>Automatisch bewaarbeleid voor realtime-gegevens

Het automatisch bewaarbeleid in de Power BI-service is een querytekenreeksparameter waarmee een standaard bewaarbeleid wordt ingeschakeld om automatisch oude gegevens op te ruimen, terwijl er een constante stroom nieuwe gegevens in uw dashboard binnenkomt. Het eerste retentiebeleid heet *basic first in first out (FIFO)*. Wanneer dit beleid is ingeschakeld, worden de gegevens verzameld in een tabel totdat er 200.000 rijen zijn gevuld. Nadat er meer dan 200.000 rijen met gegevens zijn gevuld, worden de oudste rijen verwijderd uit de gegevensset. Zo worden er 200.000 tot 210.000 rijen bewaard met alleen de meest recente gegevens.  
  
<center>

![bewaarbeleid](media/api-Automatic-retention-policy-for-real-time-data/retention-policy.png) 

</center>

Bewaarbeleid wordt ingeschakeld wanneer u uw eerste gegevenssets maakt. Het enige dat u moet doen is de queryparameter 'defaultRetentionPolicy' toevoegen aan uw aanroep NA gegevenssets en het gelijkstellen aan *basicFIFO*.  
  
    POST https://api.powerbi.com/v1.0/myorg/datasets?defaultRetentionPolicy={None | basicFIFO}