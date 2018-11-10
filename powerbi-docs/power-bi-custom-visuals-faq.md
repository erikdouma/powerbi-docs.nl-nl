---
title: Veelgestelde vragen over aangepaste Power BI-visuals
description: Hier vindt u een lijst met veelgestelde vragen en antwoorden over aangepaste Power BI-visuals
author: markingmyname
ms.author: maghan
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 10/29/2018
LocalizationGroup: Visualizations
ms.openlocfilehash: 064d32944f52f6e391d4a7ec4df41ecbf09b7e3f
ms.sourcegitcommit: 02f918a4f27625b6f4e47473193ebc8219db40e2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/07/2018
ms.locfileid: "51223071"
---
# <a name="frequently-asked-questions-about-power-bi-custom-visuals"></a>Veelgestelde vragen over aangepaste Power BI-visuals

## <a name="organizational-custom-visuals"></a>Aangepaste visuals van organisaties

**Hoe kan de beheerder de aangepaste visuals van organisaties beheren?**

In de beheerportal, op het tabblad Aangepaste visuals van bedrijven, kan de beheerder [alle aangepaste visuals van bedrijven van het bedrijf zien en beheren](https://docs.microsoft.com/power-bi/service-admin-portal#organization-visuals): toevoegen, uitschakelen, inschakelen en verwijderen.
Het is niet meer nodig om die visuals via e-mail of gedeelde mappen te delen. Nadat de visuals in de opslagplaats van de organisatie zijn geïmplementeerd, kunnen gebruikers in de organisatie de visuals eenvoudig vinden en de aangepaste visuals voor organisaties direct vanuit Power BI Desktop of de Power BI-service in hun rapporten importeren. De aangepaste visuals van organisaties kunnen worden gevonden in de ingebouwde opslag (in desktop en service), op het tabblad Mijn organisatie. Nadat de beheerder een nieuwe versie van een aangepaste visual van bedrijven heeft geüpload, ontvangt iedereen in de organisatie dezelfde bijgewerkte versie. Rapportauteurs hoeven de visual niet uit hun rapport te verwijderen om de nieuwe versie van deze visuals te ontvangen, omdat alle rapporten met deze visual automatisch worden bijgewerkt. Het updatemechanisme is vergelijkbaar met visuals uit de narketplace.

**Als een beheerder een aangepaste visual uploadt vanuit de openbare marketplace naar een zakelijke opslag, wordt de visual dan automatisch bijgewerkt nadat een leverancier de visual in de openbare marketplace heeft bijgewerkt?**

Nee, er zijn geen automatische updates vanuit de openbare marketplace.
Het is de verantwoordelijkheid van de organisatie om de versie die zij hebben, desgewenst bij te werken.

**Is er een manier om de zakelijke opslag uit te schakelen?**

Nee, gebruikers kunnen het tabblad Mijn organisatie altijd zien in Power BI Desktop en de Power BI-service. Beheerders kunnen alle aangepaste visuals van organisaties uitschakelen of verwijderen vanuit de beheerportal en de zakelijke opslag leegmaken.
  
**Als de beheerder aangepaste visuals vanuit de beheerportal (tenantinstellingen) uitschakelt, hebben gebruikers dan nog steeds toegang tot de aangepaste visuals van organisaties?**

Ja, als de beheerder de aangepaste visuals vanuit de beheerportal uitschakelt, heeft dat geen invloed op de zakelijke opslag. Sommige organisaties schakelen aangepaste visuals uit en schakelen alleen geselecteerde visuals in die door de Power BI-beheerder zijn geïmporteerd en geüpload naar de zakelijke opslag. Aangepaste visuals uitschakelen vanuit de beheerportal is niet mogelijk in Power BI Desktop. Desktop-gebruikers kunnen nog steeds aangepaste visuals in hun rapporten gebruiken en toevoegen vanuit de openbare marketplace. Die openbare aangepaste visuals worden echter niet meer weergegeven nadat ze zijn gepubliceerd naar de Power BI-service en geven vervolgens een bijbehorende foutmelding. Wanneer u de Power BI-service gebruikt, kunt u aangepaste visuals niet importeren vanuit de openbare marketplace. Alleen visuals uit de zakelijke opslag kunnen worden geïmporteerd, aangezien de instelling van aangepaste visuals in de beheerportal wordt geregeld via de Power BI-service.

**Waarom zijn de zakelijke opslag en aangepaste visuals van organisaties een effectieve oplossing voor bedrijven?**

* Iedereen krijgt dezelfde versie van de visual. De versie wordt beheerd door de Power BI-beheerder. Wanneer de beheerder de versie van de visual bijwerkt in de beheerportal, krijgen alle gebruikers in de organisatie automatisch de bijgewerkte versie.

* Het is niet meer nodig om bestanden van visuals via e-mail of gedeelde mappen te delen. Voortaan is er één plek die zichtbaar is voor alle leden die zijn aangemeld.

* Beveiliging en ondersteuning: nieuwe versies van aangepaste visuals van organisaties worden automatisch in alle rapporten bijgewerkt, net als visuals uit de marketplace.

* Gebruikers in de organisatie die de aangepaste visuals van de organisatie gebruiken, moeten zijn aangemeld om de aangepaste visuals van organisaties te zien en te gebruiken, omdat die visuals een beveiligingselement zijn voor organisaties.

* Beheerders kunnen bepalen welke aangepaste visuals er beschikbaar zijn binnen de organisatie.

* Beheerders kunnen visuals inschakelen/uitschakelen vanuit de beheerportal, zodat deze kunnen worden getest. Zo wordt beveiliging beter afgedwongen, aangezien die visuals alleen toegankelijk zijn voor leden van de organisatie.

## <a name="certified-custom-visuals"></a>Gecertificeerde aangepaste visuals

**Wat zijn gecertificeerde aangepaste visuals?**

Gecertificeerde aangepaste visuals zijn visuals in de [marketplace](https://appsource.microsoft.com/marketplace/apps?page=1&product=power-bi-visuals) die voldoen aan bepaalde [opgegeven](power-bi-custom-visuals-certified.md) codevereisten en tests van het Power BI-team.  De tests die zijn uitgevoerd, zijn ontworpen om te controleren of de visual geen gebruik maakt van externe services of resources. Microsoft is echter niet de auteur van externe aangepaste visuals; we raden klanten dan ook aan om rechtstreeks met de auteur op te nemen om de functionaliteit van een dergelijke visual te verifiëren.

## <a name="next-steps"></a>Volgende stappen

Ga naar [Problemen met aangepaste visuals voor Power BI oplossen](power-bi-custom-visuals-troubleshoot.md) voor informatie over het oplossen van problemen.
