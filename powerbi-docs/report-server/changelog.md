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
ms.date: 11/17/2017
ms.author: jaimeta
ms.openlocfilehash: e56976943e58aba8c9ef36c576a16ab5eba4c796
ms.sourcegitcommit: 7d4ad2ba92a932d7cc6637348e0774be6623559e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/18/2017
---
# <a name="changelog-for-power-bi-report-server"></a>Wijzigingenlogboek voor Power BI Report Server

Dit is een wijzigingenlogboek voor Power BI Report Server met een overzicht van nieuwe items en oplossingen voor problemen voor elke uitgebrachte build.

Zie [Wat is er nieuw in Power BI Report Server](whats-new.md) voor gedetailleerde informatie over nieuwe functies.

## <a name="october-2017"></a>Oktober 2017

- **Power BI Report Server**
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

## <a name="next-steps"></a>Volgende stappen

[Gebruikershandboek](user-handbook-overview.md)  
[Beheerdershandboek](admin-handbook-overview.md)  
[Snelstartgids: Power BI Report Server installeren](quickstart-install-report-server.md)  
[Report Builder installeren](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder)  
[SQL Server Data Tools (SSDT) downloaden](http://go.microsoft.com/fwlink/?LinkID=616714)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](https://community.powerbi.com/).