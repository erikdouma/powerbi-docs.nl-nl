---
title: Verbinding maken met Troux via Power BI
description: Troux voor Power BI
services: powerbi
documentationcenter: 
author: SarinaJoan
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
ms.author: sarinas
ms.openlocfilehash: cc5bccad484f6fcc4f7a59e1789fd1a12526874c
ms.sourcegitcommit: c24e5d7bd1806e0d637e974b5143ab5125298fc6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/19/2018
---
# <a name="connect-to-troux-for-power-bi"></a>Verbinding maken met Troux voor Power BI
Met het Troux-inhoudspakket kunt u de opslagplaats van uw ondernemingsstructuur op geheel nieuwe manieren rechtstreeks in Power BI weergeven. Het inhoudspakket geeft inzicht in de bedrijfsfunctionaliteit, de toepassingen die deze functionaliteit leveren en de technologieën die ondersteuning bieden voor deze toepassingen die volledig kunnen worden aangepast met Power BI.

Maak verbinding met het [Troux-inhoudspakket](https://app.powerbi.com/getdata/services/troux) voor Power BI.

## <a name="how-to-connect"></a>Verbinding maken
1. Selecteer **Gegevens ophalen** onder in het linkernavigatievenster.
   
   ![](media/service-connect-to-troux/getdata.png)
2. Selecteer in het vak **Services** de optie **Ophalen**.
   
   ![](media/service-connect-to-troux/services.png)
3. Selecteer **Troux** \> **Ophalen**.
   
   ![](media/service-connect-to-troux/troux.png)
4. Geef de URL voor Troux OData op. Bekijk hieronder de details voor [het vinden van die parameters](#FindingParams).
   
   ![](media/service-connect-to-troux/params.png)
5. Selecteer voor **Verificatiemethode** de optie **Standaard** en geef uw gebruikersnaam en wachtwoord (hoofdlettergevoelig) op. Selecteer vervolgens **Aanmelden**.
   
    ![](media/service-connect-to-troux/creds.png)
6. Nadat uw aanmelding is goedgekeurd, wordt het importeren automatisch gestart. Nadat het importeren is voltooid, bevat het navigatiedeelvenster een nieuw dashboard, rapport en model. Selecteer het dashboard om uw geïmporteerde gegevens weer te geven.
   
     ![](media/service-connect-to-troux/dashboard.png)

**Wat nu?**

* [Stel vragen in het vak Q&A](power-bi-q-and-a.md) boven in het dashboard.
* [Wijzig de tegels](service-dashboard-edit-tile.md) in het dashboard.
* [Selecteer een tegel](service-dashboard-tiles.md) om het onderliggende rapport te openen.
* Als uw gegevensset is ingesteld op dagelijks vernieuwen, kunt u het vernieuwingsschema wijzigen of de gegevensset handmatig vernieuwen met **Nu vernieuwen**.

## <a name="system-requirements"></a>Systeemvereisten
Toegang tot de Troux OData-feed en Troux 9.5.1 of hoger is vereist.

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Parameters zoeken
Uw klantenondersteuningsteam kan u de unieke URL voor de Troux OData-feed verstrekken

## <a name="troubleshooting"></a>Probleemoplossing
Als er een foutmelding wordt weergegeven vanwege een time-out, maakt u opnieuw verbinding.

## <a name="next-steps"></a>Volgende stappen
[Aan de slag in Power BI](service-get-started.md)

[Gegevens ophalen in Power BI](service-get-data.md)

