---
title: Power BI - basisconcepten
description: Power BI - basisconcepten
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: B2vd4MQrz4M
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: get-started-article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 05/31/2017
ms.author: mihart
ms.openlocfilehash: f20ea18fb46928bf7533caacf55a0cdb3d761571
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2017
---
# <a name="power-bi---basic-concepts-for-power-bi-service"></a>Power BI - basisconcepten van de Power BI-service
<!-- Shared newnav Include -->
[!INCLUDE [newnavbydefault](./includes/newnavbydefault.md)]

In dit artikel wordt ervan uitgegaan dat u al bent[aangemeld voor Power BI](service-self-service-signup-for-power-bi.md) en [enkele gegevens hebt toegevoegd](service-get-data.md).

Wanneer u de Power BI-service opent, ziet u dat er een ***dashboard*** wordt weergegeven. Dashboards zijn de elementen waarmee de Power BI-service zich onderscheidt van Power BI Desktop.

![](media/service-basic-concepts/completenewer.png)

De belangrijkste functies in de gebruikersinterface van de Power BI-service:

1. Navigatiebalk
2. Dashboard met tegels
3. Q&A-vragenvak
4. De knoppen Help en Feedback
5. Dashboardtitel
6. Startprogramma voor de Office 365-app
7. Knop voor de startpagina van Power BI
8. Aanvullende dashboardacties

Meer informatie hierover volgt later, maar laten we eerst enkele concepten van Power BI bekijken.

U kunt ook eerst deze video bekijken voordat u de rest van dit artikel leest.  In de video bespreekt Will de basisconcepten aan de hand van een rondleiding door de Power BI-service.

<iframe width="560" height="315" src="https://www.youtube.com/embed/B2vd4MQrz4M" frameborder="0" allowfullscreen></iframe>


## <a name="power-bi-concepts"></a>Power BI-concepten
De drie primaire bouwstenen van Power BI zijn: ***dashboards***, ***rapporten*** en ***gegevenssets***. U kunt geen dashboards of rapporten maken zonder gegevens (u kunt uiteraard een lege dashboards en rapporten maken, maar deze zijn pas bruikbaar wanneer ze gegevens bevatten). Laten we beginnen met **gegevenssets**.

## <a name="datasets"></a>Gegevenssets
Een *gegevensset* is een verzameling gegevens die u *importeert* of waar u *verbinding* mee maakt. Met Power BI kunt u diverse soorten gegevenssets importeren of hier verbinding mee maken en alle gegevens samen te brengen op één locatie.  

De gegevenssets waarmee u verbinding hebt gemaakt, worden vermeld in de navigatiebalk, onder de kop **Gegevenssets**. Elke vermelde gegevensset vertegenwoordigt één bron van gegevens, bijvoorbeeld een Excel-werkmap in OneDrive, een on-premises SSAS-gegevensset in tabelvorm of een Salesforce-gegevensset. Er worden diverse verschillende gegevensbronnen ondersteund en er worden voortdurend nieuwe bronnen toegevoegd. [Zie de lijst met typen gegevenssets die kunnen worden gebruikt met Power BI](service-get-data.md).

**Eén** dataset

* kan telkens opnieuw worden gebruikt en
* kan worden in tal van verschillende rapporten.
* De visualisatie uit die ene gegevensset kunnen worden weergegeven op een groot aantal verschillende dashboards.
  
  ![](media/service-basic-concepts/drawing2.png)

Als u [verbinding met een gegevensset wilt maken of een gegevensset wilt importeren](service-get-data.md), selecteert u **Gegevens ophalen** (onderaan de navigatiebalk) of het pluspictogram naast de kop **Gegevenssets**. Volg de instructies om verbinding te maken met de specifieke bron of om deze te importeren en de gegevensset aan uw werkruimte toe te voegen. Nieuwe gegevenssets worden vermeld in de linkernavigatiebalk en gemarkeerd met een geel sterretje. Uw werkzaamheden in Power BI zijn niet van invloed op de onderliggende gegevensset. Deze blijft ongewijzigd.

Als u [deel uitmaakt van een ***app-werkruimte***](service-collaborate-power-bi-workspace.md), zijn de gegevenssets die worden toegevoegd door een lid van de werkruimte ook beschikbaar voor de andere leden van de werkruimte.

U kunt gegevenssets vernieuwen, een andere naam geven, verkennen, verwijderen of gebruiken om rapporten te maken. Selecteer een gegevensset om deze te verkennen In werkelijkheid opent de gegevensset in de rapporteditor, waar u de gegevens echt kunt doorspitten en visualisaties kunt maken. Laten we doorgaan met het volgende onderwerp: rapporten.

### <a name="dig-deeper"></a>Dieper graven:
* [Wat is Power BI Premium?](service-premium.md)
* [Gegevens ophalen voor Power BI](service-get-data.md)
* [Voorbeeldgegevenssets en inhoudspakketten voor Power BI](sample-datasets.md)

## <a name="reports"></a>Rapporten
Een Power BI-rapport bestaat uit een of meer pagina's met visualisaties (grafieken en diagrammen zoals lijndiagrammen, cirkeldiagrammen treemaps en nog veel meer). Visualisaties worden ook wel ***visuals*** genoemd. Alle visualisaties in een rapport zijn afkomstig uit één gegevensset. U kunt compleet nieuwe rapporten maken in Power BI, rapporten importeren met dashboards die collega's met u hebben gedeeld, maar u kunt ook rapporten maken wanneer u verbinding maakt met gegevenssets in Excel, Power BI Desktop, databases, SaaS-toepassingen en [inhoudspakketten](service-organizational-content-pack-introduction.md).  Als u bijvoorbeeld verbinding maakt met een Excel-werkmap die Power View-werkbladen bevat, wordt er een rapport in Power BI gemaakt op basis van die werkbladen. En als u verbinding met een SaaS-toepassing maakt, wordt er een vooraf samengestelde rapport in Power BI geïmporteerd.

U kunt in twee modi met rapporten werken: in de [leesweergave](service-report-open-in-reading-view.md) en de [bewerkingsweergave](service-interact-with-a-report-in-editing-view.md).  Alleen de persoon die het rapport heeft gemaakt, mede-eigenaren en diegenen waaraan een machtiging is verleend, hebben toegang tot alle verken-, ontwerp- en deelmogelijkheden die in de ***bewerkingsweergave*** voor dat rapport worden geboden. De personen met wie het rapport wordt gedeeld, kunnen het rapport verkennen en gebruiken in de ***leesweergave***.   

Uw rapporten worden vermeld in het navigatievenster, onder de kop **Rapporten**. Elk rapport dat wordt vermeld, vertegenwoordigt een of meer pagina's met visualisaties die zijn gebaseerd op een of meer onderliggende gegevenssets. Selecteer een rapport om het te openen. Het rapport wordt standaard eerst geopend in de leesweergave.  Selecteer **Rapport bewerken** om het rapport te openen in bewerkingsweergave (als u over de benodigde machtigingen beschikt).  Als u een gedeeld dashboard rapporten bevat, worden de rapporten niet weergegeven in de navigatiebalk. Open gedeelde rapporten in plaats daarvan rechtstreeks via het gedeelde dashboard door een dashboardtegel te selecteren (meer informatie hierover volgt later).

**Eén** rapport

* kan worden gekoppeld aan meerdere dashboards (tegels die zijn vastgemaakt vanuit dat rapport, kunnen worden weergegeven in meerdere dashboards) en
* kan worden gemaakt van gegevens uit één gegevensset. (Een kleine uitzondering hierop is dat Power BI Desktop meer dan één gegevensset in één rapport kan combineren en dat dat rapport kan worden geïmporteerd in Power BI.)
  
  ![](media/service-basic-concepts/drawing3new.png)

## <a name="dashboards"></a>Dashboards
Een *dashboard* is iets wat u maakt of iets wat een collega maakt en met u deelt. Het dashboard bestaat uit één canvas dat nul of meer tegels en widgets bevat. Elke tegel geeft één [visualisatie](power-bi-report-visualizations.md) weer die is gemaakt van een gegevensset en die is vastgemaakt aan het dashboard. Er zijn tal van manieren om tegels aan uw dashboard toe te voegen. Teveel om in dit overzichtsonderwerp te bespreken. Zie [Dashboardtegels in Power BI](service-dashboard-tiles.md) voor meer informatie. 

'Uw' dashboards worden in de navigatiebalk weergegeven onder de kop **Dashboards**. 'Uw' betekent dat ze toegankelijk voor u zijn. Het hoeft niet te betekenen dat u ze hebt gemaakt. Elk dashboard vertegenwoordigt een aangepaste weergave of een subset van de onderliggende gegevenssets.  Als eigenaar van het dashboard bent, hebt u ook toegang tot een of meer onderliggende gegevenssets en worden deze in de navigatiebalk weergegeven onder **Gegevenssets**.  Als het dashboard met u is gedeeld, wordt er een pictogram voor delen ![](media/service-basic-concepts/sharing-icon.png) naast het dashboard weergegeven. Daarnaast is het mogelijk dat de onderliggende gegevenssets in uw navigatiebalk worden vermeld. Dit is afhankelijk van hoe het dashboard is gedeeld.

> [!NOTE]
> In de sectie Dashboards met tegels vindt u meer informatie over vastmaken en tegels.
> 
> 

**Eén** dashboard

* kan visualisaties weergeven uit diverse gegevenssets,
* uit verschillende rapporten en
* en kan visualisaties weergeven die zijn vastgemaakt vanuit andere hulpprogramma's (bijvoorbeeld Excel).
  
  ![](media/service-basic-concepts/drawing1.png)

### <a name="dig-deeper"></a>Dieper graven:
**U kunt een [compleet nieuw dashboard maken](service-dashboard-create.md)**  (een leeg dashboard) en vervolgens gegevens ophalen. 

**U of uw collega's kunnen een dashboard maken en dit vervolgens [delen](service-share-dashboards.md)** . Wanneer u de uitnodiging accepteert, wordt het gedeelde dashboard (en eventuele bijbehorende rapporten en gegevenssets) toegevoegd aan de navigatiebalk. U hebt Power BI Pro nodig om dashboard te kunnen delen, maar ook om een gedeeld dashboard weer te geven.

**Sommige dashboards worden geïmporteerd met de gegevensset of worden gemaakt wanneer u verbinding maakt met de gegevensset**. In de wizard **Gegevens ophalen** voor Salesforce wordt u bijvoorbeeld gevraagd of u een dashboard en/of rapport van de gegevensset wilt maken. 

**Waarom zou ik dashboards willen maken?**  Hier volgen slechts enkele van de redenen:

* U kunt in één oogopslag alle benodigde informatie weergeven om een beslissing te nemen.
* U kunt de belangrijkste informatie over uw bedrijf bewaken.
* U kunt er met dashboards voor zorgen dat alle collega's hetzelfde voor ogen hebben en allemaal dezelfde informatie weergeven en gebruiken.
* U kunt met dashboards de status van een bedrijf, product, afdelingen of marketingcampagne, enzovoort in de gaten houden.
* U kunt een gepersonaliseerde weergave van een groter dashboard maken met alle metrische die voor u belangrijk zijn.

## <a name="my-workspace"></a>Mijn werkruimte
We zijn weer terug bij uw Power BI-dashboard en werkruimte. Laten we de onderdelen van de bestemmingspagina voor de Power BI-service eens nader bekijken.

![](media/service-basic-concepts/completenewer.png)

### <a name="1-navigation-bar-navbar"></a>1. **Navigatiebalk**
Gebruik de navigatiebalk om te schakelen tussen de bouwstenen van Power BI: dashboards, rapporten en gegevenssets.  

  ![](media/service-basic-concepts/navpane-new.png)

* Selecteer **Gegevens ophalen** om [gegevenssets, rapporten en dashboards toe te voegen aan Power BI](service-get-data.md).
* U kunt de navigatiebalk uitvouwen of samenvouwen met dit pictogram ![](media/service-basic-concepts/expand-icon.png).
* Gebruik **Zoeken** om specifieke items in de navigatiebalk te zoeken.
* Selecteer een pluspictogram ![](media/service-basic-concepts/pbi_nancy_plus.png) om een nieuw dashboard te maken of een nieuwe gegevensset op te halen.
* De vermelde **dashboards, rapporten** en **gegevenssets** zijn beschikbaar voor gebruik.  Gedeelde dashboards zijn alleen-lezen en worden aangeduid met het pictogram voor delen![](media/service-basic-concepts/sharing-icon.png).
* De namen van dashboards, rapporten en gegevenssets komen doorgaans overeen met de naam van het onderliggende gegevenssetbestand. Desgewenst kunt u de [naam wijzigen](service-rename.md).
* Klik met de rechtermuisknop op een dashboard, rapport of gegevensset om contextafhankelijke menu weer te geven. 
  
  ![](media/service-basic-concepts/menu.png)

Eén klik

* een kop samenvouwen of uitvouwen
* een dashboard weergeven
* een rapport openen in de leesweergave
* een gegevensset verkennen

### <a name="2-dashboard-with-tiles"></a>2. **Dashboard met tegels**
Dashboards bestaan uit [tegels](service-dashboard-tiles.md).  Tegels worden gemaakt in een rapport in de leesweergave, in Q&A of in andere dashboards en kunnen worden vastgemaakt vanuit Excel, SSRS en meer. Een speciaal type tegel, een [widget](service-dashboard-add-widget.md), wordt rechtstreeks aan het dashboard toegevoegd. De tegels die worden weergegeven op een dashboard, daar bewust neergezet door een maker of eigenaar van een rapport.  De bewerking waarmee een tegel wordt toegevoegd aan een dashboard, noemen we *vastmaken*.

![](media/service-basic-concepts/canvas.png)

Zie **Dashboards** (hierboven) voor meer informatie.

### <a name="3-qa-question-box"></a>3. **Q&A-vragenvak**
U kunt uw gegevens onder andere verkennen door vragen te stellen die door Power BI Q&A worden beantwoord de vorm van een visualisatie. Q&A kan niet worden gebruikt om inhoud toe te voegen aan een rapport. Er kan alleen inhoud aan dashboards worden toegevoegd in de vorm van tegels.

U zoekt met Q&A naar antwoorden in een of meer gegevenssets die zijn verbonden met het dashboard.  Een verbonden gegevensset is een gegevensset waarvoor ten minste één tegel is vastgemaakt aan het desbetreffende dashboard.

![](media/service-basic-concepts/qna.png)

Zodra u een vraag begint te typen, wordt u door Q&A omgeleid naar Q&A-pagina. Terwijl u typt, helpt Q&A u de juiste vraag te stellen en het antwoord te zoeken met herformuleringen, automatisch doorvoeren en suggesties. Wanneer u een gewenste visualisatie (antwoord) hebt gevonden, kunt u deze vastmaken aan uw dashboard. Zie [Q&A in Power BI](service-q-and-a.md) voor meer informatie.

### <a name="4-full-screen-notifications-settings-downloads-help-and-feedback"></a>4. **Volledig scherm, Meldingen, Instellingen, Downloaden, Help en Feedback**
De pictogrammen in de rechterbovenhoek zijn uw resources voor instellingen, meldingen, downloads, hulp en feedback aan het Power BI-team. Selecteer de dubbele pijl om het dashboard te open in een **volledig scherm**.  

![](media/service-basic-concepts/help-new.png)

### <a name="5-dashboard-title-aka-what-dashboard-is-active"></a>5. **Dashboardtitel** (oftewel welk dashboard is actief?)
Het is niet altijd eenvoudig om te achterhalen welk dashboard actief is.  De titel van het dashboard wordt weergegeven op de pagina met een weergave van het dashboard, op de Q&A-pagina, in de bewerkings- en leesweergave van het rapport en bij het openen van een gegevensset.   

![](media/service-basic-concepts/dash-title-new.png)

### <a name="6-office-365-app-launcher"></a>6. **Startprogramma voor de Office 365-app**
Het startprogramma voor apps is ontworpen om naar uw Office 365-apps te gaan.

![](media/service-basic-concepts/basicconcepts2-newer.png)

### <a name="7-power-bi-home"></a>7. **Power BI-startknop**
Hiermee keert u terug naar het laatste dashboard dat u hebt bekeken.

   ![](media/service-basic-concepts/version-new.png)

### <a name="8-options"></a>8. **Opties**
Dit gedeelte van de werkruimte bevat pictogrammen voor interactie met het dashboard.  Als u het beletselteken naast **Tegel toevoegen**, **Favoriet** en **Delen** selecteert, worden er onder andere opties weergegeven waarmee u het dashboard kunt dupliceren, afdrukken en vernieuwen.

   ![](media/service-basic-concepts/options.png)

## <a name="next-steps"></a>Volgende stappen
[Aan de slag met Power BI](service-get-started.md)  
[Power BI-video's](videos.md)  
[Wat is Power BI Premium?](service-premium.md)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

