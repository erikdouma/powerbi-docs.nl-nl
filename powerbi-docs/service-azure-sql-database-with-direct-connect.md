---
title: Azure SQL Database met DirectQuery
description: Azure SQL Database met DirectQuery
services: powerbi
documentationcenter: 
author: guyinacube
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
ms.date: 08/10/2017
ms.author: asaxton
ms.openlocfilehash: 83613f0ed915a03b65b90d4bf61e37568b922182
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/15/2017
---
# <a name="azure-sql-database-with-directquery"></a>Azure SQL Database met DirectQuery
Ontdek hoe u rechtstreeks verbinding met Azure SQL Database maakt en rapporten kunt maken waarin dynamische gegevens worden gebruikt. U kunt uw gegevens in de bron in plaats van Power BI bewaren.

Met DirectQuery worden query’s teruggestuurd naar Azure SQL Database wanneer u de gegevens in de rapportweergave verkent. Deze ervaring wordt aangeraden voor gebruikers die vertrouwd zijn met de databases en entiteiten waarmee ze verbinding maken.

**Opmerkingen:**

* Geef de volledige servernaam op wanneer u verbinding maakt (zie hieronder voor meer informatie).
* Zorg ervoor dat de firewallregels voor de database zijn ingesteld op [Toegang tot Azure-services toestaan](https://msdn.microsoft.com/library/azure/ee621782.aspx).
* Voor elke actie, zoals het selecteren van een kolom of het toevoegen van een filter, wordt er een query terug naar de database gestuurd.
* Tegels worden ongeveer elke 15 minuten vernieuwd (vernieuwen hoeft niet te worden gepland). Dit kan worden aangepast in de geavanceerde instellingen wanneer u verbinding maakt.
* Q&A is niet beschikbaar voor DirectQuery-gegevenssets.
* Wijzigingen in het schema worden niet automatisch doorgevoerd.

Deze beperkingen en opmerkingen kunnen veranderen, aangezien we de ervaring voortdurend proberen te verbeteren. De stappen om verbinding te maken, worden hieronder beschreven. 

## <a name="power-bi-desktop-and-directquery"></a>Power BI Desktop en DirectQuery
Als u verbinding met Azure SQL Database via DirectQuery, moet u Power BI Desktop gebruiken. Deze benadering biedt extra flexibiliteit en mogelijkheden. Rapporten die zijn gemaakt met Power BI Desktop, kunnen vervolgens worden gepubliceerd naar de Power BI-service. Meer informatie over hoe u verbinding maakt met [Azure SQL Database via DirectQuery](desktop-use-directquery.md) vindt u in Power BI Desktop. 

## <a name="connecting-through-power-bi"></a>Verbinding maken via Power BI
Het is niet langer mogelijk om rechtstreeks verbinding met Azure SQL Database te maken via de Power BI-service. Wanneer u de [Azure SQL Database-connector](https://app.powerbi.com/getdata/bigdata/azure-sql-database-with-live-connect) selecteert, wordt u gevraagd de verbinding via Power BI Desktop te maken. Vervolgens kunt u de Power BI Desktop-rapporten publiceren naar de Power BI-service. 

![](media/service-azure-sql-database-with-direct-connect/azure-sql-database-in-power-bi.png)

### <a name="finding-parameter-values"></a>Parameterwaarden zoeken
De volledige servernaam en databasenaam vindt u in Azure Portal.

![](media/service-azure-sql-database-with-direct-connect/azureportnew_update.png)

![](media/service-azure-sql-database-with-direct-connect/azureportal_update.png)

## <a name="next-steps"></a>Volgende stappen
[DirectQuery in Power BI Desktop gebruiken](desktop-use-directquery.md)  
[Aan de slag met Power BI](service-get-started.md)  
[Gegevens ophalen voor Power BI](service-get-data.md)  
Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/).

