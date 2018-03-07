---
title: Gegevensbronnen die worden ondersteund door DirectQuery in Power BI
description: Hier vindt u een lijst met ondersteunde gegevensbronnen voor DirectQuery.
services: powerbi
documentationcenter: 
author: davidiseminger
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
ms.date: 01/24/2018
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: 3630d876f3e32cbe981d7fb5bcc38d9da1a257f2
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/24/2018
---
# <a name="data-sources-supported-by-directquery-in-power-bi"></a>Gegevensbronnen die worden ondersteund door DirectQuery in Power BI
In **Power BI Desktop** en de **Power BI-service** kunt u met allerlei gegevensbronnen verbinding maken en toegang tot gegevens verkrijgen. In dit artikel wordt beschreven welke gegevensbronnen voor Power BI worden ondersteund voor de verbindingsmethode **DirectQuery**. Zie [**DirectQuery in Power BI**](desktop-directquery-about.md) voor meer informatie over DirectQuery.

De volgende gegevensbronnen worden ondersteund door DirectQuery in Power BI:

* Amazon Redshift
* Azure HDInsight Spark (bèta)
* Azure SQL Database
* Azure SQL Data Warehouse
* Google BigQuery (bèta)
* IBM Netezza (bèta)
* Impala (versie 2.x)
* Oracle Database (versie 12 en hoger)
* SAP Business Warehouse (bèta)
* SAP HANA
* Snowflake
* Spark (bèta) (versie 0.9 en hoger)
* SQL Server
* Teradata-database
* Vertica (bèta)

Gegevensbronnen met **(bèta)** of **(voorbeeld)** achter de naam zijn onderhevig aan wijzigingen, en worden niet ondersteund voor productiegebruik. Mogelijk worden ze ook niet ondersteund na publicatie van een rapport naar de **Power BI-service**. Dit betekent dat het openen van een gepubliceerd rapport of het verkennen van de gegevensset kan resulteren in een fout.

Het enige verschil tussen **bèta**- en **voorbeeld**gegevensbronnen is dat **voorbeeld**bronnen moeten zijn ingeschakeld als voorbeeldfunctie voordat ze beschikbaar worden voor gebruik. U schakelt een **voorbeeld**gegevensconnector als volgt in: ga in **Power BI Desktop** naar **Bestand > Opties en instellingen** en kies **Instellingen > Opties > Voorbeeldfuncties**.

## <a name="on-premises-gateway-requirements"></a>Vereisten voor on-premises gateway
In de volgende tabel wordt aangegeven of u een **on-premises gegevensgateway** nodig hebt om verbinding te maken met de opgegeven gegevensbron, na publicatie van een rapport naar de **Power BI-service**.

| Bron | Gateway vereist? |
| --- | --- |
| SQL Server |Ja |
| Azure SQL Database |Nee |
| Azure SQL Data Warehouse |Nee |
| SAP HANA |Ja |
| Oracle Database |Ja |
| Teradata-database |Ja |
| Amazon Redshift |Nee |
| Impala (versie 2.x) |Ja |
| Snowflake (voorbeeld) |Nog niet ondersteund in de **Power BI-service** |
| Spark (bèta), versie 0.9 en hoger |Nog niet ondersteund in de **Power BI-service** |
| Azure HDInsight Spark (bèta) |Nog niet ondersteund in de **Power BI-service** |
| IBM Netezza (bèta) |Nog niet ondersteund in de **Power BI-service** |
| SAP Business Warehouse (bèta) |Nog niet ondersteund in de **Power BI-service** |

## <a name="next-steps"></a>Volgende stappen
Bekijk de volgende bronnen voor meer informatie over DirectQuery:

* [DirectQuery in Power BI](desktop-directquery-about.md)
* [DirectQuery en SAP HANA](desktop-directquery-sap-hana.md)
* [DirectQuery en SAP BW](desktop-directquery-sap-bw.md)
* [On-premises data gateway](service-gateway-onprem.md) (On-premises gegevensgateway)

