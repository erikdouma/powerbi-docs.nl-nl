---
title: Verbinding maken met Projectplace met Power BI
description: Projectplace voor Power BI
author: SarinaJoan
manager: kfile
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: 70dcc7beb4525c84f1d52c511fa6a9f2ba666f94
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2018
ms.locfileid: "34249178"
---
# <a name="connect-to-projectplace-by-planview-with-power-bi"></a>Verbinding maken met Projectplace by Planview met Power BI
Met het inhoudspakket van Projectplace by Planview kunt u uw gezamenlijke projectgegevens op geheel nieuwe manieren rechtstreeks in Power BI visualiseren. Gebruik uw aanmeldingsgegevens van Projectplace om de belangrijkste projectstatistieken interactief te bekijken, te ontdekken wie uw meest actieve en productieve teamleden zijn en de risicokaarten en activiteiten in verschillende projecten in uw Projectplace-account te identificeren. U kunt het kant-en-klare dashboard en de rapporten ook uitbreiden om de inzichten te krijgen die voor u het belangrijkst zijn.

[Verbinding maken met het Projectplace-inhoudspakket in Power BI](https://app.powerbi.com/getdata/services/projectplace)

>[!NOTE]
>Als u uw Projectplace-gegevens wilt importeren in Power BI, moet u een Projectplace-gebruiker zijn. Zie hieronder voor aanvullende vereisten.

## <a name="how-to-connect"></a>Verbinding maken
1. Selecteer **Gegevens ophalen** onder in het linkernavigatievenster.
   
    ![](media/service-connect-to-projectplace/get.png)
2. Selecteer in het vak **Services** de optie **Ophalen**.
   
    ![](media/service-connect-to-projectplace/services.png)
3. Selecteer op de pagina van Power BI **Projectplace by Planview** en daarna **Ophalen**:  
   
    ![](media/service-connect-to-projectplace/projectplace.png)
4. Typ in het tekstvak URL voor OData-feed de URL voor de Projectplace OData-feed die u wilt gebruiken, zoals weergegeven in de volgende afbeelding:
   
    ![](media/service-connect-to-projectplace/params.png)
5. Selecteer in de lijst Verificatiemethode **OAuth** als dit nog niet is geselecteerd. Klik op **Aanmelden** en volg de aanmeldprocedure.  
   
   ![](media/service-connect-to-projectplace/creds.png)
6. Selecteer in het linkerdeelvenster **Projectplace** in de lijst met dashboards. De Projectplace-gegevens worden door Power BI geïmporteerd in het dashboard. Houd er rekening mee dat het laden van de gegevens even kan duren.  
   
    Het dashboard bevat tegels die gegevens uit uw Projectplace-database weergeven. De volgende afbeelding toont een voorbeeld van het standaard Projectplace-dashboard in Power BI.
   
    ![](media/service-connect-to-projectplace/dashboard.png)

**Wat nu?**

* [Stel vragen in het vak Q&A](power-bi-q-and-a.md) boven in het dashboard.
* [Wijzig de tegels](service-dashboard-edit-tile.md) in het dashboard.
* [Selecteer een tegel](service-dashboard-tiles.md) om het onderliggende rapport te openen.
* Als uw gegevensset is ingesteld op dagelijks vernieuwen, kunt u het vernieuwingsschema wijzigen of de gegevensset handmatig vernieuwen met **Nu vernieuwen**.

## <a name="system-requirements"></a>Systeemvereisten
Als u uw Projectplace-gegevens wilt importeren in Power BI, moet u een Projectplace-gebruiker zijn. Deze procedure gaat ervan uit dat u zich al met een Power BI-account hebt aangemeld op de startpagina van Microsoft Power BI. Als u geen Power BI-account hebt, kunt u gratis een nieuw Power BI-account maken op de startpagina van Power BI. Klik vervolgens op Gegevens ophalen.

## <a name="next-steps"></a>Volgende stappen
[Aan de slag met Power BI](service-get-started.md)

[Power BI - basisconcepten](service-basic-concepts.md)

