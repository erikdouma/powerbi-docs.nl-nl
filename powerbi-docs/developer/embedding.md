---
title: Insluiten met Power BI
description: Power BI biedt API's voor het insluiten van uw dashboards en rapporten in toepassingen.
services: powerbi
documentationcenter: 
author: markingmyname
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 11/30/17
ms.author: mihart
ms.openlocfilehash: 4d112ae4c25f080a3eb90de596c056366da3fe1d
ms.sourcegitcommit: 6e693f9caf98385a2c45890cd0fbf2403f0dbb8a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2018
---
# <a name="embedding-with-power-bi"></a>Insluiten met Power BI
Power BI biedt API's voor het insluiten van uw dashboards en rapporten in toepassingen. De Power BI API's bieden een consistente set mogelijkheden en toegang tot de nieuwste functies van Power BI (zoals dashboards, gateways en app-werkruimten) voor het insluiten van inhoud.

## <a name="a-single-api"></a>Enkele API
Er zijn twee hoofdscenario's voor het insluiten van Power BI-inhoud.  Insluiting voor gebruikers in uw organisatie (die licenties hebben voor Power BI) en insluiting voor uw gebruikers en klanten zonder dat deze Power BI-licenties nodig hebben. U kunt beide scenario’s uitvoeren met de Power BI REST-API. 

Voor klanten en gebruikers zonder een Power Bi-licentie kunt u met dezelfde API dashboards en rapporten insluiten in uw aangepaste toepassing voor zowel uw organisatie als uw klanten. Uw klanten ziende gegevens die door de toepassing worden beheerd. Power BI-gebruikers in uw organisatie hebben aanvullende opties om *hun eigen gegevens* weer te geven, rechtstreeks in Power BI of in de context van de ingesloten toepassing. U kunt profiteren van de JavaScript- en REST-API's voor uw behoeften bij het insluiten van inhoud.

Voor een voorbeeld van hoe het insluiten van inhoud werkt, raadpleegt u het [Insluitvoorbeeld voor JavaScript](https://microsoft.github.io/PowerBI-JavaScript/demo/).

## <a name="embedding-for-your-organization"></a>Inhoud insluiten voor uw organisatie
Met het insluiten van inhoud voor uw organisatie kunt u de Power BI-service uitbreiden. Hiervoor moeten gebruikers van uw toepassing zich aanmelden bij de Power BI-service wanneer deze hun inhoud willen weergeven. Als iemand zich in uw organisatie zich heeft aangemeld, heeft hij alleen toegang tot zijn hun eigen dashboards en rapporten of de dashboards en rapporten die met hem zijn gedeeld in de Power BI-service. 

*Voorbeelden van het insluiten van inhoud voor uw organisatie zijn interne webtoepassingen, het webonderdeel voor SharePoint Online en Microsoft Teams-integratie.*

Zie de volgende scenario's voor informatie over het insluiten van inhoud voor uw organisatie:

* [Een dashboard in een app integreren](integrate-dashboard.md)
* [Een tegel in een app integreren](integrate-tile.md)
* [Een rapport in een app integreren](integrate-report.md)

Mogelijkheden voor selfservice, zoals bewerken, opslaan en meer, zijn beschikbaar via de [JavaScript-API](https://github.com/Microsoft/PowerBI-JavaScript) wanneer u inhoud insluit voor Power BI-gebruikers.

## <a name="embedding-for-your-customers"></a>Inhoud voor uw klanten insluiten
Door inhoud voor uw klanten in te sluiten kunt u dashboards en rapporten insluiten voor gebruikers die geen account voor Power BI hebben. Uw klanten hebben geen voorkennis over Power BI nodig. Er is ten minste een Power BI Pro-account nodig voor het maken van een ingesloten toepassing. Het Power BI Pro-account fungeert als hoofdaccount voor uw toepassing. U kunt dit account zien als een proxyaccount. Met het Power BI Pro-account kunt u ook insluittokens genereren die toegang bieden tot dashboards en rapporten in de Power BI-service die eigendom zijn van of worden beheerd door uw toepassing. 

*Een voorbeeld van het insluiten van inhoud voor uw klanten is een ISV-toepassing die wordt verkocht aan andere bedrijven.*

![Stroom voor het insluiten van inhoud voor uw klanten](media/embedding/powerbi-embed-flow.png)

Als u dashboards, rapporten en tegels wilt insluiten, gebruikt u de API's die u ook zou gebruiken voor het insluiten van inhoud voor uw organisatie.

> [!IMPORTANT]
> Het insluiten is afhankelijk van de Power BI-service, maar uw klanten zijn niet afhankelijk van Power BI. Ze hoeven zich niet aan te melden voor Power BI om de ingesloten inhoud in uw toepassing te bekijken.
> 
> 

Wanneer u klaar bent om tot productie over te gaan, moet uw app-werkruimte worden toegewezen aan een capaciteit. Power BI Embedded, binnen Microsoft Azure, biedt capaciteit voor gebruik met uw toepassingen.

Zie [Power BI-dashboards, -rapporten en -tegels insluiten](embedding-content.md) voor informatie over het insluiten.

Zie [Inhoud migreren van de Power BI Workspace Collections-service in Azure](migrate-from-powerbi-embedded.md) als u de Power BI Workspace Collections-service in Azure gebruikt en op zoek bent naar meer informatie over het migreren van uw inhoud.

## <a name="next-steps"></a>Volgende stappen
[Dashboards, rapporten en tegels van Power BI insluiten](embedding-content.md)  
[Inhoud van de Power BI Embedded-werkruimteverzameling migreren naar Power BI](migrate-from-powerbi-embedded.md)  
[Power BI Premium - wat is het?](../service-premium.md)  
[Git-opslagplaats voor JavaScript-API](https://github.com/Microsoft/PowerBI-JavaScript)  
[Git-opslagplaats voor Power BI C#](https://github.com/Microsoft/PowerBI-CSharp)  
[Voorbeeld van het insluiten van JavaScript](https://microsoft.github.io/PowerBI-JavaScript/demo/)  
[Technisch document over Embedded-analysecapaciteitsplanning](https://aka.ms/pbiewhitepaper)  
[Technisch document over Power BI Premium](https://aka.ms/pbipremiumwhitepaper)  

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

