---
title: Releaseopmerkingen bij Power BI Report Server
description: Dit onderwerp beschrijft de beperkingen en problemen met Power BI Report Server.
services: powerbi
documentationcenter: 
author: guyinacube
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
ms.date: 11/01/2017
ms.author: asaxton
ms.openlocfilehash: ffd0d1ce38a989121225a666ca4aa924df130216
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2017
---
# <a name="power-bi-report-server-release-notes"></a>Releaseopmerkingen bij Power BI Report Server
Dit onderwerp beschrijft de beperkingen en problemen met Power BI Report Server.

Ga naar [On-premises rapportage met Power BI Report Server](https://powerbi.microsoft.com/report-server/) om Power BI Report Server en de geoptimaliseerde versie van Power BI Desktop voor Power BI Report Server te downloaden.

## <a name="october-2017"></a>Oktober 2017
* Ondersteuning voor geïmporteerde gegevens in Power BI-rapporten
* Mogelijkheid om Excel-werkmappen weer te geven in de webportal. Dit wordt gedaan door Office Online Server te configureren.
* Ondersteuning voor de nieuwe visuele tabel- of matrixelementen van Power BI.
* REST-API-ondersteuning

## <a name="june-2017"></a>Juni 2017
* Er zijn geen nieuwe items voor juni 2017.

## <a name="may-2017"></a>Mei 2017
* Power BI-rapporten moeten worden gemaakt met Power BI Desktop, dat is geoptimaliseerd voor de Power BI-rapportserver, om te kunnen werken met de Power BI-rapportserver. U kunt Power BI Desktop downloaden via de downloadkoppeling boven aan deze pagina.
* Power BI-rapporten ondersteunen alleen live-verbindingen met Analysis Services (in tabelvorm of multidimensionaal).
* Er is geen ondersteuning voor visuele R-elementen.

**Probleem en de mogelijke gevolgen voor de klant:** als SQL Server Reporting Services en Power BI Report Server zich op dezelfde computer bevinden en u de installatie van een van beide ongedaan hebt gemaakt, kunt u niet langer verbinding maken via de resterende rapportserver met het configuratiebeheer van de rapportserver.

**Tijdelijke oplossing** U moet, om dit probleem te omzeilen, de volgende bewerkingen uitvoeren wanneer de installatie van een van de servers ongedaan is gemaakt.

1. Start een opdrachtprompt in de beheerdersmodus.
2. Ga naar de map waarin de resterende rapportserver is geïnstalleerd.
   
    *De standaardlocatie voor de Power BI-rapportserver: C:\Program Files\Microsoft Power BI Report Server*
   
    *De standaardlocatie voor SQL Server Reporting Services: C:\Program Files\Microsoft SQL Server Reporting Services*
3. Ga vervolgens naar de volgende map. Dit is *SSRS* of *PBIRS*, afhankelijk van welke server is overgebleven.
4. Ga naar de WMI-map.
5. Voer de volgende opdracht uit:
   
    ```
    regsvr32 /i ReportingServicesWMIProvider.dll
    ```
   
    Als deze wordt weergegeven, kunt u de volgende fout negeren.
   
    ```
    The module "ReportingServicesWMIProvider.dll" was loaded but the entry-point DLLInstall was not found. Make sure that "ReportingServicesWMIProvider.dll" is a valid DLL or OCX file and then try again.
    ```

## <a name="next-steps"></a>Volgende stappen
[Wat is er nieuw in Power BI Report Server](whats-new.md)  
[Gebruikershandboek](user-handbook-overview.md)  
[Beheerdershandboek](admin-handbook-overview.md)  
[Snelstartgids: Power BI Report Server installeren](quickstart-install-report-server.md)  
[Report Builder installeren](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder)  
[SQL Server Data Tools (SSDT) downloaden](http://go.microsoft.com/fwlink/?LinkID=616714)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](https://community.powerbi.com/)

