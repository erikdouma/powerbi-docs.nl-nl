---
title: Workloads configureren in Power BI Premium
description: Ontdek hoe u workloads kunt configureren in een Power BI Premium-capaciteit.
author: minewiskan
ms.author: owend
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 03/11/2019
LocalizationGroup: Premium
ms.openlocfilehash: 0baab138ee98d2ec96bc9f47e6e727525a57ed3e
ms.sourcegitcommit: f176ba9d52d50d93f264eca21bb3fd987dbf934b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2019
ms.locfileid: "57757241"
---
# <a name="configure-workloads-in-a-premium-capacity"></a>Workloads configureren in een Premium-capaciteit

In dit artikel wordt het inschakelen en configureren van workloads voor Power BI Premium-capaciteiten beschreven. Standaard bieden capaciteiten alleen ondersteuning voor de workload die aan het uitvoeren van Power BI-query's is gekoppeld. Queryworkloads zijn geoptimaliseerd voor en beperkt door de resources die voor uw Premium-capaciteit-SKU zijn vastgesteld. Premium-capaciteiten bieden bovendien ondersteuning voor extra workloads die capaciteitsresources kunnen gebruiken.

## <a name="configure-workloads"></a>Workloads configureren

U kunt extra workloads inschakelen en configureren voor AI, [gegevensstromen](service-dataflows-overview.md#dataflow-capabilities-on-power-bi-premium) en [gepagineerde rapporten](paginated-reports-save-to-power-bi-service.md). De standaardgeheugenwaarden voor deze workloads zijn gebaseerd op de capaciteitsknooppunten die voor uw SKU beschikbaar zijn. De maximale geheugeninstellingen zijn niet cumulatief. Het geheugen tot de opgegeven maximumwaarde wordt dynamisch toegewezen voor AI en gegevensstromen, maar statisch voor gepagineerde rapporten. 

### <a name="to-configure-workloads-in-the-power-bi-admin-portal"></a>Workloads configureren in de Power BI-beheerportal

1. Selecteer een capaciteit bij **Capaciteitsinstellingen** > **PREMIUM-CAPACITEITEN**.

1. Vouw **Workloads** uit onder **MEER OPTIES**.

1. Schakel een of meer workloads in en stel een waarde in voor **Maximaal geheugen**.   

    
    ![Workloads inschakelen](media/service-admin-premium-workloads/admin-portal-workloads.png)

1. Klik op **Toepassen**.

> [!NOTE]
> Als u gebruikmaakt van de workload voor gepagineerde rapporten, kunt u met gepagineerde rapporten uw eigen code uitvoeren bij het weergeven van een rapport (zoals het dynamisch wijzigen van de tekstkleur op basis van inhoud). In Power BI Premium worden gepagineerde rapporten in een ingesloten ruimte in de capaciteit uitgevoerd. De maximale hoeveelheid geheugen die u aan deze ruimte hebt toegewezen wordt gebruikt, ongeacht of de workload actief is of niet. Als u Power BI-rapporten of gegevensstromen in dezelfde capaciteit gebruikt, moet u het geheugen voor gepagineerde rapporten laag genoeg instellen, zodat deze workload geen gevolgen heeft voor de andere workloads. in zeldzame gevallen kan het gebeuren dat de workload Gepagineerde rapporten niet beschikbaar is. U ziet dan een foutstatus voor de workload in de beheerportal. Gebruikers zien time-outs als ze rapporten willen weergeven. U kunt dit probleem oplossen door de workload uit te schakelen en vervolgens weer in te schakelen.


### <a name="rest-api"></a>REST API

Workloads kunnen worden ingeschakeld en aan een capaciteit worden toegewezen met behulp van de REST API's voor [capaciteiten](https://docs.microsoft.com/rest/api/power-bi/capacities).


## <a name="next-steps"></a>Volgende stappen

[Resourcebeheer en optimalisatie van Power BI Premium-capaciteit](service-premium-understand-how-it-works.md)   
[Selfservice voor gegevensvoorbereiding in Power BI met gegevensstromen](service-dataflows-overview.md)   
[Wat zijn gepagineerde rapporten in Power BI Premium?](paginated-reports-report-builder-power-bi.md)   

Hebt u nog vragen? [Stel een vraag aan de Power BI-community](http://community.powerbi.com/)