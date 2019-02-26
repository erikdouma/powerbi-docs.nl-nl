---
title: Gegevensbronnen die worden ondersteund door DirectQuery in Power BI
description: Hier vindt u een lijst met ondersteunde gegevensbronnen voor DirectQuery.
author: davidiseminger
ms.author: davidi
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 11/01/2018
LocalizationGroup: Connect to data
ms.openlocfilehash: 84e40e9fbce07716a2250a58bfcbd396a40d2842
ms.sourcegitcommit: 796bf513bf8669676e2a44627b56221b1629a6a8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/26/2019
ms.locfileid: "56826555"
---
# <a name="data-sources-supported-by-directquery-in-power-bi"></a>Gegevensbronnen die worden ondersteund door DirectQuery in Power BI

In **Power BI Desktop** en de **Power BI-service** kunt u met allerlei gegevensbronnen verbinding maken en toegang tot gegevens verkrijgen. In dit artikel wordt beschreven welke gegevensbronnen voor Power BI worden ondersteund voor de verbindingsmethode **DirectQuery**. Zie [**DirectQuery in Power BI**](desktop-directquery-about.md) voor meer informatie over DirectQuery.

De volgende gegevensbronnen worden ondersteund door DirectQuery in Power BI:

* Amazon Redshift
* Azure HDInsight Spark (bèta)
* Azure SQL Database
* Azure SQL Data Warehouse
* Google BigQuery (bèta)
* IBM DB2-database
* IBM Netezza (bèta)
* Impala (versie 2.x)
* Oracle Database (versie 12 en hoger)
* SAP Business Warehouse-toepassingsserver
* SAP Business Warehouse-berichtenserver (bèta)
* SAP HANA
* Snowflake
* Spark (bèta) (versie 0.9 en hoger)
* SQL Server
* Teradata-database
* Vertica (bèta)

Gegevensbronnen met **(bèta)** of **(preview)** achter de naam zijn onderhevig aan wijzigingen, en worden niet ondersteund voor productiegebruik. Mogelijk worden ze ook niet ondersteund na publicatie van een rapport naar de **Power BI-service**. Dit betekent dat het openen van een gepubliceerd rapport of het verkennen van de gegevensset kan resulteren in een fout.

Het enige verschil tussen **bèta**- en **voorbeeld**gegevensbronnen is dat **voorbeeld**bronnen moeten zijn ingeschakeld als voorbeeldfunctie voordat ze beschikbaar worden voor gebruik. U schakelt een **(voorbeeld)** gegevensconnector als volgt in: ga in **Power BI Desktop** naar **Bestand > Opties en instellingen > Opties** en kies **Voorbeeldfuncties**.

> [!NOTE]
> Voor DirectQuery-query's naar SQL Server is verificatie met behulp van huidige referenties voor Windows-verificatie of databasereferenties nodig om toegang tot stand te brengen. Alternatieve referenties worden niet ondersteund.
>

## <a name="on-premises-gateway-requirements"></a>Vereisten voor on-premises gateway
In de volgende tabel wordt aangegeven of u een **On-premises gegevensgateway** nodig hebt om verbinding te maken met de opgegeven gegevensbron, na publicatie van een rapport naar de **Power BI-service**.

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
| Snowflake |Ja |
| Spark (bèta), versie 0.9 en hoger |Ja |
| Azure HDInsight Spark (bèta) |Nee |
| IBM Netezza |Ja |
| SAP Business Warehouse-toepassingsserver |Ja |
| SAP Business Warehouse-berichtenserver |Nog niet ondersteund in de **Power BI-service** |
| Google BigQuery |Nee |


## <a name="next-steps"></a>Volgende stappen
Bekijk de volgende bronnen voor meer informatie over DirectQuery:

* [DirectQuery in Power BI](desktop-directquery-about.md)
* [DirectQuery en SAP HANA](desktop-directquery-sap-hana.md)
* [DirectQuery en SAP BW](desktop-directquery-sap-bw.md)
* [On-premises data gateway](service-gateway-onprem.md) (On-premises gegevensgateway)

