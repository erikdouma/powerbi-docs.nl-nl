---
title: Beveiliging op rijniveau (RLS) met Power BI begrijpen
description: "Hoe u de beveiliging op rijniveau voor de geïmporteerde gegevenssets en DirectQuery configureert in Power BI Desktop."
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
ms.tgt_pltfrm: na
ms.workload: powerbi
ms.date: 10/12/2017
ms.author: asaxton
ms.openlocfilehash: e6b6efb976de8df6064f2eb1156237d1a1250807
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2017
---
# <a name="row-level-security-rls-with-power-bi-desktop"></a>Beveiliging op rijniveau (RLS) met Power BI
Beveiliging op rijniveau (RLS) kan in Power BI Desktop worden gebruikt om de toegang tot gegevens voor bepaalde gebruikers te beperken. Filters beperken gegevens op rijniveau. U kunt filters definiëren in rollen.

U kunt RLS nu configureren voor gegevensmodellen die met Power BI Desktop zijn geïmporteerd in Power BI. U kunt RLS ook configureren voor gegevenssets die gebruikmaken van DirectQuery, zoals SQL Server. Voorheen kon u RLS alleen implementeren binnen on-premises Analysis Services-modellen buiten Power BI. Voor Analysis Services-liveverbindingen configureert u beveiliging op rijniveau voor het on-premises model. De beveiligingsoptie wordt niet weergegeven voor gegevenssets met een liveverbinding.

> [!IMPORTANT]
> Als u rollen/regels hebt gedefinieerd in de Power BI-service, moet u deze rollen in Power BI Desktop opnieuw maken en het rapport publiceren naar de service.
> 
> 

Meer informatie over opties voor [RLS in de Power BI-service](service-admin-rls.md).

[!INCLUDE [include-short-name](./includes/rls-desktop-define-roles.md)]

[!INCLUDE [include-short-name](./includes/rls-desktop-view-as-roles.md)]

[!INCLUDE [include-short-name](./includes/rls-limitations.md)]

[!INCLUDE [include-short-name](./includes/rls-faq.md)]

## <a name="next-steps"></a>Volgende stappen
[Beveiliging op rijniveau (RLS) met de Power BI-service](service-admin-rls.md)  

Hebt u nog vragen? [Misschien dat de Power Bi-community het antwoord weet](http://community.powerbi.com/)

