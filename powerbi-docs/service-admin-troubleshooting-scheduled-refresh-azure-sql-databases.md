---
title: Problemen met een geplande vernieuwing voor Azure SQL-databases oplossen
description: Problemen met een geplande vernieuwing voor Azure SQL-databases oplossen in Power BI
services: powerbi
documentationcenter: 
author: guyinacube
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
ms.date: 09/06/2017
ms.author: davidi
ms.openlocfilehash: ff219e3032837e91f3c63e0c08f3abd1121e72ff
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2017
---
# <a name="troubleshooting-scheduled-refresh-for-azure-sql-databases-in-power-bi"></a>Problemen met een geplande vernieuwing voor Azure SQL-databases oplossen in Power BI
Voor gedetailleerde stappen voor het instellen van de geplande vernieuwing, kunt u [Gegevens vernieuwen in Power BI](refresh-data.md) raadplegen.

Als u tijdens het instellen van de geplande vernieuwing voor Azure SQL een fout met foutcode 400 krijgt bij het bewerken van de referenties, probeert u het volgende om de juiste firewallregel in te stellen:

1. Meld u aan bij de Azure Management Portal
2. Ga naar de Azure SQL-server waarvoor u de vernieuwing wilt configureren
3. Schakel 'Windows Azure-services' in het gedeelte Toegestane services in

![](media/service-admin-troubleshooting-scheduled-refresh-azure-sql-databases/azurerefresh.png)  

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

