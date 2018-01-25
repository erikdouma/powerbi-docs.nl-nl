---
title: Verbinding met SparkPost maken via Power BI
description: SparkPost voor Power BI
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
ms.openlocfilehash: 0547f288649ef9d2c494d979c39bb9661b8b35f4
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/19/2018
---
# <a name="connect-to-sparkpost-with-power-bi"></a>Verbinding met SparkPost maken via Power BI
Met het Power BI-inhoudspakket voor SparkPost kunt u waardevolle gegevenssets extraheren uit uw SparkPost-account en in een inzichtelijk dashboard weergeven. Met behulp van het SparkPost-inhoudspakket kunt u uw algemene e-mailstatistieken visualiseren, inclusief domeinen, campagnes en betrokkenheid per serviceprovider.

Maak verbinding met het [SparkPost-inhoudspakket voor Power BI](https://app.powerbi.com/getdata/services/spark-post).

## <a name="how-to-connect"></a>Verbinding maken
1. Selecteer **Gegevens ophalen** onder in het linkernavigatievenster.
   
   ![](media/service-connect-to-sparkpost/getdata.png)
2. Selecteer in het vak **Services** de optie **Ophalen**.
   
   ![](media/service-connect-to-sparkpost/services.png)
3. Selecteer het **SparkPost**-inhoudspakket en klik op **Ophalen**. 
   
   ![](media/service-connect-to-sparkpost/sparkpost.png)
4. Geef desgevraagd uw SparkPost API-sleutel op en selecteer Aanmelden. Meer informatie over het [zoeken van deze parameters](#FindingParams) vindt u hieronder.
   
   ![](media/service-connect-to-sparkpost/creds.png)
5. Uw gegevens worden geladen. Afhankelijk van de grootte van uw account kan dit enige tijd duren. Nadat de gegevens in Power BI zijn geïmporteerd, wordt het standaarddashboard, -rapport en de standaardgegevensset weergegeven in het linkernavigatievenster, met daarin de e-mailstatistieken voor de afgelopen 90 dagen. Nieuwe items zijn gemarkeerd met een geel sterretje \*.
   
   ![](media/service-connect-to-sparkpost/dashboard.png)

**Wat nu?**

* [Stel vragen in het vak Q&A](power-bi-q-and-a.md) boven in het dashboard.
* [Wijzig de tegels](service-dashboard-edit-tile.md) in het dashboard.
* [Selecteer een tegel](service-dashboard-tiles.md) om het onderliggende rapport te openen.
* Als uw gegevensset is ingesteld op dagelijks vernieuwen, kunt u het vernieuwingsschema wijzigen of de gegevensset handmatig vernieuwen met **Nu vernieuwen**.

## <a name="whats-included"></a>Wat is inbegrepen?
De inhoudspakket voor Power BI bevat informatie zoals unieke klikken, acceptatiepercentages, bouncepercentages, vertragingspercentage, afwijzingspercentages en meer.

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Parameters zoeken
Er wordt een API-sleutel gebruikt om uw SparkPost-account te verbinden met Power BI. U vindt uw API-sleutel in uw account onder Account \> API en SMTP (meer informatie vindt u [hier](https://support.sparkpost.com/customer/portal/articles/1933377-create-api-keys)). U kunt het beste een API-sleutel met machtigingen voor `Message Events: Read-only ` en `Metrics: Read-only` gebruiken.

![](media/service-connect-to-sparkpost/sparkpost1.png)

