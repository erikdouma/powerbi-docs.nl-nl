---
title: Verbinding maken met Smartsheet via Power BI
description: Smartsheet voor Power BI
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
ms.openlocfilehash: 6e212f1a3cf114ebdd4eeba59aee20cfa4e02182
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-smartsheet-with-power-bi"></a>Verbinding maken met Smartsheet via Power BI 
Smartsheet biedt een gebruiksvriendelijk platform voor samenwerking en het delen van bestanden. Het Smartsheet-inhoudspakket voor Power BI bevat een dashboard, rapporten en een gegevensset die een overzicht geven van uw Smartsheet-account. U kunt ook [Power BI Desktop](desktop-connect-to-data.md) gebruiken om rechtstreeks verbinding te maken met afzonderlijke werkbladen in uw account. 

Maak verbinding met het [Smartsheet-inhoudspakket](https://app.powerbi.com/groups/me/getdata/services/smartsheet) voor Power BI.

>[!NOTE]
>U kun het beste een Smartsheet-beheerdersaccount gebruiken om verbinding te maken en het Power BI-inhoudspakket te laden omdat dit account over meer toegangsmogelijkheden beschikt.

## <a name="how-to-connect"></a>Verbinding maken
1. Selecteer **Gegevens ophalen** onder in het linkernavigatievenster.
   
   ![](media/service-connect-to-smartsheet/pbi_getdata.png)
2. Selecteer in het vak **Services** de optie **Ophalen**.
   
   ![](media/service-connect-to-smartsheet/pbi_getservices.png) 
3. Selecteer **Smartsheet \> Ophalen**.
   
   ![](media/service-connect-to-smartsheet/smartsheet.png)
4. Selecteer voor de verificatiemethode de optie **oAuth2 \> Aanmelden**.
   
   Geef desgevraagd uw Smartsheet-referenties op en voer het verificatieproces uit.
   
   ![](media/service-connect-to-smartsheet/creds.png)
   
   ![](media/service-connect-to-smartsheet/creds2.png)
5. Nadat de gegevens in Power BI zijn geïmporteerd, ziet u een nieuw dashboard, een nieuw rapport en een nieuwe gegevensset in het navigatiedeelvenster aan de linkerzijde. Nieuwe items worden gemarkeerd met een geel sterretje \*. Selecteer de vermelding voor Smartsheet.
   
   ![](media/service-connect-to-smartsheet/dashboard.png)

**Wat nu?**

* [Stel vragen in het vak Q&A](service-q-and-a.md) boven in het dashboard
* [Wijzig de tegels](service-dashboard-edit-tile.md) in het dashboard.
* [Selecteer een tegel](service-dashboard-tiles.md) om het onderliggende rapport te openen.
* Als uw gegevensset is ingesteld op dagelijks vernieuwen, kunt u het vernieuwingsschema wijzigen of de gegevensset handmatig vernieuwen met **Nu vernieuwen**

## <a name="whats-included"></a>Wat is inbegrepen
Het Smartsheet-inhoudspakket voor Power BI bevat een overzicht van uw Smartsheet-account, zoals het aantal werkruimten, uw rapporten en werkbladen, het tijdstip waarop deze zijn gewijzigd, enzovoort. Voor beheerders worden ook bepaalde gegevens weergegeven over gebruikers in hun systeem, zoals de belangrijkste makers van werkbladen.  

Als u rechtstreeks verbinding wilt maken met afzonderlijke werkbladen in uw account, kunt u de Smartsheet-connector in [Power BI Desktop](desktop-connect-to-data.md) gebruiken.  

## <a name="next-steps"></a>Volgende stappen:

[Aan de slag met Power BI](service-get-started.md)

[Gegevens ophalen voor Power BI](service-get-data.md)