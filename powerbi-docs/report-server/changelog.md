---
title: Wijzigingenlogboek voor Power BI Report Server
description: Dit is een wijzigingenlogboek voor Power BI Report Server met een overzicht van nieuwe items en oplossingen voor problemen voor elke uitgebrachte build.
ms.author: jtarquino
author: jtarquino
manager: kfile
ms.reviewer: maggies
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: conceptual
ms.date: 03/31/2018
ms.openlocfilehash: 9589c2cf5277995459a9f43f573b6e19c4c8f748
ms.sourcegitcommit: e9c45d6d983e8cd4cb5af938f838968db35be0ee
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2019
ms.locfileid: "57327959"
---
# <a name="changelog-for-power-bi-report-server"></a>Wijzigingenlogboek voor Power BI Report Server

Dit is een wijzigingenlogboek voor Power BI Report Server met een overzicht van nieuwe items en oplossingen voor problemen voor elke uitgebrachte build.

Zie [Wat is er nieuw in Power BI Report Server](whats-new.md) voor gedetailleerde informatie over nieuwe functies. 

## <a name="january-2019"></a>Januari 2019

- **Power BI Report Server**            
    - *Versie 1.4.6969.7395 (build 15.0.1102.235), uitgebracht: 30 januari 2019*
        - Opgeloste fouten
            - Power BI-rapporten
                - Oplossing voor een probleem met de basisreferenties bij het gebruik van DirectQuery
                - Oplossing voor toegepaste filters bij bidirectionele relaties met beveiliging op rijniveau
                - Oplossing voor verlopen gegevens na het vernieuwen van een model in een uitgeschaalde omgeving
                - Oplossing voor dubbele scrollbalk voor tabel/matrix in Firefox 63+
                - Oplossing voor pictogramgrootte +/- in Internet Explorer
            - Gepagineerde rapporten
                - Oplossing voor probleem bij het gebruik van een gedeelde gegevensbron voor een rapport

    - *Versie 1.4.6960.38798 (build 15.0.1102.222), uitgebracht: 22 januari, 2019*
        - Functies
            - Power BI-rapporten 
                - Ondersteuning voor beveiliging op rijniveau
                - Uitvouwen of samenvouwen op rijkoppen van matrix
                - Kopiëren en plakken tussen .pbix-bestanden
                - Slimme uitlijningshulplijnen
                - Ondersteuning voor SAP BW 2.0-connector
            - Beheerders
                - Mogelijkheid om extensies van resources te beperken die kunnen worden geüpload naar de rapportserver
                - Mogelijkheid om ondersteunde hyperlinkschema's te beperken
            - Programmeerbaarheid
                - Nieuwe Web-API: /PowerBIReports({Id})/DataModelRoles (GET)
                - Nieuwe Web-API: /PowerBIReports({Id})/DataModelRoleAssignments (GET & PUT)
                - Zie [REST-API voor Power BI Report Server](https://app.swaggerhub.com/apis/microsoft-rs/PBIRS/2.0) voor meer informatie
        - Opgeloste fouten
            - Beveiligingsprobleem met HTML-injectie
            - Exporteren naar PDF geeft geen euroteken weer
            - Door het opslaan van een wachtwoord met meerdere gegevensbronnen in Power BI-rapporten worden niet-gewijzigde wachtwoorden ongeldig
            - Visuele elementen geven problemen weer in Mobiele Power BI-app na inactiviteit

- **Power BI Report (geoptimaliseerd voor Power BI Report Server)**
    - *Versie: 2.65.5313.1562 (januari 2019), uitgebracht: 30 januari 2019*
        - Snelkoppeling en vastgemaakte pictogrammen blijven bestaan na het verwijderen van Power BI Report Server
        - Oplossing voor probleem waarbij het vastmaken van Power BI Report Server aan het startmenu leidt tot zwarte tekst op een zwart pictogram

    - *Versie: 2.65.5313.1421 (januari 2019), uitgebracht: 22 januari, 2019*
        - Bevat de vereiste wijzigingen om verbinding te maken met Power BI Report Server (januari 2019)  

## <a name="august-2018"></a>Augustus 2018

- **Power BI Report Server**
    - *Versie 1.3.6816.37243 (build 15.0.2.557), uitgebracht: 30 augustus 2018*
        - Opgeloste fouten
            - Er is een probleem opgelost waarbij na het upgraden van een eerdere versie van PBI-rapportserver waarbij een bindingsomleiding niet werd bijgewerkt, klanten het volgende zagen:      
            *`
            Failed to load expression host assembly. Details: Could not load file or assembly 'Microsoft.ReportingServices.ProcessingObjectModel, Version=2018.7.0.0, Culture=neutral, PublicKeyToken=89845dcd8080cc91' or one of its dependencies. The located assembly's manifest definition does not match the assembly reference. (Exception from HRESULT: 0x80131040) (rsErrorLoadingExprHostAssembly)
             `*
             
            - Fout voor transparantie van gegevenslabel is nu opgelost.
            
    - *Versie 1.3.6801.38816 (build 15.0.2.540), uitgebracht: 15 augustus 2018*
        - Functies
            - SAP HANA SSO DirectQuery-ondersteuning met Kerberos is nu beschikbaar voor Power BI-rapporten
            - Aangepaste API voor visuals beschikbaar bij de release - versie 1.13.0
            - Er wordt een oudere versie van de functie voor aangepaste visuals geïntroduceerd die compatibel is met de huidige versie van de server-API (indien beschikbaar)

- **Power BI Report (geoptimaliseerd voor Power BI Report Server)**
    - *Versie: 2.61.5192.641 (augustus 2018), uitgebracht: 15 augustus 2018*
        - Bevat de vereiste wijzigingen om verbinding te maken met Power BI Report Server (augustus 2018)         
        
## <a name="march-2018"></a>Maart 2018

- **Power BI Report Server**
    - *Versie 1.2.6690.34729 (build 15.0.2.402), uitgebracht: 27 april 2018*
        - Opgeloste fouten
            - Migratie van SQL Server Reporting Services 2017-catalogussen inschakelen
            - Voor Power BI-rapporten (PBIX)
                - Rapporten kunnen worden vernieuwd wanneer een server is geconfigureerd om aangepaste verificatie te gebruiken
                - De gegevensbronreferenties worden niet opnieuw ingesteld door de eigenschappen van een rapport te wijzigen
            - Voor Gepagineerde rapporten (RDL)
                - Het gebruik van `Lookup()` of afgeleide functies zoals `LookupSet()` en `MultiLookup()` in RDL-expressies heeft niet meer dit resultaat: `#Error`
                - Gekoppelde rapporten worden tijdens het afdrukken aangepast aan de paginagrootte van het doelrapport
                - Abonnementen kunnen worden gemaakt voor gekoppelde rapporten die gebruikmaken van trapsgewijze parameters
                - Standaardparameters voor meerdere waarden kunnen worden gewijzigd wanneer u IE11 gebruikt
                - Gegevensgestuurde bezorgingsopties voor abonnementen kunnen worden bewerkt
                - Abonnementen kunnen worden bekeken en bewerkt terwijl het abonnement wordt uitgevoerd
                - Verbindingsreeksen op basis van expressies worden niet verwijderd door de gegevensbronreferenties in te stellen
            - Voor KPI's
                - Trendregels worden vernieuwd wanneer de gegevens worden bijgewerkt
            - Algemene verbeteringen in de stabiliteit

    - *Versie 1.2.6660.39920 (build 15.0.2.389), uitgebracht: 28 maart 2018*
        - Opgeloste fouten
            - Voor Power BI-rapporten (PBIX) werkt de oplossing voor het exporteren van gegevens niet vanuit Power BI Visuals
            - Voor Power BI-rapporten (PBIX) werkt de oplossing voor het herstellen van URL-filters niet
            - Voor gepagineerde rapporten (RDL), wordt de oplossing voor het weergeven van installatiekopieën niet juist weergegeven in IE11 na de upgrade naar de maart-release van Power BI Report Server

    - *Versie 1.2.6648.38132 (build 15.0.2.378), uitgebracht: 19 maart 2018*
        - Beveiligingsupdates
        - Verbeterde toegankelijkheid
        - Opgeloste fouten
            - Er is voor gepagineerde rapporten (RDL) een fout opgelost, waarbij de zichtbaarheid van de parameters in een gekoppeld rapport werd teruggedraaid nadat de eigenschappen ervan waren bewerkt
            - Voor de webportal is een fout opgelost voor de verificatie van aangepaste formulieren, waarbij de cookie voor een verschuivende verloopdatum werd genegeerd
            - Er is een fout opgelost voor het exporteren naar Word, waarbij een ongelijke rijhoogte werd gemaakt als de inhoud van de rij leeg was
            - Er is voor gepagineerde rapporten (RDL) een fout opgelost, waarbij een verbindingsreeks die is gebaseerd op een expressie werd verwijderd wanneer de referenties voor de gegevensbron werden gewijzigd
            - Er is een fout opgelost zodat KPI kan worden gebruikt met tekstwaarden
            - Er is voor gepagineerde rapporten (RDL) een fout opgelost, zodat een nieuwe gegevensset kan worden toegewezen aan een bestaand gepagineerd rapport (RDL)
            - Andere foutoplossingen met betrekking tot de stabiliteit en het gebruik

- **Power BI Report (geoptimaliseerd voor Power BI Report Server)**
    - Versie: 2.56.5023.1043 (maart 2018), uitgebracht: 19 maart 2018
        - Bevat de vereiste wijzigingen om verbinding te maken met Power BI Report Server (maart 2018)

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
    - *Versie: 2.51.4885.3981 (oktober 2017), uitgebracht: 10 april 2018*
        - Beveiligingsupdates

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

    - *Build 14.0.600.305, uitgebracht: 19 september 2017*  
        - Opgeloste fouten
            - Update naar de nieuwste [webbesturingselement voor Bing Kaarten](https://msdn.microsoft.com/library/mt712542.aspx)

    - *Build 14.0.600.301, uitgebracht: 11 juli 2017*
        - Opgeloste fouten
            - De tag `{{UserId}}` wordt omgezet in de opgeslagen referenties in plaats van dat de gebruiker het rapport uitvoert in Power BI-rapporten
            - Sommige afbeeldingen worden niet weergegeven in Power BI Report Server-rapporten.
            - De naam van een Power BI-rapport in Power BI Report Server kan niet worden gewijzigd.
            - Kan geen aangepaste visuals in de mobiele Power BI-app laden (de mobiele app moet opnieuw worden geïnstalleerd om de lokale cache te wissen).

    - *Build 14.0.600.271, uitgebracht: 12 juni 2017*
        - Eerste release van Power BI Report Server

- **Power BI Report (geoptimaliseerd voor Power BI Report Server)**
    - *Versie: 2.47.4766.4901 (juni 2017), uitgebracht: 10 januari 2018*
        - Beveiligingsupdates

## <a name="next-steps"></a>Volgende stappen

[Wat is Power BI Report Server?](get-started.md)
[Administratoroverzicht](admin-handbook-overview.md)  
[Power BI Report Server installeren](install-report-server.md)  
[Report Builder downloaden](https://www.microsoft.com/download/details.aspx?id=53613)  
[SQL Server Data Tools (SSDT) downloaden](http://go.microsoft.com/fwlink/?LinkID=616714)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](https://community.powerbi.com/)
