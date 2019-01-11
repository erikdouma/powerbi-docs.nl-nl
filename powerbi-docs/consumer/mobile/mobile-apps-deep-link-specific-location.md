---
title: Maak een koppeling naar een specifieke locatie in de Power BI - Mobiel-apps
description: Informatie over het maken van de dieptekoppeling naar een specifiek dashboard, tegel of rapport in de Power BI - Mobiel-app met een uniform resource identifier (URI).
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-mobile
ms.topic: conceptual
ms.date: 06/28/2018
ms.author: maggies
ms.openlocfilehash: 1f9503980ba19b290fa5d0fd1f521bb85ef93759
ms.sourcegitcommit: 5206651c12f2b91a368f509470b46f3f4c5641e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/02/2019
ms.locfileid: "53983572"
---
# <a name="create-a-link-to-a-specific-location-in-the-power-bi-mobile-apps"></a>Maak een koppeling naar een specifieke locatie in de Power BI - Mobiel-apps
U kunt een uniform resource identifier (URI) gebruiken om een koppelen te maken met een specifieke locatie (een *dieptekoppeling*) in de Power BI - Mobiel-apps op alle mobiele platforms: iOS, Android-apparaten en Windows 10.

URI-koppelingen kunnen rechtstreeks verwijzen naar dashboards, tegels en rapporten.

De bestemming van de dieptekoppeling bepaalt de indeling van de URI. Volg deze stappen om dieptekoppelingen naar verschillende locaties te maken. 

## <a name="open-the-power-bi-mobile-app"></a>De Power BI - Mobiel-app openen
Gebruik deze URI om de Power BI - Mobiel-app te openen op elk apparaat:

    mspbi://app/


## <a name="open-to-a-specific-dashboard"></a>Naar een specifiek dashboard openen
Met deze URI wordt de Power BI - Mobiel-app geopend naar een specifiek dashboard:

    mspbi://app/OpenDashboard?DashboardObjectId=<36-character-dashboard-id>

Ga naar het specifieke dashboard in de Power BI-service (https://powerbi.com)) om de dashboardobject-id met 36 tekens op te halen. Zie bijvoorbeeld het gemarkeerde gedeelte van deze URL:

`https://powerbi.com/groups/me/dashboards/**61b7e871-cb98-48ed-bddc-6572c921e270**`

Voeg `&GroupObjectId=<36-character-group-id>` toe vóór of na de dashboard-id wanneer het dashboard zich in een groep bevindt die niet Mijn werkruimte is. Bijvoorbeeld, 

mspbi://app/OpenDashboard?DashboardObjectId=e684af3a-9e7f-44ee-b679-b9a1c59b5d60 **&GroupObjectId=8cc900cc-7339-467f-8900-fec82d748248**

Let op het en-teken (&) tussen de twee.

## <a name="open-to-a-specific-tile-in-focus"></a>Een specifieke tegel in focus openen
Met deze URI wordt een specifieke tegel in focus geopend in de Power BI - Mobiel-app:

    mspbi://app/OpenTile?DashboardObjectId=<36-character-dashboard-id>&TileObjectId=<36-character-tile-id>

Ga naar het specifieke dashboard in de Power BI-service (https://powerbi.com)) en open de tegel in de focusmodus om de dashboard- en tegelobject-id met 36 tekens op te halen. Zie bijvoorbeeld de gemarkeerde gedeelten van deze URL:

`https://powerbi.com/groups/me/dashboards/**3784f99f-b460-4d5e-b86c-b6d8f7ec54b7**/tiles/**565f9740-5131-4648-87f2-f79c4cf9c5f5**/infocus`

Voor deze zou, zou de URI als volgt zijn:

    mspbi://app/OpenTile?DashboardObjectId=3784f99f-b460-4d5e-b86c-b6d8f7ec54b7&TileObjectId=565f9740-5131-4648-87f2-f79c4cf9c5f5

Let op het en-teken (&) tussen de twee.

Voeg toe `&GroupObjectId=<36-character-group-id>` als het dashboard zich in een groep bevindt die niet Mijn werkruimte is

## <a name="open-to-a-specific-report"></a>Naar een specifiek rapport openen
Met deze URI wordt een specifiek rapport geopend in de Power BI - Mobiel-app:

    mspbi://app/OpenReport?ReportObjectId=<36-character-report-id>

Ga naar het specifiek rapport in de Power BI-service (https://powerbi.com)) om de rapportobject-id met 36 tekens op te halen. Zie bijvoorbeeld het gemarkeerde gedeelte van deze URL:

`https://powerbi.com/groups/me/reports/df9f0e94-31df-450b-b97f-4461a7e4d300`

Voeg `&GroupObjectId=<36-character-group-id>` toe vóór of na de rapport-id wanneer het rapport zich in een groep bevindt die niet Mijn werkruimte is. Bijvoorbeeld, 

mspbi://app/OpenReport?ReportObjectId=e684af3a-9e7f-44ee-b679-b9a1c59b5d60 **&GroupObjectId=8cc900cc-7339-467f-8900-fec82d748248**

Let op het en-teken (&) tussen de twee.

## <a name="open-to-a-specific-report-page"></a>Naar een specifieke rapportpagina openen
Met deze URI wordt een specifieke rapportpagina geopend in de Power BI - Mobiel-app:

    mspbi://app/OpenReport?ReportObjectId=<36-character-report-id>&reportPage=ReportSection<number>

De rapportpagina heet ReportSection, gevolgd door een getal. Open nogmaals het rapport in de Power BI-service (https://powerbi.com)) en ga naar de specifieke rapportpagina. 

Zie bijvoorbeeld het gemarkeerde gedeelte van deze URL:

`https://powerbi.com/groups/me/reports/df9f0e94-31df-450b-b97f-4461a7e4d300/ReportSection11`

## <a name="open-in-full-screen-mode"></a>In de volledige-schermmodus openen
Voeg de vetgedrukte parameter toe om een specifiek rapport in de volledige-schermmodus te openen:

    mspbi://app/OpenReport?ReportObjectId=<36-character-report-id>**&openFullScreen=true**

Bijvoorbeeld: 

mspbi://app/OpenReport?ReportObjectId=500217de-50f0-4af1-b345-b81027224033&openFullScreen=true

## <a name="add-context-optional"></a>Context toevoegen (optioneel)
U kunt ook context toevoegen aan de tekenreeks. Deze context kan worden gebruikt om onze gegevens naar uw app te filteren als u contact met ons op moet nemen. Voeg `&context=<app-name>` toe aan de koppeling

Zie bijvoorbeeld het gemarkeerde gedeelte van deze URL: 

`https://powerbi.com/groups/me/reports/df9f0e94-31df-450b-b97f-4461a7e4d300/&context=SlackDeepLink`

## <a name="next-steps"></a>Volgende stappen
Op basis van uw feedback kunnen we bepalen wat in de toekomst moet worden geïmplementeerd. Vergeet dus niet op andere functies te stemmen die u graag in de mobiele Power BI-apps zou willen zien. 

* [Power BI-apps voor mobiele apparaten](mobile-apps-for-mobile-devices.md)
* Volg @MSPowerBI op Twitter
* Deelnemen aan conversaties in de [Power BI-community](http://community.powerbi.com/)
* [Wat is Power BI?](../../power-bi-overview.md)

