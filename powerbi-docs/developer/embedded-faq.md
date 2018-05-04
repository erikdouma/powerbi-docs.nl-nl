---
title: Veelgestelde vragen over Power BI Embedded
description: Hier vindt u een lijst met veelgestelde vragen en antwoorden over Power BI Embedded.
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
ms.date: 04/23/2018
ms.author: maghan
ms.openlocfilehash: 24e4dbaf6ede92436ff05c8cb57756e3ab7e8526
ms.sourcegitcommit: 3f2f254f6e8d18137bae879ddea0784e56b66895
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/26/2018
---
# <a name="frequently-asked-questions-about-power-bi-embedded"></a>Veelgestelde vragen over Power BI Embedded

* Als u andere vragen hebt, kunt u deze stellen [in de Power BI-community](http://community.powerbi.com/).
* Nog steeds geen antwoord? Ga naar de [ondersteuningspagina van Power BI](https://powerbi.microsoft.com/support/).

## <a name="general"></a>Algemeen

### <a name="what-is-power-bi-embedded"></a>Wat is Power BI Embedded?

Microsoft Power BI Embedded zorgt ervoor dat ontwikkelaars van toepassingen schitterende, volledig interactieve rapporten, dashboards en tegels kunnen insluiten in toepassingen, zonder dat ze hiervoor tijd en geld kwijt zijn om hun eigen gegevensvisualisaties en besturingselementen helemaal zelf te bouwen.

### <a name="who-is-the-target-audience-for-power-bi-embedded"></a>Wie is de doelgroep voor Power BI Embedded?

Ontwikkelaars en softwarebedrijven die hun eigen toepassingen maken en die onafhankelijke softwareleveranciers (ISV's) worden genoemd.

### <a name="how-is-power-bi-embedded-different-from-power-bi-the-service"></a>Hoe verschilt Power BI Embedded van de Power BI-service?

Power BI Embedded is bedoeld voor ISV's of ontwikkelaars die toepassingen bouwen en visuele elementen willen insluiten in deze toepassingen om hun klanten te helpen bij het besluitvormingsproces zonder dat ze hiervoor helemaal zelf een oplossing voor analytische gegevens hoeven te bouwen. Ingesloten functies voor analytische gegevens bieden zakelijke gebruikers toegang tot de zakelijke gegevens en stellen ze in staat query's uit te voeren voor het genereren van inzichten met behulp van deze gegevens in de toepassing.

Power BI, daarentegen, is een SaaS-oplossing (Software as a Service) voor analytische gegevens waarmee organisaties in één weergave alle meest kritieke zakelijke gegevens kunnen bekijken.

### <a name="what-is-the-difference-between-power-bi-premium-and-power-bi-embedded"></a>Wat is het verschil tussen Power BI Premium en Power BI Embedded?

Power BI Premium is qua capaciteit afgestemd op ondernemingen die de beschikking willen over een volledige BI-oplossing met één weergave van de organisatie, partners, klanten en leveranciers. Power BI Premium helpt uw organisatie bij het nemen van beslissingen. Power BI Premium is een SaaS-product en wordt geleverd met de mogelijkheid voor gebruikers om inhoud via de Power BI-portal, mobiele app en intern ontwikkelde apps te gebruiken.

Power BI Embedded is voor ISV's of ontwikkelaars die toepassingen bouwen en visuele elementen willen insluiten in deze toepassingen. Power BI Embedded helpt uw klanten bij de besluitvorming omdat Power BI Embedded is bedoeld voor ontwikkelaars van toepassingen en klanten van die toepassingen toegang hebben tot inhoud die is opgeslagen in capaciteit van Power BI Embedded, met inbegrip van iedereen binnen of buiten de organisatie. Inhoud in capaciteit van Power BI Embedded kan niet worden gedeeld via publiceren met één klik op internet of via publiceren met één klik naar SharePoint, en biedt geen ondersteuning voor SSRS-rapporten.

### <a name="what-is-the-microsoft-recommendation-for-when-a-customer-should-buy-power-bi-premium-vs-power-bi-embedded"></a>Wat is de aanbeveling van Microsoft voor de keuze tussen Power BI Premium en Power BI Embedded?

De aanbeveling van Microsoft is dat ondernemingen Power BI Premium kopen, een hoogwaardige cloudoplossing voor BI met selfservice, en dat ISV's Power BI Embedded kopen, vanuit de cloud ingesloten componenten voor analytische gegevens. Er zijn echter geen beperkingen voor welk product een klant kan kopen.

Er zijn misschien enkele situaties waarin een ISV (meestal groot) een P-SKU wil gebruiken om te beschikken over de extra voordelen van de vooraf verpakte Power BI-service binnen hun organisatie, maar ook elementen wil insluiten in hun toepassingen. En natuurlijk kunnen sommige ondernemingen besluiten om te kiezen voor A-SKU's in Azure als ze alleen geïnteresseerd zijn in het bouwen van LoB-toepassingen (Line-of-Business) met ingesloten analytische gegevens en niet zijn geïnteresseerd in het gebruik van de vooraf verpakte Power BI-service.

### <a name="how-many-embed-tokens-can-i-create"></a>Hoeveel insluitingstokens kan ik maken?

Insluitingstokens met een PRO-licentie zijn bedoeld voor ontwikkelingstesten, dus een Power BI-masteraccount kan maar een beperkt aantal insluitingstokens genereren. U moet [een capaciteit aanschaffen](https://docs.microsoft.com/power-bi/developer/embedded-faq#technical) voor het insluiten van items in een productieomgeving. Wanneer u een capaciteit hebt aangeschaft, kunt u een onbeperkt aantal insluitingstokens genereren.

## <a name="technical"></a>Technisch

### <a name="what-is-the-difference-between-the-a-skus-in-azure-and-the-em-skus-in-office-365"></a>Wat is het verschil tussen de A-SKU's in Azure en de EM-SKU's in Office 365?

PowerBI.com is een bedrijfsoplossing die veel mogelijkheden biedt, zoals sociale samenwerking, e-mailabonnementen enzovoort, in een SaaS-aanbieding (Software as a Service).

Power BI Embedded bestaat uit een set API's die beschikbaar zijn voor ontwikkelaars voor het maken van een ingesloten oplossing voor analytische gegevens in een PaaS-aanbieding (Platform als een Service). Voor het scenario met ingesloten analytische gegevens moet PowerBI.com worden gebruikt om ISV's en ontwikkelaars te helpen bij het beheer van de inhoud van hun ingesloten oplossing voor analytische gegevens en instellingen op tenantniveau.

Hier volgt een (niet volledige) lijst met verschillen tussen de versies.

|Functie  |Power BI Embedded<br>(A-SKU's) |Power BI Premium-capaciteit<br>(EM-SKU's)  | 
|---------|---------|---------|
|Artefacten uit Power BI-App-werkruimten insluiten     |Azure capaciteit |Office 365-capaciteit |
|Power BI-licentie vereist voor gebruiken van rapporten |Nee  |Ja |
|Power BI-rapporten gebruiken in een ingesloten toepassing |Ja  |Ja |
|Power BI-rapporten gebruiken in SharePoint |Nee |Ja |
|Power BI-rapporten gebruiken in Teams |Nee |Ja |

### <a name="power-bi-now-offers-three-skus-for-embedding-a-skus-em-skus-and-p-skus-which-one-should-i-purchase-for-my-scenario"></a>Power BI biedt nu drie SKU's voor insluiten: A-SKU's, EM-SKU's en P-SKU's. Welke moet ik kopen voor mijn scenario?

|  |A-SKU (Power BI Embedded)  |EM-SKU (Power BI Premium)  |P-SKU (Power BI Premium)  |
|---------|---------|---------|---------|
|Kopen     |Azure-portal |Office |Office |
|Gebruiksvoorbeelden |* Inhoud insluiten in uw eigen toepassing |* Inhoud insluiten in uw eigen toepassing<br>* Inhoud delen met gebruikers van de gratis versie van Power BI buiten PowerBI.com en insluiten in andere SaaS-toepassingen (SharePoint, Teams) |* Inhoud insluiten in uw eigen toepassing<br>* Inhoud delen met gebruikers van de gratis versie van Power BI buiten PowerBI.com en insluiten in andere SaaS-toepassingen (SharePoint, Teams)<br>* Inhoud delen met gebruikers van de gratis versie van Power BI via PowerBI.com  |
|Facturering |Per uur |Per maand |Per maand |
|Min. periode  |Geen minimumperiode |Jaar  |Maand/jaar |
|Differentiatie |Volledige elasticiteit: omhoog/omlaag schalen, resources onderbreken/hervatten in Azure-portal of via API  |Kan worden gebruikt voor het insluiten van inhoud in SharePoint Online en Microsoft Teams |Insluiten in toepassingen combineren met het gebruik van de Power BI-service in dezelfde capaciteit |

### <a name="what-are-the-prerequisites-to-create-a-pbie-capacity-in-azure"></a>Wat zijn de vereisten voor het maken van een PBIE-capaciteit in Azure?

- U moet zich aanmelden bij uw bedrijfsdirectory (MSA-accounts worden niet ondersteund).
- U moet een Power BI-tenant hebben; dat wil zeggen dat ten minste één gebruiker in uw directory moet zijn aangemeld bij Power BI. 
- U moet een Azure-abonnement hebben in uw bedrijfsdirectory.

### <a name="how-can-i-monitor-capacity-consumption"></a>Hoe kan ik het capaciteitsverbruik controleren?

Controle via Azure staat op de planning voor de korte termijn. De Azure-resource, Power BI Embedded, zal controle-KPI's bevatten die informatie geven over status en gebruik.

### <a name="will-my-capacity-scale-automatically-to-adjust-to-the-consumption-of-my-app"></a>Wordt mijn capaciteit automatisch geschaald op basis van het verbruik van mijn app?

Hoewel er op dit moment nog geen functie voor automatisch schalen is, zijn alle API's beschikbaar op om ieder gewenst moment te schalen.

### <a name="what-is-the-authentication-model-for-power-bi-embedded"></a>Wat is het verificatiemodel voor Power BI Embedded?

Power BI Embedded blijft Azure AD gebruiken voor de verificatie van de hoofdgebruiker (een aangewezen gebruiker met een Power BI Pro-licentie), waarbij de toepassing binnen Power BI wordt geverifieerd.

De verificatie en autorisatie van de toepassingsgebruikers wordt geïmplementeerd door de ISV. ISV's kunnen hun eigen verificatie implementeren voor hun toepassingen.

Als u al een Azure AD-tenant hebt, kunt u uw bestaande adreslijst gebruiken of u kunt een nieuwe Azure AD-tenant maken voor de beveiliging van de inhoud van uw ingesloten toepassing.

### <a name="how-is-power-bi-embedded-different-from-other-azure-services"></a>Hoe verschilt Power BI Embedded van andere Azure-services?

De ISV of ontwikkelaar moet een Power BI-account hebben vóór de aankoop van Power BI Embedded in Azure. De implementatieregio van Power BI Embedded wordt bepaald door uw Power BI-account. U kunt uw Power BI Embedded-resource beheren in Azure om het volgende in te stellen:

* Omhoog/omlaag schalen
* Capaciteitsbeheerders toevoegen
* Service onderbreken/hervatten

Gebruik PowerBI.com om werkruimten toe te wijzen aan uw Power BI Embedded-capaciteit of om hun toewijzing ongedaan te maken.

### <a name="what-deploy-regions-are-supported"></a>Welke implementatieregio's worden ondersteund?

Australië - zuidoost, Brazilië - zuid, Canada Centraal, VS - oost 2, India, westen, Japan - oost, VS Noord-Centraal, Noord-Europa, VS - zuiden (midden), Zuidoost-Azië, VK Zuid, West-Europa, VS-West en VS-West 2.

### <a name="what-type-of-content-pack-data-can-be-embedded"></a>Welk type inhoudspakketgegevens kan worden ingesloten?

**Dashboards** en **tegels** die zijn gebouwd op basis van gegevenssets van het inhoudspakket *kunnen niet* worden ingesloten. **Rapporten** die zijn gebouwd op basis van een gegevensset van het inhoudspakket *kunnen* echter wel worden ingesloten.

## <a name="licensing"></a>Licentieverlening

### <a name="how-do-i-purchase-power-bi-embedded"></a>Hoe kan ik Power BI Embedded kopen?

Power BI Embedded is beschikbaar via Azure.

### <a name="what-happens-if-i-already-purchased-power-bi-premium-and-now-i-want-some-of-the-benefits-of-power-bi-embedded-in-azure"></a>Wat gebeurt er als ik Power BI Premium al heb gekocht en ik nu in Azure wil beschikken over enkele voordelen van Power BI Embedded?

Klanten blijven betalen voor bestaande Power BI Premium-aankopen tot het einde van hun huidige abonnementsperiode en kunnen hun Power BI Premium-aankopen op dat moment overzetten.

### <a name="do-i-still-have-to-buy-power-bi-premium-to-get-access-to-power-bi-embedded"></a>Moet ik toch nog Power BI Premium kopen om toegang te krijgen tot Power BI Embedded?

Nee, Power BI Embedded omvat de op Azure gebaseerde capaciteit die u nodig hebt om uw oplossing te implementeren en distribueren naar klanten.

### <a name="whats-the-purchase-commitment-for-power-bi-embedded"></a>Wat is de aankoopverplichting voor Power BI Embedded? 

Klanten kunnen hun gebruik op uurbasis aanpassen. Er is geen maandelijkse of jaarlijkse verplichting voor de Power BI Embedded-service.

### <a name="how-does-the-usage-of-power-bi-embedded-show-up-on-my-bill"></a>Hoe wordt het gebruik van Power BI Embedded weergegeven op mijn factuur?

De facturering voor Power BI Embedded vindt plaats volgens een voorspelbaar uurtarief op basis van het geïmplementeerde type knooppunt (of typen knooppunten). Houd er rekening dat er kosten in rekening worden gebracht zolang uw bron actief is, ook als u hier geen gebruik van maakt. U moet uw bron actief onderbreken als u niet meer wilt worden gefactureerd.

### <a name="who-needs-a-power-bi-pro-license-for-power-bi-embedded-and-why"></a>Wie moet een Power BI Pro-licentie voor Power BI Embedded hebben en waarom?

Een licentie voor Power BI Pro is vereist voor analisten die rapporten moeten toevoegen aan een Power BI-werkruimte, ontwikkelaars die de REST-API's willen gebruiken en tenantbeheerders die de Power BI-tenant en -capaciteit moeten beheren.

Omdat Power BI Embedded het gebruik van de Power BI-portal toestaat voor het beheren en valideren van ingesloten inhoud, is de Power BI Pro-licentie vereist voor het verifiëren van de app in PowerBI.com voor toegang tot de rapporten in de juiste opslagplaatsen.

### <a name="can-i-get-started-for-free"></a>Kan ik gratis aan de slag?

Ja, u kunt uw [Azure-tegoed](https://azure.microsoft.com/free/) gebruiken voor Power BI Embedded.

### <a name="can-i-get-a-trial-experience-for-power-bi-embedded-in-azure"></a>Is er een evaluatieversie voor Power BI Embedded in Azure?

Power BI Embedded maakt deel uit van Azure en dus is het mogelijk om de service te gebruiken met het [tegoed van $ 200 dat u hebt ontvangen bij het aanmelden voor Azure](https://azure.microsoft.com/free/).

### <a name="is-there-a-limit-to-the-number-of-embed-tokens-a-power-bi-master-account-can-generate"></a>Is er een limiet aan het aantal insluittokens dat kan worden gegenereerd door een Power BI-hoofdaccount? 

Ja, het aantal is beperkt omdat deze insluittokens alleen bedoeld zijn voor ontwikkeltests. [Er moet een capaciteit worden aangeschaft](#technical) voor insluitingsscenario's voor de productie. Het aantal te genereren insluitingstokens is onbeperkt wanneer een capaciteit is aangeschaft. Ga naar [Beschikbare functies ophalen](https://msdn.microsoft.com/en-us/library/mt846473.aspx) om te controleren hoeveel gratis insluittokens zijn gebruikt.

### <a name="is-power-bi-embedded-available-for-sovereign-clouds-us-government-germany-china"></a>Is Power BI Embedded beschikbaar voor soevereine clouds (US Government, Duitsland, China)?

Power BI Embedded is beschikbaar voor sommige [soevereine clouds](embed-sample-for-customers-sovereign-clouds.md). Het is **NIET** beschikbaar voor de China-cloud.

### <a name="is-power-bi-embedded-available-for-non-profits-and-educational"></a>Is Power BI Embedded beschikbaar voor non-profitorganisaties en het onderwijs?

Non-profitorganisaties en onderwijsinstellingen kunnen Azure kopen. Er zijn geen speciale prijzen voor deze typen klanten in Azure.

Zie voor meer informatie [Problemen oplossen met uw ingesloten toepassing](embedded-troubleshoot.md)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)



