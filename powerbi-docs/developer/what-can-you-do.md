---
title: Wat kunnen ontwikkelaars doen met Power BI?
description: Power BI biedt tal van opties voor ontwikkelaars. Dit varieert van het insluiten van items tot aangepaste visuals en het streamen van gegevenssets.
author: markingmyname
ms.author: maghan
ms.date: 05/25/2018
ms.topic: overview
ms.service: powerbi
ms.component: powerbi-developer
ms.custom: mvc
manager: kfile
ms.openlocfilehash: 07fb8d365a6fe4a874b057a71a90a99fc8a9e5fa
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2018
ms.locfileid: "34564691"
---
# <a name="what-can-developers-do-with-power-bi"></a>Wat kunnen ontwikkelaars doen met Power BI?

Ontwikkelaars hebben verschillende mogelijkheden om Power BI-inhoud in toepassingen op te nemen. Zo kunnen zij **inhoud insluiten met Power BI**, **aangepaste visuals** opnemen en **gegevens pushen naar Power BI**.

## <a name="embedding"></a>Insluiten
De Power BI-service (SaaS) en de Power BI Embedded-service in Azure (PaaS) bevatten API's voor het insluiten van uw dashboards en rapporten. Dit houdt in dat u een set mogelijkheden en toegang tot de nieuwste functies van Power BI (zoals dashboards, gateways en app-werkruimten) gebruikt voor het insluiten van uw inhoud.

U kunt het [hulpprogramma voor de onboarding-ervaring](https://aka.ms/embedsetup) uitvoeren om snel aan de slag te gaan en een voorbeeldtoepassing te downloaden.

Kies de oplossing die het beste bij u past:
* [Door inhoud voor uw klanten in te sluiten](embedding.md#embedding-for-your-customers) kunt u dashboards en rapporten insluiten voor gebruikers die geen account voor Power BI hebben. Voer de oplossing [Insluiten voor uw klanten](https://aka.ms/embedsetup/AppOwnsData) uit.
* [Met het insluiten van inhoud voor uw organisatie](embedding.md#embedding-for-your-organization) kunt u Power BI-service uitbreiden. Voer de oplossing [Insluiten voor uw organisatie](https://aka.ms/embedsetup/UserOwnsData) uit.

![Voorbeeld van PBIE](media/what-can-you-do/what-can-you-do-02.png)

## <a name="develop-custom-visuals"></a>Aangepaste visuals ontwikkelen
Met aangepaste visuele elementen kunt u uw eigen visuele elementen maken voor gebruik in Power BI-rapporten. Aangepaste visuals zijn geschreven in TypeScript, een hoofdverzameling van JavaScript. TypeScript biedt ondersteuning voor bepaalde geavanceerde functies en vroege toegang tot de ES6/ES7-functionaliteit. De stijl van visuele elementen wordt afgehandeld met behulp van Cascading Styles Sheets (CSS). Voor uw gemak gebruiken we de Less-precompiler die enkele geavanceerde functies ondersteunt, zoals nesten, variabelen, voorwaarden, lussen, enzovoort. Als u geen van deze functies wilt gebruiken, kunt u gewone css gebruiken in het Less-bestand.

![Voorbeeld van aangepaste visuals](media/what-can-you-do/powerbi-custom-visual-store.png)

## <a name="push-data-into-power-bi"></a>Gegevens pushen naar Power BI
U kunt de Power BI-API gebruiken om gegevens naar een gegevensset te pushen. Hiermee kunt u een rij aan een tabel in een gegevensset toevoegen. De nieuwe gegevens kunnen vervolgens worden weergegeven in tegels op een dashboard en in visuele elementen binnen uw rapport.

![Voorbeeld van pushen van gegevens](media/what-can-you-do/powerbi-push-data.png)

## <a name="next-steps"></a>Volgende stappen
[Insluiten met Power BI](embedding.md)  
[Aangepaste visuals publiceren naar de Office Store](office-store.md)  
[Gegevens in een dashboard pushen](walkthrough-push-data.md)
