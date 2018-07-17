---
title: Verbinding met Azure Search maken via Power BI
description: Autditlogboeken van Azure voor Power BI
author: SarinaJoan
manager: kfile
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 02/06/2018
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: 903f2a345ba4d87cb217ececa459a3cca14d72fa
ms.sourcegitcommit: e8d924ca25e060f2e1bc753e8e762b88066a0344
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/29/2018
ms.locfileid: "37134634"
---
# <a name="connect-to-azure-audit-logs-with-power-bi"></a>Verbinding met Azure Search maken via Power BI
U kunt met het inhoudspakket van Azure controleren logboeken analyseren en visualiseren van gegevens die zijn opgeslagen in de auditlogboeken. Power BI haalt uw gegevens op en bouwt vervolgens een kant-en-klaar dashboard. Daarnaast worden er rapporten op basis van die gegevens gemaakt.

[Maak verbinding met het inhoudspakket van de auditlogboeken van Azure](https://app.powerbi.com/getdata/services/azure-audit-logs) of lees meer over de [integratie van auditlogboeken van Azure ](https://powerbi.microsoft.com/integrations/azure-audit-logs) met Power BI.

## <a name="how-to-connect"></a>Verbinding maken
1. Selecteer **Gegevens ophalen** onder in het linkernavigatievenster.  
   
    ![](media/service-connect-to-azure-audit-logs/getdata.png)
2. Selecteer in het vak **Services** de optie **Ophalen**.  
   
    ![](media/service-connect-to-azure-audit-logs/services.png) 
3. Selecteer **Auditlogboeken van Azure** > **Ophalen**.  
   
   ![](media/service-connect-to-azure-audit-logs/azureauditlogs.png)
4. Voer desgevraagd uw **Azure-abonnements-id** in. Hieronder vindt u meer informatie over hoe u uw [abonnements-id](#FindingParams) kunt vinden.   
   
    ![](media/service-connect-to-azure-audit-logs/parameters.png)
5. Selecteer voor **Verificatiemethode** **oAuth2**\> **Aanmelden**.
   
    ![](media/service-connect-to-azure-audit-logs/creds.png)
6. Voer uw accountreferenties in het aanmeldingsproces te voltooien.
   
    ![](media/service-connect-to-azure-audit-logs/login.png)
7. Power BI haalt de gegevens in uw auditlogboeken van Azure op en maakt een gebruiksklaar dashboard en rapport. 
   
    ![](media/service-connect-to-azure-audit-logs/dashboard.png)

**Wat nu?**

* [Stel vragen in het vak Q&A](power-bi-q-and-a.md) boven in het dashboard.
* [Wijzig de tegels](service-dashboard-edit-tile.md) in het dashboard.
* [Selecteer een tegel](service-dashboard-tiles.md) om het onderliggende rapport te openen.
* Als uw gegevensset is ingesteld op dagelijks vernieuwen, kunt u het vernieuwingsschema wijzigen of de gegevensset handmatig vernieuwen met **Nu vernieuwen**.

## <a name="system-requirements"></a>Systeemvereisten
Het inhoudspakket van de auditlogboeken van Azure vereist toegang tot de logboeken voor controle in Azure Portal. Meer informatie hierover vindt u [hier](https://azure.microsoft.com/documentation/articles/insights-debugging-with-events/).

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Parameters zoeken
Er zijn twee eenvoudige manieren om uw abonnements-id te vinden.

1. Via https://portal.azure.com -&gt; Bladeren -&gt; Abonnementen -&gt; Abonnements-id
2. Via https://manage.windowsazure.com -&gt; Instellingen -&gt; Abonnements-id

Uw abonnements-id bestaat uit een lange reeks cijfers en tekens, vergelijkbaar met het voorbeeld in stap \#4 hierboven. 

## <a name="troubleshooting"></a>Probleemoplossing
Als u een referentiefout of een fout waarbij er vanwege ongeldige referenties wordt geprobeerd te vernieuwen, verwijdert u alle instanties van de auditlogboeken van Azure en maakt u opnieuw verbinding.

## <a name="next-steps"></a>Volgende stappen
[Wat is Power BI?](power-bi-overview.md)  
[Power BI - basisconcepten](service-basic-concepts.md)  

