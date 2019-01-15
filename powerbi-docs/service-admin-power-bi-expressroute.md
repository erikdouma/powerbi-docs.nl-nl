---
title: Power BI en ExpressRoute
description: Power BI en ExpressRoute
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 12/03/2018
ms.author: mblythe
LocalizationGroup: Administration
ms.openlocfilehash: 0c4618150094a4eabb0dc9745e9ac93e4f342ff1
ms.sourcegitcommit: c8c126c1b2ab4527a16a4fb8f5208e0f7fa5ff5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2019
ms.locfileid: "54291091"
---
# <a name="power-bi-and-expressroute"></a>Power BI en ExpressRoute

**ExpressRoute** is een Azure-service waarmee u particuliere verbindingen kunt opzetten tussen Azure-datacenters (waarin Power BI zich bevindt) en uw on-premises infrastructuur, of particuliere verbindingen tussen Azure-datacenters en uw co-locatieomgeving.

Met **Power BI** en **ExpressRoute** kunt u een verbinding via een particulier netwerk opzetten tussen uw organisatie en Power BI (of met behulp van de co-locatievoorziening van een internetprovider), om zo internet te omzeilen en uw gevoelige gegevens en verbindingen van Power BI beter te beveiligen.

Raadpleeg [Overzicht van ExpressRoute](/azure/expressroute/expressroute-introduction) voor meer informatie. Power BI is compatibel met ExpressRoute, met een aantal uitzonderingen waarin Power BI gegevens ophaalt of verstuurt via het openbare internet. Raadpleeg [Power BI-URL's](power-bi-whitelist-urls.md) voor een lijst van de URL's die door Power BI worden gebruikt.

![ExpressRoute-diagram](media/service-admin-power-bi-expressroute/pbi_expressroute_1.png)