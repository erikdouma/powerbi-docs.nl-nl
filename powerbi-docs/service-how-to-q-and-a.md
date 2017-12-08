---
title: De Q&A-functie van Power BI gebruiken
description: De Q&A-functie van Power BI gebruiken
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
editor: 
tags: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 09/25/2017
ms.author: mihart
ms.openlocfilehash: a6736916a4bb2e94c1f5e1e3c3c3e5339cf990ec
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2017
---
# <a name="how-to-use-power-bi-qa"></a>De Q&A-functie van Power BI gebruiken
## <a name="ask-questions-of-your-data-using-natural-language"></a>In natuurlijke taal vragen stellen over uw gegevens
Begin op een dashboard. Het Q&A-vraagvak is de locatie waar u uw vraag in natuurlijke taal typt. Q&A herkent de woorden die u typt, en zoekt uit waar (in welke gegevensset) het antwoord kan worden gevonden. Ook helpt Q&A u uw vraag te formuleren door middel van automatisch aanvullen, anders formuleren en andere tekstuele en visuele hulpmiddelen.

![](media/service-how-to-q-and-a/powerbi-qna.png)

Het antwoord op uw vraag wordt weergegeven als een interactieve visualisatie en wordt bijgewerkt als u de vraag wijzigt.

Q&A is interactief en zelfs leuk, en u zult zien dat één vraag heel vaak zal leiden tot vele andere vragen, aangezien de visualisaties interessante dingen opleveren om te volgen. Kijk hoe Amanda demonstreert hoe ze met Q&A visuals maakt, verder met deze visuals doorgaat en de visuals aan dashboards vastmaakt.

> [!NOTE]
> Q&A is ook beschikbaar in de [Microsoft Power BI-app voor iOS op iPads, iPhones en iPod Touch-apparaten](mobile-apps-ios-qna.md).
> 
> 

<iframe width="560" height="315" src="https://www.youtube.com/embed/qMf7OLJfCz8?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>

## <a name="use-natural-language-to-ask-questions-about-your-data"></a>Natuurlijke taal gebruiken om vragen over uw gegevens te stellen
1. Plaats de cursor in het vraagvak. Voordat u begint te typen, worden in een nieuw scherm suggesties weergegeven om u te helpen uw vraag te formuleren.
   
   ![](media/service-how-to-q-and-a/powerbi-qna-cursor.png)  
   
   Deze lijst bevat:  
   a.  de vragen die zijn gebruikt om [tegels ](service-dashboard-tiles.md)te maken die al aan het dashboard zijn vastgemaakt, en  
   b.  de naam van tabellen in de [onderliggende gegevensset(s)](service-get-data.md).  
   
   U kunt altijd een van deze vragen als beginpunt kiezen en de vraag verder verfijnen voor het specifieke antwoord dat u zoekt. U kunt ook een tabelnaam gebruiken om een nieuwe vraag te formuleren.
2. Maak een selectie in de vervolgkeuzelijst of begin uw eigen vraag te typen.  
   
   ![](media/service-how-to-q-and-a/powerbi-qna-list.png)
3. Als u een vraag typt, kiest de Q&A-functie van Power BI de beste [visualisatie ](power-bi-visualization-types-for-reports-and-q-and-a.md)om uw antwoord weer te geven. De visualisatie wordt dynamisch gewijzigd als u de vraag wijzigt. Ook wordt u bij het formuleren van de vraag geholpen door middel van automatisch aanvullen, anders formuleren van de vraag en andere tekstuele en visuele hulpmiddelen.  
   ![](media/service-how-to-q-and-a/powerbi-qna-viz.png)
4. Wanneer u een query typt, zoekt Power BI een antwoord in de gegevenssets die een tegel op dat dashboard hebben.  Als alle tegels van *gegevenssetA* zijn, is het antwoord afkomstig van *gegevenssetA*.  Als er tegels van *gegevenssetA* en *gegevenssetB* zijn, wordt het beste antwoord in deze twee gegevenssets gezocht.
   
   > [!TIP]
   > Wanneer u dus slechts een tegel van *gegevenssetA* hebt en u deze van uw dashboard verwijdert, heeft Q&A niet langer toegang tot *gegevenssetA*.
   > 
   > 
5. Wanneer u tevreden bent met het resultaat, [maakt u de visualisatie aan een dashboard vast](service-dashboard-pin-tile-from-q-and-a.md) door het speldpictogram in de rechterbovenhoek te selecteren. Als het dashboard met u is gedeeld of deel uitmaakt van een app, kunt u de visualisatie niet vastmaken.
   
   ![](media/service-how-to-q-and-a/pbi_qna_finish-typing-question.jpg)

### <a name="tell-qa-which-visualization-to-use"></a>Laat Q&A weten welke visualisatie moet worden gebruikt.
U kunt met Q&A niet alleen uw gegevens voor zichzelf laten spreken, u kunt ook aangeven hoe de gegevens moeten worden weergegeven. U hoeft alleen maar 'as a <visualization type>' aan het einde van uw vraag te typen.  Bijvoorbeeld 'show inventory volume by plant as a map' en 'show total inventory as a card'.  Probeer het zelf maar eens.

## <a name="how-does-qa-know-how-to-answer-questions"></a>Hoe weet Q&A hoe vragen moeten worden beantwoord?
### <a name="which-datasets-does-qa-use"></a>Welke gegevenssets gebruikt Q&A?
Hoe weet Q&A hoe gegevensspecifieke vragen moeten worden beantwoord? Q&A baseert zich op de namen van de tabellen, kolommen en berekende velden in de onderliggende gegevensset. Het is dus belangrijk welke naam u (of de eigenaar van de gegevensset) aan dingen geeft. 

Stel bijvoorbeeld dat u een Excel-tabel genaamd Sales hebt en dat deze tabel de kolommen Product, Month, Units Sold, Gross Sales en Profit bevat. U kunt dan over elk van deze entiteiten een vraag stellen.  U kunt vragen stellen als 'show *sales*', 'total *profit* by *month*', 'sort *products* by *units sold*' enzovoort.

Q&A kan vragen beantwoorden die zijn gebaseerd op hoe uw gegevensset is georganiseerd. Hoe werkt dit voor gegevens in Salesforce? Als u verbinding met uw salesforce.com-account maakt, genereert Power BI automatisch een dashboard.  Bekijk voordat u vragen gaat stellen met Q&A de gegevens die worden weergegeven in de dashboardvisualisaties, en ook de gegevens die worden weergegeven in de Q&A-vervolgkeuzelijst.

* Als de aslabels en -waarden van de visualisaties 'sales', 'account', 'month' en 'opportunities' bevatten, kunt u vragen stellen zoals: ‘Which *account* has the highest *opportunity*, or show *sales* by month as a bar chart.’
* Als de vervolgkeuzelijst 'salesperson', 'state' en 'year' bevat, kunt u vragen stellen zoals: which *salesperson* had the lowest *sales* in *Florida* in *2013*.

Als u de prestatiegegevens van de website in Google Analytics hebt, kunt u Q&A vragen over de tijd die aan een webpagina is besteed, het aantal unieke paginabezoeken en de percentages gebruikersbetrokkenheid. Of als u query's hebt voor demografische gegevens, kunt u vragen stellen over leeftijd en huishoudinkomens per locatie.

### <a name="which-visualization-does-qa-use"></a>Welke visualisatie gebruikt Q&A?
Q&A kiest de beste visualisatie op basis van de gegevens die worden weergegeven. Soms worden gegevens in de onderliggende gegevensset(s) gedefinieerd als een bepaald type of een bepaalde categorie waardoor het voor Q&A duidelijker wordt hoe de gegevens moeten worden weergegeven. Als gegevens bijvoorbeeld zijn gedefinieerd als een gegevenstype, ligt het voor de hand ze als een lijndiagram weer te geven. Gegevens die zijn gecategoriseerd als een plaats, zullen eerder als een kaart worden weergegeven.

U kunt ook zelf bij de vraag opgeven welke visualisatie moet worden gebruikt. Het is echter niet altijd mogelijk de gegevens in het door u gevraagde type visualisatie weer te geven.

Zie [Tips voor het stellen van vragen](service-q-and-a-tips.md) voor informatie over trefwoorden die door Q&A worden herkend.

## <a name="next-steps"></a>Volgende stappen
Terug naar [Q&A in Power BI](service-q-and-a.md)  
[Zelfstudie: Q&A gebruiken met het Retail Sales-voorbeeld](power-bi-visualization-introduction-to-q-and-a.md)  
[Tips voor het stellen van vragen in Q&A](service-q-and-a-tips.md)  
[Een werkmap voorbereiden voor Q&A](service-prepare-data-for-q-and-a.md)  
[Een tegel vastmaken aan het dashboard vanuit Q&A](service-dashboard-pin-tile-from-q-and-a.md)  

