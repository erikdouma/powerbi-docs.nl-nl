---
title: Verbinding maken met Microsoft Azure Enterprise met Power BI
description: Microsoft Azure Enterprise voor Power BI
services: powerbi
documentationcenter: 
author: joeshoukry
manager: kfile
backup: maggiesMSFT
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/16/2017
ms.author: yshoukry
ms.openlocfilehash: 39c3fd776e3aed821c7c10c1e905d7400ca64efd
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-microsoft-azure-enterprise-with-power-bi"></a>Verbinding maken met Microsoft Azure Enterprise met Power BI
Verken en bewaak uw Microsoft Azure Enterprise-gegevens in Power BI met het Power BI-inhoudspakket. De gegevens worden eenmaal per dag automatisch vernieuwd.

Maak verbinding met het [Microsoft Azure Enterprise-inhoudspakket](https://app.powerbi.com/getdata/services/azure-enterprise) voor Power BI.

## <a name="how-to-connect"></a>Verbinding maken
1. Selecteer **Gegevens ophalen** onder in het linkernavigatievenster.
   
    ![](media/service-connect-to-azure-enterprise/getdata.png)
2. Selecteer in het vak **Services** de optie **Ophalen**.
   
   ![](media/service-connect-to-azure-enterprise/services.png)
3. Selecteer **Microsoft Azure Enterprise** \> **Ophalen**.
   
   ![](media/service-connect-to-azure-enterprise/mazureenterprise.png)
4. Geef de URL van de Azure-omgeving, het aantal maanden van de gegevens die u wilt importeren en uw Azure Enterprise-inschrijvingsnummer op. De URL van uw Azure-omgeving is `https://ea.azure.com` of `https://ea.windowsazure.cn`. Zie details over [het vinden van deze parameters](#FindingParams) hieronder.
   
    ![](media/service-connect-to-azure-enterprise/params.png)
5. Geef uw toegangssleutel op om verbinding te maken. De sleutel voor uw inschrijving vindt u in uw Azure EA-portal.
   
    ![](media/service-connect-to-azure-enterprise/creds.png)
6. Het importproces wordt automatisch gestart. Nadat het importeren is voltooid, bevat het navigatiedeelvenster een nieuw dashboard, rapport en model. Selecteer het dashboard om uw geïmporteerde gegevens weer te geven.
   
   ![](media/service-connect-to-azure-enterprise/dashboard.png)

**Wat nu?**

* [Stel vragen in het vak Q&A](service-q-and-a.md) bovenin het dashboard
* [Wijzig de tegels ](service-dashboard-edit-tile.md) in het dashboard.
* [Selecteer een tegel](service-dashboard-tiles.md) om het onderliggende rapport te openen.
* Als uw gegevensset is ingesteld op dagelijks vernieuwen, kunt u het vernieuwingsschema wijzigen of de gegevensset handmatig vernieuwen met **Nu vernieuwen**

## <a name="whats-included"></a>Wat is opgenomen
Het Azure Enterprise-inhoudspakket bevat maandelijkse rapportagegegevens voor het bereik van de maanden die u tijdens de verbindingsprocedure opgeeft. Het bereik is een zwevend venster, zodat de opgenomen datums worden bijgewerkt zodra de gegevensset wordt vernieuwd.

## <a name="system-requirements"></a>Systeemvereisten
Voor het inhoudspakket is toegang vereist tot de bedrijfsfuncties binnen de Azure-portal.

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Parameters zoeken
Power BI-rapportage is beschikbaar voor EA Direct, partners en indirecte klanten die geen factuurgegevens kunnen bekijken. Lees de sectie hieronder voor meer informatie over het vinden van elk van de waarden die de verbindingsstroom verwacht.

**URL van de Azure-omgeving**

* Deze waarde is doorgaans https://ea.azure.com, maar u kunt de URL controleren als u zich aanmeldt.
  
    ![](media/service-connect-to-azure-enterprise/params3.png)

**Aantal maanden**

* Dit moet een getal zijn tussen 1-36 dat het aantal maanden van gegevens (vanaf vandaag) aangeeft dat u wilt importeren.

I**nschrijvingsnummer**

* Dit is het Azure Enterprise-inschrijvingsnummer dat u op het startscherm kunt vinden van de [Azure Enterprise-portal](https://ea.azure.com/) onder Inschrijvingsdetails.
  
    ![](media/service-connect-to-azure-enterprise/params2.png)

**Toegangssleutel**

* Uw sleutel vindt u in de Azure Enterprise-portal onder Gebruiksgegevens downloaden > API-toegangssleutel
  
    ![](media/service-connect-to-azure-enterprise/creds2.png)

**Aanvullende Help**

* Voor extra hulp bij het instellen van het Azure Enterprise Power BI-pakket kunt u inloggen op de Azure Enterprise-portal om het API-helpbestand te bekijken onder Help en aanvullende instructies onder Rapporten -> Gebruiksgegevens downloaden -> API-toegangssleutel.

## <a name="next-steps"></a>Volgende stappen
[Aan de slag in Power BI](service-get-started.md)

[Gegevens ophalen in Power BI](service-get-data.md)

