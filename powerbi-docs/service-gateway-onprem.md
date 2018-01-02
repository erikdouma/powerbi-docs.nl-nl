---
title: On-premises gegevensgateway
description: Dit is een overzicht van de on-premises gegevensgateway voor Power BI. U kunt deze gateway gebruiken om te werken met DirectQuery-gegevensbronnen. U kunt deze gateway ook gebruiken om cloud-gegevenssets te vernieuwen met on-premises gegevens.
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
ms.tgt_pltfrm: na
ms.workload: powerbi
ms.date: 11/27/2017
ms.author: davidi
ms.openlocfilehash: 4693349715e7a38ae936318e9a8750e0b2f3fab0
ms.sourcegitcommit: 7742f952c20695dfb475f74965c0065b02c01521
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/29/2017
---
# <a name="on-premises-data-gateway"></a>On-premises gegevensgateway
De on-premises gegevensgateway fungeert als een brug waarmee u over snelle en veilige gegevensoverdracht beschikt tussen on-premises gegevens (gegevens die zich niet in de cloud bevinden) en de services van Power BI, Microsoft Flow, Logic Apps en PowerApps.

U kunt één gateway met verschillende services tegelijk gebruiken. Als u Power BI en PowerApps gebruikt, kan één gateway worden gebruikt voor beiden. Dit is afhankelijk van het account waarmee u zich aanmeldt.

> [!NOTE]
> Via de on-premises gegevensgateway worden gegevenscompressie en transportversleuteling in alle modi geïmplementeerd.
> 
> 

<!-- Shared Requirements Include -->
[!INCLUDE [gateway-onprem-requirements-include](./includes/gateway-onprem-requirements-include.md)]

### <a name="limitations-of-analysis-services-live-connections"></a>Beperkingen van liveverbindingen van Analysis Services
U kunt een liveverbinding gebruiken voor tabelvormige of multidimensionale exemplaren.

| **Server-versie** | **Vereiste SKU** |
| --- | --- |
| 2012 SP1 CU4 of hoger |Business Intelligence en Enterprise-SKU |
| 2014 |Business Intelligence en Enterprise-SKU |
| 2016 |Standaard-SKU of hoger |

* Opmaak op celniveau en vertaalfuncties worden niet ondersteund.
* Acties en benoemde sets zijn niet beschikbaar in Power BI, maar u kunt wel verbinding maken met multidimensionale kubussen die ook acties of benoemde sets bevatten. Ook kunt u visuele elementen en rapporten maken.

<!-- Shared Install steps Include -->
[!INCLUDE [gateway-onprem-datasources-include](./includes/gateway-onprem-datasources-include.md)]

## <a name="download-and-install-the-on-premises-data-gateway"></a>De on-premises gegevensgateway downloaden en installeren
Selecteer **Gegevensgateway** in het menu Downloads om de gateway te downloaden. Download de [on-premises gegevensgateway](http://go.microsoft.com/fwlink/?LinkID=820925).

![](media/service-gateway-onprem/powerbi-download-data-gateway.png)

<!-- Shared Install steps Include -->
[!INCLUDE [gateway-onprem-install-include](./includes/gateway-onprem-install-include.md)]

## <a name="install-the-gateway-in-personal-mode"></a>De gateway in persoonlijke modus installeren
> [!NOTE]
> Persoonlijk werkt alleen met Power BI.
> 
> 

Nadat de persoonlijke gateway is geïnstalleerd, moet u de **Power BI Gateway - Persoonlijke configuratiewizard** starten.

![](media/service-gateway-onprem/personal-gateway-launch-configuration.png)

Vervolgens moet u zich aanmelden bij Power BI om de gateway te registreren bij de cloudservice.

![](media/service-gateway-onprem/personal-gateway-signin.png)

U moet ook de Windows-gebruikersnaam en het wachtwoord invoeren dat hoort bij de Windows-service. U kunt een ander Windows-account van uzelf opgeven. De gateway-service wordt uitgevoerd met dit account.

![](media/service-gateway-onprem/personal-gateway-windows-service.png)

Nadat de installatie is voltooid, gaat u naar de gegevenssets in Power BI en controleert u of de referenties zijn ingevoerd voor uw on-premises gegevensbronnen.

<a name="credentials"></a>

## <a name="storing-encrypted-credentials-in-the-cloud"></a>Versleutelde referenties opslaan in de cloud
Wanneer u een gegevensbron aan de gateway toevoegt, moet u referenties opgeven voor de gegevensbron. Alle query's over de gegevensbron worden uitgevoerd met deze referenties. Voordat de referenties worden opgeslagen in de cloud, worden ze veilig versleuteld met behulp van asymmetrische codering zodat ze in de cloud niet kunnen niet worden ontsleuteld. De referenties worden verzonden naar de machine waarop de gateway wordt uitgevoerd, waar ze worden ontsleuteld als de gegevensbronnen worden geopend.

<!-- Account and Port information -->
[!INCLUDE [gateway-onprem-accounts-ports-more](./includes/gateway-onprem-accounts-ports-more.md)]

<!-- How the gateway works -->
[!INCLUDE [gateway-onprem-how-it-works-include](./includes/gateway-onprem-how-it-works-include.md)]

## <a name="troubleshooting"></a>Probleemoplossing
Zie [Problemen met de on-premises gegevensgateway oplossen](service-gateway-onprem-tshoot.md) als u problemen hebt bij het installeren en configureren van een gateway. Als u denkt dat er een probleem is met uw firewall, raadpleegt u de sectie [Firewall of proxyserver](service-gateway-onprem-tshoot.md#firewall-or-proxy) in het artikel over probleemoplossing.

Zie [Proxy-instellingen voor de Power BI-gateways configureren](service-gateway-proxy.md) als u denkt dat er proxy-problemen met de gateway zijn.

## <a name="next-steps"></a>Volgende stappen
[Manage your data source - Analysis Services](service-gateway-enterprise-manage-ssas.md) (Uw gegevensbron beheren - Analysis Services)  
[Manage your data source - SAP HANA](service-gateway-enterprise-manage-sap.md) (Gegevensbron beheren - SAP HANA)  
[Manage your data source - SQL Server](service-gateway-enterprise-manage-sql.md) (Gegevensbron beheren - SQL Server)  
[Manage your data source - Oracle](service-gateway-onprem-manage-oracle.md) (Gegevensbron beheren - Oracle)  
[Manage your data source - Import/Scheduled refresh](service-gateway-enterprise-manage-scheduled-refresh.md) (Gegevensbron beheren - importeren/geplande vernieuwing)  
[On-premises data gateway in-depth](service-gateway-onprem-indepth.md) (On-premises gegevensgateway - uitgebreid)  
[On-premises data gateway (personal mode) - the new version of the personal gateway (On-premises gegevensgateway (persoonlijke modus) - de nieuwe versie van de persoonlijke gateway)](service-gateway-personal-mode.md)
[Proxy-instellingen voor de on-premises gegevensgateway configureren](service-gateway-proxy.md)  
Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

