---
title: Beveiliging op rijniveau (RLS) met Power BI begrijpen
description: Hoe u de beveiliging op rijniveau voor de geïmporteerde gegevenssets en DirectQuery configureert in Power BI Desktop.
author: markingmyname
ms.author: maghan
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 05/03/2018
LocalizationGroup: Create reports
ms.openlocfilehash: a6d5e768cfb2f42f6abbcf21ee75529ac74f0a62
ms.sourcegitcommit: 05303d3e0454f5627eccaa25721b2e0bad2cc781
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/28/2018
ms.locfileid: "52578101"
---
# <a name="row-level-security-rls-with-power-bi-desktop"></a>Beveiliging op rijniveau (RLS) met Power BI

Met Beveiliging op rijniveau (RLS) met Power BI wordt de toegang tot gegevens voor bepaalde gebruikers beperkt. Filters beperken gegevens op rijniveau. U kunt filters definiëren in rollen.

U kunt RLS nu configureren voor gegevensmodellen die met Power BI Desktop zijn geïmporteerd in Power BI. U kunt RLS ook configureren voor gegevenssets die gebruikmaken van DirectQuery, zoals SQL Server. Voorheen kon u RLS alleen implementeren binnen on-premises Analysis Services-modellen buiten Power BI. Voor Analysis Services-liveverbindingen configureert u beveiliging op rijniveau voor het on-premises model. De beveiligingsoptie wordt niet weergegeven voor gegevenssets met live verbinding.

> [!IMPORTANT]
> Als u rollen en regels hebt gedefinieerd binnen de Power BI-service moet u deze rollen opnieuw maken binnen Power BI Desktop en het rapport publiceren naar de service.

Meer informatie over opties voor [RLS in de Power BI-service](service-admin-rls.md).

[!INCLUDE [include-short-name](./includes/rls-desktop-define-roles.md)]

[!INCLUDE [include-short-name](./includes/rls-desktop-view-as-roles.md)]

[!INCLUDE [include-short-name](./includes/rls-limitations.md)]

[!INCLUDE [include-short-name](./includes/rls-faq.md)]

## <a name="next-steps"></a>Volgende stappen

[Beveiliging op rijniveau (RLS) met de Power BI-service](service-admin-rls.md)  

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)