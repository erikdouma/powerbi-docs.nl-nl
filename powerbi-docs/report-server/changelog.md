---
title: Wijzigingenlogboek voor Power BI Report Server
description: Dit is een wijzigingenlogboek voor Power BI Report Server met een overzicht van nieuwe items en oplossingen voor problemen voor elke uitgebrachte build.
services: powerbi
documentationcenter: 
author: jtarquino
manager: jonhp
backup: maggies
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 12/11/2017
ms.author: tankas
ms.openlocfilehash: deff79bba0f7f191a8343629300c725f3150e509
ms.sourcegitcommit: a44c29bbc220ecb1ed80810cb1e7df0db8ea611a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/12/2018
---
# <a name="changelog-for-power-bi-report-server"></a>Wijzigingenlogboek voor Power BI Report Server

Dit is een wijzigingenlogboek voor Power BI Report Server met een overzicht van nieuwe items en oplossingen voor problemen voor elke uitgebrachte build.

Zie [Wat is er nieuw in Power BI Report Server](whats-new.md) voor gedetailleerde informatie over nieuwe functies.

## <a name="october-2017"></a>Oktober 2017

- **Power BI Report Server**
    - *Versie 1.1.6582.41691 (build 14.0.600.442), uitgebracht: 10 januari 2018*
        - Beveiligingsupdates
        - Opgeloste fouten
            - Oplossing voor Model.GetParameters met 400 geretourneerd
            - Oplossing voor het instellen van gedeelde gegevensset voor bestaande gepagineerde rapporten (RDL)
            - Oplossing voor ExecutionNotFoundException wanneer het rapport met andere parameterwaarden naar PDF wordt geëxporteerd

    - *Versie 1.1.6551.5155 (build 14.0.600.438), uitgebracht: 11 december 2017*
        - Opgeloste fouten
            - Fout bij opslaan van gegevens na het vernieuwen van bepaalde Power BI Desktop-rapporten.

    - *Versie 1.1.6530.30789 (build 14.0.600.437), uitgebracht: 17 november 2017*
        - Opgeloste fouten
            - Oplossing voor basisverificatiescenario's. 
            - Oplossing voor het probleem met niet-selecteerbare weekdagen op de planningspagina voor abonnementen, in cachevernieuwingsplannen en voor momentopnamen van rapportgeschiedenis op de portal.
            - Oplossing voor het probleem met gepagineerde rapporten (RDL) waarbij expressies in het tekstvak waarvoor de CanGrow-eigenschap is ingesteld op false (onwaar), resulteren in waarden zonder kleur en lettertypen die niet goed worden weergegeven.
            - Oplossing voor het probleem met Power BI rapporten (PBIX) waarbij het toevoegen van legenda's aan een lijndiagram resulteert in een lege visual.

    - *Versie 1.1.6514.9163 (build 14.0.600.434), uitgebracht: 1 november 2017*
        - Opgeloste fouten
            - Oplossing voor problemen met de uploadbetrouwbaarheid van PBIX-rapporten van meer dan 500 MB.
            - Oplossing voor het probleem met het laden van PBIX-rapporten van meer dan 1 GB

    - *Versie 1.1.6513.3500 (build 14.0.600.433), uitgebracht: 31 oktober 2017*
        - Functies
            - Ondersteuning voor ingesloten gegevensmodellen
            - Weergeven van Excel-werkmappen (met Office Online Server-integratie ingeschakeld)
            - Geplande gegevensvernieuwing
            - Ondersteuning van DirectQuery
            - Ondersteuning voor grote bestanden (tot 2 GB)
            - Openbare REST API
            - Ondersteuning voor gedeelde gegevenssets in Power BI Desktop (oData)
            - Ondersteuning voor URL-parameters voor PBIX-bestanden
            - Verbeterde toegankelijkheid

- **Power BI Report (geoptimaliseerd voor Power BI Report Server)**
    - *Versie: 2.51.4885.2501 (oktober 2017), uitgebracht: 10 januari 2018*
        - Beveiligingsupdates

    - *Versie: 2.51.4885.1423 (oktober 2017), uitgebracht: 17 november 2017*
        - Opgeloste fouten
            - Oplossing voor het probleem dat de 32-bits versie van Power BI Desktop niet kan worden uitgevoerd op x86-besturingssystemen.
            - Oplossing voor het probleem met de weergave van x-asrasterlijnen in Power BI Reports (PBIX).
            - Overige kleine correcties

    - *Versie: 2.51.4885.1041 (oktober 2017), uitgebracht: 31 oktober 2017*
        - Functies
            - Bevat de vereiste wijzigingen om verbinding te maken met Power BI Report Server (oktober 2017)

## <a name="june-2017"></a>Juni 2017

- **Power BI Report Server**
    - *Build 14.0.600.309, uitgebracht: 10 januari 2018*
        - Beveiligingsupdates

    - *Build 14.0.600.305, uitgebracht: 19 September 2017*  
        - Opgeloste fouten
            - Update naar de nieuwste [webbesturingselement voor Bing Kaarten](https://msdn.microsoft.com/library/mt712542.aspx)

    - *Build 14.0.600.301, uitgebracht: 11 juli 2017*
        - Opgeloste fouten
            - De tag {{UserId}} in Power BI-rapporten wordt omgezet in de opgeslagen referenties in plaats dat de gebruiker het rapport uitvoert.
            - Sommige afbeeldingen worden niet weergegeven in Power BI Report Server-rapporten.
            - De naam van een Power BI-rapport in Power BI Report Server kan niet worden gewijzigd.
            - Kan geen aangepaste visuals in de mobiele Power BI-app laden (de mobiele app moet opnieuw worden geïnstalleerd om de lokale cache te wissen).

    - *Build 14.0.600.271, uitgebracht: 12 juni 2017*
        - Eerste release van Power BI Report Server

- **Power BI Report (geoptimaliseerd voor Power BI Report Server)**
    - *Versie: 2.47.4766.4901 (juni 2017), uitgebracht: 10 januari 2018*
        - Beveiligingsupdates

## <a name="next-steps"></a>Volgende stappen

[Gebruikershandboek](user-handbook-overview.md)  
[Beheerdershandboek](admin-handbook-overview.md)  
[Snelstartgids: Power BI Report Server installeren](quickstart-install-report-server.md)  
[Report Builder installeren](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder)  
[SQL Server Data Tools (SSDT) downloaden](http://go.microsoft.com/fwlink/?LinkID=616714)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](https://community.powerbi.com/)