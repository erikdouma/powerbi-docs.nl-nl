---
title: 'Voorbeeld van klantwinstgevendheid in Power BI: een rondleiding'
description: 'Voorbeeld van klantwinstgevendheid in Power BI: een rondleiding'
services: powerbi
documentationcenter: 
author: amandacofsky
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
ms.date: 10/29/2017
ms.author: mihart
ms.openlocfilehash: 9a100b7d13c11a8bd066b72a570f45d0c2bc08be
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2017
---
# <a name="customer-profitability-sample-for-power-bi-take-a-tour"></a>Voorbeeld van klantwinstgevendheid in Power BI: een rondleiding
Het inhoudspakket Voorbeeld van klantwinstgevendheid bevat een dashboard, rapport en gegevensset voor een bedrijf dat marketingmateriaal maakt. Dit dashboard is gemaakt door een CFO om de belangrijkste metrische gegevens te verzamelen over haar vijf business unit managers, producten, klanten en brutomarges. In een oogopslag kan ze zien welke factoren van invloed zijn op de winstgevendheid.

Dit voorbeeld is onderdeel van een serie die laat zien hoe u Power BI kunt gebruiken met bedrijfsgegevens, -rapporten en -dashboards. Dit zijn echte gegevens die afkomstig zijn van obviEnce ([www.obvience.com)](http://www.obvience.com/) die zijn geanonimiseerd.

U kunt ook [alleen de gegevensset (Excel-werkmap)](http://go.microsoft.com/fwlink/?LinkId=529781) voor dit voorbeeld downloaden.  
![](media/sample-customer-profitability/power-bi-dash.png)

## <a name="what-is-our-dashboard-telling-us"></a>Wat vertelt het dashboard ons?
### <a name="company-wide-dashboard-tiles"></a>Dashboardtegels voor de gehele onderneming
Deze tegels geven onze CFO een weergave van metrische gegevens op hoog niveau die belangrijk voor haar zijn.  Wanneer ze iets interessants ziet, kan ze een tegel selecteren om dieper in de gegevens te graven.

1. De brutomarge van het bedrijf is 42,5 %.
2. We hebben 80 klanten.
3. We verkopen 5 verschillende producten.
4. We hadden ons laagste omzetvariantiepercentage ten opzichte van budget in februari, gevolgd door het hoogste in maart.
5. Het grootste deel van onze omzet is afkomstig uit de regio’s Oost en Noord. Brutomarge heeft nooit het budget overschreden, waarbij voor ER-0 en MA-0 enig verder onderzoek nodig is.
6. Totale omzet van het jaar is bijna gelijk aan het budget.

### <a name="manager-specific-dashboard-tiles"></a>Managerspecifieke dashboardtegels
Deze tegels bieden een team-scorecard. De CFO moet haar managers blijven volgen. Deze tegels bieden haar een overzicht op hoog niveau van de winst - op grond van het brutomargepercentage. Als de trend in het brutomargepercentage voor een manager afwijkt van de verwachting, dan kan ze dit verder onderzoeken.

Het brutomargepercentage van Annelie is het laagste, maar we zien een constante stijging sinds maart. Valery heeft haar brutomargepercentage daarentegen aanzienlijk zien afnemen. En Andrew had een sterk wisselend jaar. Klik op een van de managerspecifieke tegels om het onderliggende rapport te openen. Het rapport heeft 3 pagina's en opent met de pagina Industry Margin Analysis (analyse van de marge in de bedrijfstak).

## <a name="explore-the-pages-in-the-report"></a>De pagina's in het rapport verkennen
Ons rapport heeft 3 pagina's:

* Team-scorecard richt zich op de prestaties van de 5 managers en hun bedrijfscijfers.
* Analyse van marge in de bedrijfstak biedt een manier om onze winst te analyseren ten opzichte van de gehele bedrijfstak.
* Executive-scorecard biedt een weergave van elk van onze managers met een indeling die geschikt is voor Cortana.

### <a name="team-scorecard-page"></a>De pagina Team-scorecard
![](media/sample-customer-profitability/customer2.png)

Laten we in detail kijken naar twee van de teamleden en zien welke inzichten kunnen worden verkregen. Selecteer in de slicer aan de linkerkant de naam Andrew om de rapportpagina zo te filteren dat alleen gegevens over Andrew worden weergegeven.

* Kijk voor een snelle KPI naar Andrews **Omzetstatus** - deze is groen. Zijn prestaties zijn goed.
* Het vlakdiagram Omzetvariatiepercentage ten opzichte van budget per maand laat zien dat met uitzondering van een dip in februari Andrew het over het algemeen prima doet. Zijn dominante regio is Oost en hij verwerkt 49 klanten en 5 (van de 7) producten. Zijn brutomargepercentage is niet het hoogste of laagste.
* De waarde bij Omzet dit jaar en omzetvariantiepercentage ten opzichte van budget per maand laat een constante gelijkmatige winst zien. Maar als op het vierkant voor **Centraal** in de regiotreemap klikt om te filteren, ontdekt u dat Andrew alleen in maart omzet heeft en alleen in Indiana. Is dit de bedoeling of is dit iets dat moet worden onderzocht?

Nu naar Valery. Selecteer in de slicer de naam Valery om de rapportpagina zo te filteren dat alleen gegevens over haar worden weergegeven.  
![](media/sample-customer-profitability/customer3.png)

* U ziet de rode KPI voor **Status omzet dit jaar**. Dit moet zeker verder worden onderzocht.
* Haar omzetvariantie schetst ook een zorgwekkend beeld - ze haalt haar inkomstenmarges niet.
* Valery heeft slechts 9 klanten, verwerkt slechts 2 producten en werkt bijna exclusief met klanten in het noorden. Deze specialisatie kan de grote schommelingen in haar metrische gegevens verklaren.
* Als u het vierkant **Noord** in de treemap selecteert, kunt u zien dat de brutomarge van Valery in het noorden consistent is met haar totale marge.
* Als u de andere vakken **Regio** selecteert, verschijnt een interessant verhaal: haar brutomargepercentage reikt van 23% tot 79% en haar inkomstencijfers zijn in alle regio's behalve het noorden sterk seizoensgebonden.

Blijf spitten om erachter te komen waarom het gebied van Valery niet goed presteert. Bekijk de regio's, de andere bedrijfsonderdelen en de volgende pagina in het rapport Analyse van marge in de bedrijfstak.

### <a name="industry-margin-analysis"></a>Analyse van marge in de bedrijfstak
Deze rapportpagina bevat een ander deel van de gegevens. Hier wordt gekeken naar de brutomarge voor de gehele bedrijfstak, opgedeeld per segment. De CFO gebruikt deze pagina om de metrische gegevens van het bedrijf en bedrijfsonderdelen te vergelijken met de gegevens uit de bedrijfstak om trends en winstgevendheid te kunnen verklaren. U vraagt zich misschien af waarom een vlakdiagram Brutomarge per maand en naam van executive op deze pagina staat, aangezien dit teamspecifiek is. Doordat dit diagram hier staat, kunnen we de pagina filteren per business unit manager.  
![](media/sample-customer-profitability/customer6.png)

Hoe verschilt de winstgevendheid per bedrijfstak? Hoe worden de producten en klanten onderverdeeld per bedrijfstak? Selecteer een of meer bedrijfstakken linksboven. (Start vanaf de bedrijfstak CPG) Als u het filter wilt wissen, selecteert u het gumpictogram.

Op de bellengrafiek zoekt de CFO naar de grootste bellen, omdat deze de grootste invloed hebben op de omzet. Doordat de pagina per manager kan worden gefilterd door op hun namen te klikken in het vlakdiagram, kan de invloed van elke manager per branche eenvoudig worden bekeken.

* De invloed van Andrew omvat veel verschillende bedrijfstaksegmenten met breed uiteenlopende brutomargepercentages (de meeste aan de positieve kant) en variantiepercentages. 
* De grafiek van Annelie is vergelijkbaar, behalve dat ze zich op slechts een handvol bedrijfstakken richt met een focus op het segment Federal en het product Gladius. 
* Carlos richt zich duidelijk op het segment Services, met een hoge winst. Hij heeft het variantiepercentage sterk verbeterd voor het High Tech-segment en een voor hem nieuw segment, Industrieel, vertoont uitzonderlijk goede prestaties in vergelijking met het budget. 
* Tina werkt met een handvol segmenten en heeft het hoogste brutomargepercentage. De voornamelijk kleine bellen laten echter zien dat haar invloed op de winstgevendheid van het bedrijf minimaal is. 
* Valery, die verantwoordelijk is voor slechts één product, werkt in slechts 5 bedrijfstakken. Haar invloed voor de bedrijfstak is seizoensgebonden, maar produceert altijd een grote bel, die wijst op een grote invloed op de winstgevendheid van het bedrijf. Biedt de bedrijfstak een verklaring voor haar negatieve prestaties?

### <a name="executive-scorecard"></a>Executive-scorecard
Deze pagina wordt opgemaakt als een antwoordkaart voor Cortana. Zie [Antwoordkaarten maken voor Cortana](service-cortana-answer-cards.md) voor meer informatie.

## <a name="dig-into-the-data-by-asking-questions-with-qa"></a>Dieper graven in de gegevens door vragen te stellen met Q&A
Voor onze analyse zou het handig zijn als we bepalen welke bedrijfstak de meeste omzet voor Valery genereert. Hiervoor gebruiken we Q&A.

1. Selecteer **Power BI** in de bovenste navigatiebalk om terug te keren naar het dashboard.
2. Selecteer het vakje Q&A bovenin het dashboard.
   
    ![](media/sample-customer-profitability/customer4.png)
3. Typ **totale omzet per branche voor Valery**. Kijk hoe de visualisatie wordt bijgewerkt terwijl u de vraag typt.
   
    ![](media/sample-customer-profitability/customer5.png)
   
   Distributie is het grootste opbrengstgebied voor Valery.

### <a name="dig-deeper-by-adding-filters"></a>Dieper graven door filters toe te voegen
Laten we kijken naar de branche *Distributie*.  

1. Ga terug naar het dashboard en selecteer het vlakdiagram met de brutomargetrend van Andrew. Het rapport wordt geopend op de pagina Analyse van marge in de bedrijfstak.
2. Vouw het filterdeelvenster rechts uit zonder visualisaties te selecteren op de rapportagepagina. In het deelvenster Filters mogen alleen filters op paginaniveau worden weergegeven.  
   
   ![](media/sample-customer-profitability/power-bi-filters.png)
3. Zoek het filter voor **bedrijfstak** en selecteer de pijl om de lijst uit te vouwen. We gaan een paginafilter voor de bedrijfstak Distributie toevoegen. Wis eerst alle selecties door het selectievakje **Alles selecteren** uit te schakelen. Selecteer vervolgens **Distributie.**  
   
   ![](media/sample-customer-profitability/customer7.png)
4. Het vlakdiagram Brutomarge per maand en naam executive laat zien dat alleen Valery en Tina klanten hebben in deze bedrijfstak en dat Valery alleen van juni tot en met november met deze bedrijfstak heeft gewerkt.   
5. Selecteer **Tina** en vervolgens **Valery** in de legenda van het vlakdiagram Brutomarge per maand en naam executive. U ziet dat het deel van Tina van de Totale omzet per product echt klein is vergeleken met dat van Valery. 
6. Als u de werkelijke omzet wilt bekijken, gaat u terug naar het dashboard en gebruikt u Q&A om de **totale opbrengsten voor distributie van scenario per executive** op te vragen.  
   
   ![](media/sample-customer-profitability/customer8.png)

We kunnen ook andere bedrijfstakken verkennen en zelfs klanten toevoegen aan onze visuele elementen om inzicht te krijgen in de oorzaken voor de prestaties van Valery.

Dit is een veilige omgeving om in te spelen. U kunt er altijd voor kiezen om de wijzigingen niet op te slaan. Als u deze wel opslaat, kunt u altijd naar **Gegevens ophalen** gaan voor een nieuwe kopie van dit voorbeeld.

## <a name="next-steps-connect-to-your-data"></a>Volgende stappen: koppelen aan uw gegevens
We hopen dat deze rondleiding heeft laten zien hoe Power BI-dashboards, Q&A en rapporten inzicht kunnen geven in klantgegevens. Nu is het uw beurt: aan uw eigen gegevens koppelen. Met Power BI kunt u koppelen met een groot aantal gegevensbronnen. Meer informatie over [Aan de slag met Power BI](service-get-started.md).

[Terug naar de voorbeelden in Power BI](sample-datasets.md)  

