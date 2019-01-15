---
title: Veelgestelde vragen over aangepaste Power BI-visuals
description: Hier vindt u een lijst met veelgestelde vragen en antwoorden over aangepaste Power BI-visuals
author: markingmyname
ms.author: maghan
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: conceptual
ms.custom: ''
ms.date: 12/17/2018
ms.openlocfilehash: 0418016fd7a194ff2e37e979219b97e94520f9ae
ms.sourcegitcommit: c8c126c1b2ab4527a16a4fb8f5208e0f7fa5ff5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2019
ms.locfileid: "54282098"
---
# <a name="frequently-asked-questions-about-power-bi-custom-visuals"></a>Veelgestelde vragen over aangepaste Power BI-visuals

## <a name="organizational-custom-visuals"></a>Aangepaste visuals van organisaties

### <a name="how-can-the-admin-manage-the-organizational-custom-visuals"></a>Hoe kan de beheerder de aangepaste visuals van organisaties beheren?

In de beheerportal, op het tabblad Aangepaste visuals van bedrijven, kan de beheerder [alle aangepaste visuals van bedrijven van het bedrijf zien en beheren](https://docs.microsoft.com/power-bi/service-admin-portal#organization-visuals): toevoegen, uitschakelen, inschakelen en verwijderen.
Het is niet meer nodig om die visuals via e-mail of gedeelde mappen te delen. Nadat de visuals in de opslagplaats van de organisatie zijn geïmplementeerd, kunnen gebruikers in de organisatie de visuals eenvoudig vinden en de aangepaste visuals voor organisaties direct vanuit Power BI Desktop of de Power BI-service in hun rapporten importeren. De aangepaste visuals van organisaties bevinden zich in de ingebouwde opslag (in desktop en service), op het tabblad *Mijn organisatie*. Nadat de beheerder een nieuwe versie van een aangepaste visual van bedrijven heeft geüpload, ontvangt iedereen in de organisatie dezelfde bijgewerkte versie. Rapportauteurs hoeven de visual niet uit hun rapport te verwijderen om de nieuwe versie van deze visuals te ontvangen, omdat alle rapporten met deze visual automatisch worden bijgewerkt. Het updatemechanisme is vergelijkbaar met visuals uit de narketplace.

### <a name="if-an-admin-uploads-a-custom-visual-from-the-public-marketplace-to-the-organization-store-is-it-automatically-updated-once-a-vendor-updates-the-visual-in-the-public-marketplace"></a>Als een beheerder een aangepaste visual uploadt vanuit de openbare marketplace naar een zakelijke opslag, wordt de visual dan automatisch bijgewerkt nadat een leverancier de visual in de openbare marketplace heeft bijgewerkt?

Nee, er zijn geen automatische updates vanuit de openbare marketplace.
Het is de verantwoordelijkheid van de beheerder om de versie van de organisatie desgewenst bij te werken.

### <a name="is-there-a-way-to-disable-the-organizational-store"></a>Is er een manier om de zakelijke opslag uit te schakelen?

Nee, gebruikers kunnen het tabblad Mijn organisatie altijd zien in Power BI Desktop en de Power BI-service. Beheerders kunnen alle aangepaste visuals van organisaties uitschakelen of verwijderen vanuit de beheerportal en de zakelijke opslag leegmaken.
  
### <a name="if-the-administrator-disables-custom-visuals-from-the-admin-portal-tenant-settings-do-users-still-have-access-to-the-organizational-custom-visuals"></a>Als de beheerder aangepaste visuals vanuit de beheerportal (tenantinstellingen) uitschakelt, hebben gebruikers dan nog steeds toegang tot de aangepaste visuals van organisaties?

Ja, als de beheerder de aangepaste visuals vanuit de beheerportal uitschakelt, heeft dat geen invloed op de zakelijke opslag. Sommige organisaties schakelen aangepaste visuals uit en schakelen alleen geselecteerde visuals in die door de Power BI-beheerder zijn geïmporteerd en geüpload naar de zakelijke opslag. Aangepaste visuals uitschakelen vanuit de beheerportal is niet mogelijk in Power BI Desktop. Desktop-gebruikers kunnen nog steeds aangepaste visuals in hun rapporten gebruiken en toevoegen vanuit de openbare marketplace. Die openbare aangepaste visuals worden echter niet meer weergegeven nadat ze zijn gepubliceerd naar de Power BI-service en geven vervolgens een bijbehorende foutmelding. Wanneer u de Power BI-service gebruikt, kunt u aangepaste visuals niet importeren vanuit de openbare marketplace. Alleen visuals uit de zakelijke opslag kunnen worden geïmporteerd, aangezien de instelling van aangepaste visuals in de beheerportal wordt geregeld via de Power BI-service.

### <a name="why-does-the-organizational-store-and-organizational-custom-visuals-make-a-great-enterprise-solution"></a>Waarom zijn de zakelijke opslag en aangepaste visuals van organisaties een effectieve oplossing voor bedrijven?

* Iedereen krijgt dezelfde versie van de visual. De versie wordt beheerd door de Power BI-beheerder. Wanneer de beheerder de versie van de visual bijwerkt in de beheerportal, krijgen alle gebruikers in de organisatie automatisch de bijgewerkte versie.

* Het is niet meer nodig om bestanden van visuals via e-mail of gedeelde mappen te delen. Voortaan is er één plek die zichtbaar is voor alle leden die zijn aangemeld.

* Beveiliging en ondersteuning: nieuwe versies van aangepaste visuals van organisaties worden automatisch in alle rapporten bijgewerkt, net als visuals uit de marketplace.

* Gebruikers in de organisatie die de aangepaste visuals van de organisatie gebruiken, moeten zijn aangemeld om de aangepaste visuals van organisaties te zien en te gebruiken, omdat die visuals een beveiligingselement zijn voor organisaties.

* Beheerders kunnen bepalen welke aangepaste visuals er beschikbaar zijn binnen de organisatie.

* Beheerders kunnen visuals inschakelen/uitschakelen vanuit de beheerportal, zodat deze kunnen worden getest. Zo wordt beveiliging beter afgedwongen, aangezien die visuals alleen toegankelijk zijn voor leden van de organisatie.

## <a name="certified-custom-visuals"></a>Gecertificeerde aangepaste visuals

### <a name="what-are-certified-custom-visuals"></a>Wat zijn gecertificeerde aangepaste visuals?

Gecertificeerde aangepaste visuals zijn visuals in de [marketplace](https://appsource.microsoft.com/marketplace/apps?page=1&product=power-bi-visuals) die voldoen aan bepaalde [opgegeven](power-bi-custom-visuals-certified.md) codevereisten en tests van het Power BI-team.  De testen die worden uitgevoerd, zijn ontworpen om te controleren of de visual geen toegang heeft tot externe services of resources. Microsoft is echter niet de auteur van aangepaste visuals van derden. Klanten wordt aangeraden om rechtstreeks contact op te nemen met de auteur om de functionaliteit van dergelijke visuals te controleren.

## <a name="visuals-with-additional-purchases"></a>Visuals met aanvullende aankopen

### <a name="what-is-a-visual-with-additional-purchases"></a>Wat is een visual met aanvullende aankopen?

Aanvullende aankopen voor visuals zijn vergelijkbaar met invoegtoepassingen voor aankopen in apps (IAP) in de marketplace. Deze invoegtoepassingen zijn voorzien van het prijslabel  **Er kan een aanvullende aankoop vereist zijn**.

Aangepaste IAP-visuals zijn gratis te downloaden. Gebruikers betalen niets voor het downloaden van de aangepaste visuals uit de marketplace. IAP-visuals bieden optionele aankopen in de app om te kunnen profiteren van geavanceerde functies.  

### <a name="whats-the-benefit-to-developers"></a>Wat is het voordeel voor ontwikkelaars?

Aangepaste IAP-visuals in AppSource zijn door de vele dagelijkse bezoekers te ontdekken. Dit leidt tot waardevol verkeer en meer bekendheid voor uw aangepaste IAP-visuals én voor u als ontwikkelaar.

Als u tot recent de visuals beheerde via uw website, kunt u ze nu indienen bij AppSource. Dit maakt de IAP-visuals beter zichtbaar en beter te ontdekken in de Power BI-community.

Bij aangepaste IAP-visuals in AppSource profiteert u van rechtstreekse feedback van de klanten die ze gebruiken. U ontvangt deze feedback aan de hand van reviews en beoordelingen in de Store.  

Zodra een IAP-visual is goedgekeurd door het AppSource-validatieteam kunt u ze indienen voor certificering. Dit is optioneel.  

Wanneer de visual is gecertificeerd, kunnen aangepaste IAP-visuals worden geëxporteerd naar PowerPoint en worden weergegeven in de e-mailberichten die gebruikers ontvangen wanneer deze zich op rapportpagina's abonneren. Als u op dit moment dus IAP-visuals indient bij de marketplace, kunt u ze ook laten certificeren en profiteert u van extra functies.  

### <a name="do-iap-visuals-need-to-be-certified"></a>Moeten IAP-visuals worden gecertificeerd?

Het certificeringsproces is optioneel. Het is aan de ontwikkelaar om te bepalen of deze zijn of haar aangepaste IAP-visuals wil laten certificeren, net als bij gratis visuals.

### <a name="what-is-changing-in-the-submission-process"></a>Hoe verandert het indieningsproces?

Het indieningsproces voor aangepaste IAP-visuals uit de marketplace is hetzelfde als voor gratis visuals. Dit gebeurt via het verkopersdashboard.  Het enige verschil in het indieningsproces is dat ontwikkelaars in de ontwikkelaarsopmerkingen in het verkopersdashboard het volgende moeten opgeven: 'Visual met aankopen in de app'. U moet indien nodig ook een licentiesleutel/-token opgeven voor het valideren van de betaalde/geavanceerde functies.  

Er wordt geen nieuwe optie beschikbaar in het verkopersdashboard naast *gratis met aankopen in de app*. U moet uw IAP-visuals indienen als zijnde *gratis*.

Laat daarnaast gebruikers precies weten wat ze kunnen verwachten. Geef hiervoor een lange beschrijving in de Store op met informatie over welke functies gratis zijn en voor welke functies moet worden betaald.  

### <a name="what-should-i-do-beforesubmittingmy-iap-custom-visual"></a>Wat moet ik doen voordat ik mijn aangepaste IAP-visual indien?

Als u aan een aangepaste IAP-visual werkt of als u er al een hebt, zorgt u ervoor dat deze aan de richtlijnen voldoet.  

Als u een logo in de aangepaste visual gebruikt, zorgt u ervoor dat deze aan de richtlijnen voor logo's voldoet (kleur, plaatsing, grootte en actietriggers).

In de richtlijnen staan ook aanbevolen procedures.  

### <a name="can-i-get-my-iap-custom-visual-certified"></a>Kan ik mijn aangepaste IAP-visual laten certificeren?

Ja, net als gratis visuals.  Zodra uw aangepaste IAP-visual is goedgekeurd door het AppSource-team kunt u uw visual indienen voor certificering.

Als u uw visual wilt laten certificeren, moet deze voldoen aan de certificeringsvereisten. De visual mag bijvoorbeeld toegang hebben tot externe services voor het valideren van licenties.

Certificeren is optioneel. Het is aan u om te beslissen of u uw IAP-visual wilt laten certificeren.

## <a name="additional-questions"></a>Aanvullende vragen

### <a name="how-to-get-support"></a>Ondersteuning verkrijgen

U kunt in de volgende gevallen contact opnemen met het ondersteuningsteam voor aangepaste visuals: *pbicvsupport@microsoft.com* bij vragen, opmerkingen of problemen.  

## <a name="next-steps"></a>Volgende stappen

Ga naar [Problemen met aangepaste visuals voor Power BI oplossen](power-bi-custom-visuals-troubleshoot.md) voor meer informatie.
