---
title: Gecertificeerde visualisaties in Power BI
description: Vereisten en proces voor het indienen van een aangepast visueel element voor certificering. En een lijst met al gecertificeerde aangepaste visuele elementen.
author: mihart
manager: kfile
ms.reviewer: ''
featuredvideoid: ''
ms.service: powerbi
ms.component: powerbi-developer
ms.topic: conceptual
ms.date: 02/13/2018
ms.author: mihart
ms.openlocfilehash: a1d3a18fd2f325cd82cd682feb52205f17dacf93
ms.sourcegitcommit: 638de55f996d177063561b36d95c8c71ea7af3ed
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/17/2018
ms.locfileid: "34297004"
---
# <a name="getting-a-custom-visual-certified"></a>Een aangepast visueel element laten *certificeren*
## <a name="what-is-meant-by-certified"></a>Wat is *gecertificeerd*?
Een *gecertificeerd aangepast visueel element* is een visueel element dat voldoet aan bepaalde vereisten en strenge beveiligingstesten heeft doorstaan.  Wanneer een aangepast visueel element is gecertificeerd, kan het worden [geëxporteerd naar PowerPoint](service-publish-to-powerpoint.md) en wordt het weergegeven in de e-mailberichten die gebruikers ontvangen wanneer deze zich [op rapportpagina's abonneren](service-report-subscribe.md). Natuurlijk kan het ook worden gebruikt als [standaard aangepaste visuals](power-bi-custom-visuals.md) die worden toegevoegd aan rapporten van Power BI-service en Power BI Desktop en worden weergegeven in Power BI mobile en ingevoegd.

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
| [Asterdiagram](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380759) | |
| [Beyondsoft-agenda](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381096) | |
| [Vlinderdasdiagram door MAQ Software](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380838) | [Video](https://youtu.be/So5xKMSpVJI) |
| [Box-and-whisker-grafiek](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380831) | |
| [Box-and-whisker-grafiek door MAQ Software](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381351) | [Video](https://youtu.be/JoHaFLfhXdo) |
| [Bouwsteendiagram door MAQ Software](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380836) | [Video](https://youtu.be/hA3DOsvn2xY) |
| [Belgrafiek door Akvelon](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381340) | |
| [Opsommingstekendiagram](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380755) | [Video](https://youtu.be/AOlsFYkfkcw) |
| [Opsommingstekendiagram door OKViz](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380953) | [Video](https://youtu.be/mtvUNl9bMjA) |
| [Kalender door Tallan](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381146) | |
| [Candlestick door OKViz](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380952) | [Video](https://youtu.be/nT_18gyRxPo) |
| [Kaart met staten door OKViz](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380967) | |
| [Chiclet-slicer](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380756) | |
| [Chord](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380761) | [Video](https://youtu.be/AQvd2FhRyCI) |
| [Ronde meter door MAQ Software](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380837) | [Video](https://youtu.be/9NHXALkBXuY) |
| [Cluster-kaart](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380806) | |
| [Cilindrische meter door MAQ Software](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380874) | [Video](https://youtu.be/DgdoWi7Gcxo) |
| [Meetklok](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381184) | |
| [Puntdiagram](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380760) | |
| [Puntdiagram door OKViz](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380949) | [Video](https://youtu.be/By16pX9KT40) |
| [Inzoom-cartogram](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381045) | |
| [Inzoom-choropleth](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381044) | |
| [Inzoom-kolomdiagram](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380857) | [Video](https://youtu.be/lBy2gQQ5YsQ) |
| [Inzoom-kolomdiagram voor op tijd gebaseerde gegevens](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380881) | [Video](https://youtu.be/T_mRou18vx0) |
| [Inzoom-ringdiagram](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380858) | [Video](https://youtu.be/AUVFrSHmPeo) |
| [Dual KPI](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380774) | |
| [Dynamische knopinfo door MAQ Software](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380983) | [Video](https://youtu.be/Z-tl97BpEr0) |
| [Verbeterde spreidingsgrafiek](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380762) | [Video](https://youtu.be/xCfM0cjM4do) |
| [Enlighten Aquarium](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381112) | |
| [Enlighten Slicer](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380960) | |
| [Enlighten Stack Shuffle](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380849) | |
| [Enlighten-wafeldiagram](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380850) | |
| [Krachtgestuurde grafiek](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380764) | [Video](https://youtu.be/YsTa7uyJ4sg) |
| [Trechter met bron door MAQ Software](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381334) | [Video](https://youtu.be/R_EcimsLI8U) |
| [Gantt](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380765) | [Video](https://youtu.be/qJ7s_KrGiUU) |
| [Opgeefdiagram door MAQ Software](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381364) | [Video](https://youtu.be/vJLV9JRCpI8) |
| [Globe-gegevensbalken](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381344) | |
| [Hiërarchische grafiek door Akvelon](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381333) | [Video](https://youtu.be/0ZGzJaq_KT4) |
| [Histogram](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380776) | |
| [Histogram met punten door MAQ Software](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381032) | [Video](https://youtu.be/-ILF--wExrw) |
| [Horizontale trechter door MAQ Software](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380846) | [Video](https://youtu.be/SudZei68PPo) |
| [Afbeelding door CloudScope](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381297) | |
| [Afbeeldingenraster](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381355) | |
| [Infographic Designer](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380898) | |
| [KPI-grafiek door Akvelon](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381432) | |
| [KPI-kolom door MAQ Software](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380996) | [Video](https://youtu.be/rU0xoOlIq1U) |
| [KPI-indicator](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380832) | |
| [KPI-ticker door MAQ Software](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380946) | [Video](https://youtu.be/cudG4gsZ2V8) |
| [Lineaire meter door MAQ Software](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380821) | [Video](https://youtu.be/7_jFaM30dkc) |
| [LineDot-grafiek](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380766) | |
| [Mekkodiagram](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380785) | [Video](https://youtu.be/90FLCKpgicA) |
| [Overzicht door CloudScope](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381477) | |
| [Afspeelas (dynamische slicer)](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380981) | |
| [Power KPI](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381083) | [Video](https://youtu.be/IvfIP3E6-1Q) |
| [Power KPI Matrix](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381299) | [Video](https://youtu.be/1enze8pcGzY) |
| [Pulse-grafiek](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381006) | [Video](https://youtu.be/DQWdcQtjDVw) |
| [Kwadrantdiagram door MAQ Software](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381011) | [Video](https://youtu.be/ppBnyhqWNC0) |
| [Radardiagram](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380771) | |
| [Ringgrafiek door MAQ Software](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380824) | [Video](https://youtu.be/pDToHDFHnq8) |
| [Draaigrafiek door MAQ Software](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381007) | [Video](https://youtu.be/d5xBCMmb3hU) |
| [Sankeydiagram](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380777) | [Video](https://youtu.be/WWP9wVUHGaA) |
| [Bladerscherm](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381018) | |
| [Slim filter door OKViz](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380859) | [Video](https://youtu.be/gcJsDDRQq28) |
| [Sparkline door OKViz](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380910) | [Video](https://youtu.be/0m3Vnvso9tY) |
| [Stroomgrafiek](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380772) | |
| [Zonnestraal](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380767) | |
| [Synoptic Panel door OKViz](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380873) | |
| [Tabelheatmap](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380818) | |
| [Tachometer](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380937) | [Video](https://youtu.be/C3OXdETbS9o) |
| [Tekstfilter](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381309) | |
| [Tekst-wrapper door MAQ Software](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380826) | |
| [Thermometer door MAQ Software](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380847) | [Video](https://youtu.be/SPX9mgrAdBc) |
| [Tijdlijnslicer](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380786) | [Video](https://youtu.be/ozMtZ4_NZ10) |
| [Tornadodiagram](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380768) | [Video](https://www.youtube.com/watch?v=AQvd2FhRyCI) |
| [Handelsgrafiek door MAQ Software](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380823) | [Video](https://youtu.be/xhTR6y6J9Ko) |
| [Ultieme afwijking](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381140) | [Video](https://youtu.be/pDYF8iZxERs) |
| [Ultieme waterval](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380956) | [Video](https://youtu.be/0BZsVCQdEkc) |
| [Gebruikerslijst door CloudScope](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381426) | |
| [Wafeldiagram](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381049) | [Video](https://youtu.be/1vRqYUsm3Vk) |
| [Woordwolk](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380752) | [Video](https://youtu.be/AblTenl9fqo) |

## <a name="next-steps"></a>Volgende stappen
[Aan de slag met ontwikkelhulpprogramma's voor aangepaste visuele elementen (Preview)](service-custom-visuals-getting-started-with-developer-tools.md)      
[Microsoft-afspeellijst voor aangepaste visuele elementen op YouTube](https://www.youtube.com/playlist?list=PL1N57mwBHtN1vIjfvuBIzZllrmKo-Vz6x)  
[Visualisaties in Power BI](power-bi-report-visualizations.md)  
[Aangepaste visualisaties in Power BI](power-bi-custom-visuals.md)  
[Aangepaste visuele elementen publiceren naar Microsoft AppSource](developer/office-store.md)  
Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

