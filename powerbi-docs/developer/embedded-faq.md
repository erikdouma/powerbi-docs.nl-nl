---
title: Veelgestelde vragen over Power BI Embedded
description: Hier vindt u een lijst met veelgestelde vragen en antwoorden over Power BI Embedded.
author: markingmyname
ms.author: maghan
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-developer
ms.topic: conceptual
ms.date: 09/17/2018
ms.openlocfilehash: 56b6c954aa49f8adf0aa479f143fb11b932c107e
ms.sourcegitcommit: ac63e6a082ca8397909217837e8d98c9389b23ac
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2018
ms.locfileid: "50736959"
---
# <a name="frequently-asked-questions-about-power-bi-embedded"></a>Veelgestelde vragen over Power BI Embedded

* Als u andere vragen hebt, kunt u deze stellen [in de Power BI-community](http://community.powerbi.com/).
* Nog steeds geen antwoord? Ga naar de [ondersteuningspagina van Power BI](https://powerbi.microsoft.com/support/).

## <a name="general"></a>Algemeen

### <a name="what-is-power-bi-embedded"></a>Wat is Power BI Embedded?

Microsoft Power BI Embedded (PBIE) zorgt ervoor dat ontwikkelaars van toepassingen schitterende, volledig interactieve rapporten kunnen insluiten in toepassingen, zonder dat ze hiervoor tijd en geld kwijt zijn om hun eigen gegevensvisualisaties en besturingselementen helemaal zelf te bouwen.

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

Er zijn misschien enkele situaties waarin een ISV (meestal groot) een P-SKU wil gebruiken om te beschikken over de extra voordelen van de vooraf verpakte Power BI-service binnen hun organisatie, maar ook elementen wil insluiten in hun toepassingen. En natuurlijk kunnen sommige ondernemingen besluiten om te kiezen voor A-SKU's in Azure als ze alleen geïnteresseerd zijn in het bouwen van Line-Of-Business-toepassingen met ingesloten analytische gegevens en niet zijn geïnteresseerd in het gebruik van de vooraf verpakte Power BI-service.

### <a name="how-many-embed-tokens-can-i-create"></a>Hoeveel insluitingstokens kan ik maken?

Insluitingstokens met een PRO-licentie zijn bedoeld voor ontwikkelingstesten, dus een Power BI-hoofdaccount kan maar een beperkt aantal insluitingstokens genereren. U moet [een capaciteit aanschaffen](#technical) voor het insluiten van items in een productieomgeving. Wanneer u een capaciteit hebt aangeschaft, kunt u een onbeperkt aantal insluitingstokens genereren. Ga naar [Beschikbare functies](https://docs.microsoft.com/rest/api/power-bi/availablefeatures) om de waarde voor het gebruik te controleren. Hiermee wordt het huidige gebruik van insluittokens in procenten aangegeven.

## <a name="technical"></a>Technisch

### <a name="what-is-the-difference-between-the-a-skus-in-azure-and-the-em-skus-in-office-365"></a>Wat is het verschil tussen de A-SKU's in Azure en de EM-SKU's in Office 365?

PowerBI.com is een bedrijfsoplossing die veel mogelijkheden biedt, zoals sociale samenwerking, e-mailabonnementen enzovoort, in een SaaS-aanbieding (Software as a Service).

Power BI Embedded bestaat uit een set API's die beschikbaar zijn voor ontwikkelaars voor het maken van een ingesloten oplossing voor analytische gegevens in een PaaS-aanbieding (Platform als een Service). Voor het scenario met ingesloten analytische gegevens moet PowerBI.com worden gebruikt om ISV's en ontwikkelaars te helpen bij het beheer van de inhoud van hun ingesloten oplossing voor analytische gegevens en instellingen op tenantniveau.

Hier volgt een (niet volledige) lijst met verschillen tussen de versies.

| Functie | Power BI Embedded | Power BI Premium-capaciteit | Power BI Premium-capaciteit |
|----------------------------------------------------------------------------------|-------------------|---------------------------|---------------------------|
|   | (A-SKU's) | (EM-SKU's) | (P-SKU's) |
| Artefacten uit Power BI-app-werkruimten insluiten | Azure capaciteit | Office 365-capaciteit | Office 365-capaciteit |
| Power BI-rapporten gebruiken in een ingesloten toepassing | Ja | Ja | Ja |
| Power BI-rapporten gebruiken in SharePoint | Nee | Ja | Ja |
| Power BI-rapporten gebruiken in Dynamics | Nee | Ja | Ja |
| Power BI-rapporten gebruiken in Teams (uitgezonderd de mobiele app) | Nee | Ja | Ja |
| Inhoud op Powerbi.com en in de mobiele Power BI-app openen met een GRATIS Power BI-licentie | Nee | Nee | Ja |
| Inhoud die is ingesloten in MS Office-apps openen met een GRATIS Power BI-licentie | Nee | Ja | Ja |

### <a name="power-bi-now-offers-three-skus-for-embedding-a-skus-em-skus-and-p-skus-which-one-should-i-purchase-for-my-scenario"></a>Power BI biedt nu drie SKU's voor insluiten: A-SKU's, EM-SKU's en P-SKU's. Welke moet ik kopen voor mijn scenario?

|  |A-SKU (Power BI Embedded)  |EM-SKU (Power BI Premium)  |P-SKU (Power BI Premium)  |
|---------|---------|---------|---------|
|Kopen  |Azure-portal |Office |Office |
|Gebruiksvoorbeelden | Inhoud insluiten in uw eigen toepassing | <li> Inhoud insluiten in uw eigen toepassing <br><br></br> <li> Inhoud insluiten in Microsoft Office-toepassingen: <br> - [SharePoint](https://powerbi.microsoft.com/blog/integrate-power-bi-reports-in-sharepoint-online/) <br> - [Teams (uitgezonderd de mobiele app)](https://powerbi.microsoft.com/blog/power-bi-teams-up-with-microsoft-teams/) <br> - [Dynamics 365](https://docs.microsoft.com/dynamics365/customer-engagement/basics/add-edit-power-bi-visualizations-dashboard) | <li> Inhoud insluiten in uw eigen toepassing <br><br></br> <li> Inhoud insluiten in Microsoft Office-toepassingen: <br> - [SharePoint](https://powerbi.microsoft.com/blog/integrate-power-bi-reports-in-sharepoint-online/) <br> - [Teams (uitgezonderd de mobiele app)](https://powerbi.microsoft.com/blog/power-bi-teams-up-with-microsoft-teams/) <br> - [Dynamics 365](https://docs.microsoft.com/dynamics365/customer-engagement/basics/add-edit-power-bi-visualizations-dashboard) <br><br></br> <li> Inhoud delen met gebruikers van Power BI via [Power BI-service](https://powerbi.microsoft.com/en-us/)  |
|Facturering |Per uur |Per maand |Per maand |
|Min. periode  |Geen minimumperiode |Jaar  |Maand/jaar |
|Differentiatie |Volledige elasticiteit: omhoog/omlaag schalen, resources onderbreken/hervatten in Azure-portal of via API  |Kan worden gebruikt voor het insluiten van inhoud in SharePoint Online en Microsoft Teams (uitgezonderd de mobiele app) |Insluiten in toepassingen combineren met het gebruik van de Power BI-service in dezelfde capaciteit |

### <a name="what-are-the-prerequisites-to-create-a-pbie-capacity-in-azure"></a>Wat zijn de vereisten voor het maken van een PBIE-capaciteit in Azure?

* U moet zich aanmelden bij uw bedrijfsdirectory (MSA-accounts worden niet ondersteund).
* U moet een Power BI-tenant hebben; dat wil zeggen dat ten minste één gebruiker in uw directory moet zijn aangemeld bij Power BI. 
* U moet een Azure-abonnement hebben in uw bedrijfsdirectory.

### <a name="how-can-i-monitor-power-bi-embedded-capacity-consumption"></a>Hoe kan ik het verbruik van de Power BI Embedded-capaciteit bewaken?

* De [Power BI-beheerportal](../service-admin-portal.md#power-bi-embedded) gebruiken.

* De [metrische app](https://review.docs.microsoft.com/power-bi/service-admin-premium-monitor-capacity) in Power BI downloaden.

* [Logboekregistratie van diagnostische gegevens in Azure](azure-pbie-diag-logs.md) gebruiken.

### <a name="will-my-capacity-scale-automatically-to-adjust-to-the-consumption-of-my-app"></a>Wordt mijn capaciteit automatisch geschaald op basis van het verbruik van mijn app?

Hoewel er op dit moment nog geen functie voor automatisch schalen is, zijn alle API's beschikbaar op om ieder gewenst moment te schalen.

### <a name="why-creatingscalingresuming-a-capacity-results-in-putting-the-capacity-into-a-suspended-state"></a>Waarom wordt een capaciteit bij het maken/schalen/hervatten in de status onderbroken geplaatst?

Het inrichten van een capaciteit (schalen/hervatten/maken) mislukt mogelijk. De aanroeper van de inrichtingsaanroep moet de ProvisioningState van een capaciteit controleren met de API voor gegevens ophalen: [Capaciteiten - Details ophalen](https://docs.microsoft.com/rest/api/power-bi-embedded/capacities/getdetails).

### <a name="why-can-i-only-create-pbie-in-a-specific-region"></a>Waarom kan ik PBIE alleen in een bepaalde regio maken?

U kunt alleen PBIE-capaciteiten voor uw PBI-tenantregio maken.

### <a name="how-can-i-find-what-is-my-pbi-tenant-region"></a>Waar kan ik zien wat mijn PBI-tenantregio is?

U kunt de PBI-portal gebruiken om te zien wat uw PBI-tenantregio is.

https://app.powerbi.com/ > ? > Over Power BI

![Over Power BI](media/embedded-faq/about-01.png)
![Tenantregio](media/embedded-faq/tenant-location-01.png)

### <a name="what-is-supported-with-the-communicating-sequential-processes-csp-channel"></a>Wat wordt ondersteund met het CSP-kanaal (communicating sequential processes)?

* U kunt PBIE maken voor uw tenant met het abonnementstype CSP
* Het partneraccount kan zich aanmelden bij de klanttenant en PBIE kopen voor de klanttenant. Geef de gebruiker van de klanttenant op als Power BI-capaciteitsbeheerder.

### <a name="why-do-i-get-an-unsupported-account-message"></a>Waarom krijg ik een bericht over een niet-ondersteund account?

Voor Power BI moet u zich aanmelden met een organisatieaccount. Het aanmelden voor Power BI met een MSA (Microsoft-account) wordt niet ondersteund.

### <a name="can-i-use-apis-to-create--manage-azure-capacities"></a>Kan ik API's gebruiken voor het maken en beheren van Azure-capaciteiten?

Ja, er zijn Powershell-cmdlets en API's voor Azure Resource Manager (ARM) die u kunt gebruiken voor het maken en beheren van PBIE-resources.

* REST-API's - https://docs.microsoft.com/rest/api/power-bi-embedded/
* PowerShell-cmdlets - https://docs.microsoft.com/powershell/module/azurerm.powerbiembedded/

### <a name="what-is-the-pbi-embedded-dedicated-capacity-role-in-a-pbi-embedded-solution"></a>Wat is de rol van de toegewezen PBI Embedded-capaciteit in een PBI Embedded-oplossing?

Als u [uw oplossing wilt verhogen naar productie](https://docs.microsoft.com/power-bi/developer/embedding-content#step-3-promote-your-solution-to-production), moet u de Power BI-inhoud (app-werkruimte) die u in uw toepassing gebruikt, toewijzen aan een Power BI Embedded (A SKU)-capaciteit.

### <a name="what-are-the-azure-regions-pbi-embedded-is-available"></a>Wat zijn de Azure-regio's waar PBI Embedded beschikbaar is?

[PAM](https://ecosystemmanager.azurewebsites.net/home) (EcoManager) - Zie Product availability manager

Beschikbare regio's (16 - dezelfde regio's als Power BI)
* US (6) - US - oost, US - oost 2, US - noord-centraal, US - zuid-centraal, US - west, US - west 2
* Europa (2) - Europa - noord, Europa - west
* Azië en Stille Oceaan (2) - Azië - zuidoost, Azië - oost
* Brazilië (1) - Brazilië - zuid
* Japan (1) Japan - oost
* Australië (1) - Australië - zuidoost
* India (1) - India - west
* Canada (1) Canada Centraal
* Verenigd Koninkrijk (1) - UK - zuid

### <a name="what-is-the-authentication-model-for-power-bi-embedded"></a>Wat is het verificatiemodel voor Power BI Embedded?

Power BI Embedded blijft Azure AD gebruiken voor de verificatie van de hoofdgebruiker (een aangewezen gebruiker met een Power BI Pro-licentie), waarbij de toepassing binnen Power BI wordt geverifieerd.

De verificatie en autorisatie van de toepassingsgebruikers wordt geïmplementeerd door de ISV. ISV's kunnen hun eigen verificatie implementeren voor hun toepassingen.

Als u al een Azure AD-tenant hebt, kunt u uw bestaande adreslijst gebruiken of u kunt een nieuwe Azure AD-tenant maken voor de beveiliging van de inhoud van uw ingesloten toepassing.

Als u een AAD-token wilt ophalen, kunt u één van de Azure Active Directory-verificatiebibliotheken gebruiken: https://docs.microsoft.com/azure/active-directory/develop/active-directory-authentication-libraries. Er zijn clientbibliotheken beschikbaar voor meerdere platformen.

### <a name="my-application-already-uses-aad-for-user-authentication-how-can-we-use-this-identity-when-authenticating-to-power-bi-in-a-user-owns-data-scenario"></a>Mijn toepassing gebruikt al AAD voor verificatie van de gebruiker. Hoe kunnen we deze identiteit gebruiken bij de verificatie bij Power BI in een scenario waarin de gebruiker eigenaar is van de gegevens? 

Het is standaard OAuth on-behalf-of flow (https://docs.microsoft.com/azure/active-directory/develop/active-directory-authentication-scenarios#web-application-to-web-api) de toepassing moet zo worden geconfigureerd dat machtigingen zijn vereist voor Power BI-service (met de vereiste bereiken). Zodra u een gebruikerstoken voor uw app hebt, roept u de ADAL-API AcquireTokenAsync aan met het token voor gebruikerstoegang en geeft u de Power BI resource-URL op als de resource-id. Hieronder ziet u een voorbeeld van hoe u dit kunt doen:

```csharp
var context = new AD.AuthenticationContext(authorityUrl);
var userAssertion = new AD.UserAssertion(userAccessToken);
var clientAssertion = new AD.ClientAssertionCertificate(MyAppId, MyAppCertificate)
var authenticationResult = await context.AcquireTokenAsync(resourceId, clientAssertion, userAssertion);
```

### <a name="how-is-power-bi-embedded-different-from-other-azure-services"></a>Hoe verschilt Power BI Embedded van andere Azure-services?

De ISV of ontwikkelaar moet een Power BI-account hebben vóór de aankoop van Power BI Embedded in Azure. De implementatieregio van Power BI Embedded wordt bepaald door uw Power BI-account. U kunt uw Power BI Embedded-resource beheren in Azure om het volgende in te stellen:

* Omhoog/omlaag schalen
* Capaciteitsbeheerders toevoegen
* Service onderbreken/hervatten

Gebruik PowerBI.com om werkruimten toe te wijzen aan uw Power BI Embedded-capaciteit of om hun toewijzing ongedaan te maken.

### <a name="what-deploy-regions-are-supported"></a>Welke implementatieregio's worden ondersteund?

Australië - zuidoost, Brazilië - zuid, Canada Centraal, US - oost 2, India - west, Japan - oost, US - noord-centraal, Europa - noord, US - zuid-centraal, Azië - zuidoost, VK Zuid, Europa - west, US - west en US - west 2.

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

Voor het [maken of bewerken van ingesloten rapporten](https://github.com/Microsoft/PowerBI-JavaScript/wiki/Create-Report-in-Embed-View) binnen uw eigen toepassing heeft de eindgebruiker echter geen Pro-licentie nodig omdat deze helemaal geen Power BI-gebruiker hoeft te zijn.

### <a name="can-i-get-started-for-free"></a>Kan ik gratis aan de slag?

Ja, u kunt uw [Azure-tegoed](https://azure.microsoft.com/free/) gebruiken voor Power BI Embedded.

### <a name="can-i-get-a-trial-experience-for-power-bi-embedded-in-azure"></a>Is er een evaluatieversie voor Power BI Embedded in Azure?

Power BI Embedded maakt deel uit van Azure en dus is het mogelijk om de service te gebruiken met het [tegoed van $ 200 dat u hebt ontvangen bij het aanmelden voor Azure](https://azure.microsoft.com/free/).

### <a name="is-power-bi-embedded-available-for-sovereign-clouds-us-government-germany-china"></a>Is Power BI Embedded beschikbaar voor soevereine clouds (US Government, Duitsland, China)?

Power BI Embedded is beschikbaar voor sommige [soevereine clouds](embed-sample-for-customers-sovereign-clouds.md). Het is **NIET** beschikbaar voor de China-cloud.

### <a name="is-power-bi-embedded-available-for-non-profits-and-educational"></a>Is Power BI Embedded beschikbaar voor non-profitorganisaties en het onderwijs?

Non-profitorganisaties en onderwijsinstellingen kunnen Azure kopen. Er zijn geen speciale prijzen voor deze typen klanten in Azure.

## <a name="power-bi-workspace-collection"></a>Power BI-werkruimteverzameling

### <a name="what-is-power-bi-workspace-collection"></a>Wat is de Power BI-werkruimteverzameling?

De **Power BI-werkruimteverzameling** (**Power BI Embedded** versie 1) is een oplossing die is gebaseerd op de Azure-resource **Power BI-werkruimteverzameling**. Met deze oplossing kunt u **Power BI Embedded**-toepassingen voor uw klanten maken met behulp van Power BI-inhoud in de **Power BI-werkruimteverzameling**, toegewezen API's en werkruimteverzamelingsleutels waarmee de toepassing kan worden geverifieerd in Power BI.

### <a name="can-i-migrate-from-power-bi-workspace-collection-to-power-bi-embedded"></a>Kan ik inhoud van de Power BI-werkruimteverzameling migreren naar Power BI Embedded?

1. U kunt het hulpprogramma voor migratie gebruiken om inhoud van de **Power BI-werkruimteverzameling** te migreren naar Power BI - https://docs.microsoft.com/power-bi/developer/migrate-from-powerbi-embedded#content-migration.

2. U begint met de POC van de **Power BI Embedded**-toepassing waarin gebruik wordt gemaakt van de Power BI-inhoud.

3. Wanneer u klaar bent voor productie, koopt u toegewezen capaciteit van **Power BI Embedded** en wijst u uw Power BI-inhoud (werkruimte) aan die capaciteit toe.

> [!Note]
> U kunt de **Power BI-werkruimteverzameling** blijven gebruiken terwijl u daarnaast een **Power BI Embedded**-oplossing bouwt. Zodra u klaar bent, kunt u uw klant naar de nieuwe **Power BI Embedded**-oplossing verplaatsen en de **Power BI-werkruimteverzameling** buiten gebruik stellen.

Zie [Inhoud van de Power BI-werkruimteverzameling migreren naar Power BI Embedded](https://docs.microsoft.com/power-bi/developer/migrate-from-powerbi-embedded) voor meer informatie.

### <a name="is-power-bi-workspace-collection-on-a-path-to-be-deprecated"></a>Wordt de Power BI-werkruimteverzameling afgeschaft?

Ja, maar de klanten die al gebruikmaken van de oplossing **Power BI-werkruimteverzameling** kunnen deze blijven gebruiken totdat deze wordt afgeschaft. Daarnaast kunnen klanten nieuwe werkruimteverzamelingen maken en **Power BI Embedded**-toepassingen die nog steeds gebruikmaken van de oplossing **Power BI-werkruimteverzameling**.

Dit betekent echter wel dat er geen nieuwe functies worden toegevoegd aan de oplossingen voor de **Power BI-werkruimteverzameling** en dat klanten wordt aangeraden de migratie naar de nieuwe **Power BI Embedded**-oplossing te plannen.
### <a name="when-will-power-bi-workspace-collection-support-be-discontinued"></a>Wanneer wordt ondersteuning voor de Power BI-werkruimteverzameling stopgezet?

Klanten die al gebruikmaken van de oplossing voor de **Power BI-werkruimteverzamelingen** kunnen deze blijven gebruiken tot eind juni 2018 of tot het einde van de ondersteuningsovereenkomst.

### <a name="in-what-regions-can-pbi-workspace-collection-be-created"></a>In welke regio's kunnen PBI-werkruimteverzameling worden gemaakt?

Beschikbare regio's zijn Australië - zuidoost, Brazilië - zuid, Canada Centraal, US - oost 2, Japan - oost, US - noord-centraal, Europa - noord, US - zuid-centraal, Azië - zuidoost, VK Zuid, Europa - west, India - west en US - west.

### <a name="why-should-i-migrate-from-pbi-workspace-collection-to-power-bi-embedded"></a>Waarom moet ik inhoud van PBI-werkruimteverzameling migreren naar Power BI Embedded?

Er zijn nieuwe functies en mogelijkheden geïntroduceerd in de **Power BI Embedded**-oplossing die niet beschikbaar zijn in de **Power BI-werkruimteverzameling**.

Hieronder vindt u enkele voorbeelden van deze functies:
* Alle PBI-gegevensbronnen worden ondersteund, in tegenstelling tot de twee gegevensbronnen die in de **Power BI-werkruimteverzameling** worden ondersteund. 
* Nieuwe functies, zoals functies voor Q&A, vernieuwen, bladwijzers, het insluiten van dashboards en tegels, aangepaste menu's, enzovoort, worden alleen ondersteund in de **Power BI Embedded**-oplossing.
* Model voor facturering van capaciteit.

## <a name="embedding-setup-tool-for-embedding"></a>Installatieprogramma voor insluiten

### <a name="what-is-the-embedding-setup-tool"></a>Wat is het installatieprogramma voor insluiten?

Met het [installatieprogramma voor insluiten](https://aka.ms/embedsetup) kunt u snel aan de slag en een voorbeeldtoepassing downloaden om met het insluiten van inhoud met behulp van Power BI te beginnen.

### <a name="which-solution-should-i-choose"></a>Welke oplossing moet ik kiezen?

* [Door inhoud voor uw klanten in te sluiten](embedding.md#embedding-for-your-customers) kunt u dashboards en rapporten insluiten voor gebruikers die geen account voor Power BI hebben. Voer de oplossing [Insluiten voor uw klanten](https://aka.ms/embedsetup/AppOwnsData) uit.
* [Met het insluiten van inhoud voor uw organisatie](embedding.md#embedding-for-your-organization) kunt u Power BI-service uitbreiden. Voer de oplossing [Insluiten voor uw organisatie](https://aka.ms/embedsetup/UserOwnsData) uit.

### <a name="ive-downloaded-the-sample-app-which-solution-do-i-choose"></a>Ik heb de voorbeeld-app gedownload. Welke oplossing moet ik kiezen?

Als u met de ervaring **Insluiten voor uw klanten** werkt, moet u het bestand *PowerBI-Developer-Samples.zip* opslaan en uitpakken. Open vervolgens de map *PowerBI-Developer-Samples-master\App Owns Data* en voer het bestand *PowerBIEmbedded_AppOwnsData.sln* uit.

Als u met de ervaring **Insluiten voor uw organisatie** werkt, moet u het bestand *PowerBI-Developer-Samples.zip* opslaan en uitpakken. Open vervolgens de map *PowerBI-Developer-Samples-master\User Owns Data\integrate-report-web-app* en voer het bestand *pbi-saas-embed-report.sln* uit.

### <a name="how-can-i-edit-my-registered-application"></a>Hoe kan ik mijn geregistreerde toepassing bewerken?

U kunt [hier](https://docs.microsoft.com/azure/active-directory/develop/active-directory-integrating-applications#updating-an-application) leren hoe u geregistreerde AAD-toepassingen bewerkt.

### <a name="how-can-i-edit-my-power-bi-user-profile-or-data"></a>How kan ik mijn Power BI-gebruikersprofiel of -gegevens bewerken?

U kunt [hier](https://docs.microsoft.com/power-bi/service-basic-concepts) leren hoe u uw Power BI-gegevens bewerkt.

Zie voor meer informatie [Problemen oplossen met uw ingesloten toepassing](embedded-troubleshoot.md)

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)
