---
title: Problemen met een geplande vernieuwing voor Azure SQL-databases oplossen
description: Problemen met een geplande vernieuwing voor Azure SQL-databases oplossen in Power BI
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 12/06/2017
ms.author: mblythe
LocalizationGroup: Troubleshooting
ms.openlocfilehash: 9439ac6bd0b4df568b964f548372fb94d2fd0b26
ms.sourcegitcommit: 998b79c0dd46d0e5439888b83999945ed1809c94
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/17/2018
---
# <a name="troubleshooting-scheduled-refresh-for-azure-sql-databases-in-power-bi"></a>Problemen met een geplande vernieuwing voor Azure SQL-databases oplossen in Power BI
Voor gedetailleerde stappen voor het instellen van de geplande vernieuwing, kunt u [Gegevens vernieuwen in Power BI](refresh-data.md) raadplegen.

Als u tijdens het instellen van de geplande vernieuwing voor Azure SQL een fout met foutcode 400 krijgt bij het bewerken van de referenties, probeert u het volgende om de juiste firewallregel in te stellen:

1. Meld u aan bij de Azure Management Portal
2. Ga naar de Azure SQL-server waarvoor u de vernieuwing wilt configureren
3. Schakel 'Windows Azure-services' in het gedeelte Toegestane services in

![](media/service-admin-troubleshooting-scheduled-refresh-azure-sql-databases/azurerefresh.png)  

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

