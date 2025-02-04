---
title: Gecertificeerde aangepaste visuals in Power BI
description: Vereisten en proces voor het indienen van een aangepast visueel element voor certificering. En een lijst met al gecertificeerde aangepaste visuele elementen.
author: sranins
ms.author: rasala
manager: kfile
ms.reviewer: maghan
featuredvideoid: ''
ms.service: powerbi
ms.topic: conceptual
ms.subservice: powerbi-custom-visuals
ms.date: 03/10/2019
ms.openlocfilehash: 719ec49dd560461dfa3cec66e8f8f1a5b92b8951
ms.sourcegitcommit: f176ba9d52d50d93f264eca21bb3fd987dbf934b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2019
ms.locfileid: "57757387"
---
# <a name="certified-custom-visuals"></a>Gecertificeerde aangepaste visuals

## <a name="what-are-certified-custom-visuals"></a>Wat zijn **_gecertificeerde_** aangepaste visuals?

Gecertificeerde aangepaste visuals zijn visuals in de **Marketplace** die voldoen aan bepaalde vereisten voor **opgegeven code** die zijn getest en goedgekeurd door het **Microsoft Power BI-team**. Zodra een aangepaste visual is gecertificeerd, zijn hiervoor meer functies beschikbaar. U kunt bijvoorbeeld [exporteren naar PowerPoint](consumer/end-user-powerpoint.md) en de visual weergeven in e-mails die worden ontvangen wanneer een gebruiker zich [op rapportpagina's abonneert](consumer/end-user-subscribe.md).

**Gecertificeerde aangepaste visuals** worden gebruikt als [standaard aangepaste visuals](power-bi-custom-visuals.md). Gecertificeerde aangepaste visuals kunnen worden toegevoegd aan de **Power BI-service**, een **Power BI Desktop-rapport** en bekeken met **Power BI Mobile** en **Power BI Embedded**.

De testen die worden uitgevoerd, zijn ontworpen om te controleren of de visual geen toegang heeft tot externe services of resources. **Microsoft** is *niet* de auteur van externe aangepaste visuals en klanten wordt aangeraden om rechtstreeks contact op te nemen met de auteur om de functionaliteit van dergelijke visuals te controleren.

Het certificeringsproces is een optioneel proces en de ontwikkelaars mogen zelf bepalen of ze hun visual in de marketplace willen laten certificeren.  

**Niet-gecertificeerde aangepaste visuals** zijn niet automatisch onveilige visuals. Sommige visuals zijn niet gecertificeerd omdat ze niet aan een of meer [certificeringsvereisten](https://docs.microsoft.com/power-bi/power-bi-custom-visuals-certified?#certification-requirements) voldoen. Bijvoorbeeld als er verbinding wordt gemaakt met een externe service zoals kaartvisuals of visuals waarvoor commerciële bibliotheken worden gebruikt.

Bent u webontwikkelaar en bent u geïnteresseerd in het maken van uw eigen visualisaties en wilt u deze toevoegen aan  **[Microsoft AppSource](https://appsource.microsoft.com)**? Zie  **[Een aangepaste visual voor Power BI ontwikkelen](developer/custom-visual-develop-tutorial.md)** voor meer informatie.

## <a name="removal-of-power-bi-certified-custom-visuals"></a>Gecertificeerde aangepaste visuele elementen uit Power BI verwijderen

Microsoft kan naar eigen goeddunken een visual uit de [lijst met gecertificeerde visuals](#list-of-custom-visuals-that-have-been-certified) verwijderen.

## <a name="getting-a-custom-visualcertified"></a>Een aangepaste visual laten certificeren

### <a name="certification-requirements"></a>Vereisten voor certificering

Als u uw aangepaste visual wilt laten [certificeren](#certified-custom-visuals), moet u ervoor zorgen dat uw aangepaste visual aan de onderstaande voorwaarden voldoet:  

* Goedgekeurd door Microsoft AppSource. Uw aangepaste visual moet in onze [marketplace](https://appsource.microsoft.com/marketplace/apps?page=1&product=power-bi-visuals) staan.
* De aangepaste visual is geschreven met API-versie 1.2 of hoger.
* Er moet een codeopslagplaats beschikbaar zijn die door een Power BI-team kan worden beoordeeld (bijvoorbeeld broncode (JavaScript of TypeScript) in een voor mensen leesbare indeling die voor ons beschikbaar is via GitHub).

    >[!Note]
    > U hoeft uw code niet openbaar te delen in Github.

* Er worden alleen openbaar leesbare OSS-onderdelen gebruiken (JS-bibliotheken of TypeScript die openbaar zijn. De broncode is beschikbaar voor beoordeling en bevat geen bekende beveiligingsproblemen). We kunnen aangepaste visuals met een commercieel onderdeel niet verifiëren.

* Heeft geen toegang tot externe services of resources, inclusief maar niet beperkt tot, geen HTTP/S- of WebSocket-aanvragen van Power BI naar eender welke services. 

> [!TIP]
> U wordt aangeraden EsLint met de standaardbeveiligingsregelset te gebruiken om uw code voorafgaand aan het indienen te valideren.

## <a name="process-for-submitting-a-custom-visual-for-certification"></a>Proces voor het indienen van een aangepaste visual voor certificering

Een aangepast visueel element indienen voor certificering:

1. Verzend een e-mailbericht naar het ondersteuningsteam van Power BI voor aangepaste visuals (pbicvsupport@microsoft.com). Neem de volgende informatie op in het e-mailbericht:
    * Titel: Aanvraag voor certificering van visual
    * Koppeling naar de GitHub-opslagplaats waar de broncode van de door mensen leesbare broncode wordt gehost
    * [Voldoen aan de vereisten](#certification-requirements)
    * Voldoen aan de codebeoordeling

2. U krijgt bericht van het Microsoft-team voor aangepaste visuals wanneer uw aangepaste visual is gecertificeerd en toegevoegd aan de [lijst met gecertificeerde visuals](#list-of-custom-visuals-that-have-been-certified), of wanneer uw visual is geweigerd. In dat geval ontvangt u een rapport van de problemen die moeten worden verholpen. Het is de verantwoordelijkheid van de ontwikkelaar om contact te houden met Microsoft en hun gecertificeerde visuals waar nodig bij te werken.

## <a name="list-of-custom-visuals-that-have-been-certified"></a>Lijst met aangepaste visuele elementen die zijn gecertificeerd

| Koppeling naar AppSource | Koppeling naar video |
| --- | --- |
| [3AG Systems - Kolomdiagram met relatieve afwijking](https://appsource.microsoft.com/product/power-bi-visuals/WA104381803) | |
| [Geavanceerde ringvisual](https://appsource.microsoft.com/product/power-bi-visuals/WA104381941) | |
| [Geavanceerde netwerkvisualisatie](https://appsource.microsoft.com/product/power-bi-visuals/WA104381942) | |
| [Geavanceerde TimeSeries-visual](https://appsource.microsoft.com/product/power-bi-visuals/WA104381943) | |
| [Geavanceerde combinatievisual](https://appsource.microsoft.com/product/power-bi-visuals/WA104381944) | |
| [Asterdiagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380759) | |
| [Beyondsoft-agenda](https://appsource.microsoft.com/product/power-bi-visuals/WA104381096) | |
| [Vlinderdasdiagram door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380838) | [Video](https://youtu.be/So5xKMSpVJI) |
| [Box-and-whisker-grafiek](https://appsource.microsoft.com/product/power-bi-visuals/WA104380831) | |
| [Box-and-whisker-grafiek door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104381351) | [Video](https://youtu.be/JoHaFLfhXdo) |
| [Bouwsteendiagram door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380836) | [Video](https://youtu.be/hA3DOsvn2xY) |
| [Belgrafiek door Akvelon](https://appsource.microsoft.com/product/power-bi-visuals/WA104381340) | |
| [Opsommingstekendiagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380755) | [Video](https://youtu.be/AOlsFYkfkcw) |
| [Opsommingstekendiagram door OKViz](https://appsource.microsoft.com/product/power-bi-visuals/WA104380953) | [Video](https://youtu.be/mtvUNl9bMjA) |
| [Kalender door Tallan](https://appsource.microsoft.com/product/power-bi-visuals/WA104381146) | |
| [Candlestick door OKViz](https://appsource.microsoft.com/product/power-bi-visuals/WA104380952) | [Video](https://youtu.be/nT_18gyRxPo) |
| [Kaart met staten door OKViz](https://appsource.microsoft.com/product/power-bi-visuals/WA104380967) | |
| [Chiclet-slicer](https://appsource.microsoft.com/product/power-bi-visuals/WA104380756) | |
| [Chord](https://appsource.microsoft.com/product/power-bi-visuals/WA104380761) | [Video](https://youtu.be/AQvd2FhRyCI) |
| [Ronde meter door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380837) | [Video](https://youtu.be/9NHXALkBXuY) |
| [Cluster-kaart](https://appsource.microsoft.com/product/power-bi-visuals/WA104380806) | |
| [Cilindrische meter door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380874) | [Video](https://youtu.be/DgdoWi7Gcxo) |
| [Meetklok](https://appsource.microsoft.com/product/power-bi-visuals/WA104381184) | |
| [Puntdiagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380760) | |
| [Puntdiagram door OKViz](https://appsource.microsoft.com/product/power-bi-visuals/WA104380949) | [Video](https://youtu.be/By16pX9KT40) |
| [Inzoom-cartogram](https://appsource.microsoft.com/product/power-bi-visuals/WA104381045) | |
| [Inzoom-choropleth](https://appsource.microsoft.com/product/power-bi-visuals/WA104381044) | |
| [Inzoom-kolomdiagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380857) | [Video](https://youtu.be/lBy2gQQ5YsQ) |
| [Inzoom-kolomdiagram voor op tijd gebaseerde gegevens](https://appsource.microsoft.com/product/power-bi-visuals/WA104380881) | [Video](https://youtu.be/T_mRou18vx0) |
| [Inzoom-ringdiagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380858) | [Video](https://youtu.be/AUVFrSHmPeo) |
| [Dual KPI](https://appsource.microsoft.com/product/power-bi-visuals/WA104380774) | |
| [Dynamische knopinfo door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380983) | [Video](https://youtu.be/Z-tl97BpEr0) |
| [Verbeterde spreidingsgrafiek](https://appsource.microsoft.com/product/power-bi-visuals/WA104380762) | [Video](https://youtu.be/xCfM0cjM4do) |
| [Enlighten Aquarium](https://appsource.microsoft.com/product/power-bi-visuals/WA104381112) | |
| [Enlighten Slicer](https://appsource.microsoft.com/product/power-bi-visuals/WA104380960) | |
| [Enlighten Stack Shuffle](https://appsource.microsoft.com/product/power-bi-visuals/WA104380849) | |
| [Enlighten-wafeldiagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380850) | |
| [Filter by List door Devscope](https://appsource.microsoft.com/product/power-bi-visuals/WA104381413) | [Video](https://youtu.be/RetEWGwBu0I) |
| [Krachtgestuurde grafiek](https://appsource.microsoft.com/product/power-bi-visuals/WA104380764) | [Video](https://youtu.be/YsTa7uyJ4sg) |
| [Trechter met bron door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104381334) | [Video](https://youtu.be/R_EcimsLI8U) |
| [Gantt](https://appsource.microsoft.com/product/power-bi-visuals/WA104380765) | [Video](https://youtu.be/qJ7s_KrGiUU) |
| [Opgeefdiagram door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104381364) | [Video](https://youtu.be/vJLV9JRCpI8) |
| [Globe-gegevensbalken](https://appsource.microsoft.com/product/power-bi-visuals/WA104381344) | |
| [Raster door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380825) | [Video](https://youtu.be/VOPoDJgZfOY) |
| [Hiërarchische grafiek door Akvelon](https://appsource.microsoft.com/product/power-bi-visuals/WA104381333) | [Video](https://youtu.be/0ZGzJaq_KT4) |
| [Histogram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380776) | |
| [Histogram met punten door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104381032) | [Video](https://youtu.be/-ILF--wExrw) |
| [Horizontale trechter door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380846) | [Video](https://youtu.be/SudZei68PPo) |
| [Afbeelding door CloudScope](https://appsource.microsoft.com/product/power-bi-visuals/WA104381297) | |
| [Afbeeldingenraster](https://appsource.microsoft.com/product/power-bi-visuals/WA104381355) | |
| [Infographic Designer](https://appsource.microsoft.com/product/power-bi-visuals/WA104380898) | |
| [KPI-grafiek door Akvelon](https://appsource.microsoft.com/product/power-bi-visuals/WA104381432) | |
| [KPI-kolom door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380996) | [Video](https://youtu.be/rU0xoOlIq1U) |
| [KPI-raster door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380947) | [Video](https://youtu.be/dM4PvZh71V0) |
| [KPI-indicator](https://appsource.microsoft.com/product/power-bi-visuals/WA104380832) | |
| [KPI-ticker door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380946) | [Video](https://youtu.be/cudG4gsZ2V8) |
| [Lineaire meter door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380821) | [Video](https://youtu.be/7_jFaM30dkc) |
| [LineDot-grafiek](https://appsource.microsoft.com/product/power-bi-visuals/WA104380766) | |
| [Mekkodiagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380785) | [Video](https://youtu.be/90FLCKpgicA) |
| [Multi-KPI](https://appsource.microsoft.com/product/power-bi-visuals/WA104381763) | |
| [Overzicht door CloudScope](https://appsource.microsoft.com/product/power-bi-visuals/WA104381477) | |
| [Afspeelas (dynamische slicer)](https://appsource.microsoft.com/product/power-bi-visuals/WA104380981) | |
| [Power KPI](https://appsource.microsoft.com/product/power-bi-visuals/WA104381083) | [Video](https://youtu.be/IvfIP3E6-1Q) |
| [Power KPI Matrix](https://appsource.microsoft.com/product/power-bi-visuals/WA104381299) | [Video](https://youtu.be/1enze8pcGzY) |
| [Pulse-grafiek](https://appsource.microsoft.com/product/power-bi-visuals/WA104381006) | [Video](https://youtu.be/DQWdcQtjDVw) |
| [Kwadrantdiagram door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104381011) | [Video](https://youtu.be/ppBnyhqWNC0) |
| [Radardiagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380771) | |
| [Ringgrafiek door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380824) | [Video](https://youtu.be/pDToHDFHnq8) |
| [Draaigrafiek door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104381007) | [Video](https://youtu.be/d5xBCMmb3hU) |
| [Sankeydiagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380777) | [Video](https://youtu.be/WWP9wVUHGaA) |
| [Spreidingsdiagram door Akvelon](https://appsource.microsoft.com/product/power-bi-visuals/WA104381703) | |
| [Bladerscherm](https://appsource.microsoft.com/product/power-bi-visuals/WA104381018) | |
| [Slim filter door OKViz](https://appsource.microsoft.com/product/power-bi-visuals/WA104380859) | [Video](https://youtu.be/gcJsDDRQq28) |
| [Sparkline door OKViz](https://appsource.microsoft.com/product/power-bi-visuals/WA104380910) | [Video](https://youtu.be/0m3Vnvso9tY) |
| [Stroomgrafiek](https://appsource.microsoft.com/product/power-bi-visuals/WA104380772) | |
| [Zonnestraal](https://appsource.microsoft.com/product/power-bi-visuals/WA104380767) | |
| [Synoptic Panel door OKViz](https://appsource.microsoft.com/product/power-bi-visuals/WA104380873) | |
| [Tabelheatmap](https://appsource.microsoft.com/product/power-bi-visuals/WA104380818) | |
| [Tachometer](https://appsource.microsoft.com/product/power-bi-visuals/WA104380937) | [Video](https://youtu.be/C3OXdETbS9o) |
| [Tekstfilter](https://appsource.microsoft.com/product/power-bi-visuals/WA104381309) | |
| [Tekst-wrapper door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380826) | |
| [Thermometer door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380847) | [Video](https://youtu.be/SPX9mgrAdBc) |
| [Time Brush Slicer](https://appsource.microsoft.com/product/power-bi-visuals/WA104380798) | |
| [Tijdlijnslicer](https://appsource.microsoft.com/product/power-bi-visuals/WA104380786) | [Video](https://youtu.be/ozMtZ4_NZ10) |
| [Tijdlijn door CloudScope](https://appsource.microsoft.com/product/power-bi-visuals/WA104381427) | [Video](https://youtu.be/szNi9YgXFJc) |
| [Tornadodiagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380768) | [Video](https://www.youtube.com/watch?v=AQvd2FhRyCI) |
| [Handelsgrafiek door MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380823) | [Video](https://youtu.be/xhTR6y6J9Ko) |
| [Ultieme afwijking](https://appsource.microsoft.com/product/power-bi-visuals/WA104381140) | [Video](https://youtu.be/pDYF8iZxERs) |
| [Ultieme waterval](https://appsource.microsoft.com/product/power-bi-visuals/WA104380956) | [Video](https://youtu.be/0BZsVCQdEkc) |
| [Gebruikerslijst door CloudScope](https://appsource.microsoft.com/product/power-bi-visuals/WA104381426) | |
| [Wafeldiagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104381049) | [Video](https://youtu.be/1vRqYUsm3Vk) |
| [Woordwolk](https://appsource.microsoft.com/product/power-bi-visuals/WA104380752) | [Video](https://youtu.be/AblTenl9fqo) |

## <a name="faq"></a>Veelgestelde vragen

Voor meer informatie over visuals gaat u naar [Veelgestelde vragen over gecertificeerde visuals](power-bi-custom-visuals-faq.md#certified-custom-visuals).

## <a name="next-steps"></a>Volgende stappen

* [Een aangepaste visual voor Power BI ontwikkelen](developer/custom-visual-develop-tutorial.md)
* [Microsoft-afspeellijst voor aangepaste visuele elementen op YouTube](https://www.youtube.com/playlist?list=PL1N57mwBHtN1vIjfvuBIzZllrmKo-Vz6x)  
* [Visualisaties in Power BI](visuals/power-bi-report-visualizations.md)  
* [Aangepaste visualisaties in Power BI](power-bi-custom-visuals.md)  
* [Aangepaste visuele elementen publiceren naar Microsoft AppSource](developer/office-store.md)  

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)
