---
title: "Verbinding met Azure Consumption Insights-gegevens maken in Power BI Desktop (bèta)"
description: Eenvoudig verbinding maken met Azure en inzicht verkrijgen over het verbruik en gebruik met behulp van Power BI Desktop
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
ms.date: 12/06/2017
ms.author: davidi
ms.openlocfilehash: 3f0bca9114b163531adcd1a1921b8617a5f2eb75
ms.sourcegitcommit: d91436de68a0e833ecff18d976de9d9431bc4121
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/06/2017
---
# <a name="connect-to-azure-consumption-insights-in-power-bi-desktop-beta"></a>Verbinding met Azure Consumption Insights maken in Power BI Desktop (bèta)
Met de **Azure Consumption Insights**-connector kunt u vanuit **Power BI Desktop** verbinding maken met Azure en gedetailleerde gegevens en informatie over het gebruik van Azure-services van uw organisatie verkrijgen. U kunt ook metingen, aangepaste kolommen en visuele elementen maken om rapporten over het gebruik van Azure van uw organisatie te maken en te delen. Deze versie van de **Azure Consumption and Insights**-connector is een bètaversie en kan worden gewijzigd.

![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_01.png)

In dit artikel leert u hoe u verbinding maakt met de **Azure Consumption Insights**-connector, hoe u de benodigde gegevens ophaalt, en hoe u een migratie van de Azure Enterprise-connector uitvoert. Ook vindt u een toewijzing van beschikbare *gebruiksgegevenskolommen* in de **ACI** (Azure Consumption Insights) API.

## <a name="connect-to-azure-consumption-insights"></a>Verbinding met Azure Consumption Insights maken
Om verbinding te maken met behulp van de **Azure Consumption Insights**-connector, moet u toegang hebben tot de Enterprise-functies binnen Azure Portal.

Om verbinding te maken met behulp van de **Azure Consumption Insights**-connector, selecteert u **Gegevens ophalen** in het lint **Start** in **Power BI Desktop**. Selecteer **Onlineservices** in de categorieën aan de linkerkant en u ziet **Azure Consumption Insights (bèta)**. Selecteer **Verbinding maken**.

![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_01b.png)

Geef uw *inschrijvingsnummer* op in het dialoogvenster dat wordt weergegeven.

![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_02.png)

* U kunt uw inschrijvingsnummer ophalen vanuit de [Azure Enterprise-portal](https://ea.azure.com), op de locatie die wordt weergegeven in de volgende afbeelding.
  
  ![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_08.png)
  
  In deze versie van de connector worden alleen Enterprise-inschrijvingen van https://ea.azure.com ondersteund. China-inschrijvingen worden momenteel niet ondersteund.

Geef vervolgens uw *toegangssleutel* op om verbinding te maken.

![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_03.png)

* U vindt de toegangssleutel voor inschrijving in de [Azure Enterprise-portal](https://ea.azure.com).
  
  ![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_09.png)

Als u de *toegangssleutel* hebt opgegeven en **Verbinding maken** selecteert, wordt het venster **Navigator** weergegeven met de vier tabellen die voor u beschikbaar zijn: *Samenvatting*, *Gebruik*, *Prijzenoverzicht* en *Marketplace*. U kunt het selectievakje naast een tabel inschakelen om een voorbeeld van de tabel weer te geven. U kunt een of meer tabellen selecteren door de betreffende selectievakjes in te schakelen en **Laden** te selecteren.

![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_04.png)

> [!NOTE]
> De tabellen *Samenvatting en *Prijzenoverzicht* zijn alleen beschikbaar voor de API-sleutel op inschrijvingsniveau. Deze tabellen bevatten bovendien standaard de gegevens voor *Gebruik* en *Prijzenoverzicht* van de huidige maand. De tabellen *Samenvatting* en *Marketplace* zijn niet beperkt tot de huidige maand.
> 
> 

Wanneer u **Laden** selecteert, worden de gegevens in **Power BI Desktop** geladen.

![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_05.png)

Nadat de geselecteerde gegevens zijn geladen, worden de geselecteerde tabellen en velden weergegeven in het deelvenster **Velden**.

![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_06.png)

## <a name="using-azure-consumption-insights"></a>Werken met Azure Consumption Insights
Om de **Azure Consumption Insights**-connector te kunnen gebruiken, moet u toegang hebben tot de Enterprise-functies binnen Azure Portal.

Als u gegevens hebt geladen met de **Azure Consumption Insights**-connector, kunt u uw eigen aangepaste metingen en kolommen maken met **Query-editor** en visuele elementen, rapporten en dashboards maken en deze vervolgens delen in de **Power BI-service**.

Azure bevat ook een verzameling voorbeelden van aangepaste query's die u kunt ophalen met een lege query. Om dit te doen, selecteert u in het lint **Start** van **Power BI Desktop** de vervolgkeuzepijl in **Gegevens ophalen** en vervolgens **Lege query**. U kunt dit ook doen in **Query-editor** door met de rechtermuisknop op het deelvenster **Query's** aan de linkerkant te klikken en vervolgens **Nieuwe query > Lege query** te selecteren in het menu dat wordt weergegeven.

Typ het volgende in de **formulebalk**:

    = MicrosoftAzureConsumptionInsights.Contents

Er wordt een verzameling voorbeelden weergegeven, zoals wordt weergegeven in de volgende afbeelding.

![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_07.png)

Gebruik het volgende bij het werken met rapporten en het maken van query's:

* Gebruik *noOfMonths* voor het definiëren van het aantal maanden vanaf de huidige datum
  * Gebruik een waarde tussen 1 en 36 voor het aantal maanden, gerekend vanaf de huidige datum, dat u wilt importeren. U wordt aangeraden niet meer dan 12 maanden aan gegevens op te halen, om te voorkomen dat u drempelwaarden met importbeperkingen en de toegestane hoeveelheid gegevens voor query's in Power BI overschrijdt.
* Gebruik *startBillingDataWindow* en *endBillingDataWindow* voor het definiëren van een aantal maanden in een historisch tijdvenster
* Gebruik *noOfMonths* *niet* in combinatie met *startBillingDataWindow* of *endBillingDataWindow*

## <a name="migrating-from-the-azure-enterprise-connector"></a>Migratie van de Azure Enterprise-connector uitvoeren
Sommige klanten hebben visuele elementen gemaakt met de *Azure Enterprise-connector (bèta)*, die uiteindelijk buiten gebruik wordt gesteld en wordt vervangen door de **Azure Consumption Insights**-connector. De **Azure Consumption Insights**-connector bevat onder andere de volgende functies en verbeteringen:

* Extra gegevensbronnen voor *Saldo-overzicht* en *Marketplace-aankopen*
* Nieuwe en geavanceerde parameters, zoals *startBillingDataWindow* en *endBillingDataWindow*
* Betere prestaties en reactietijd

Om klanten te helpen met de overgang naar de nieuwe **Azure Consumption Insights**-connector en ervoor te zorgen dat de door hun gemaakte aangepaste dashboards of rapporten niet verloren gaan, wordt in de volgende stappen beschreven hoe u de nieuwe connector in gebruik neemt.

### <a name="step-1-connect-to-azure-using-the-new-connector"></a>Stap 1: Verbinding maken met Azure met behulp van de nieuwe connector
Eerst moet u verbinding maken met Azure via de **Azure Consumption Insights**-connector, die eerder in dit artikel in detail is beschreven. In deze stap selecteert u **Gegevens ophalen > Lege query** in het lint **Start** in **Power BI Desktop**.

### <a name="step-2-use-the-advanced-editor-to-create-a-query"></a>Stap 2: Een query maken met de geavanceerde editor
In **Query-editor** selecteert u **Geavanceerde editor** in de sectie **Query** van het lint **Start**. In het **Geavanceerde editor**-venster dat wordt weergegeven, voert u de volgende query in.

    let    
        enrollmentNumber = "100",
        optionalParameters = [ numberOfMonth = 6, dataType="DetailCharges" ],
        data = MicrosoftAzureConsumptionInsights.Contents(enrollmentNumber, optionalParameters)   
    in     
        data

![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_10.png)

Uiteraard moet u de waarde van *enrollmentNumber* vervangen door uw eigen inschrijvingsnummer, dat u kunt ophalen uit de [Azure Enterprise-portal](https://ea.azure.com). De parameter *numberOfMonth* is het aantal maanden aan gegevens dat u wilt bewaren, teruggerekend vanaf de huidige datum. Nul (0) staat voor de huidige maand.

Als u **Gereed** selecteert in het **Geavanceerde editor**-venster, wordt het voorbeeldweergave vernieuwd en ziet u de gegevens van het opgegeven maandbereik in de tabel. Selecteer **Sluiten en toepassen** om terug te keren.

### <a name="step-3-move-measures-and-custom-columns-to-the-new-report"></a>Stap 3: Metingen en aangepaste kolommen naar het nieuwe rapport verplaatsen
Vervolgens moet u alle aangepaste kolommen of metingen die u hebt gemaakt, verplaatsen naar de nieuwe detailtabel. Dit zijn de stappen.

1. Open Kladblok (of een andere teksteditor).
2. Selecteer de meting die u wilt verplaatsen en kopieer de tekst van het veld *Formule* en plak deze in Kladblok.
   
   ![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_11.png)
3. Wijzig de naam van *Query1* in de oorspronkelijke naam van de detailtabel.
4. Maak nieuwe metingen en aangepaste kolommen in de tabel. Klik hiertoe met de rechtermuisknop op de tabel en kies **Nieuwe meting**. Knip en plak vervolgens al uw opgeslagen metingen en kolommen erin totdat u klaar bent.

### <a name="step-4-re-link-tables-that-had-relationships"></a>Stap 4: Tabellen met eerdere relaties opnieuw koppelen
Veel dashboards bevatten aanvullende zoek- of filtertabellen, zoals datumtabellen of tabellen die worden gebruikt voor aangepaste projecten. Als u de relaties van die tabellen opnieuw instelt, zijn de meeste resterende problemen opgelost. U kunt dit als volgt doen.

- Selecteer op het tabblad **Modelleren** in **Power BI Desktop** de optie **Relaties beheren**. Er wordt een venster weergegeven waarin u de relaties binnen het model kunt beheren. Koppel uw tabellen opnieuw naar behoefte.
   
    ![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_12.png)

### <a name="step-5-verify-your-visuals-and-adjust-field-formatting-as-needed"></a>Stap 5: Uw visuele elementen controleren en de veldopmaak zo nodig aanpassen
Als u tot hier bent gekomen, zal het merendeel van uw oorspronkelijke visuele elementen, tabellen en detailweergaven werken zoals verwacht. Mogelijk zijn er echter enkele kleine aanpassingen nodig in de opmaak, om alles geheel naar wens weer te geven. Neem de tijd om te controleren of alle dashboards en visuele elementen eruitzien zoals u wilt.

## <a name="using-the-azure-consumption-and-insights-aci-api-to-get-consumption-data"></a>Verbruiksgegevens ophalen met de Azure Consumption and Insights (ACI) API
Azure wordt geleverd met de [**Azure Consumption and Insights (ACI) API**](https://azure.microsoft.com/blog/announcing-general-availability-of-consumption-and-charge-apis-for-enterprise-azure-customers/). Hiermee kunt u uw eigen aangepaste oplossingen maken voor verzameling, rapportage en visualisatie van het Azure-verbruik met de ACI API.

### <a name="mapping-names-and-usage-details-between-the-portal-the-connector-and-the-api"></a>Namen en gebruiksgegevens toewijzen tussen de portal, de connector en de API
De kolommen en namen van detailgegevens in Azure Portal zijn vergelijkbaar in de API en de connector, maar zijn niet altijd identiek. Ter illustratie, de volgende tabel bevat een toewijzing tussen de API, de connector en kolommen die worden weergegeven in Azure Portal. Ook wordt aangegeven of de kolom verouderd is. Zie de [data dictionary voor Azure-facturering](https://docs.microsoft.com/azure/billing/billing-enterprise-api-usage-detail) voor meer informatie over en definities van deze termen.

| Kolomnaam ACI-connector / inhoudspakket | Kolomnaam ACI API | Kolomnaam EA | Verouderd / aanwezig voor achterwaartse compatibiliteit |
| --- | --- | --- | --- |
| AccountName |accountName |Account Name |Nee |
| AccountId |accountId | |Ja |
| AccountOwnerId |accountOwnerEmail |AccountOwnerId |Nee |
| AdditionalInfo |additionalInfo |AdditionalInfo |Nee |
| AdditionalInfold | | |Ja |
| Consumed Quantity |consumedQuantity |Consumed Quantity |Nee |
| Consumed Service |consumedService |Consumed Service |Nee |
| ConsumedServiceId |consumedServiceId | |Ja |
| Cost |cost |ExtendedCost |Nee |
| Cost Center |costCenter |Cost Center |Nee |
| Date |date |Date |Nee |
| Day | |Day |Nee |
| DepartmentName |departmentName |Department Name |Nee |
| DepartmentID |departmentId | |Ja |
| Instance ID | | |Ja |
| InstanceId |instanceId |Instance ID |Nee |
| Location | | |Ja |
| Meter Category |meterCategory |Meter Category |Nee |
| Meter ID | | |Ja |
| Meter Name |meterName |Meter Name |Nee |
| Meter Region |meterRegion |Meter Region |Nee |
| Meter Sub-Category |meterSubCategory |Meter Sub-Category |Nee |
| MeterId |meterId |Meter ID |Nee |
| Month | |Month |Nee |
| Product |product |Product |Nee |
| ProductId |productId | |Ja |
| Resource Group |resourceGroup |Resource Group |Nee |
| Resource Location |resourceLocation |Resource Location |Nee |
| ResourceGroupId | | |Ja |
| ResourceLocationId |resourceLocationId | |Ja |
| ResourceRate |resourceRate |ResourceRate |Nee |
| ServiceAdministratorId |serviceAdministratorId |ServiceAdministratorId |Nee |
| ServiceInfo1 |serviceInfo1 |ServiceInfo1 |Nee |
| ServiceInfo1Id | | |Ja |
| ServiceInfo2 |serviceInfo2 |ServiceInfo2 |Nee |
| ServiceInfo2Id | | |Ja |
| Store Service Identifier |storeServiceIdentifier |Store Service Identifier |Nee |
| StoreServiceIdentifierId | | |Ja |
| Subscription Name |subscriptionName |Subscription Name |Nee |
| Tags |tags |Tags |Nee |
| TagsId | | |Ja |
| Unit Of Measure |unitOfMeasure |Unit Of Measure |Nee |
| Year | |Year |Nee |
| SubscriptionId |subscriptionId |SubscriptionId |Ja |
| SubscriptionGuid |subscriptionGuid |SubscriptionGuid |Nee |

## <a name="next-steps"></a>Volgende stappen
Met Power BI Desktop kunt u verbinding maken met allerlei andere gegevens. Bekijk de volgende bronnen voor meer informatie over gegevensbronnen:

* [Getting Started with Power BI Desktop](desktop-getting-started.md) (Aan de slag met Power BI Desktop)
* [Data Sources in Power BI Desktop](desktop-data-sources.md) (Gegevensbronnen in Power BI Desktop)
* [Shape and Combine Data with Power BI Desktop](desktop-shape-and-combine-data.md) (Gegevens vormgeven en combineren met Power BI Desktop)
* [Connect to Excel workbooks in Power BI Desktop](desktop-connect-excel.md) (Verbinding maken met Excel-werkmappen in Power BI Desktop)   
* [Enter data directly into Power BI Desktop](desktop-enter-data-directly-into-desktop.md) (Rechtstreeks gegevens in Power BI Desktop invoeren)   

