---
title: On-premises en cloudgegevensbronnen samenvoegen of toevoegen
description: Gebruik de on-premises gegevensgateway om on-premises en cloudgegevensbronnen samen te voegen in of om ze toe te voegen aan één query.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-gateways
ms.topic: conceptual
ms.date: 06/06/2018
ms.author: mblythe
LocalizationGroup: Gateways
ms.openlocfilehash: 7b863af882604be8c2c59fd21f26cd8441f9e170
ms.sourcegitcommit: c8c126c1b2ab4527a16a4fb8f5208e0f7fa5ff5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2019
ms.locfileid: "54272645"
---
# <a name="merge-or-append-on-premises-and-cloud-data-sources"></a>On-premises en cloudgegevensbronnen samenvoegen of toevoegen

Met de on-premises gegevensgateway kunt u on-premises en cloudgegevensbronnen samenvoegen in of ze toevoegen aan één query. Dit is handig als u gegevens uit verschillende bronnen wilt samenvoegen zonder afzonderlijke query's te hoeven gebruiken.

## <a name="prerequisites"></a>Vereisten

- Een [gateway die is geïnstalleerd](service-gateway-install.md) op een lokale computer.
- Een Power BI Desktop-bestand met query's waarin on-premises en cloudgegevensbronnen worden gecombineerd.

1. Selecteer rechtsboven in de Power BI-service het tandwielpictogram ![tandwielpictogram Instellingen](media/service-gateway-mashup-on-premises-cloud/icon-gear.png) > **Gateways beheren**.

    ![Gateways beheren](media/service-gateway-mashup-on-premises-cloud/manage-gateways.png)

2. Selecteer de gateway die u wilt configureren.

3. Onder **Clusterinstellingen van de gateway** selecteert u **Toestaan dat de cloudgegevensbronnen van gebruikers worden vernieuwd via dit gatewaycluster** > **Toepassen**.

    ![Vernieuwen via dit gatewaycluster](media/service-gateway-mashup-on-premises-cloud/refresh-gateway-cluster.png)

4. Via dit gatewaycluster voegt u alle [on-premises gegevensbronnen](service-gateway-enterprise-manage-scheduled-refresh.md#add-a-data-source) toe die u gebruikt in uw query's. U hoeft hier niet de cloudgegevensbronnen toe te voegen.

5. Upload uw Power BI Desktop-bestand naar de Power BI-service. Dit bestand bevat de query's waarin on-premises en cloudgegevensbronnen worden gecombineerd.

6. Op de pagina **Gegevenssetinstellingen** van de nieuwe gegevensset:

   - Voor de on-premises bron selecteert u de gateway die is gekoppeld aan deze gegevensbron.

   - Bij **Gegevensbronreferenties** bewerkt u de referenties van de cloudgegevensbronnen waar nodig.

     ![Gegevenssetinstellingen](media/service-gateway-mashup-on-premises-cloud/dataset-settings.png)

7. Als de cloudreferenties zijn ingesteld, kunt u de gegevensset vernieuwen via de optie **Nu vernieuwen**, of u kunt instellen dat er periodiek wordt vernieuwd.


## <a name="next-steps"></a>Volgende stappen

Zie [De gegevensbron gebruiken voor geplande vernieuwing](service-gateway-enterprise-manage-scheduled-refresh.md#using-the-data-source-for-scheduled-refresh) voor meer informatie over gegevensvernieuwing voor gateways.