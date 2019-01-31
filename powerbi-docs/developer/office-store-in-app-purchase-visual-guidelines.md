---
title: Extra aankoop mogelijk vereist - Richtlijnen voor Power BI-visuals
description: Meer informatie over het publiceren van aangepaste visuals naar AppSource, zodat anderen deze na aanschaf kunnen gebruiken.
author: markingmyname
ms.author: maghan
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: conceptual
ms.date: 11/26/2018
ms.openlocfilehash: 280f60d0ae60a445d94a640af974a2624c73bb83
ms.sourcegitcommit: a36f82224e68fdd3489944c9c3c03a93e4068cc5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2019
ms.locfileid: "55429999"
---
# <a name="guidelines-for-power-bi-visuals-with-additional-purchases"></a>Richtlijnen voor Power BI-visuals met extra aankopen

Tot voor kort accepteerde de **Marketplace (AppSource)** alleen Power BI-visuals die gratis waren. Dit beleid wordt gewijzigd zodat visuals met het prijslabel 'mogelijk extra aankoop vereist' ook kunnen worden ingediend bij de **AppSource**. Visuals met Mogelijk extra aankoop vereist zijn vergelijkbaar met IAP-invoegtoepassingen (in-app aankoop) in Office Store. Ontwikkelaars kunnen deze visuals ook indienen voor certificering nadat ze door het **AppSource**-team zijn goedgekeurd en nadat is gecontroleerd of ze aan de certificeringsvereisten voldoen, zoals beschreven in het artikel over [Gecertificeerde aangepaste visuals](../power-bi-custom-visuals-certified.md).

> [!Note]
> Visuals kunnen alleen worden gecertificeerd als deze geen toegang hebben tot externe services of resources.

## <a name="whats-changing-in-the-submission-process"></a>Hoe verandert het indieningsproces?

Ontwikkelaars uploaden hun IAP-visuals naar AppSource via het Verkopersdashboard, zoals ze dat ook al deden voor gratis visuals. Om aan te geven dat de ingediende visual over IAP-functies beschikt, moeten ontwikkelaars de volgende opmerking in het Verkopersdashboard toevoegen: 'Visual met in-app aankoop'. Bovendien moeten ontwikkelaars een licentiesleutel of token opgeven zodat het validatieteam de IAP-functies kan valideren. Zodra de visual is gevalideerd en goedgekeurd, wordt bij de prijsopties in de AppSource-lijst voor de IAP-visual 'Mogelijk extra aankoop vereist' vermeld.

## <a name="what-is-a-power-bi-visual-with-iap-features"></a>Wat is een Power BI-visual met IAP-functies?

Een IAP-visual is een gratis visual die gratis functies biedt, maar die ook extra functies biedt waarvoor extra kosten kunnen worden berekend om ze te kunnen gebruiken. Ontwikkelaars moeten gebruikers via de beschrijving van de visual informeren over de functies waarvoor extra aankopen moeten worden gedaan om ze te kunnen gebruiken. Op dit moment biedt Microsoft geen systeemeigen API's (Application Programming Interfaces) voor de ondersteuning van aankopen in apps en invoegtoepassingen. Ontwikkelaars kunnen een extern betalingssysteem voor die aankopen gebruiken. Raadpleeg ons [Store-beleid](https://docs.microsoft.com/office/dev/store/validation-policies#2-apps-or-add-ins-can-display-certain-ads).

## <a name="logo-guidelines"></a>Richtlijnen voor logo's

In deze sectie worden de specificaties voor het toevoegen van logo's en logotypes in visuals beschreven.

> [!NOTE]
> Logo's zijn alleen in de bewerkingsmodus toegestaan. Logo's kunnen niet worden weergegeven in de weergavemodus.

![definities](media/office-store-in-app-purchase-visual-guidelines/definitions.png)

![dingen-om-te-bewaren](media/office-store-in-app-purchase-visual-guidelines/things-to-keep-in-mind.png)

![dingen-om-te](media/office-store-in-app-purchase-visual-guidelines/things-to-avoid.png)

![grootte-en-formaat ](media/office-store-in-app-purchase-visual-guidelines/size-and-format.png)

![marges-en](media/office-store-in-app-purchase-visual-guidelines/margins-and-sizes.png)

![bewerkingsmodus](media/office-store-in-app-purchase-visual-guidelines/logos-in-edit-mode.png)

## <a name="best-practices"></a>Aanbevolen procedures

### <a name="visual-landing-page"></a>Landingspagina van visual

Gebruik de landingspagina om gebruikers te informeren hoe zij uw visual kunnen gebruiken en waar ze de licentie kunnen aanschaffen. Sluit geen video's in die automatisch worden geactiveerd. Voeg uitsluitend materiaal toe die de gebruikerservaring verbetert, zoals informatie of koppelingen naar details over de aankoop van licenties en instructies over het gebruik van de IAP-functies.

### <a name="license-key-and-token"></a>Licentiesleutel en token

Voor het gemak van de gebruiker kunt u boven in het deelvenster Opmaak velden met betrekking tot licentiesleutels of tokens toevoegen, zodat gebruikers deze velden beter kunnen vinden.

## <a name="faq"></a>Veelgestelde vragen

Voor meer informatie en antwoorden op vragen gaat u naar [Veelgestelde vragen over visuals met aanvullende aankopen](https://docs.microsoft.com/power-bi/power-bi-custom-visuals-faq#visuals-with-additional-purchases).

## <a name="next-steps"></a>Volgende stappen

Meer informatie over het publiceren van aangepaste visuals naar [AppSource](office-store.md), zodat anderen deze kunnen gebruiken.
