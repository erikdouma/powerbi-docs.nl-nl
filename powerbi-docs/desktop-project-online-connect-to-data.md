---
title: 'Project Online: verbinding met gegevens maken via Power BI Desktop'
description: 'Project Online: verbinding met gegevens maken via Power BI Desktop'
services: powerbi
documentationcenter: ''
author: davidiseminger
manager: kfile
backup: ''
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 05/02/2018
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: c8293499059b66879b7e52fba579fd0ae15aba3d
ms.sourcegitcommit: f679c05d029ad0765976d530effde744eac23af5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2018
---
# <a name="project-online-connect-to-data-through-power-bi-desktop"></a>Project Online: verbinding met gegevens maken via Power BI Desktop
U kunt verbinding maken met gegevens maken in Project Online via Power BI Desktop.

### <a name="step-1-download-power-bi-desktop"></a>Stap 1: Power BI Desktop downloaden
1. [Download Power BI Desktop](http://go.microsoft.com/fwlink/?LinkID=521662) en voer vervolgens het installatieprogramma uit om **Power BI Desktop** op uw computer te installeren.

### <a name="step-2-connect-to-project-online-with-odata"></a>Stap 2: verbinding maken met Project Online met OData
1. Open **Power BI Desktop**.
2. Op het *welkomstscherm* selecteert u **Gegevens ophalen.**
3. Kies **OData-feed** en selecteer **Verbinding maken**.
4. Voer het adres voor uw OData-feed in het URL-vak in en klik op OK.
   
   Als het adres voor uw Project Web App-site op https://\<tenantname\>.sharepoint.com/sites/pwa lijkt, is het adres dat u invoert voor uw OData-feed https://\<tenantname\>.sharepoint.com/sites/pwa/\_api/Projectdata.
   
   Voor ons voorbeeld gebruiken we https://contoso.sharepoint.com/sites/pwa/default.aspx
5. Power BI Desktop vraagt u om te verifiëren met uw Office 365-account. Selecteer Organisatieaccount en voer uw referenties in.
   
   ![](media/desktop-project-online-connect-to-data/image.png)

Het account waarmee u verbinding maakt met de OData-feed, moet ten minste Portfolioviewer-toegang tot de Project Web App-site hebben. 

Vanaf hier kunt u kiezen met welke tabellen u verbinding wilt maken en een query bouwen.  Wilt u een idee krijgen van hoe u aan de slag kunt gaan?  In de volgende blogbost wordt beschreven hoe u een burndowndiagram kunt maken van uw Project Online-gegevens.  Deze blogpost verwijst naar het gebruik van Power Query om verbinding te maken met Project Online, maar dit is ook van toepassing op Power BI Desktop.

[Burndowndiagrammen maken voor project met behulp van Power Pivot en Power Query](http://blogs.office.com/2014/03/24/creating-burndown-charts-for-project-using-power-pivot-and-power-query/)

