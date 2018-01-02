---
title: Verbinding maken met Acumatica met Power BI
description: Acumatica voor Power BI
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
ms.openlocfilehash: dd64f4fb4651e393e770dda9323c10356424c780
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-acumatica-with-power-bi"></a>Verbinding maken met Acumatica met Power BI
Met het Acumatica-inhoudspakket voor Power BI kunt u snel inzicht verkrijgen in uw verkoopkansgegevens. Power BI haalt uw gegevens op inclusief kansen, accounts en klanten, en bouwt vervolgens een standaard dashboard en gerelateerde rapporten op basis van die gegevens.

Maak verbinding met het [Acumatica-inhoudspakket](https://app.powerbi.com/getdata/services/acumatica) of lees meer over de [Acumatica-integratie](https://powerbi.microsoft.com/integrations/acumatica) met Power BI.

>[!NOTE]
>Dit inhoudspakket vereist Acumatica v5.2 of hoger.

## <a name="how-to-connect"></a>Verbinding maken
1. Selecteer **Gegevens ophalen** onder in het linkernavigatievenster.
   
   ![](media/service-connect-to-acumatica/getdata3.png)
2. Selecteer in het vak **Services** de optie **Ophalen**.
   
   ![](media/service-connect-to-acumatica/getdata2.png)
3. Selecteer **Acumatica** \> **Ophalen**.
   
   ![](media/service-connect-to-acumatica/acumatica.png)
4. Voer uw Acumatica OData-eindpunt in. Met een OData-eindpunt kan een extern systeem gegevens aanvragen van Acumatica. Een Acumatica OData-eindpunt is als volgt ingedeeld en moet HTTPS gebruiken:
   
     https://[sitedomain]/odata/[companyname]
   
   De naam van het bedrijf is alleen vereist als u een implementatie voor meerdere bedrijven hebt. Hieronder vindt u meer informatie over het zoeken naar deze parameter in uw Acumatica-account.
   
   ![](media/service-connect-to-acumatica/parameters.png)
5. Selecteer voor verificatiemethode **Basisverificatie**. Voer uw gebruikersnaam en wachtwoord van uw Acumatica-account in en klik op **Aanmelden**.
   
    ![](media/service-connect-to-acumatica/creds2.png)
6. Nadat de gegevens in Power BI zijn geïmporteerd, ziet u een nieuw dashboard, een nieuw rapport en een nieuwe gegevensset in het navigatiedeelvenster aan de linkerzijde. Nieuwe items worden gemarkeerd met een geel sterretje \* dat na het selecteren verdwijnt. Het dashboard wordt weergegeven in een indeling die vergelijkbaar is met die hieronder:
   
    ![](media/service-connect-to-acumatica/dashboard.png)

**Wat nu?**

* [Stel vragen in het vak Q&A](service-q-and-a.md) boven in het dashboard
* [Wijzig de tegels](service-dashboard-edit-tile.md) in het dashboard.
* [Selecteer een tegel](service-dashboard-tiles.md) om het onderliggende rapport te openen.
* Als uw gegevensset is ingesteld op dagelijks vernieuwen, kunt u het vernieuwingsschema wijzigen of de gegevensset handmatig vernieuwen met **Nu vernieuwen**

## <a name="system-requirements"></a>Systeemvereisten
Voor dit inhoudspakket is Acumatica v5.2 of hoger vereist. Controleer de versie bij uw Acumatica-beheerder.

## <a name="finding-parameters"></a>Parameters zoeken
**Acumatica OData-eindpunt**

Een Acumatica OData-eindpunt is als volgt ingedeeld en moet HTTPS gebruiken:

    https://[sitedomain]/odata/[companyname]

Het domein van de toepassingssite vindt u in de adresbalk van uw browser wanneer u zich bij Acumatica aanmeldt. In het onderstaande voorbeeld is het domein van de site https://pbi.acumatica.com. Het OData-eindpunt zou dus https://pbi.acumatica.com/odata moeten zijn.

 ![](media/service-connect-to-acumatica/url.png)

De naam van het bedrijf is alleen vereist als u een implementatie voor meerdere bedrijven hebt. U vindt deze informatie op de aanmeldpagina van Acumatica.

![](media/service-connect-to-acumatica/signin2.png)

## <a name="troubleshooting"></a>Probleemoplossing
Als u zich niet kunt aanmelden, controleer dan of het Acumatica OData-eindpunt dat u hebt opgegeven de juiste indeling heeft.

    https://<application site domain>/odata/<company name>

Als u problemen ondervindt bij het verbinding maken, controleer dan uw Acumatica-versie bij uw beheerder. Voor dit inhoudspakket is versie 5.2 of hoger vereist.

## <a name="next-steps"></a>Volgende stappen
[Aan de slag in Power BI](service-get-started.md)

[Gegevens ophalen in Power BI](service-get-data.md)

