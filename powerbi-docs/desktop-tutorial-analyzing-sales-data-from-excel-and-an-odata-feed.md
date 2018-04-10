---
title: 'Zelfstudie: Verkoopgegevens uit Excel en een OData-feed analyseren in Power BI Desktop'
description: 'Zelfstudie: Verkoopgegevens uit Excel en een OData-feed analyseren'
services: powerbi
documentationcenter: ''
author: davidiseminger
manager: kfile
backup: ''
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 01/24/2018
ms.author: davidi
LocalizationGroup: Learn more
ms.openlocfilehash: aad93a6c636fb0d75ad89f9e3d9eb70ec203cc88
ms.sourcegitcommit: afa10c016433cf72d6d366c024b862187a8692fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/04/2018
---
# <a name="tutorial-analyzing-sales-data-from-excel-and-an-odata-feed"></a>Zelfstudie: Verkoopgegevens uit Excel en een OData-feed analyseren
Met **Power BI Desktop** kunt u allerlei verschillende gegevensbronnen met elkaar verbinden en ze vervolgens combineren en indelen, zodat u gemakkelijk interessante en boeiende gegevensanalyse en -visualisaties kunt maken. In deze zelfstudie leert u hoe u gegevens van twee gegevensbronnen kunt combineren. 

Het is gebruikelijk dat gegevens over meerdere gegevensbronnen zijn verdeeld, zoals productgegevens in de ene database en verkoopgegevens in de andere. U leert in dit document technieken die onder andere een Excel-werkmap en een OData-feed omvatten, maar deze technieken kunnen ook worden toegepast op andere gegevensbronnen, zoals SQL Server-query's, CSV-bestanden of een gegevensbron in Power BI Desktop.

In deze zelfstudie importeert u gegevens uit Excel (dit omvat productinformatie) en uit een OData-feed (met daarin gegevens over bestellingen). U voert stappen voor transformatie en aggregatie uit, en combineert gegevens van beide bronnen om een rapport voor **Totale verkoop per product en jaar** te maken dat interactieve visualisaties bevat. 

Zo ziet het uiteindelijk rapport eruit:

![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/18.png)

U hebt voor de stappen in deze zelfstudie de werkmap Products nodig, die u kunt downloaden: **[ klik hier om Products.xlsx](http://download.microsoft.com/download/1/4/E/14EDED28-6C58-4055-A65C-23B4DA81C4DE/Products.xlsx)** te downloaden.

In het dialoogvenster **Opslaan als** noemt u het bestand **Products.xlsx**.

## <a name="task-1-get-product-data-from-an-excel-workbook"></a>Taak 1: productgegevens uit een Excel-werkmap ophalen
In deze taak importeert u producten uit het bestand Products.xlsx in Power BI Desktop.

### <a name="step-1-connect-to-an-excel-workbook"></a>Stap 1: verbinding maken met een Excel-werkmap
1. Start Power BI Desktop.
2. Selecteer in het lint Start **Gegevens ophalen**. Excel is een van de **meest voorkomende** gegevensverbindingen, en u kunt deze rechtstreeks vanuit het menu **Gegevens ophalen** selecteren.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_1.png)
3. Als u direct de knop Gegevens ophalen selecteert, kunt u ook **Bestand \> Excel** selecteren en voor **Verbinden** kiezen.
4. In het dialoogvenster **Bestand openen** selecteert u het bestand **Products.xlsx**.
5. In het deelvenster **Navigator** selecteert u de tabel **Products** en selecteert u vervolgens **Bewerken**.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_2.png)

### <a name="step-2-remove-other-columns-to-only-display-columns-of-interest"></a>Stap 2: andere kolommen verwijderen, zodat alleen kolommen die van belang zijn worden weergegeven
In deze stap verwijdert u alle kolommen behalve **ProductID**, **ProductName**, **UnitsInStock** en **QuantityPerUnit**. In Power BI Desktop zijn er vaak een aantal manieren om dezelfde taak uit te voeren. Veel knoppen op het lint zijn bijvoorbeeld ook toegankelijk via het snelmenu wanneer u met de rechtermuisknop op een kolom of cel klikt.

Power BI Desktop bevat Query-editor, waarin u uw gegevensverbindingen kunt indelen en transformeren. Query-editor wordt automatisch geopend wanneer u in **Navigator** **Bewerken** selecteert. U kunt Query-editor ook openen door in het lint **Start** van Power BI Desktop **Query's bewerken** te selecteren. De volgende stappen worden uitgevoerd in Query-editor.

1. Selecteer in Query-editor de kolommen **ProductID**, **ProductName**, **QuantityPerUnit**, en **UnitsInStock**. Gebruik **Ctrl+klikken** om meer dan één kolom te selecteren of **Shift+klikken** om kolommen naast elkaar te selecteren).
2. Selecteer in het lint **Kolommen verwijderen** \> **Andere kolommen verwijderen**, of klik met de rechtermuisknop op een kolomkop en klik op **Andere kolommen verwijderen**.

![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/anlayzingsalesdata_removeothercolumns.png)

### <a name="step-3-change-the-data-type-of-the-unitsinstock-column"></a>Stap 3: het gegevenstype van de kolom UnitsInStock wijzigen
Wanneer Query-editor verbinding met gegevens maakt, controleert de editor elk veld om het beste gegevenstype te bepalen. Voor de Excel-werkmap is 'producten op voorraad' altijd een geheel getal, dus in deze stap bevestigt u dat het gegevenstype van de kolom **UnitsInStock** Geheel getal is.

1. Selecteer de kolom **UnitsInStock**.
2. Selecteer in het lint **Start** de vervolgkeuzeknop **Gegevenstype**.
3. Als hier niet al een geheel getal staat, selecteert u **Geheel getal** voor het gegevenstype in de vervolgkeuzelijst (de knop **Gegevenstype:** geeft ook het gegevenstype voor de huidige selectie weer).
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/anlayzingsalesdata_wholenumber.png)      

### <a name="power-bi-desktop-steps-created"></a>Gemaakte stappen in Power BI Desktop
Als u queryhandelingen uitvoert in Query-editor, worden er querystappen gemaakt en vermeld in het deelvenster **Queryinstellingen** in de lijst **Toegepaste stappen**. Elke querystap heeft een bijbehorende formule, die ook wel bekendstaat als de M-taal. Zie [Learn about Power BI formulas](https://support.office.com/Article/Learn-about-Power-Query-formulas-6bc50988-022b-4799-a709-f8aafdee2b2f) (Meer informatie over Power BI-formules) voor meer informatie over de M-formuletaal.

| Taak | Querystap | Formule |
| --- | --- | --- |
| Verbinding maken met een Excel-werkmap |Bron |Source{[Name="Products"]}[Data] |
| Van de eerste rij tabelkolomkoppen maken |FirstRowAsHeader |[Table.PromoteHeaders](https://support.office.com/Article/TablePromoteHeaders-b8eaeb95-042a-42e1-9164-6d3c646acadc "Table.PromoteHeaders") <br /> (Products) |
| Andere kolommen verwijderen, zodat alleen kolommen die van belang zijn worden weergegeven |RemovedOtherColumns |[Table.SelectColumns](https://support.office.com/Article/TableSelectColumns-20bb9e28-9fd3-4cd2-a21b-97972c82ec22 "Table.SelectColumns")  <br />(FirstRowAsHeader,{"ProductID", "ProductName", "QuantityPerUnit", "UnitsInStock"}) |
| Gegevenstype wijzigen |Changed Type |Table.TransformColumnTypes(\#"Removed Other Columns",{{"UnitsInStock", Int64.Type}}) |

## <a name="task-2-import-order-data-from-an-odata-feed"></a>Taak 2: bestelgegevens importeren uit een OData-feed
In deze taak gaat u bestelgegevens importeren. Deze stap is representatief voor het verbinding maken met een verkoopsysteem. U importeert gegevens in Power BI Desktop vanuit de voorbeeld-OData-feed Northwind via de volgende URL, die u kunt kopiëren (en plakken) in de onderstaande stappen: <http://services.odata.org/V3/Northwind/Northwind.svc/> 

### <a name="step-1-connect-to-an-odata-feed"></a>Stap 1: verbinding maken met een OData-feed
1. Vanuit het tabblad **Start** in Query-editor selecteert u **Gegevens ophalen**.
2. Blader naar de gegevensbron van de **OData-feed**.
3. In het dialoogvenster **OData-feed** plakt u de **URL** voor de OData-feed Northwind.
4. Selecteer **OK**.
5. In het deelvenster **Navigator** selecteert u de tabel **Orders** en selecteert u vervolgens **Bewerken**.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/anlayzingsalesdata_odatafeed.png)

>[!NOTE]
>U kunt op een tabelnaam klikken zonder het selectievakje te selecteren om een voorbeeld te bekijken.

### <a name="step-2-expand-the-orderdetails-table"></a>Step 2: de tabel Order\_Details uitbreiden
De tabel **Orders** bevat een verwijzing naar een tabel **Details**, die de afzonderlijke producten in elke bestelling bevat. Wanneer u verbinding maakt met gegevensbronnen met meerdere tabellen (zoals een relationele database) kunt u deze verwijzingen gebruiken om uw query te maken. 

In deze stap breidt u de tabel **Order\_Details** uit die is gerelateerd aan de tabel **Orders** om de kolommen **ProductID**, **UnitPrice** en **Quantity** uit **Order\_Details** te combineren in de tabel **Orders**. Dit is een weergave van de gegevens in deze tabellen:

![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/orderdetails.png)

Met de bewerking **Uitbreiden** combineert u kolommen uit een verwante tabel in een onderwerptabel. Wanneer de query wordt uitgevoerd, worden rijen uit de gerelateerde tabel (**Order\_Details**) gecombineerd in rijen van de onderwerptabel (**Orders**).

Nadat u de tabel **Order\_Details** hebt uitgebreid, worden er drie nieuwe kolommen en extra rijen toegevoegd aan de tabel **Orders**, één voor elke rij in de geneste of gerelateerde tabel.

1. Scrol in de **Queryweergave** naar de kolom **Order\_Details**.
2. Selecteer in de kolom **Order\_Details** het uitbreidpictogram (![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/expand.png)).
3. In de vervolgkeuzelijst **Uitbreiden**:
   1. Selecteer **(Alle kolommen selecteren)** om alle kolommen te wissen.
   2. Selecteer **ProductID**, **UnitPrice** en **Quantity**.
   3. Klik op **OK**.
      ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/7.png)

### <a name="step-3-remove-other-columns-to-only-display-columns-of-interest"></a>Stap 3: andere kolommen verwijderen, zodat alleen kolommen die van belang zijn worden weergegeven
In deze stap verwijdert u alle kolommen behalve **OrderDate, ShipCity**, **ShipCountry**, **Order\_Details.ProductID**, **Order\_ Details.UnitPrice** en **Order\_Details.Quantity**. U hebt in de vorige taak **Andere kolommen verwijderen** gebruikt. Bij deze taak verwijdert u de geselecteerde kolommen.

1. Selecteer in de **Queryweergave** alle kolommen door a. en b. te voltooien:
   1. Klik op de eerste kolom (**OrderID**).
   2. Shift+klik op de laatste kolom (**Shipper**).
   3. Nu dat alle kolommen zijn geselecteerd, gebruikt u Ctrl+klikken om de selectie van de volgende kolommen op te heffen: **OrderDate**, **ShipCity**, **ShipCountry**, **Order\_Details.ProductID**, **Order\_Details.UnitPrice** en **Order\_Details.Quantity**.
2. Nu alleen de kolommen die we willen verwijderen zijn geselecteerd, klikt u met de rechtermuisknop op een geselecteerde kolomkop en klikt u vervolgens op **Kolommen verwijderen**.

### <a name="step-4-calculate-the-line-total-for-each-orderdetails-row"></a>Stap 4: het regeltotaal voor elke Order\_Details-rij berekenen
Met Power BI Desktop kunt u berekeningen maken op basis van de kolommen die u importeert, zodat u de gegevens waarmee u verbinding maakt, kunt aanvullen. In deze stap maakt u een **Aangepaste kolom** om het regeltotaal van elke **Order\_Details**-rij te berekenen.

Het regeltotaal voor elke **Order\_Details**-rij berekenen:

1. Klik in het linttabblad **Kolom toevoegen** op **Toevoegen** **Aangepaste kolom**.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_4.png)
2. Voer in het dialoogvenster **Aangepaste kolom toevoegen** in het tekstvak **Aangepaste kolomformule** het volgende in: **[Order\_Details.UnitPrice]** \* **[Order\_Details.Quantity]**
3. Voer in het tekstvak **Nieuwe kolomnaam** **LineTotal** in.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/8.png)
4. Klik op **OK**.

### <a name="step-5-set-the-datatype-of-the-linetotal-field"></a>Stap 5: het gegevenstype van het veld LineTotal instellen
1. Klik met de rechtermuisknop op de kolom **LineTotal**.
2. Selecteer **Type wijzigen** en kies **Decimaal getal**.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/9.png)

### <a name="step-6-rename-and-reorder-columns-in-the-query"></a>Stap 6: de naam en de volgorde van kolommen in de query wijzigen
In deze stap zorgt u ervoor dat het model eenvoudig te gebruiken is bij het maken van rapporten door de naam van de uiteindelijke kolommen en de volgorde te wijzigen.

1. Sleep in **Query-editor** de kolom **LineTotal** naar links, achter **ShipCountry**.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/10.png)
2. Verwijder het voorvoegsel *Order\_Details.* uit de kolommen **Order\_Details.ProductID**, **Order\_Details.UnitPrice** en **Order\_Details.Quantity** door te dubbelklikken op elke kolomkop en vervolgens de tekst uit de kolomnaam te verwijderen.

### <a name="power-bi-desktop-steps-created"></a>Gemaakte stappen in Power BI Desktop
Als u queryhandelingen uitvoert in Query-editor, worden er querystappen gemaakt en vermeld in het deelvenster **Queryinstellingen** in de lijst **Toegepaste stappen**. Elke querystap heeft een bijbehorende Power Query-formule, die ook wel bekendstaat als de M-taal. Zie [Learn about Power BI formulas](https://support.office.com/Article/Learn-about-Power-Query-formulas-6bc50988-022b-4799-a709-f8aafdee2b2f "Learn about Power Query formulas") (Meer informatie over Power BI-formules) voor meer informatie over deze formuletaal.

| Taak | Querystap | Formule |
| --- | --- | --- |
| Verbinding maken met een OData-feed |Bron |Source{[Name="Orders"]}[Data] |
| De tabel Order\_Details uitbreiden |Order\_Details uitbreiden |[Table.ExpandTableColumn](https://support.office.com/Article/TableExpandTableColumn-54903f25-75a2-4a44-a9a3-52a9d895ee98 "Table.ExpandTableColumn") <br /> (Orders, "Order\_Details", {"ProductID", "UnitPrice", "Quantity"}, {"Order\_Details.ProductID", "Order\_Details.UnitPrice", "Order\_Details.Quantity"}) |
| Andere kolommen verwijderen, zodat alleen kolommen die van belang zijn worden weergegeven |RemovedColumns |[Table.RemoveColumns](https://support.office.com/Article/TableRemoveColumns-6265190e-2f58-4300-85b8-df88fc1a67d3 "Table.RemoveColumns") <br />(\#"Expand Order\_Details",{"OrderID", "CustomerID", "EmployeeID", "RequiredDate", "ShippedDate", "ShipVia", "Freight", "ShipName", "ShipAddress", "ShipCity", "ShipRegion", "ShipPostalCode", "ShipCountry", "Customer", "Employee", "Shipper"}) |
| Het regeltotaal voor elke Order\_Details-rij berekenen |InsertedColumn |[Table.AddColumn](https://support.office.com/Article/TableAddColumn-6c64d0a5-9654-4d15-bfb6-9cc380aaf3c0 "Table.AddColumn") <br /> (RemovedColumns, "Custom", each [Order\_Details.UnitPrice] \* [Order\_Details.Quantity]) |

## <a name="task-3-combine-the-products-and-total-sales-queries"></a>Taak 3: de query's Producten en Totale verkoop combineren
In Power BI Desktop hoeft u niet query's te combineren om erover te rapporteren. In plaats daarvan kunt u **relaties** tussen gegevenssets maken. Deze relaties kunnen worden gemaakt op basis van elke kolom die veel voorkomt in uw gegevenssets. Zie [Relaties maken en beheren](desktop-create-and-manage-relationships.md) voor meer informatie.

In deze zelfstudie delen de gegevens voor Orders en Products een gemeenschappelijk ProductID-veld, dus er moet een relatie tussen deze gegevens bestaan in het model dat we met Power BI Desktop gebruiken. Geef in Power BI Desktop op dat de kolommen uit elke tabel gerelateerd zijn (dat wil zeggen kolommen die dezelfde waarden hebben). Power BI Desktop bepaalt de richting en kardinaliteit van de relatie. In sommige gevallen kan het programma zelfs de relaties automatisch detecteren.

In deze taak controleert u of er in Power BI Desktop een relatie tot stand is gebracht tussen de query's **Producten** en **Totale verkoop**.

### <a name="step-1-confirm-the-relationship-between-products-and-total-sales"></a>Stap 1: de relatie tussen Producten en Totale verkoop controleren
1. Eerst moet het model dat in Query-editor is gemaakt in Power BI Desktop worden geladen. Vanuit het lint **Start** in Query-editor selecteert u **Sluiten en laden**.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_4.png)
2. Power BI Desktop laadt de gegevens van de twee query's.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/11.png)      
3. Zodra de gegevens zijn geladen, selecteert u de knop **Relaties beheren** in het lint **Start**.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_5.png)
4. Selecteer de **Nieuw...**- knop
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_6.png)
5. Als u nu probeert een relatie te maken, ziet u dat er al een bestaat. Zoals wordt weergegeven in het dialoogvenster **Relatie maken** (door de gearceerde kolommen), hebben de **ProductsID**-velden in elke query al een bestaande relatie.
   
    ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/12.png)
6. Selecteer **Annuleren** en selecteer vervolgens de weergave **Relatie** in Power BI Desktop.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_7.png)
7. U ziet het volgende: een visualisatie van de relatie tussen de query's.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_8.png)
8. Wanneer u dubbelklikt op de pijl in de regel die de twee query's verbindt, wordt het dialoogvenster **Relatie bewerken** weergegeven.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_9.png)
9. U hoeft niets te wijzigen, dus u kunt gewoon **Annuleren** selecteren om het dialoogvenster **Relatie bewerken** te sluiten.

## <a name="task-4-build-visuals-using-your-data"></a>Taak 4: visuals maken met behulp van uw gegevens
Met Power BI Desktop kunt u een aantal visualisaties maken om inzicht in uw gegevens te krijgen. U kunt rapporten met meerdere pagina's maken en elke pagina kan meerdere visuals hebben. U kunt acties uitvoeren op uw visualisaties om uw gegevens te analyseren en er meer inzicht in te krijgen. Zie [Een rapport bewerken](service-interact-with-a-report-in-editing-view.md) voor meer informatie over het bewerken van rapporten.

In deze taak maakt u een rapport op basis van de gegevens die eerder zijn geladen. U gebruikt het deelvenster Velden om de kolommen te selecteren waarvan u de visualisaties maakt.

### <a name="step-1-create-charts-showing-units-in-stock-by-product-and-total-sales-by-year"></a>Stap 1: grafieken maken die aantal in voorraad weergeven per product en totale verkoop per jaar
Sleep **UnitsInStock** van het deelvenster Velden (aan de rechterkant van het scherm) naar een lege ruimte op het canvas. Er wordt een tabelvisualisatie gemaakt. Sleep vervolgens ProductName naar het vak As, in de onderste helft van het deelvenster Visualisaties. Vervolgens selecteert u **Sorteren op \> UnitsInStock** met behulp van de opties in de rechterbovenhoek van de visualisatie.

![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/14.png)

Sleep **OrderDate** naar het canvas onder de eerste grafiek en sleep vervolgens LineTotal (ook vanuit het deelvenster Velden) naar de visual. Selecteer Lijndiagram. De volgende visualisatie wordt gemaakt.

![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/15.png)

 Sleep nu **ShipCountry** naar een ruimte op het canvas in de rechterbovenhoek. Omdat u een geografisch veld hebt geselecteerd, wordt er automatisch een kaart gemaakt. Sleep nu **LineTotal** naar het veld **Waarden**. De cirkels op de kaart voor elk land hebben nu een grootte in verhouding met **LineTotal** voor bestellingen die naar dat land zijn verzonden.

![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/17.png)

### <a name="step-2-interact-with-your-report-visuals-to-analyze-further"></a>Stap 2: acties uitvoeren op de visuals in uw rapport voor verdere analyse
Met Power BI Desktop kunt u acties uitvoeren op uw visuals, zoals kruislings markeren en filteren, om verdere trends te ontdekken. Zie [Filtering and Highlighting in Reports](power-bi-reports-filters-and-highlighting.md) (Filteren en markeren in rapporten) voor meer informatie

1. Klik op de lichtblauwe cirkel in het midden van **Canad***a**. De andere visuals worden gefilterd, zodat alleen de voorraad (**ShipCountry**) en het totaalaantal bestellingen (**LineTotal**) voor Canada worden weergegeven.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/18.png)

## <a name="complete-sales-analysis-report"></a>Verkoopanalyserapport voltooien
Nadat u al deze stappen hebt uitgevoerd, hebt u een verkooprapport waarin alle gegevens uit het bestand Products.xlsx en de OData-feed Northwind zijn gecombineerd. Het rapport bevat visuals waarmee u verkoopgegevens voor verschillende landen kunt analyseren. U kunt [hier](http://download.microsoft.com/download/1/4/E/14EDED28-6C58-4055-A65C-23B4DA81C4DE/Analyzing_Sales_Data.pbix) een voltooid Power BI Desktop-bestand downloaden voor deze zelfstudie.

## <a name="next-steps"></a>Volgende stappen
* [Andere zelfstudies voor Power BI Desktop lezen](http://go.microsoft.com/fwlink/?LinkID=521937)
* [Power BI Desktop-video's bekijken](http://go.microsoft.com/fwlink/?LinkID=519322)
* [Een bezoek brengen aan het Power BI-forum](http://go.microsoft.com/fwlink/?LinkID=519326)
* [Het Power BI-blog lezen](http://go.microsoft.com/fwlink/?LinkID=519327)


