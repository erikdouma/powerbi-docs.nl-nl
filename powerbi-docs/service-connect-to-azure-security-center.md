---
title: Verbinding maken met het Azure Security Center via Power BI
description: Azure Security Center voor Power BI
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
ms.openlocfilehash: e26a26d7cba2ae3d68586a2e0dcdf87481009bd6
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/19/2018
---
# <a name="connect-to-azure-security-center-with-power-bi"></a>Verbinding maken met het Azure Security Center via Power BI
Verkrijg inzicht in de beveiliging van uw Azure-workload door met Power BI verbinding te maken van Azure Security-gegevens. Power BI maakt automatisch een dashboard en rapport op basis van de gegevens van uw Azure Security Center zodat u de gegevens kunt analyseren en verkennen.

Verbinding maken met het [inhoudspakket van Azure Security Center](https://app.powerbi.com/getdata/services/azure-security-center) voor Power BI.

## <a name="how-to-connect"></a>Verbinding maken
1. Selecteer **Gegevens ophalen** onder in het linkernavigatievenster.
   
   ![](media/service-connect-to-azure-security-center/getdata.png)
2. Selecteer in het vak **Services** de optie **Ophalen**.
   
   ![](media/service-connect-to-azure-security-center/services.png)
3. Selecteer **Azure Security Center** \>  **Ophalen**.
   
   ![](media/service-connect-to-azure-security-center/asc.png)
4. Geef uw abonnementssleutel op. Hieronder vindt u meer informatie over [hoe u deze parameters kunt vinden](#FindingParams).
   
   ![](media/service-connect-to-azure-security-center/params.png)
5. Selecteer voor de **verificatiemethode** **oAuth2**\> **Aanmelden**. Geef desgevraagd uw Azure-referenties op.
   
    ![](media/service-connect-to-azure-security-center/creds.png)
6. Nadat uw aanmelding is goedgekeurd, wordt het importeren automatisch gestart. Nadat het importeren is voltooid, bevat het navigatiedeelvenster een nieuw dashboard, rapport en model. Selecteer het dashboard om uw geïmporteerde gegevens weer te geven.
   
     ![](media/service-connect-to-azure-security-center/dashboard.png)

**Wat nu?**

* [Stel vragen in het vak Q&A](power-bi-q-and-a.md) boven in het dashboard.
* [Wijzig de tegels](service-dashboard-edit-tile.md) in het dashboard.
* [Selecteer een tegel](service-dashboard-tiles.md) om het onderliggende rapport te openen.
* Als uw gegevensset is ingesteld op dagelijks vernieuwen, kunt u het vernieuwingsschema wijzigen of de gegevensset handmatig vernieuwen met **Nu vernieuwen**.

## <a name="whats-included"></a>Wat is inbegrepen
Het inhoudspakket bevat inzichten met betrekking tot de status, de waarschuwingsanalyse en de preventieanalyse voor bronbeveiliging.

## <a name="system-requirements"></a>Systeemvereisten
Dit inhoudspakket vereist toegang tot een abonnements-ID terwijl Azure Security Center is ingeschakeld. Zie voor meer informatie de [Azure Security Center](https://portal.azure.com/#blade/Microsoft_Azure_Security/SecurityDashboardStartBladeV2) in de Azure-portal.

Het inhoudspakket verplicht de gebruiker om verbinding te maken met een organisatieaccount (niet een persoonlijk account).

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Parameters zoeken
Er zijn twee eenvoudige manieren om uw abonnements-id te vinden.

1. Via https://portal.azure.com -&gt; Bladeren -&gt; Abonnementen -&gt; Abonnements-id
2. Via https://manage.windowsazure.com -&gt; Instellingen -&gt; Abonnements-id

Uw abonnements-id bestaat uit een lange reeks cijfers en tekens, vergelijkbaar met het voorbeeld in stap \#4 hierboven. 

## <a name="troubleshooting"></a>Probleemoplossing
Het kan even duren voordat alle gegevens zijn geladen. Dit is afhankelijke van de grootte van uw account. Controleer, als tijdens uw aanmelding een fout optreedt, of uw parameters correct zijn en of Azure Security Center voor uw account is ingeschakeld.

Controleer, als het inhoudspakket wordt geladen maar niet alle gegevens worden weergegeven, of u verbinding maakt met een organisatieaccount. Hoewel persoonlijke accounts worden ondersteund door Azure Security Center, retourneert de API (en dus het inhoudspakket) niet de verwachte waarden als de gebruiker verbinding met een niet-organisatieaccount maakt. Zorg dat u toegang hebt tot een organisatie-account en probeer opnieuw verbinding te maken.

## <a name="next-steps"></a>Volgende stappen
[Aan de slag in Power BI](service-get-started.md)

[Gegevens ophalen in Power BI](service-get-data.md)

