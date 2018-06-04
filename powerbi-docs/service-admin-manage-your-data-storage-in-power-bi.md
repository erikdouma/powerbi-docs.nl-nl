---
title: Uw gegevensopslag beheren
description: Meer informatie over hoe u uw persoonlijke gegevensopslag, of opslag van de app-werkruimte, kunt beheren om ervoor te zorgen dat u rapporten en gegevenssets kunt blijven publiceren.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 06/28/2017
ms.author: mblythe
LocalizationGroup: Administration
ms.openlocfilehash: e7c0399072bfef35a1103a5db448da183f64f74c
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2018
ms.locfileid: "34245357"
---
# <a name="manage-your-data-storage"></a>Uw gegevensopslag beheren
Meer informatie over hoe u uw persoonlijke gegevensopslag, of opslag van de app-werkruimte, kunt beheren om ervoor te zorgen dat u rapporten en gegevenssets kunt blijven publiceren.

Gebruikers en app-werkruimten hebben hun eigen gegevenscapaciteit

* Gebruikers van gratis versies en Pro-versies hebben maximaal 10 GB gegevensopslag.
* Gebruikers van Pro-versies kunnen app-werkruimten maken, die elk maximaal 10 GB gegevensopslag hebben.

Op tenantniveau kan het totale gebruik niet 10 GB per Pro-gebruiker overschrijden over alle Pro-gebruikers van app-werkruimten in de tenant.

Meer informatie over andere functies van het [Power BI-prijsmodel](https://powerbi.microsoft.com/pricing).

Tot uw gegevensopslag behoren uw eigen gegevenssets en Excel-rapporten, en gegevenssets en rapporten die iemand met u heeft gedeeld. Gegevenssets zijn alle gegevensbronnen die u hebt geüpload of waarmee u verbinding hebt gemaakt, inclusief Power BI Desktop-bestanden en Excel-werkmappen die u gebruikt. Het volgende is ook opgenomen in uw gegevenscapaciteit.

* Excel-adresbereiken die zijn vastgemaakt aan dashboard.
* On-premises visualisaties van Reporting Services die zijn vastgemaakt aan een Power BI-dashboard.
* Geüploade afbeeldingen.

De grootte van een dashboard dat u deelt, is afhankelijk van waaraan het is vastgemaakt. Als u bijvoorbeeld items uit twee rapporten vastmaakt die deel uitmaken van twee verschillende gegevenssets, omvat de grootte beide gegevenssets.

<a name="manage"/>

## <a name="manage-items-owned-by-you"></a>Items beheren waarvan u eigenaar bent
Zie hoeveel gegevensopslag u gebruikt in uw Power BI-account en beheer uw account.

1. Om uw eigen opslag te beheren, gaat u naar **Mijn werkruimte** in het navigatiedeelvenster links.
   
    ![](media/service-admin-manage-your-data-storage-in-power-bi/pbi_myworkspace.png)
2. Selecteer het tandwielpictogram ![](media/service-admin-manage-your-data-storage-in-power-bi/pbi_gearicon.png) in de rechterbovenhoek \> **Persoonlijke opslag beheren**.
   
    In de bovenste balk ziet u hoeveel u hebt gebruikt van uw opslaglimiet.
   
    ![](media/service-admin-manage-your-data-storage-in-power-bi/pbi_persnlstorage.png)
   
    De gegevenssets en rapporten worden gescheiden op twee tabbladen:
   
    **Items waarvan ik eigenaar ben:** dit zijn de rapporten en gegevenssets die u hebt geüpload naar uw Power BI-account, waaronder servicegegevenssets zoals Salesforce en Dynamics CRM.  
    **Items waarvan anderen eigenaar zijn:** anderen hebben deze rapporten en gegevenssets met u gedeeld.
3. Als u een gegevensset of rapport wilt verwijderen, selecteert u het prullenbakpictogram ![](media/service-admin-manage-your-data-storage-in-power-bi/pbi_deleteicon.png).

Bedenk dat u of iemand anders mogelijk rapporten en dashboards heeft die zijn gebaseerd op een gegevensset. Als u de gegevensset verwijdert, werken die rapporten en dashboards niet meer.

## <a name="manage-your-app-workspace"></a>Uw app-werkruimte beheren
1. Selecteer de pijl naast **Werkruimten** \> en selecteer de naam van de app-werkruimte.
   
    ![](media/service-admin-manage-your-data-storage-in-power-bi/pbi_groupworkspaces.png)
2. Selecteer het tandwielpictogram ![](media/service-admin-manage-your-data-storage-in-power-bi/pbi_gearicon.png) in de rechterbovenhoek \> **Persoonlijke opslag beheren**.
   
    In de bovenste balk ziet u hoeveel opslaglimiet van de groep is gebruikt.
   
    ![](media/service-admin-manage-your-data-storage-in-power-bi/pbi_groupstorage.png)
   
    De gegevenssets en rapporten worden gescheiden op twee tabbladen:
   
    **Items waarvan wij eigenaar zijn:** dit zijn rapporten en gegevenssets die u of iemand anders heeft geüpload naar het Power BI-account van de groep, waaronder servicegegevenssets zoals Salesforce en Dynamics CRM.
    **Items waarvan anderen eigenaar zijn:** anderen hebben deze rapporten en gegevenssets met uw groep gedeeld.
3. Als u een gegevensset of rapport wilt verwijderen, selecteert u het prullenbakpictogram ![](media/service-admin-manage-your-data-storage-in-power-bi/pbi_deleteicon.png).
   
   > [!NOTE]
   > Elk lid, met bewerkingsmachtigingen, van een app-werkruimte is gemachtigd om gegevenssets en rapporten uit de app-werkruimte te verwijderen.
   > 
   > 

Bedenk dat u of iemand anders in de groep mogelijk rapporten en dashboards heeft die zijn gebaseerd op een gegevensset. Als u de gegevensset verwijdert, werken die rapporten en dashboards niet meer.

## <a name="dataset-limits"></a>Limieten voor de gegevensset
Er is een limiet van 1 GB per gegevensset die wordt geïmporteerd in Power BI. Als u ervoor hebt gekozen om de Excel-ervaring te houden, in plaats van de gegevens te importeren, bent u beperkt tot maximaal 250 MB voor de gegevensset.

## <a name="what-happens-when-you-hit-a-limit"></a>Wat er gebeurt wanneer u een limiet bereikt
Als u de gegevenscapaciteitslimiet bereikt, ziet u instructies in de service. 

Wanneer u het tandwielpictogram ![](media/service-admin-manage-your-data-storage-in-power-bi/pbi_gearicon.png) selecteert, ziet u een rode balk die aangeeft dat u de limiet van uw gegevenscapaciteit hebt overschreden.

![](media/service-admin-manage-your-data-storage-in-power-bi/manage-storage-limit.png)

Dit wordt ook aangegeven in **Persoonlijke opslag beheren**.

 ![](media/service-admin-manage-your-data-storage-in-power-bi/manage-storage-limit2.png)

 Wanneer u probeert een actie uit te voeren waardoor een limiet wordt bereikt, ziet u een waarschuwing waarin wordt aangegeven dat u de limiet hebt overschreden. U kunt uw opslag [beheren](#manage) om uw opslagruimte te verlagen en de limiet te omzeilen.

 ![](media/service-admin-manage-your-data-storage-in-power-bi/powerbi-pro-over-limit.png)

 Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

