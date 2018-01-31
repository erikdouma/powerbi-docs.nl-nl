---
title: Veelgestelde vragen over on-premises gegevensgateways
description: Hier vindt u antwoorden op veelgestelde vragen over on-premises gegevensgateways. Dit is de plek waar u antwoorden vindt op veelgestelde vragen over de gateway.
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
ms.tgt_pltfrm: na
ms.workload: powerbi
ms.date: 01/24/2018
ms.author: davidi
ms.openlocfilehash: 626a99467dc02481e004e0472d38cb733f836332
ms.sourcegitcommit: 7249ff35c73adc2d25f2e12bc0147afa1f31c232
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/25/2018
---
# <a name="on-premises-data-gateway-faq"></a>Veelgestelde vragen over on-premises gegevensgateways
<!-- Shared FAQ shared Include -->
[!INCLUDE [gateway-onprem-faq-shared-include](./includes/gateway-onprem-faq-shared-include.md)]

## <a name="analysis-services"></a>Analysis Services
**Vraag:** Kan ik msdmpump.dll gebruiken voor het maken van effectieve toewijzingen van aangepaste gebruikersnamen voor Analysis Services?  
**Antwoord:** Nee. Dit wordt op dit moment niet ondersteund.

**Vraag:** Kan ik de gateway gebruiken om verbinding te maken met een multidimensionaal exemplaar (OLAP).  
**Antwoord:** Ja. De on-premises gegevensgateway ondersteunt live-verbindingen met zowel tabellaire modellen van Analysis Services als multidimensionale modellen.

**Vraag:** Wat gebeurt er als ik de gateway installeer op een computer in een ander domein dan mijn on-premises server die gebruikmaakt van Windows-authenticatie?  
**Antwoord:** Hier kunnen we helaas geen duidelijk antwoord geven. Het hangt allemaal af van de vertrouwensrelatie tussen de twee domeinen. Als de twee verschillende domeinen deel uitmaken van een model op basis van vertrouwde domeinen, kan de gateway mogelijk verbinding maken met de Analysis Services-server en kan de effectieve gebruikersnaam mogelijk worden omgezet. Als dat niet het geval is, kan de aanmelding mislukken.

**Vraag:** Hoe kom ik erachter welke effectieve gebruikersnaam wordt doorgegeven aan mijn on-premises Analysis Services-server?  
**Antwoord:** Het antwoord op deze vraag vindt u in dit [artikel voor probleemoplossing](service-gateway-onprem-tshoot.md).

**Vraag:** Ik heb 25 databases in Analysis Services. Is er een manier om deze in één keer in te schakelen voor de gateway?  
**Antwoord:** Nee. Dit staat wel op de planning, maar we weten nog niet wanneer dit klaar zal zijn.

## <a name="administration"></a>Beheer
**Vraag:** Kan ik meer dan één beheerder hebben voor een gateway?  
**Antwoord:** Ja. Wanneer u een gateway beheert, kunt u naar het tabblad van de beheerder gaan om extra beheerders toe te voegen.

**Vraag:** Moet de beheerder van de gateway een beheerder zijn van de computer waarop de gateway wordt geïnstalleerd?  
**Antwoord:** Nee. De beheerder van de gateway heeft als taak de gateway te beheren binnen de service.

**Vraag:** Kan ik voorkomen dat gebruikers in mijn organisatie een gateway maken?  
**Antwoord:** Nee. Dit staat wel op de planning, maar we weten nog niet wanneer dit klaar zal zijn.

**Vraag:** Kan ik gebruiksgegevens en statistische gegevens opvragen van de gateways in mijn organisatie?  
**Antwoord:** Nee. Dit staat wel op de planning, maar we weten nog niet wanneer dit klaar zal zijn.

## <a name="power-bi"></a>Power BI
**Vraag:** Moet ik de persoonlijke gateway upgraden?
**Antwoord:** Nee, u kunt de persoonlijke gateway blijven gebruiken voor Power BI.

**Vraag:** Hoe vaak worden tegels in een dashboard, in Power BI, vernieuwd wanneer er verbinding is via de on-premises gegevensgateway?  
**Antwoord:** Ongeveer elke tien minuten. DirectQuery-verbindingen werken zoals hun naam suggereert. Dit betekent niet dat een tegel een query naar de on-premises server verstuurt en elke tien minuten nieuwe gegevens laat zien.

**Vraag:** Kan ik Excel-werkmappen met Power Pivot-gegevensmodellen uploaden die verbinding maken met on-premises gegevensbronnen? Heb ik een gateway nodig voor dit scenario?  
**Antwoord:** Ja, u kunt de werkmap uploaden. En nee, u hebt geen gateway nodig. Maar omdat de gegevens zich bevinden in het gegevensmodel van Excel, zijn rapporten in Power BI die zijn gebaseerd op de Excel-werkmap niet live. Om rapporten te vernieuwen in Power BI, moet u elke keer een bijgewerkte werkmap uploaden. U kunt de gateway ook gebruiken met geplande vernieuwing.

**Vraag:** Als gebruikers dashboards delen die een DirectQuery-verbinding hebben, kunnen die andere gebruikers dan de gegevens zien, ook als ze misschien niet dezelfde machtigingen hebben?  
**Antwoord:** Voor een dashboard dat is verbonden met Analysis Services zien gebruikers alleen de gegevens waartoe ze toegang hebben. Als de gebruikers niet dezelfde machtigingen hebben, kunnen ze helemaal geen gegevens zien. Voor andere gegevensbronnen delen alle gebruikers de referenties die door de beheerder zijn ingevoerd voor de gegevensbron.

**Vraag:** Waarom kan ik geen verbinding maken met mijn Oracle-server?  
**Antwoord:** Mogelijk moet u de Oracle-client installeren en het bestand tnsnames.ora configureren met de juiste servergegevens om verbinding te kunnen maken met de Oracle-server. Dit is een afzonderlijke installatie buiten de gateway. Zie [De Oracle-client installeren](service-gateway-onprem-manage-oracle.md#installing-the-oracle-client) voor meer informatie.

**Vraag:** Werkt de gateway met ExpressRoute?  
**Antwoord:** Ja. Zie [Power BI en ExpressRoute](service-admin-power-bi-expressroute.md) voor meer informatie over ExpressRoute en Power BI.

## <a name="next-steps"></a>Volgende stappen
[On-premises gegevensgateway](service-gateway-onprem.md)  
[On-premises data gateway in-depth](service-gateway-onprem-indepth.md) (On-premises gegevensgateway - uitgebreid)  
[Problemen met de on-premises gegevensgateway oplossen](service-gateway-onprem-tshoot.md)  
Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

