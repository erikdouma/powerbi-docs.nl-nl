---
title: Power BI en ExpressRoute
description: Power BI en ExpressRoute
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-admin
ms.topic: conceptual
ms.date: 12/03/2018
ms.author: mblythe
LocalizationGroup: Administration
ms.openlocfilehash: 62289c974e25207f3a991e7f17a0ee965c729b8a
ms.sourcegitcommit: b03912343a5a214c6bb972aaa6aa051c2a5f4332
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2018
ms.locfileid: "52900124"
---
# <a name="power-bi-and-expressroute"></a>Power BI en ExpressRoute

**ExpressRoute** is een Azure-service waarmee u particuliere verbindingen kunt opzetten tussen Azure-datacenters (waarin Power BI zich bevindt) en uw on-premises infrastructuur, of particuliere verbindingen tussen Azure-datacenters en uw co-locatieomgeving.

Met **Power BI** en **ExpressRoute** kunt u een verbinding via een particulier netwerk opzetten tussen uw organisatie en Power BI (of met behulp van de co-locatievoorziening van een internetprovider), om zo internet te omzeilen en uw gevoelige gegevens en verbindingen van Power BI beter te beveiligen.

Raadpleeg [Overzicht van ExpressRoute](/azure/expressroute/expressroute-introduction) voor meer informatie. Power BI is compatibel met ExpressRoute, met een aantal uitzonderingen waarin Power BI gegevens ophaalt of verstuurt via het openbare internet. Raadpleeg [Power BI-URL's](power-bi-whitelist-urls.md) voor een lijst van de URL's die door Power BI worden gebruikt.

![ExpressRoute-diagram](media/service-admin-power-bi-expressroute/pbi_expressroute_1.png)