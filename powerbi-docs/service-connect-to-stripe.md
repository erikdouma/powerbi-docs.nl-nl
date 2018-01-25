---
title: Via Power BI verbinding maken met Stripe
description: Stripe voor Power BI
services: powerbi
documentationcenter: 
author: joeshoukry
manager: kfile
backup: maggiesMSFT
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/16/2017
ms.author: yshoukry
ms.openlocfilehash: 5ed68a3ee64803fa895ad9837fe37351163d09af
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/19/2018
---
# <a name="connect-to-stripe-with-power-bi"></a>Via Power BI verbinding maken met Stripe
Visualiseer en verken uw Stripe-gegevens in Power BI met het Power BI-inhoudspakket. Met het Power BI Stripe-inhoudspakket haalt u gegevens op over uw klanten, kosten, gebeurtenissen en facturen. De gegevens bevatten de meest recente 10.000 gebeurtenissen en 5000 kostengegevens gedurende de afgelopen 30 dagen. De inhoud wordt automatisch een keer per dag vernieuwd volgens een schema dat u bepaalt. 

Maak verbinding met het [Stripe-inhoudspakket voor Power BI](https://app.powerbi.com/getdata/services/stripe).

## <a name="how-to-connect"></a>Verbinding maken
1. Selecteer Gegevens ophalen onder in het linkernavigatievenster.  
   
    ![](media/service-connect-to-stripe/getdata.png)
2. Selecteer in het vak **Services** de optie **Ophalen**.  
   
    ![](media/service-connect-to-stripe/services.png)  
3. Selecteer **Stripe** &gt; **Ophalen**.  
   
    ![](media/service-connect-to-stripe/stripe.png)  
4. Geef de [API-sleutel](https://dashboard.stripe.com/account/apikeys) van Stripe op om verbinding te maken.  
   
    ![](media/service-connect-to-stripe/creds.png)
5. Het importproces wordt automatisch gestart. Als het proces is voltooid, worden een nieuw dashboard, rapport en model in het navigatiedeelvenster weergegeven. Deze zijn gemarkeerd met een sterretje. Selecteer het dashboard om uw geïmporteerde gegevens weer te geven.
   
    ![](media/service-connect-to-stripe/dashboard.png)

**Wat nu?**

* [Stel vragen in het vak Q&A](power-bi-q-and-a.md) boven in het dashboard.
* [Wijzig de tegels](service-dashboard-edit-tile.md) in het dashboard.
* [Selecteer een tegel](service-dashboard-tiles.md) om het onderliggende rapport te openen.
* Als uw gegevensset is ingesteld op dagelijks vernieuwen, kunt u het vernieuwingsschema wijzigen of de gegevensset handmatig vernieuwen met **Nu vernieuwen**

## <a name="next-steps"></a>Volgende stappen
[Aan de slag met Power BI](service-get-started.md)

[Gegevens ophalen voor Power BI](service-get-data.md)

