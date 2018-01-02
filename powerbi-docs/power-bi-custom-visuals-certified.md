---
title: Gecertificeerde visualisaties in Power BI
description: Vereisten en proces voor het indienen van een aangepast visueel element voor certificering. En een lijst met al gecertificeerde aangepaste visuele elementen.
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 11/20/2017
ms.author: mihart
ms.openlocfilehash: 3d51475b300fadc55f33960b03c3adc0031a39b8
ms.sourcegitcommit: 12236d08c27c7ee3fabb7ef9d767e9dee693f8aa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/21/2017
---
# <a name="getting-a-custom-visual-certified"></a>Een aangepast visueel element laten *certificeren*
## <a name="what-is-meant-by-certified"></a>Wat is *gecertificeerd*?
Een *gecertificeerd aangepast visueel element* is een visueel element dat voldoet aan bepaalde vereisten en strenge beveiligingstesten heeft doorstaan.  Wanneer een aangepast visueel element is gecertificeerd, kan het worden [geëxporteerd naar PowerPoint](service-publish-to-powerpoint.md) en wordt het weergegeven in de e-mailberichten die gebruikers ontvangen wanneer deze zich [op rapportpagina's abonneren](service-report-subscribe.md).

Bent u een webontwikkelaar en bent u geïnteresseerd in het maken van uw eigen visualisaties en wilt u deze toevoegen aan [Microsoft AppSource](https://appsource.microsoft.com)? Zie [Aan de slag met hulpprogramma's voor ontwikkelaars](service-custom-visuals-getting-started-with-developer-tools.md) voor meer informatie.


## <a name="certification-requirements"></a>Vereisten voor certificering
* Goedgekeurd door Microsoft AppSource    
* Het aangepaste visuele element is geschreven met API-versie 1.2 of hoger    
* De codeopslagplaats is beschikbaar voor controle (de code van het visuele element is bijvoorbeeld beschikbaar voor ons via GitHub)    
* Er is alleen gebruikgemaakt van openbare controleerbare OSS-onderdelen    
* Er worden geen externe services of bronnen gebruikt    

> **TIP**: U wordt aangeraden EsLint met de standaardbeveiligingsregelset te gebruiken om uw code te valideren voordat u het visuele element indient.
> 
> 

## <a name="process-for-submitting-a-custom-visual-for-certification"></a>Proces voor het indienen van een aangepast visueel element voor certificering
Een aangepast visueel element indienen voor certificering:

1. Verzend een e-mailbericht naar de ondersteuning van Power BI voor aangepaste visuele elementen (pbicvsupport@microsoft.com). Neem de volgende informatie op in het e-mailbericht:    
   
   * Titel: Aanvraag voor certificering van visueel element    
   * Koppeling naar de GitHub-opslagplaats waar de broncode van het visuele element wordt gehost    
   * Voldoen aan de vereisten (zie hierboven)    
   * De code- en beveiligingscontrole doorstaan    
2. U krijgt bericht van het Microsoft-team voor aangepaste visuele elementen wanneer uw aangepaste visuele element is gecertificeerd en toegevoegd aan de lijst met gecertificeerde elementen (hieronder), of dat uw visuele element is geweigerd. In dat geval ontvangt u een rapport van de problemen die moeten worden verholpen. Het is de verantwoordelijkheid van de ontwikkelaar om contact te houden met Microsoft en hun gecertificeerde visuele elementen waar nodig bij te werken.

## <a name="removal-of-power-bi-certified-custom-visuals"></a>Gecertificeerde aangepaste visuele elementen uit Power BI verwijderen
Microsoft kan naar eigen goeddunken een visueel element uit de lijst met gecertificeerde visuele elementen verwijderen.  

## <a name="list-of-custom-visuals-that-have-been-certified"></a>Lijst met aangepaste visuele elementen die zijn gecertificeerd
| Koppeling naar AppSource | Koppeling naar video |
| --- | --- |
| [Asterdiagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380759?src=office&tab=Overview) | |
| [Vlinderdasdiagram door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380838?src=office&tab=Overview) |[Video](https://youtu.be/So5xKMSpVJI) |
| [BciCalendar (Beyondsoft-kalender)](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381096?src=office&tab=Overview)  | |
| [Box-and-whisker](https://appsource.microsoft.com/product/power-bi-visuals/WA104380831?src=office&tab=Overview) | |
| [Opsommingstekendiagram](https://store.office.com/app.aspx?assetid=WA104380755) |[Video1](https://youtu.be/AOlsFYkfkcw)   [Video2](https://youtu.be/AQvd2FhRyCI) |
| [Opsommingstekendiagram door OKViz](https://store.office.com/bullet-chart-by-okviz-WA104380953.aspx) |[Video](https://youtu.be/mtvUNl9bMjA) |
| [Kalender door Tallan](https://appsource.microsoft.com/product/power-bi-visuals/WA104381146?src=office&tab=Overview) | |
| [Chiclet-slicer](https://store.office.com/chiclet-slicer-WA104380756.aspx) |[Video](https://youtu.be/iYOkJ1APueY) |
| [Koordediagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380761?src=office&tab=Overview) |[Video](https://youtu.be/AQvd2FhRyCI) |
| [Ronde meter door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380837?tab=Overview) | |
| [Cilindrische meter](https://appsource.microsoft.com/product/power-bi-visuals/WA104380874) | |
| [Meetklok](https://appsource.microsoft.com/product/power-bi-visuals/WA104381184) |[Video](https://youtu.be/AOlsFYkfkcw) |
| [Ringdiagram (cirkelgrafiek) door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380824?tab=Overview) |[Video](https://youtu.be/pDToHDFHnq8) |
| [Puntdiagram door OKViz](https://appsource.microsoft.com/product/power-bi-visuals/WA104381101?src=office&tab=Overview) |[Video](https://youtu.be/4lskRgcpFJY) |
| [Inzoom-ringdiagram door ZoomCharts](https://appsource.microsoft.com/product/power-bi-visuals/WA104380858) | |
| [Dual KPI](https://store.office.com/dual-kpi-WA104380774.aspx) |[Video](https://youtu.be/821o0-eVBXo?list=PL1N57mwBHtN1vIjfvuBIzZllrmKo-Vz6x) |
| [Enlighten Aquarium](https://appsource.microsoft.com/product/power-bi-visuals/WA104381112?src=office&tab=Overview) | |
| Enlighten World Flags: binnenkort beschikbaar | |
| Enlighten Stack Shuffle: binnenkort beschikbaar | |
| [Gantt](https://store.office.com/gantt-WA104380765.aspx) |[Video](https://youtu.be/qJ7s_KrGiUU) |
| [Histogram](https://store.office.com/histogram-chart-WA104380776.aspx) | |
| [Horizontale trechter](https://appsource.microsoft.com/product/power-bi-visuals/WA104380846) |[Video](https://youtu.be/SudZei68PPo) |
| [KPI-indicator](https://store.office.com/kpi-indicator-WA104380832.aspx) | |
| [Lineaire meter door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380821?src=office&tab=Overview) |[Video](https://youtu.be/AOlsFYkfkcw) |
| [Mekkodiagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380785?src=office&tab=Overview)  | [Video](https://youtu.be/90FLCKpgicA)|
| [Afspeelas (dynamische slicer)](https://store.office.com/play-axis-dynamic-slicer-WA104380981.aspx) | |
| [Power KPI](https://appsource.microsoft.com/product/power-bi-visuals/WA104381083) |[Video](https://youtu.be/IvfIP3E6-1Q) |
| [Radardiagram](https://store.office.com/radar-chart-WA104380771.aspx) | |
| [Cirkelgrafiek (ringdiagram) door MAQ Software](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380824?src=office&tab=Overview) | [Video](https://youtu.be/pDToHDFHnq8)|
| [Sankeydiagram](https://store.office.com/app.aspx?assetid=WA104380777.aspx) |[Video](https://youtu.be/WWP9wVUHGaA) |
| [Bladerscherm](https://store.office.com/scroller-WA104381018.aspx) |[Video](https://youtu.be/uhRFQF2cGSY) |
| [Slim filter door SQLBI](https://store.office.com/smart-filter-by-okviz-WA104380859.aspx) |[Video](https://youtu.be/gcJsDDRQq28) |
| [Sparkline door OKViz](https://appsource.microsoft.com/product/power-bi-visuals/WA104380910?src=office&tab=Overview) |[Video](https://youtu.be/0m3Vnvso9tY) |
| [Zonnestraal](https://appsource.microsoft.com/product/power-bi-visuals/WA104380767?src=office&tab=Overview) | |
| [Tachometer](https://store.office.com/tachometer-WA104380937.aspx?) |[Video](https://www.youtube.com/watch?v=C3OXdETbS9o) |
| [Thermometer](https://appsource.microsoft.com/product/power-bi-visuals/WA104380847?src=office&tab=Overview) | [Video](https://youtu.be/SPX9mgrAdBc)|
| [Time Series-ontleding](https://appsource.microsoft.com/product/power-bi-visuals/WA104380897) | |
| [Tabelheatmap](https://store.office.com/table-heatmap-WA104380818.aspx) | |
| [Tekstwrapper](https://appsource.microsoft.com/product/power-bi-visuals/WA104380826) | |
| [Tijdlijnslicer](https://store.office.com/timeline-slicer-WA104380786.aspx) |[Video](https://youtu.be/ozMtZ4_NZ10) |
| [Tornadodiagram](https://store.office.com/tornado-chart-WA104380768.aspx) |[Video](https://youtu.be/AQvd2FhRyCI) |
| [Wafeldiagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104381049?src=office&tab=Overview) |[Video](https://youtu.be/1vRqYUsm3Vk) |
| [Woordwolk](https://store.office.com/word-cloud-WA104380752.aspx?) |[Video](https://www.youtube.com/watch?v=AblTenl9fqo) |

## <a name="next-steps"></a>Volgende stappen
[Aan de slag met ontwikkelhulpprogramma's voor aangepaste visuele elementen (Preview)](service-custom-visuals-getting-started-with-developer-tools.md)      
[Microsoft-afspeellijst voor aangepaste visuele elementen op YouTube](https://www.youtube.com/playlist?list=PL1N57mwBHtN1vIjfvuBIzZllrmKo-Vz6x)  
[Visualisaties in Power BI](power-bi-report-visualizations.md)  
[Aangepaste visualisaties in Power BI](power-bi-custom-visuals.md)  
[Aangepaste visuele elementen publiceren naar Microsoft AppSource](developer/office-store.md)  
Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

