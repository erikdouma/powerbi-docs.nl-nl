---
title: Hardware- en softwarevereisten voor het installeren van Power BI Report Server
description: Hier worden de minimale hardware- en softwarevereisten voor het installeren en uitvoeren van Power BI Report Server behandeld.
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-report-server
ms.topic: conceptual
ms.date: 06/13/2018
ms.author: maghan
ms.openlocfilehash: c2784bf8e8dca857ae2a1b55d1ad8560e552cafb
ms.sourcegitcommit: 127df71c357127cca1b3caf5684489b19ff61493
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/03/2018
ms.locfileid: "37780553"
---
# <a name="hardware-and-software-requirements-for-installing-power-bi-report-server"></a>Hardware- en softwarevereisten voor het installeren van Power BI Report Server
Hier worden de minimale hardware- en softwarevereisten voor het installeren en uitvoeren van Power BI Report Server behandeld.

## <a name="processor-memory-and-operating-system-requirements"></a>Eisen voor processor, geheugen en besturingssysteem

| Component | Vereiste |
| --- | --- |
| .NET Framework |4.6<br><br>U kunt .NET Framework handmatig installeren vanaf [Microsoft .NET Framework 4.6 (webinstallatie) voor Windows](http://support.microsoft.com/kb/3045560).<br/><br/> Zie de [.NET Framework-implementatiehandleiding voor ontwikkelaars](http://msdn.microsoft.com/library/ee942965\(v=vs.110\).aspx) voor meer informatie, aanbevelingen en richtlijnen met betrekking tot .NET Framework 4.6.<br/><br/>Voor Windows 8.1 en Windows Server 2012 R2 is [KB2919355](http://support.microsoft.com/kb/2919355) vereist voordat u .NET Framework 4.6 installeert. |
| Harde schijf |Voor Power BI Report Server is een minimum van 1 GB aan beschikbare schijfruimte vereist.<br><br>Er is ook ruimte nodig op de databaseserver die als host voor de rapportserverdatabase fungeert. |
| Geheugen |**Minimaal:** 1 GB<br/><br/> **Aanbevolen:** ten minste 4 GB |
| Processorsnelheid |**Minimaal:** x64 processor: 1,4 GHz<br/><br/> **Aanbevolen:** 2,0 GHz of sneller |
| Processortype |x64 processor: AMD Opteron, AMD Athlon 64, Intel Xeon met Intel EM64T-ondersteuning, Intel Pentium IV met EM64T-ondersteuning |
| Besturingssysteem |Windows Server 2016 Datacenter<br><br>Windows Server 2016 Standard<br><br>Windows Server 2012 R2 Datacenter<br><br>Windows Server 2012 R2 Standard<br><br>Windows Server 2012 R2 Essentials<br><br>Windows Server 2012 R2 Foundation<br><br>Windows Server 2012 Datacenter<br><br>Windows Server 2012 Standard<br><br>Windows Server 2012 Essentials<br><br>Windows Server 2012 Foundation<br><br>Windows 10 Home<br><br>Windows 10 Professional<br><br>Windows 10 Enterprise<br><br>Windows 8.1<br><br>Windows 8.1 Pro<br><br>Windows 8.1 Enterprise<br><br>Windows 8<br><br>Windows 8 Pro<br><br>Windows 8 Enterprise |

> [!NOTE]
> Installatie van Power BI Report Server wordt alleen ondersteund op x64-processoren.
> 
> 

## <a name="database-server-version-requirements"></a>Vereisten voor de databaseserver-versie
SQL Server wordt gebruikt om de rapportserverdatabases te hosten. Het exemplaar van SQL Server Database Engine kan een lokaal of extern exemplaar zijn. Hier volgen de ondersteunde versies van SQL Server Database Engine waarop de rapportserverdatabases kunnen worden gehost:

* SQL Server 2017
* SQL Server 2016
* SQL Server 2014
* SQL Server 2012

Als u de rapportserverdatabase op een externe computer wilt maken, moet u de verbinding zo configureren dat een domeingebruikersaccount of een serviceaccount met netwerktoegang wordt gebruikt. Als u een extern exemplaar van SQL Server gebruikt, moet u zorgvuldig overwegen welke referenties de rapportserver moet gebruiken om verbinding te maken met het SQL Server-exemplaar. Zie [De verbinding van een rapportserverdatabase configureren](https://docs.microsoft.com/sql/reporting-services/install-windows/configure-a-report-server-database-connection-ssrs-configuration-manager) voor meer informatie.

## <a name="considerations"></a>Overwegingen
In Power BI Report Server worden standaardwaarden geïnstalleerd om de basisinstellingen te configureren die nodig zijn om de rapportserver operationeel te maken. Hiervoor gelden de volgende vereisten:

* Er moet een SQL Server Database Engine beschikbaar zijn na de installatie en voordat u de database voor de rapportserver configureert. Het exemplaar van de Database Engine fungeert als host voor de rapportserverdatabase die door Reporting Services Configuration Manager wordt gemaakt. De Database Engine is niet vereist voor de werkelijke installatie.
* Het gebruikersaccount waarmee de installatie wordt uitgevoerd, moet lid zijn van de lokale groep Administrators.
* Het gebruikersaccount dat wordt gebruikt voor Reporting Services Configuration Manager, moet machtigingen hebben om databases te openen en te maken op het Database Engine-exemplaar dat als host fungeert voor de rapportserverdatabases.
* Setup moet de standaardwaarden kunnen gebruiken om de URL's te reserveren die toegang bieden tot de rapportserver en de webportal. Deze waarden zijn: poort 80, een sterk jokerteken en de namen van virtuele mappen in de notatie **ReportServer** en **Reports**.

## <a name="read-only-domain-controller-rodc"></a>Alleen-lezen domeincontroller (RODC)
 Terwijl de rapportserver kan worden geïnstalleerd in een omgeving met een alleen-lezen domeincontroller (RODC), is voor juiste werking van Reporting Services toegang tot een domeincontroller voor lezen en schrijven vereist. Als Reporting Services alleen toegang heeft tot een RODC, kunnen fouten optreden bij het beheren van de service.

## <a name="power-bi-reports-and-analysis-services-live-connections"></a>Liveverbindingen van Power BI-rapporten en Analysis Services
U kunt een liveverbinding gebruiken voor tabelvormige of multidimensionale exemplaren. Uw Analysis Services-server moet van de juiste versie en editie zijn.

| **Server-versie** | **Vereiste SKU** |
| --- | --- |
| 2012 SP1 CU4 of hoger |Business Intelligence en Enterprise-SKU |
| 2014 |Business Intelligence en Enterprise-SKU |
| 2016 en later |Standaard SKU of hoger |

## <a name="next-steps"></a>Volgende stappen
[Wat is Power BI Report Server?](get-started.md)  
[Administratoroverzicht](admin-handbook-overview.md)  
[Power BI Report Server installeren](install-report-server.md)  
[Report Builder installeren](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder)  
[SQL Server Data Tools (SSDT) downloaden](http://go.microsoft.com/fwlink/?LinkID=616714)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](https://community.powerbi.com/)

