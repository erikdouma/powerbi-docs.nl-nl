---
title: 'Gepagineerde rapporten in Power BI: veelgestelde vragen (preview)'
description: In dit artikel vindt u antwoorden op veelgestelde vragen over gepagineerde rapporten. Deze rapporten bevatten een uitgebreid opgemaakte, tot op de pixel nauwkeurige uitvoer die is geoptimaliseerd voor afdrukken of het genereren van PDF's.
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: report-builder
ms.topic: overview
ms.date: 11/05/2018
ms.author: maggies
ms.openlocfilehash: 0ddf95563c52af135ac7ae4fe71aeddcd2ce7313
ms.sourcegitcommit: b23fdcc0ceff5acd2e4d52b15b310068236cf8c7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/07/2018
ms.locfileid: "51267274"
---
# <a name="paginated-reports-in-power-bi-faq-preview"></a>Gepagineerde rapporten in Power BI: veelgestelde vragen (preview)

In dit artikel vindt u antwoorden op veelgestelde vragen over gepagineerde rapporten. Deze rapporten bevatten een uitgebreid opgemaakte, tot op de pixel nauwkeurige uitvoer die is geoptimaliseerd voor afdrukken of het genereren van PDF's. Ze worden 'gepagineerd' genoemd, omdat ze zo zijn opgemaakt dat ze op meerdere pagina's passen. Gepagineerde rapporten zijn gebaseerd op de RDL-rapporttechnologie in SQL Server Reporting Services. 

In dit artikel vindt u antwoorden op veelvoorkomende vragen over gepagineerde rapporten in Power BI Premium, en over Report Builder, het zelfstandige hulpprogramma voor het ontwerpen van gepagineerde rapporten. U hebt een Power BI Pro-licentie nodig om een rapport te publiceren in de service. U kunt gepagineerde rapporten publiceren en delen in Mijn werkruimte of in de app-werkruimten, zolang de werkruimte zich in een Power BI Premium-capaciteit bevindt. 

## <a name="administration"></a>Beheer

### <a name="what-size-premium-capacity-do-i-need-for-paginated-reports"></a>Hoe groot moet de Premium-capaciteit zijn voor gepagineerde rapporten?

De werkbelasting van gepagineerde rapporten is beschikbaar op P1 – P3 SKU's voor openbare preview.  U kunt deze ook gebruiken voor test-/ontwikkelscenario's met A4 – A6-SKU's.

### <a name="what-is-the-maximum-memory-threshold-i-can-put-for-paginated-reports-in-my-capacity"></a>Wat is de maximum drempelwaarde van het geheugen dat ik voor gepagineerde rapporten in mijn capaciteit kan reserveren?

Momenteel kunt u slechts vijftig procent van het geheugen voor deze werkbelasting reserveren. 

### <a name="how-does-user-access-work-for-paginated-reports"></a>Hoe werkt gebruikerstoegang voor gepagineerde rapporten?

Gebruikerstoegang voor gepagineerde rapporten is hetzelfde als gebruikerstoegang voor alle andere inhoud in de Power BI-service 

### <a name="how-do-i-turn-onoff-my-paginated-reports-workload"></a>Hoe schakel ik de werkbelasting voor mijn gepagineerde rapporten in of uit?

De capaciteitsbeheerder kan de werkbelasting voor de gepagineerde rapporten in- of uitschakelen op de portalpagina van de capaciteitsbeheerder.  

### <a name="how-can-i-monitor-usage-of-paginated-reports-in-my-tenant"></a>Hoe kan ik het gebruik van gepagineerd rapporten in mijn tenant in de gaten houden?

Het gebruik van dit rapporttype wordt in de Office 365-auditlogboeken onder de volgende gebeurtenissen uitgebreid vermeld: 

- Power BI-rapport weergeven
- Power BI-rapport verwijderen
- Power BI-rapport maken
- Power BI-rapport gedownload

Het veld ReportType heeft de waarde PaginatedReport voor het identificeren van gepagineerde rapporten in plaats van Power BI-rapporten.

De auditlogboeken vermelden de volgende gebeurtenissen voor gepagineerde rapporten:

- Verbonden Power BI-gegevensset aan gateway
- Power BI-gegevensbron detecteren
- TakeOverDatasource

### <a name="can-i-monitor-this-workload-through-the-premium-capacity-monitoring-app"></a>Kan ik deze werkbelasting bewaken via de bewakings-app voor Premium-capaciteit?

Nog niet. De mogelijkheid tot bewaking wordt beschikbaar in openbare preview als een nieuw tabblad in het bestaande rapport. Het bevat dezelfde relevante details die u voor uw Power BI-gegevenssets hebt.

### <a name="do-i-need-a-pro-license-to-create-and-publish-paginated-reports"></a>Heb ik een Pro-licentie nodig om gepagineerde rapporten te maken en publiceren?

Ja. U kunt zonder Pro-licentie geen rapporten naar de werkruimte uploaden. Zonder Pro-licentie kunt u wel Report Builder downloaden en uitproberen, maar niet de gemaakte gepagineerde rapporten publiceren. 

### <a name="what-if-i-have-a-paginated-report-in-a-workspace-and-the-paginated-report-workload-is-turned-off"></a>Wat gebeurt er als ik een gepagineerd rapport in een werkruimte heb en de werkbelasting van het gepagineerde rapport wordt uitgeschakeld?

U ontvangt een foutbericht en u kunt uw rapport pas weergeven als de werkbelasting opnieuw wordt ingeschakeld. U kunt het rapport wel uit de werkruimte verwijderen.

### <a name="what-is-the-default-memory-for-each-of-the-premium-skus-supported-for-paginated-reports"></a>Wat is de standaardgeheugenruimte in elk van de Premium SKU's die voor gepagineerde rapporten worden ondersteund?

Standaardgeheugenruimte in elke Premium-SKU voor gepagineerde rapporten:

- **P1/A4**: standaard 20%; minimaal 10%
- **P2/A5**: standaard 10%; minimaal 5%
- **P3/A6**: standaard 5%; minimaal 2,5%

## <a name="general"></a>Algemeen

### <a name="when-should-i-use-a-paginated-report-vs-a-power-bi-report"></a>Wanneer moet ik een gepagineerd rapport gebruiken in plaats van een Power BI-rapport?

Gepagineerde rapporten zijn het geschiktst voor scenario's waarvoor een uitgebreid opgemaakte, tot op de pixel nauwkeurige uitvoer is vereist, die is geoptimaliseerd voor afdrukken of het genereren van PDF's.  Een verlies- en winstrekening is een goed voorbeeld van het type rapport dat u waarschijnlijk als een gepagineerd rapport wilt opmaken.  

Power BI-rapporten zijn geoptimaliseerd voor verkenning en interactiviteit.  Een Power BI-rapport is ideaal voor een verkooprapport waarin verschillende verkopers de gegevens in hetzelfde rapport voor hun specifieke regio/branche/klant willen onderbrengen en willen bekijken hoe de cijfers veranderen.

### <a name="the-documentation-says-report-builder-is-the-preferred-authoring-tool-can-i-create-paginated-reports-in-sql-server-data-tools-for-power-bi"></a>In de documentatie staat dat Report Builder het bewerkingsprogramma van voorkeur is. Kan ik gepagineerde rapporten maken in SQL Server Data Tools voor Power BI?

Ja, maar met de Power BI-service kunt u slechts één item per keer uploaden, dus veel scenario's die ontwerpers gebruiken met SQL Server Data Tools (SSDT) worden nog niet ondersteund. Zie de volledige [lijst met ondersteunde functies](#what-paginated-report-features-in-ssrs-arent-yet-supported-in-power-bi) verderop in deze Veelgestelde vragen.  

### <a name="what-versions-of-report-builder-do-you-support"></a>Welke versie(s) van Report Builder worden ondersteund?

Gebruik de nieuwste versie van SQL Server 2016 Report Builder voor het ontwerpen en publiceren van uw rapporten in de Power BI-service. Installeer [Report Builder vanuit het Microsoft Downloadcentrum](https://www.microsoft.com/download/details.aspx?id=53613).

### <a name="how-do-i-move-existing-reports-i-have-saved-in-sql-server-reporting-services-to-power-bi"></a>Hoe kan ik bestaande rapporten die in SQL Server Reporting Services zijn opgeslagen, naar Power BI verplaatsen?

U dient het rapport van de server te downloaden en vervolgens via de portal naar Power BI te uploaden.  Er is momenteel geen migratiehulpprogramma beschikbaar, maar mogelijk wordt er een gemaakt nadat de openbare preview is voltooid en de functiepariteit tussen de producten het juiste niveau heeft.

### <a name="can-i-open-reports-and-publish-directly-to-the-service"></a>Kan ik rapporten openen en rechtstreeks in de service publiceren?

Dat kan op dit moment niet. Het openen van rapporten en het rechtstreeks publiceren in de service vanuit Report Builder (net zoals met Power BI Desktop) wordt op een later tijdstip ondersteund.

### <a name="what-paginated-report-features-in-ssrs-arent-yet-supported-in-power-bi"></a>Welke functies van gepagineerde rapporten in SSRS worden nog niet in Power BI ondersteund?

Momenteel worden de volgende items nog niet door gepagineerde rapporten ondersteund:

- Gedeelde gegevensbronnen
- Gedeelde gegevenssets
- Subrapporten
- Doorklik- en drillthrough-acties
- Gekoppelde rapporten
- Bladwijzers
- Lagen in Bing-kaarten
- Aangepaste lettertypen
- Verborgen parameters

Sorteren met in- en uitschakelen en interactief sorteren zijn nog niet in productie, maar worden binnenkort verwacht.    

U krijgt een foutbericht als u een bestand met een niet-ondersteunde functie anders dan sorteren met in- en uitschakelen, in de Power BI-service wilt uploaden.

### <a name="what-data-sources-do-you-support-currently-for-paginated-reports"></a>Welke gegevensbronnen worden op dit moment voor gepagineerde rapporten ondersteund?

Azure SQL Database en modellen in tabelvorm van SQL Server en SQL Server Analysis Services (SSAS) worden ondersteund met behulp van de on-premises gateway. Momenteel worden SSAS-modellen met multidimensionale expressie (MDX) niet ondersteund.

Bij het openen van SSAS via de gateway, heeft de gebruiker wiens referenties zijn opgeslagen, verhoogde machtigingen in SSAS nodig om via de gateway te werken.

### <a name="what-authentication-methods-do-you-support"></a>Welke verificatiemethoden worden ondersteund?

Momenteel dient u een gebruikersnaam en een wachtwoord voor de gegevensbron in de portal of gateway op te slaan.  Aanvullende verificatiemethoden voor de ondersteuning van zaken als beveiliging op rijniveau worden later aan de preview toegevoegd.

### <a name="can-i-use-a-power-bi-dataset-as-a-data-source-for-my-paginated-report"></a>Kan ik een Power BI-gegevensset als een gegevensbron gebruiken voor mijn gepagineerde rapport?

Nog niet, maar deze ondersteuning wordt binnenkort verwacht.

### <a name="can-i-use-stored-procedures-through-the-gateway"></a>Kan ik opgeslagen procedures via de gateway gebruiken?

U kunt een opgeslagen procedure via de gateway gebruiken, maar niet als de opgeslagen procedure parameters bevat.

### <a name="what-export-formats-are-available-for-my-report-in-the-power-bi-service"></a>Welke exportindelingen zijn voor mijn rapport in de Power BI-service beschikbaar?

U kunt exporteren naar Microsoft Excel, Microsoft Word, Microsoft PowerPoint, PDF, CSV, XML en MHTML.

### <a name="can-i-print-paginated-reports"></a>Kan ik gepagineerde rapporten afdrukken?

Momenteel kunt u exporteren naar PDF en het bestand afdrukken. Het rechtstreeks afdrukken van een gepagineerd rapport wordt binnenkort mogelijk. 

### <a name="are-e-mail-subscriptions-available-yet-for-paginated-reports"></a>Zijn er al e-mailabonnementen beschikbaar voor gepagineerde rapporten?

Nee, e-mailabonnementen komen later.

### <a name="what-features-from-ssrs-will-you-be-supporting-in-the-power-bi-service"></a>Welke functies in SSRS worden ondersteund in de Power BI-service?

Het is de bedoeling te zorgen voor een zo goed mogelijke pariteit tussen de twee producten.  Als u bestaande SSRS-patronen passend wilt maken, lijken bepaalde dingen over SSRS en Power BI hierbij geen zin te hebben, zoals de verschillende machtigingsmodellen in Power BI. We willen graag feedback van gebruikers en partners om hierover te kunnen beslissen.

### <a name="can-i-run-custom-code-in-my-report"></a>Kan ik aangepaste code in mijn rapport uitvoeren?

Ja, de mogelijkheid code in uw rapporten uit te voeren, net zoals in SSRS, wordt ondersteund.

### <a name="does-this-mean-ssrs-is-going-away"></a>Betekent dit dat SSRS verdwijnt?

Zeker niet.  Deze nieuwe aanbieding biedt klanten een optie in de cloud voor hun gepagineerde rapporten.  

### <a name="can-i-use-power-bi-embedded-to-embed-my-paginated-reports-into-an-app-im-hosting"></a>Kan ik Power BI Embedded gebruiken voor het insluiten van gepagineerde rapporten in een app die ik zelf host?

Het is de bedoeling dit scenario te ondersteunen met de bestaande Power BI-API's, maar er is nog keen tijdsbestek waarbinnen dit scenario beschikbaar zal zijn.

### <a name="can-i-drill-through-from-a-power-bi-report-to-a-paginated-report"></a>Kan ik vanaf een Power BI-rapport inzoomen op een gepagineerd rapport?

Dat kan nog niet, maar de ondersteuning van dit scenario staat gepland.

### <a name="can-i-share-my-paginated-report-content-through-a-power-bi-app"></a>Kan ik de inhoud van mijn gepagineerde rapport delen via een Power BI-app?

Momenteel kunt u afzonderlijke gepagineerde rapporten delen met andere gebruikers via de actie voor delen in de portal. Het delen via apps wordt nog niet ondersteund, maar dit wordt binnenkort verwacht. Dat geldt ook voor de knop voor delen in de werkbalk.

### <a name="will-other-report-specific-features-in-power-bi-like-pinning-to-report-tiles-to-dashboards-work-with-paginated-reports"></a>Werken andere rapportfuncties in Power BI, zoals het vastmaken aan rapporttegel aan dashboards, met gepagineerde rapporten?

De bedoeling is dat de rapporten dezelfde belangrijke scenario's in de service zoveel mogelijk ondersteunen.  Hoewel het hulpprogramma om de rapporten te ontwerpen verschilt, is het vanuit het standpunt van de gebruiker in het ideale geval gewoon een ander rapport in de lijst in de portal. Voor de gebruikers is het niet van belang hoe het is gemaakt; zij kunnen gewoon doen wat ze moeten doen.  Een goed voorbeeld van deze functiepariteit is de geplande ondersteuning via opmerkingen. Hoewel de functie zelf iets anders werkt voor elk rapporttype, kunt u opmerkingen voor beide gebruiken.

### <a name="are-you-planning-to-create-a-new-authoring-tool-for-paginated-reports-in-the-power-bi-service--we-cant-do-everything-we-need-to-with-report-builder-today"></a>Komt er een nieuw bewerkingsprogramma voor gepagineerde rapporten in de Power BI-service?  Momenteel kunnen we niet alles doen wat we willen met Report Builder.

Er wordt nog naar verschillende opties gekeken, maar er komt ondersteuning voor functies als ALM, aangepaste extensies en andere functies die mogelijk alleen in een van de bewerkingsprogramma's voor SSRS worden opgenomen. 

### <a name="is-a-migration-tool-planned-so-ssrs-customers-can-move-their-existing-reports-and-assets-to-power-bi"></a>Staat er een migratieprogramma gepland, zodat klanten van SSRS hun bestaande rapporten en assets naar Power BI kunnen verplaatsen?

Ja, maar dat komt pas als de belangrijkste set ondersteunde functies in de Power BI-service compleet is.

### <a name="will-i-ever-be-able-to-create-both-paginated-reports-and-power-bi-reports-in-a-single-authoring-tool"></a>Zal het ooit mogelijk zijn zowel gepagineerde rapporten als Power BI-rapporten in één bewerkingsprogramma te maken?

Eén bewerkingsprogramma hiervoor staat niet op de planning, maar er wordt gekeken naar manieren om de bewerkingsprogramma's gezamenlijk als één BI-suite te distribueren of als afzonderlijke downloads/huisstijl.

### <a name="is-there-a-report-viewer-control-for-paginated-reports-in-the-power-bi-service"></a>Is er een besturingselement voor het weergeven van gepagineerde rapporten in de Power BI-service?

Nee, er is momenteel geen besturingselement voor het weergeven van gepagineerde rapporten.

### <a name="can-you-search-for-paginated-reports-from-the-new-home-experience-in-the-power-bi-service"></a>Kan ik naar gepagineerde rapporten zoeken vanaf de nieuwe startpagina in de Power BI-service?

Nee, u kunt momenteel niet vanaf de startpagina naar uw gepagineerde rapporten zoeken.  U kunt ze echter wel zien in de andere onderdelen van de nieuwe startpagina.

## <a name="next-steps"></a>Volgende stappen

- [Report Builder installeren vanuit het Microsoft Downloadcentrum](https://www.microsoft.com/download/details.aspx?id=53613)
- [Tutorial: Create a paginated report](paginated-reports-quickstart-aw.md) (Zelfstudie: een gepagineerd rapport maken)