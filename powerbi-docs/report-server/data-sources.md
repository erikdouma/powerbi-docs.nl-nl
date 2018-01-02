---
title: Power BI-rapportgegevensbronnen in Power BI Report Server
description: Power BI-rapporten kunnen verbinding maken met verschillende gegevensbronnen. Afhankelijk van hoe de gegevens worden gebruikt, zijn er verschillende gegevensbronnen beschikbaar.
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
ms.date: 11/01/2017
ms.author: asaxton
ms.openlocfilehash: f800f79fd49854e0f26a19de1fc9475dad0e1045
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2017
---
# <a name="power-bi-report-data-sources-in-power-bi-report-server"></a>Power BI-rapportgegevensbronnen in Power BI Report Server
Power BI-rapporten kunnen verbinding maken met verschillende gegevensbronnen. Afhankelijk van hoe de gegevens worden gebruikt, zijn er verschillende gegevensbronnen beschikbaar. De gegevens kunnen worden geïmporteerd of de gegevens kunnen rechtstreeks worden opgevraagd rechtstreeks met DirectQuery of een liveverbinding met SQL Server Analysis Services.

Deze gegevensbronnen zijn specifiek voor Power BI-rapporten die in Power BI Report Server worden gebruikt. Zie [Gegevensbronnen die worden ondersteund door Reporting Services](https://docs.microsoft.com/sql/reporting-services/report-data/data-sources-supported-by-reporting-services-ssrs) voor meer informatie over gegevensbronnen die worden ondersteund met gepagineerde rapporten.

> [!IMPORTANT]
> Alle gegevensbronnen in een Power BI Desktop-rapport moeten worden ondersteund voor het configureren van een geplande vernieuwing.
> 
> 

## <a name="list-of-supported-data-sources"></a>Lijst met ondersteunde gegevensbronnen
Andere gegevensbronnen werken mogelijk ook, ondanks dat ze niet op de ondersteunde lijst staan.

| **Gegevensbron** | **In cache opgeslagen gegevens** | **Geplande vernieuwing** | **Live/DirectQuery** |
| --- | --- | --- | --- |
| SQL Server-database |Ja |Ja |Ja |
| SQL Server Analysis Services |Ja |Ja |Ja |
| Azure SQL Database |Ja |Ja |Ja |
| Azure SQL Data Warehouse |Ja |Ja |Ja |
| Excel |Ja |Ja |Nee |
| Access-database |Ja |Ja |Nee |
| Active Directory |Ja |Ja |Nee |
| Amazon Redshift |Ja |Nee |Nee |
| Azure Blob Storage |Ja |Ja |Nee |
| Azure Data Lake Store |Ja |Nee |Nee |
| Azure HDInsight (HDFS) |Ja |Ja |Nee |
| Azure HDInsight (Spark) |Ja |Ja |Nee |
| Azure Table Storage |Ja |Ja |Nee |
| Dynamics 365 (online) |Ja |Nee |Nee |
| Facebook |Ja |Nee |Nee |
| Map |Ja |Ja |Nee |
| Google Analytics |Ja |Nee |Nee |
| Hadoop-bestand (HDFS) |Ja |Nee |Nee |
| IBM DB2-database |Ja |Ja |Nee |
| Impala |Ja |Nee |Nee |
| JSON |Ja |Ja |Nee |
| Microsoft Exchange |Ja |Nee |Nee |
| Microsoft Exchange Online |Ja |Nee |Nee |
| MySQL-database |Ja |Ja |Nee |
| OData-feed |Ja |Ja |Nee |
| ODBC |Ja |Ja |Nee |
| OLE DB |Ja |Ja |Nee |
| Oracle Database |Ja |Ja |Ja |
| PostgreSQL-database |Ja |Ja |Nee |
| Power BI-service |Nee |Nee |Nee |
| R-script |Ja |Nee |Nee |
| Salesforce-objecten |Ja |Nee |Nee |
| Salesforce-rapporten |Ja |Nee |Nee |
| SAP Business Warehouse-server |Ja |Ja |Ja |
| SAP HANA-database |Ja |Ja |Ja |
| SharePoint-map (on-premises) |Ja |Ja |Nee |
| SharePoint-lijst (on-premises) |Ja |Ja |Nee |
| SharePoint Online-lijst |Ja |Nee |Nee |
| Snowflake |Ja |Nee |Nee |
| Sybase-database |Ja |Ja |Nee |
| Teradata-database |Ja |Ja |Ja |
| Tekst/CSV |Ja |Ja |Nee |
| Web |Ja |Ja |Nee |
| XML |Ja |Ja |Nee |
| appFigures (bèta) |Ja |Nee |Nee |
| SQL Server Analysis Services-database (bèta) |Ja |Nee |Nee |
| Azure Cosmos DB (bèta) |Ja |Nee |Nee |
| Azure HDInsight Spark (bèta) |Ja |Nee |Nee |
| Common Data Service (bèta) |Ja |Nee |Nee |
| comScore Digital Analytix (bèta) |Ja |Nee |Nee |
| Dynamics 365 for Customer Insights (bèta) |Ja |Nee |Nee |
| Dynamics 365 for Financials (bèta) |Ja |Nee |Nee |
| GitHub (bèta) |Ja |Nee |Nee |
| Google BigQuery (bèta) |Ja |Nee |Nee |
| IBM Informix-database (bèta) |Ja |Nee |Nee |
| IBM Netezza (bèta) |Ja |Nee |Nee |
| Kusto (bèta) |Ja |Nee |Nee |
| MailChimp (bèta) |Ja |Nee |Nee |
| Inzicht van Microsoft Azure-verbruik (bèta) |Ja |Nee |Nee |
| Mixpanel (bèta) |Ja |Nee |Nee |
| Planview Enterprise (bèta) |Ja |Nee |Nee |
| Projectplace (bèta) |Ja |Nee |Nee |
| QuickBooks Online (bèta) |Ja |Nee |Nee |
| Smartsheet |Ja |Nee |Nee |
| Spark (bèta) |Ja |Nee |Nee |
| SparkPost (bèta) |Ja |Nee |Nee |
| SQL Sentry (bèta) |Ja |Nee |Nee |
| Stripe (bèta) |Ja |Nee |Nee |
| SweetIQ (bèta) |Ja |Nee |Nee |
| Troux (bèta) |Ja |Nee |Nee |
| Twilio (bèta) |Ja |Nee |Nee |
| tyGraph (bèta) |Ja |Nee |Nee |
| Vertica (bèta) |Ja |Nee |Nee |
| Visual Studio Team Services-feed (bèta) |Ja |Nee |Nee |
| Webtrends (bèta) |Ja |Nee |Nee |
| Zendesk (bèta) |Ja |Nee |Nee |

> [!IMPORTANT]
> De beveiliging op rijniveau die is geconfigureerd voor de gegevensbron, moet werken voor DirectQuery (SQL Server, Azure SQL Database, Oracle en Teradata) en liveverbindingen, mits Kerberos goed is geconfigureerd in uw omgeving.
> 
> 

## <a name="next-steps"></a>Volgende stappen
Nu de gegevensbron is gekozen, kunt u [een rapport maken](quickstart-create-powerbi-report.md) op basis van de gegeven in die gegevensbron.

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](https://community.powerbi.com/).

