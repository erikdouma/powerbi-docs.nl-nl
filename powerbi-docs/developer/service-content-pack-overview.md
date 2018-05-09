---
title: Overzicht van het programma voor inhoudspakketten van de Power BI-service
description: Certificeringsprogramma voor inhoudspakketten
services: powerbi
documentationcenter: ''
author: markingmyname
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
ms.date: 02/20/2018
ms.author: maghan
ms.openlocfilehash: 2cc78b3d2a877e465d5f4bdc67f501b7de87f88e
ms.sourcegitcommit: 20dd809a2ef8c0d6c6f677baadb5f57f41438cbe
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/23/2018
---
# <a name="overview-of-the-power-bi-service-content-pack-program"></a>Overzicht van het programma voor inhoudspakketten van de Power BI-service
Een inhoudspakket is een set kant-en-klare elementen waarmee gebruikers direct inzicht kunnen krijgen vanuit een bron. Een inhoudspakket is doorgaans gericht op een specifiek zakelijk scenario om inzicht te bieden voor een functie, domein of workflow.

ISV's kunnen sjablooninhoudspakketten samenstellen waarmee klanten verbinding kunnen maken en die ze kunnen instantiëren vanuit hun eigen accounts. Als domeinexperts kunnen ze de gegevens ontgrendelen op een manier die eenvoudig kan worden gebruikt door zakelijke gebruikers. De inhoudspakketten bieden ad-hoc controle en analyse aan uw klanten zonder zware investeringen in de infrastructuur voor rapportage. 

Deze door ISV's gemaakte sjablooninhoudspakketten kunnen worden verzonden naar het Power BI-team en openbaar beschikbaar worden gesteld in de Power BI-galerie met inhoudspakketten (app.powerbi.com/getdata/services) en op Microsoft AppSource (appsource.microsoft.com). Een voorbeeld van het gebruiksomgeving voor openbare inhoudspakketten vindt u [hier](template-content-pack-experience.md).

## <a name="overview"></a>Overzicht
Het algemene proces om een sjablooninhoudspakket te ontwikkelen omvat meerdere stappen.

 ![Proces](media/service-content-pack-overview/developer-content-pack-overview.png)

1. [De vereisten bekijken](#requirements) en zorgen dat u eraan voldoet
2. [Inhoud bouwen](template-content-pack-authoring.md#queries) in Power BI Desktop
3. [Een dashboard maken](template-content-pack-authoring.md#dashboard) op PowerBI.com
4. [Het inhoudspakket zelf testen](template-content-pack-testing.md) binnen uw organisatie
5. De inhoud [indienen](template-content-pack-testing.md#submission) bij Power BI voor publicatie

<a name="requirements"></a>

## <a name="requirements"></a>Vereisten
Als u een inhoudspakket wilt maken en indienen voor publicatie in de Power BI-service en AppSource, moet u voldoen aan de volgende vereisten:

* U hebt een SaaS-toepassing die wordt gebruikt door zakelijke gebruikers.
* Uw SaaS-toepassing bevat gebruikersgegevens die kunnen worden gevisualiseerd in Power BI.
* Uw SaaS-toepassing heeft een API die toegankelijk is via het openbare internet. In het ideale geval is de API een op REST gebaseerde API of een OData-feed. Power BI-inhoudspakketten ondersteunen meerdere verificatietypen zoals basisverificatie, OAuth 2.0 en API-sleutel. 
* Uw Saas-toepassing is goedgekeurd om een inhoudsnpakket te publiceren. Dien uw aanvraag in bij pbiservicesapps@microsoft.com. Elke inzending wordt beoordeeld op relevantie en verwacht gebruik. 
* Ondertekende partnerovereenkomst. U doet dit in de [verzendingsstap](template-content-pack-testing.md#submission).

Controleer de sectie [Ontwerpen](template-content-pack-authoring.md) voor meer informatie over de technische vereisten.

## <a name="business-scenario"></a>Bedrijfsscenario
Inhoudspakketten bieden inzicht en metrische gegevens die zijn gericht op een specifiek bedrijfsscenario. Door inzicht te hebben in uw doelgroep en het voordeel dat zij halen uit het inhoudspakket, zorgt u ervoor dat uw gebruikers de door u verstrekte inhoud goed kunnen gebruiken.

### <a name="tips"></a>Tips
* Identificeer uw doelgroep en de taak die deze probeert te bereiken  
* Richt u op een bepaalde periode (afgelopen 90 dagen) of de laatste N resultaten  
* Importeer alleen de tabellen/kolommen die betrekking hebben op uw scenario  
* Overweeg meer dan één inhoudspakket aan te bieden voor verschillende unieke scenario's  

## <a name="frequently-asked-questions"></a>Veelgestelde vragen
**Kan ik als derde een inhoudspakket voor de Power BI-service bouwen voor een SaaS-toepassing die ik niet bezit?**

Momenteel vereisen we dat de eigenaar van de SaaS-toepassing een partnerovereenkomst ondertekent voordat het inhoudspakket in de service wordt gepubliceerd. Als derde moet u de ondertekening van de partnerovereenkomst met de eigenaar van de SaaS-toepassing vergemakkelijken.

**Ik heb geen openbare API voor ontwikkelaars voor mijn service. Kan ik nog steeds een inhoudspakket voor de Power BI-service bouwen dat de gegevens rechtstreeks ophaalt vanuit de gegevensopslag?**

Nee, inhoudspakketten voor de Power BI-service vereisen een API voor ontwikkelaars die toegankelijk is via het openbare internet.

**Welke typen API's worden ondersteund door inhoudspakketten en met welke verificatietypen kunnen ze werken?**

Inhoudspakketten voor de Power BI-service ondersteunen elke REST-API of OData-feed. Power BI kan werken met meerdere verificatietypen zoals basisverificatie, OAuth2.0 en Web API-sleutels. Meer informatie over de technische vereisten vindt u in het artikel [Ontwerpen](template-content-pack-authoring.md#dashboard).

**Ik heb een inhoudspakket gepubliceerd in Power BI. Hoe kan ik dit bijwerken?**

Gepubliceerde inhoudspakketten kunnen eenmaal per maand worden bijgewerkt. Bijwerkaanvragen die vóór de laatste dag van de huidige maand naar [pbiservicesapps@microsoft.com](mailto:pbiservicesapps@microsoft.com) worden verzonden, worden gepubliceerd in de eerste week van de volgende maand.

**Ik heb meer vragen over inhoudspakketten voor de service. Hoe kan ik contact met jullie opnemen?**

U kunt uw vragen per e-mail verzenden naar [pbiservicesapps@microsoft.com](mailto:pbiservicesapps@microsoft.com)

## <a name="support"></a>Ondersteuning
Gebruik voor ondersteuning tijdens de ontwikkeling [https://powerbi.microsoft.com/support](https://powerbi.microsoft.com/support). Deze pagina wordt actief bewaakt en beheerd. Klantincidenten worden zo snel mogelijk naar het desbetreffende team doorgestuurd.

## <a name="next-step"></a>Volgende stap
[Ontwerpen](template-content-pack-authoring.md)

