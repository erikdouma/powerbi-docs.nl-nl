---
title: Wat zijn Power BI-sjabloon-apps? (preview)
description: In dit artikel wordt een overzicht gegeven van het programma Power BI-sjabloon-app. Informatie over het bouwen van Power BI-apps met weinig of geen code en deze implementeren naar elke Power BI-klant.
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 02/04/2019
ms.author: maggies
ms.openlocfilehash: 445f5f087bd9589b18f798e8db40a63b0ddceafe
ms.sourcegitcommit: 8207c9269363f0945d8d0332b81f1e78dc2414b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/14/2019
ms.locfileid: "56249743"
---
# <a name="what-are-power-bi-template-apps-preview"></a>Wat zijn Power BI-sjabloon-apps? (preview)

Met de nieuwe Power BI-*sjabloon-apps* kunnen Power BI-partners Power BI-apps maken met weinig of geen code en deze implementeren naar elke Power BI-klant.  In dit artikel wordt een overzicht gegeven van het programma Power BI-sjabloon-app.

Sjabloon-apps zijn een vervanging voor de huidige service-inhoudspakketten. Als Power BI-partner kunt u een set met out-of-the-box-inhoud voor uw klanten maken en deze zelf publiceren.  

U maakt sjabloon-apps waarmee uw klanten verbinding kunnen maken met en exemplaren kunnen maken van hun eigen accounts. Als domeinexperts kunnen ze de gegevens zodanig ontgrendelen dat deze eenvoudig kunnen worden gebruikt door hun zakelijke gebruikers.  

U verzendt uw door uw partner ontwikkelde sjabloon-apps naar de Cloud Partner-portal. De apps worden vervolgens openbaar beschikbaar in de Power BI-appgalerie (app.powerbi.com/getdata/services) en op Microsoft AppSource (appsource.microsoft.com). Hier volgt een voorbeeld van de ervaring met openbare sjabloon-apps.  

## <a name="overview"></a>Overzicht
Het algemene proces van het ontwikkelen en verzenden van een sjabloon-app omvat verschillende fasen, waarvan sommige betrekking op meer dan één activiteit tegelijk kunnen hebben.


| Fase | Power BI Desktop |  |Power BI-service  |  |Cloud Partner-portal  |
|---|--------|--|---------|---------|---------|
| **Eén** | Bouw een gegevensmodel en een rapport in een pbix-bestand |  | Maak een werkruimte. Importeer een pbix-bestand. Een aanvullend dashboard maken  |  | Aanmelden als partner |
| **Twee** |  |  | Een testpakket maken en interne validatie uitvoeren        |  | |
| **Drie** | |  | Het testpakket promoveren naar de pre-productiefase voor validatie buiten uw Power BI-tenant en dit naar AppSource verzenden  |  | Met uw pre-productiepakket een Power BI-sjabloon-app-aanbieding maken en het validatieproces starten |
| **Vier** | |  | Het preproductie-pakket naar productie promoveren |  | Live gaan |

## <a name="requirements"></a>Vereisten

Voor het maken van de sjabloon-app hebt u machtigingen nodig om er eentje te maken. Zie de Power BI-beheerderportal en Instellingen voor sjabloon-apps voor meer informatie. 

Voor het publiceren van een sjabloon-app naar de Power BI-service en AppSource moet u voldoen aan de vereisten voor [het worden van een Cloud-Marketplace-uitgever](https://docs.microsoft.com/azure/marketplace/become-publisher).
 
## <a name="high-level-steps"></a>Stappen op hoog niveau

Hier volgen de stappen op hoog niveau. 

1. [De vereisten bekijken](#requirements) om te controleren of u eraan voldoet. 

1. Een rapport maken in Power BI Desktop. Parameters gebruiken, zodat u deze kunt opslaan als een bestand dat anderen kunnen gebruiken. 

1. Maak een werkruimte voor uw sjabloon-app in uw tenant op de Power BI-service (app.powerbi.com). 

1. Importeer uw pbix-bestand en voeg inhoud aan uw app toe, zoals een dashboard. 

1. Maak een testpakket om zelf de sjabloon-app te testen binnen uw organisatie. 

1. Promoveer de test-app naar de pre-productiefase om de app voor validatie in te dienen bij AppSource en om deze buiten uw eigen tenant te testen. 

1. Verzend de inhoud naar het Cloud-partnerplatform voor publicatie. 

1. Zorg ervoor dat uw aanbieding 'Live' gaat in AppSource en in de productiefase wordt geplaatst in Power BI.
2. U kunt nu beginnen het ontwikkelen van de volgende versie in dezelfde werkruimte, in de pre-productiefase. 

## <a name="requirements"></a>Vereisten

Voor het maken van de sjabloon-app hebt u machtigingen nodig om er eentje te maken. Zie de Power BI-[beheerderportal en Instellingen voor sjabloon-apps](service-admin-portal.md#template-apps-settings-preview) voor meer informatie. 

Voor het publiceren van een sjabloon-app naar de Power BI-service en AppSource moet u voldoen aan de vereisten voor [het worden van een Cloud-Marketplace-uitgever](https://docs.microsoft.com/azure/marketplace/become-publisher).

## <a name="tips"></a>Tips 

- Zorg ervoor dat uw app voorbeeldgegevens bevat waarmee iedereen in één klik aan de slag kan. 
- Bekijk uw toepassing zorgvuldig door deze in uw tenant en een secundaire tenant te installeren. Zorg ervoor dat klanten alleen zien wat u wilt dat ze zien. 
- Gebruik AppSource als uw onlinewinkel voor het hosten van uw toepassing. Op deze manier kan iedereen met behulp van Power BI uw app vinden. 
- Overweeg meer dan één sjabloon-app aan te bieden voor verschillende unieke scenario's. 
- Schakel aanpassing van de gegevens in, zoals ondersteuning voor aangepaste verbinding en configuratie van parameters door het installatieprogramma.

Zie [Tips voor het ontwerpen van sjabloon-apps in Power BI (preview-versie)](service-template-apps-tips.md) voor meer suggesties.

## <a name="support"></a>Ondersteuning
Gebruik [https://powerbi.microsoft.com/support](https://powerbi.microsoft.com/support) voor ondersteuning tijdens de ontwikkeling. We bewaken en beheren deze site actief. Klantincidenten worden zo snel mogelijk naar het desbetreffende team doorgestuurd.

## <a name="next-steps"></a>Volgende stappen

[Een sjabloon-app maken](service-template-apps-create.md)