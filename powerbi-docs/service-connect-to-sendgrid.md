---
title: Verbinding met SendGrid maken via Power BI
description: SendGrid voor Power BI
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
ms.openlocfilehash: d077bedcc1faa10af79cf3eba258b1dac969ae10
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/19/2018
---
# <a name="connect-to-sendgrid-with-power-bi"></a>Verbinding met SendGrid maken via Power BI
Met het Power BI-inhoudspakket voor SendGrid kunt u inzichten en statistieken verkrijgen uit uw SendGrid-account. Met behulp van het SendGrid-inhoudspakket kunt u uw statistieken van SendGrid visualiseren in een dashboard.

Maak verbinding met het [SendGrid-inhoudspakket](https://app.powerbi.com/getdata/services/sendgrid) voor Power BI.

## <a name="how-to-connect"></a>Verbinding maken
1. Selecteer **Gegevens ophalen** onder in het linkernavigatievenster.
   
   ![](media/service-connect-to-sendgrid/pbi_getdata.png) 
2. Selecteer in het vak **Services** de optie **Ophalen**.
   
   ![](media/service-connect-to-sendgrid/pbi_getservices.png) 
3. Selecteer het **SendGrid**-inhoudspakket en klik op **Ophalen**.
   
   ![](media/service-connect-to-sendgrid/sendgrid.png) 
4. Geef desgevraagd uw SendGrid-gebruikersnaam en -wachtwoord op. Selecteer **Aanmelden**.
   
   ![](media/service-connect-to-sendgrid/pbi_sendgridsignin.png)
5. Nadat de gegevens in Power BI zijn geïmporteerd, ziet u een nieuw dashboard, een nieuw rapport en een nieuwe gegevensset in het navigatiedeelvenster aan de linkerzijde. Deze bevatten de e-mailstatistieken voor de afgelopen 90 dagen. Nieuwe items zijn gemarkeerd met een geel sterretje \*.
   
   ![](media/service-connect-to-sendgrid/pbi_sendgriddash.png)

**Wat nu?**

* [Stel vragen in het vak Q&A](power-bi-q-and-a.md) boven in het dashboard.
* [Wijzig de tegels](service-dashboard-edit-tile.md) in het dashboard.
* [Selecteer een tegel](service-dashboard-tiles.md) om het onderliggende rapport te openen.
* Als uw gegevensset is ingesteld op dagelijks vernieuwen, kunt u het vernieuwingsschema wijzigen of de gegevensset handmatig vernieuwen met **Nu vernieuwen**.

## <a name="whats-included"></a>Wat is inbegrepen?
De volgende metrische gegevens zijn beschikbaar in het SendGrid-dashboard:

* Algemene e-mailstatistieken: aanvragen, bezorgd, niet bezorgbaar, geblokkeerde spam, spamrapport, enzovoort.
* E-mailstatistieken per categorie
* E-mailstatistieken per geografie
* E-mailstatistieken per serviceprovider
* E-mailbericht statistiek per apparaat, client, browser

## <a name="next-steps"></a>Volgende stappen
[Aan de slag met Power BI](service-get-started.md)

[Gegevens ophalen](service-get-data.md)

