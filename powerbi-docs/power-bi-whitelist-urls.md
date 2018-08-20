---
title: Power BI-URL’s
description: Eindpunten moeten bereikbaar zijn voor klanten die gebruikmaken van Power BI
author: markingmyname
ms.author: maghan
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 08/13/2018
ms.openlocfilehash: 8e29fa0c9471bb865619102247f38776208c3d87
ms.sourcegitcommit: 8990028a348b642ba5c96f001fe3a4280f0166ee
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/14/2018
ms.locfileid: "40101122"
---
# <a name="power-bi-urls"></a>Power BI-URL’s

Voor de **online Power BI-service**, ook wel bekend als de toepassing Power BI SaaS (Software as a Service) is een verbinding met internet vereist. De onderstaande eindpunten moeten bereikbaar zijn voor klanten die de online Power BI-service gebruiken.

Voor het gebruik van de online Power BI-service moet u toegang hebben om verbinding te maken met de eindpunten die als **Vereist** zijn gemarkeerd in de onderstaande tabellen en eindpunten die als **Vereist** zijn gemarkeerd op de gekoppelde sites. Als de koppeling naar een externe site naar een specifieke sectie verwijst, hoeft u alleen maar de eindpunten in die sectie te bekijken.

Eindpunten die zijn gemarkeerd als **Optioneel**, kunnen ook **in de lijst met toegestane items worden opgenomen** om een specifieke functionaliteit te laten werken.

Voor de online Power BI-service is alleen vereist dat TCP-poort 443 voor de vermelde eindpunten wordt geopend.

Jokertekens (*) weerspiegelen alle niveaus onder het hoofddomein, en er wordt N.v.t. gebruikt als gegevens niet beschikbaar zijn. De kolom **Bestemmingen** voorziet in een lijst met FQDN/domeinen en koppelingen naar externe sites met extra informatie over het eindpunt.

>[!Important]
>De informatie in de onderstaande tabellen betreft niet de **cloud van de Amerikaanse regering**, **de cloud van Duitsland** en **de cloud van China**.

## <a name="authentication"></a>Verificatie

Power BI is afhankelijk van de vereiste eindpunten in de Office 365-secties voor verificatie en identiteit. Voor het gebruik van Power BI moet u verbinding kunnen maken met de eindpunten in de onderstaande gekoppelde site.

| Rij | Functie | Bestemming(en) | Poort(en) |
|-----|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|--------------|---------------------------------------------|
| 1 | **Vereist:** Verificatie en identiteit | Zie de [sectie voor Office 365-verificatie en -identiteit](https://support.office.com/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2#bkmk_identity) van de site met de lijst met Office 365-items | N.v.t. |

## <a name="general-site-usage"></a>Algemeen gebruik van de website

Voor algemeen gebruik van Power BI moet u verbinding kunnen maken met de eindpunten in de tabel en de gekoppelde sites eronder.

| Rij | Functie | Bestemming(en) | Poort(en) |
|-----|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|--------------|---------------------------------------------|
| 1 | **Vereist:** Back-end-API's | *.analysis.windows.net | TCP 443 |
| 2 | **Vereist:** Office 365-integratie | Zie de [sectie voor de Office 365-portal en gedeelde services](https://support.office.com/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2#bkmk_portal-identity) van de site met de lijst met toegestane Office 365-items | N.v.t. |
| 3 | **Vereist:** Portal | app.powerbi.com | TCP 443 |
| 4 | **Vereist:** Telemetrie naar service | dc.services.visualstudio.com | TCP 443 |
| 5 | **Optioneel:** Informatieve berichten | dynmsg.modpim.com | TCP 443 |
| 6 | **Optioneel:** NPS-enquêtes | nps.onyx.azure.net | TCP 443 |

## <a name="administration"></a>Beheer

Als u beheerfuncties wilt uitvoeren in Power BI, moet u verbinding kunnen maken met de eindpunten in de onderstaande, gekoppelde sites.

| Rij | Functie | Bestemming(en) | Poort(en) |
|-----|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|--------------|---------------------------------------------|
| 1 | **Vereist:** Voor het beheren van gebruikers en het bekijken van auditlogboeken | Zie de [sectie voor de Office 365-portal en gedeelde services](https://support.office.com/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2#bkmk_portal-identity) van de site met de lijst met toegestane Office 365-items | N.v.t. |

## <a name="get-data"></a>Gegevens ophalen

Als u gegevens wilt kunnen ophalen uit specifieke gegevensbronnen, zoals OneDrive, moet u verbinding kunnen maken met de eindpunten in de onderstaande tabel.

| Rij | Functie | Bestemming(en) | Poort(en) |
|-----|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|--------------|---------------------------------------------|
| 1 | **Vereist:** AppSource (interne of externe apps in Power BI) | appsource.microsoft.com | TCP 443 |
| 2 | **Optioneel:** Bestanden importeren uit OneDrive - Persoonlijk | Zie de [Vereiste URL's en poorten voor OneDrive-site](https://support.office.com/en-ie/article/required-urls-and-ports-for-onedrive-ce15d2cc-52ef-42cd-b738-d9c6f9b03f3a) | N.v.t. |
| 3 | **Optioneel:** Power BI in zelfstudievideo van 60 seconden | *.doubleclick.net </br> *.ggpht.com </br> *.google.com </br> *.googlevideo.com </br> *.youtube.com </br> *.ytimg.com </br> fonts.gstatic.com | TCP 443 |
| 4 | **Optioneel:** Bronnen voor PubNub-streaminggegevens | Zie de [PubNub-documentatie](https://support.pubnub.com/support/solutions/articles/14000043522) | N.v.t. |

## <a name="dashboard-and-report-integration"></a>Integratie dashboard en rapport 

Power BI is afhankelijk van bepaalde eindpunten om uw dashboards en rapporten te kunnen ondersteunen. U moet verbinding kunnen maken met de eindpunten in de tabel en de gekoppelde sites eronder.

| Rij | Functie | Bestemming(en) | Poort(en) |
|-----|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|--------------|---------------------------------------------|
| 1 | **Vereist:** Excel-integratie | Zie de [sectie voor Office Online](https://support.office.com/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2#bkmk_officeonline) van de site met de lijst met toegestane Office 365-items | N.v.t. |

## <a name="custom-visuals"></a>Aangepaste visuals

Power BI is afhankelijk van bepaalde eindpunten om de aangepaste visuals te kunnen weergeven en openen. U moet verbinding kunnen maken met de eindpunten in de tabel en de gekoppelde sites eronder.

| Rij | Functie | Bestemming(en) | Poort(en) |
|-----|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|--------------|---------------------------------------------|
| 1 | **Vereist:** Een aangepaste visual en een bestand importeren uit de Marketplace-interface | *.microsoft.com </br> *.bing.com </br> *.msecnd.net </br> *.osi.office.net </br> *.azureedge.net </br> ajax.aspnetcdn.com </br> nexus.ensighten.com </br> store.office.com | TCP 443 |
| 2 | **Optioneel:** Bing Kaarten | bing.com </br> platform.bing.com </br> *.dynamic.tiles.virtualearth.net </br> *.virtualearth.net | TCP 443 |
| 3 | **Optioneel:** PowerApps | Zie het [gedeelte Vereiste services](https://docs.microsoft.com/powerapps/maker/canvas-apps/limits-and-config#required-services) van de site met systeemvereisten voor PowerApps | N.v.t. |
| 4 | **Optioneel:** Visio | Zie de [sectie voor Office Online](https://support.office.com/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2#bkmk_officeonline) van de site met de lijst met toegestane Office 365-items | N.v.t. |