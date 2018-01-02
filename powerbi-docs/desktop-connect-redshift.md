---
title: Verbinding met een Amazon Redshift-database maken in Power BI Desktop
description: Eenvoudig verbinding maken met een Amazon Redshift-database in Power BI Desktop en deze gebruiken
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
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 12/06/2017
ms.author: davidi
ms.openlocfilehash: e54bd3a9653372fdd560bd915ea09f16ee9c29f3
ms.sourcegitcommit: d91436de68a0e833ecff18d976de9d9431bc4121
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/06/2017
---
# <a name="connect-to-amazon-redshift-in-power-bi-desktop"></a>Verbinding met Amazon Redshift maken in Power BI Desktop
In **Power BI Desktop** kunt u verbinding maken met een **Amazon Redshift**-database en gebruikmaken van de onderliggende gegevens, net zoals elke andere gegevensbron in Power BI Desktop.

## <a name="connect-to-an-amazon-redshift-database"></a>Verbinding maken met een Amazon Redshift-database
Als u verbinding wilt maken met een **Amazon Redshift**-database, selecteert u **Gegevens ophalen** op het lint **Start** in Power BI Desktop. Selecteer **Database** in de categorieën aan de linkerkant en u ziet **Amazon Redshift**.

![](media/desktop-connect-redshift/connect_redshift_3.png)

In het **Amazon Redshift**-venster dat verschijnt, typt of plakt u de naam van uw **Amazon Redshift**-server en -database in het vak. In een deel van het veld *Server* kan een gebruiker een poort opgeven volgende de indeling *ServerURL:Port*

![](media/desktop-connect-redshift/connect_redshift_4.png)

Voer uw gebruikersnaam en wachtwoord in als u daarom wordt gevraagd.

![](media/desktop-connect-redshift/connect_redshift_5.png)

Als u verbinding hebt gemaakt, verschijnt er een **Navigator**-scherm waarin de gegevens worden getoond die op de server beschikbaar zijn. Hier kunt u een of meer elementen selecteren die u in **Power BI Desktop** wilt importeren en gebruiken.

![](media/desktop-connect-redshift/connect_redshift_6.png)

Als u uw selecties in het venster **Navigator** hebt gemaakt, kunt u de gegevens **laden** of **bewerken**.

* Als u de gegevens wilt **laden**, wordt u gevraagd of u *Importeren* of *DirectQuery* wilt gebruiken om de gegevens te laden. Zie [dit artikel voor uitleg over DirectQuery](desktop-use-directquery.md) (Engelstalig) voor meer informatie.
* Als u **Bewerken** selecteert om de gegevens te bewerken, wordt **Query-editor** weergegeven. Hier kunt u allerlei transformaties en filters op de gegevens toepassen, waarvan vele worden toegepast op de onderliggende **Amazon Redshift**-database zelf (indien ondersteund).

## <a name="next-steps"></a>Volgende stappen
Met Power BI Desktop kunt u verbinding maken met allerlei andere gegevens. Bekijk de volgende bronnen voor meer informatie over gegevensbronnen:

* [Getting Started with Power BI Desktop](desktop-getting-started.md) (Aan de slag met Power BI Desktop)
* [Data Sources in Power BI Desktop](desktop-data-sources.md) (Gegevensbronnen in Power BI Desktop)
* [Shape and Combine Data with Power BI Desktop](desktop-shape-and-combine-data.md) (Gegevens vormgeven en combineren met Power BI Desktop)
* [Connect to Excel workbooks in Power BI Desktop](desktop-connect-excel.md) (Verbinding maken met Excel-werkmappen in Power BI Desktop)   
* [Enter data directly into Power BI Desktop](desktop-enter-data-directly-into-desktop.md) (Rechtstreeks gegevens in Power BI Desktop invoeren)   

