---
title: Azure SQL Data Warehouse met DirectQuery
description: Azure SQL Data Warehouse met DirectQuery
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 06/20/2018
ms.author: maghan
LocalizationGroup: Data from databases
ms.openlocfilehash: a09b9bed97f34b317fadc6b60216019a6c562d0f
ms.sourcegitcommit: c8c126c1b2ab4527a16a4fb8f5208e0f7fa5ff5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2019
ms.locfileid: "54295623"
---
# <a name="azure-sql-data-warehouse-with-directquery"></a>Azure SQL Data Warehouse met DirectQuery
Door het gebruik van Azure SQL Data Warehouse in combinatie DirectQuery kunt u dynamische rapporten maken op basis van gegevens en metrische gegevens die al beschikbaar zijn in Azure SQL Data Warehouse. Met DirectQuery worden in realtime query’s teruggestuurd naar Azure SQL Database Warehouse wanneer u de gegevens in de rapportweergave verkent. Query's in realtime, in combinatie met de schaal van SQL Data Warehouse, biedt gebruikers de mogelijkheid om in enkele minuten dynamische rapporten te maken op basis van terabytes aan gegevens. Bovendien kunnen gebruikers met de introductie van de knop **Openen in Power BI** rechtstreeks via Power BI verbinding maken met hun SQL Data Warehouse, zonder dat ze de informatie handmatig hoeven op te geven.

Als u de SQL Data Warehouse-connector gebruikt:

* Geef de volledige servernaam op wanneer u verbinding maakt (zie hieronder voor meer informatie).
* Zorg ervoor dat de firewallregels voor de server zijn ingesteld op Toegang tot Azure-services toestaan.
* Voor elke actie, zoals het selecteren van een kolom of het toevoegen van een filter, wordt er rechtstreeks een query terug naar de database verzonden.
* Tegels worden ongeveer elke 15 minuten vernieuwd zonder dat hier een schema voor hoeft te worden ingesteld.  Vernieuwen kan worden aangepast in de geavanceerde instellingen wanneer u verbinding maakt.
* Q&A is niet beschikbaar voor DirectQuery-gegevenssets
* Schemawijzigingen worden niet automatisch doorgevoerd

Deze beperkingen en opmerkingen kunnen veranderen, aangezien we de ervaring voortdurend proberen te verbeteren. De stappen om verbinding te maken, worden hieronder beschreven.

## <a name="using-the-open-in-power-bi-button"></a>De knop Openen in Power BI gebruiken

> [!Important]
> De connectiviteit met Azure SQL Data Warehouse is verbeterd.  Gebruik Power BI Desktop voor de beste ervaring bij het maken van verbinding met uw Azure SQL Data Warehouse-gegevensbron.  Als u uw model en het rapport hebt gemaakt, kunt u deze publiceren naar Power BI-service.  De directe connector voor Azure SQL Data Warehouse in Power BI-service is afgeschaft.
>

De eenvoudigste manier om tussen SQL Data Warehouse en Power BI te schakelen, is met de knop **Openen in Power BI** in de Azure-portal. Met deze knop kunt u probleemloos nieuwe dashboards in Power BI maken.

1. Ga naar uw instantie van SQL Data Warehouse in de Azure-portal om aan de slag te gaan. SQL Data Warehouse is op dit moment alleen beschikbaar in de Azure-previewportal.
2. Klik op de knop **Openen in Power BI**.
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/openinpowerbi.png)
3. Als we u niet rechtstreeks kunnen aanmelden of als u geen Power BI-account hebt, moet u zich aanmelden.
4. U wordt omgeleid naar de SQL Data Warehouse-verbindingspagina met daarop de informatie uit SQL Data Warehouse. Geef uw referenties op en klik op Verbinden om verbinding te maken.

## <a name="connecting-through-power-bi"></a>Verbinding maken via Power BI
SQL Data Warehouse wordt ook vermeld op de Power BI-pagina Gegevens ophalen. 

1. Selecteer **Gegevens ophalen** linksonder in het navigatievenster.  
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/getdatabutton.png)
2. Selecteer in **Databases** de optie **Ophalen**.
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/databases.png)
3. Selecteer **SQL Data Warehouse** \> **Verbinden**.
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/azuresqldatawarehouseconnect.png)
4. Voer de benodigde informatie om verbinding te maken. In de onderstaande sectie **Parameters zoeken** wordt uitgelegd waar u deze gegevens kunt vinden in Azure Portal.
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/servername.png)
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/servernamewithadvanced.png)
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/username.png)
   
   > [!NOTE]
   > De gebruikersnaam is een gebruiker die is gedefinieerd in uw instantie van Azure SQL Data Warehouse.
   > 
   > 
5. Zoom in op de gegevensset door de nieuwe tegel of de nieuw gemaakte gegevensset, aangeduid met sterretje, te selecteren. Deze gegevensset heeft dezelfde naam als uw database.
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/dataset2.png)
6. U kunt alle tabellen en kolommen verkennen. Als u een kolom selecteert, wordt er een query teruggestuurd naar de bron en wordt uw visual op dynamische wijze gemaakt. Filters worden ook terugvertaald in query's naar uw datawarehouse. Deze visuals kunnen worden opgeslagen in een nieuw rapport en weer worden vastgemaakt aan uw dashboard.
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/explore3.png)

## <a name="finding-parameter-values"></a>Parameterwaarden zoeken
De volledige servernaam en databasenaam vindt u in de Azure-portal. SQL Data Warehouse is op dit moment alleen beschikbaar in de Azure-previewportal.

![](media/service-azure-sql-data-warehouse-with-direct-connect/azureportal.png)

> [!NOTE]
> Als uw Power BI-tenant zich in dezelfde regio bevindt als Azure SQL Data Warehouse, zijn er geen kosten voor uitgaande verkeer. U kunt nagaan waar uw Power BI-tenant zich bevindt met [deze instructies](https://docs.microsoft.com/power-bi/service-admin-where-is-my-tenant-located).
>

## <a name="next-steps"></a>Volgende stappen
[Wat is Power BI?](power-bi-overview.md)  
[Gegevens ophalen voor Power BI](service-get-data.md)  
[Azure SQL Data Warehouse](/azure/sql-data-warehouse/sql-data-warehouse-overview-what-is/)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)