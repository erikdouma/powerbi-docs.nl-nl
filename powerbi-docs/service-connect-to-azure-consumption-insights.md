---
title: Verbinding maken met Microsoft Azure Consumption Insights met Power BI
description: Microsoft Azure Consumption Insights voor Power BI
services: powerbi
documentationcenter: ''
author: SarinaJoan
manager: kfile
backup: maggies
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: 709921a98f6e06572063cf78a83e42bd6b439262
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/24/2018
---
# <a name="connect-to-microsoft-azure-consumption-insights-with-power-bi"></a>Verbinding maken met Microsoft Azure Consumption Insights met Power BI
Verken en monitor uw Microsoft Azure-verbruiksgegevens in Power BI met het Power BI-inhoudspakket. De gegevens worden een keer per dag automatisch vernieuwd.

Maak verbinding met het [Microsoft Azure Consumption Insights-inhoudspakket](https://app.powerbi.com/getdata/services/azureconsumption) voor Power BI.

## <a name="how-to-connect"></a>Verbinding maken
1. Selecteer **Gegevens ophalen** onder in het linkernavigatievenster.
   
    ![](media/service-connect-to-azure-consumption-insights/getdata.png)
2. Selecteer **Ophalen** in het vak **Services**.
   
   ![](media/service-connect-to-azure-consumption-insights/services.png)
3. Selecteer **Microsoft Azure Consumption Insights** \> **Nu downloaden**. 
   
   ![](media/service-connect-to-azure-consumption-insights/mazureconsumption.png)
4. Geef het inschrijvingsnummer voor Azure Enterprise op en het aantal maanden waarvoor u gegevens wilt importeren. Hieronder vindt u informatie over [het vinden van deze parameters](#FindingParams).
   
    ![](media/service-connect-to-azure-consumption-insights/azureconsumptionparams.png)
5. Geef uw toegangscode op om verbinding te maken. De code voor uw inschrijving vindt u in uw Azure EA-portal. 
   
    ![](media/service-connect-to-azure-consumption-insights/msazureconsumptioncreds.png)
6. Het importproces wordt automatisch gestart. Nadat het importeren is voltooid, bevat het navigatiedeelvenster een nieuw dashboard, rapport en model. Selecteer het dashboard om uw geïmporteerde gegevens weer te geven.
   
   ![](media/service-connect-to-azure-consumption-insights/msazureconsumptiondashboard.png)

**Wat nu?**

* [Stel vragen in het vak Q&A](power-bi-q-and-a.md) boven in het dashboard.
* [Wijzig de tegels](service-dashboard-edit-tile.md) in het dashboard.
* [Selecteer een tegel](service-dashboard-tiles.md) om het onderliggende rapport te openen.
* Als uw gegevensset is ingesteld op dagelijks vernieuwen, kunt u het vernieuwingsschema wijzigen of de gegevensset handmatig vernieuwen met **Nu vernieuwen**.

## <a name="whats-included"></a>Wat is inbegrepen
Het Microsoft Azure Consumption Insights-inhoudspakket bevat maandelijkse rapportagegegevens voor het bereik van maanden dat u opgeeft tijdens de verbindingsprocedure. Het bereik is een verschuivend bereik, wat betekent dat de opgenomen datums worden bijgewerkt zodra de gegevensset wordt vernieuwd.

## <a name="system-requirements"></a>Systeemvereisten
Voor het inhoudspakket is toegang vereist tot de Enterprise-functies van Azure Portal. 

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Parameters zoeken
Power BI-rapportage is beschikbaar voor EA Direct, partners en indirecte klanten die factuurgegevens kunnen bekijken. Lees de sectie hieronder voor meer informatie over het vinden van elk van de waarden die de verbindingsstroom verwacht.

**Number of Months**

* Dit moet een getal zijn tussen 1-36 dat het aantal maanden (vanaf vandaag) aangeeft waarvoor u gegevens wilt importeren.

**Enrollment Number**

* Dit is het inschrijvingsnummer voor Azure Enterprise, dat u kunt vinden op het beginscherm van de [Azure Enterprise-portal](https://ea.azure.com/), onder Enrollment Detail.
  
    ![](media/service-connect-to-azure-consumption-insights/params2.png)

**Access Key**

* Uw code vindt u in de Azure Enterprise-portal, onder Download Usage > API Access Key.
  
    ![](media/service-connect-to-azure-consumption-insights/creds2.png)

**Aanvullende informatie**

* Voor extra hulp bij het instellen van het Azure Enterprise Power BI-pakket kunt u inloggen op de Azure Enterprise-portal om het API-helpbestand te bekijken onder Help en aanvullende instructies onder Reports -> Download Usage -> API Access Key. 

## <a name="next-steps"></a>Volgende stappen
[Aan de slag in Power BI](service-get-started.md)

[Gegevens ophalen in Power BI](service-get-data.md)

