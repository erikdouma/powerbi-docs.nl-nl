---
title: Inzoomen op een visualisatie in Power BI
description: In dit document wordt beschreven hoe u kunt inzoomen op een visualisatie in Microsoft Power BI-service en Power BI Desktop.
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: MNAaHw4PxzE
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/18/2017
ms.author: mihart
ms.openlocfilehash: 83c63ee2bed5ae7674223cf2fc3f9241308926e9
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/15/2017
---
# <a name="drill-down-in-a-visualization-in-power-bi"></a>Inzoomen op een visualisatie in Power BI
## <a name="drill-down-requires-a-hierarchy"></a>Voor inzoomen is een hiërarchie vereist
Wanneer een visueel element een hiërarchie heeft, kunt u inzoomen om extra details te onthullen. U kunt bijvoorbeeld een visualisatie hebben die kijkt naar het aantal Olympische medailles door een hiërarchie bestaande uit sport, discipline en gebeurtenis. Standaard zou de visualisatie het aantal medailles weergeven per sport -- gymnastiek, skiën, watersport, enzovoort. Maar omdat deze een hiërarchie heeft, zou het selecteren van één van de visuele elementen (zoals een balk, lijn of bel) een steeds gedetailleerder beeld weergeven. Selecteer het element **Watersport** om de gegevens voor zwemmen, duiken en waterpolo te bekijken.  Selecteer het element **Duiken** om de details voor duikplank, platform en gesynchroniseerde duikgebeurtenissen te bekijken.

U kunt hiërarchieën toevoegen aan rapporten die u bezit, maar niet aan rapporten die met u worden gedeeld.
Weet u niet zeker welke Power BI-visualisaties een hiërarchie bevatten?  Beweeg met de muisaanwijzer over een visualisatie en als u deze besturingselementen voor inzoomen in de bovenhoeken ziet, heeft uw visualisatie een hiërarchie.

![](media/power-bi-visualization-drill-down/power-bi-drill-icon4.png)  ![](media/power-bi-visualization-drill-down/power-bi-drill-icon2.png)  ![](media/power-bi-visualization-drill-down/power-bi-drill-icon3.png)
![](media/power-bi-visualization-drill-down/power-bi-drill-icon5.png) ![](media/power-bi-visualization-drill-down/power-bi-drill-icon6.png)  

Data zijn een uniek type hiërarchie. Wanneer u een datumveld aan een visualisatie toevoegt, voegt Power BI automatisch een tijdshiërarchie met jaar, kwartaal, maand en dag. Zie voor meer informatie [Visuele hiërarchieën en inzoomen](guided-learning/visualizations.yml#step-18) of bekijk de onderstaande video.

  <iframe width="560" height="315" src="https://www.youtube.com/embed/MNAaHw4PxzE?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>

> [!NOTE]
> Bekijk de video [Hiërarchieën maken en toevoegen](https://youtu.be/q8WDUAiTGeU) voor meer informatie over het maken van hiërarchieën met Power BI Desktop
> 
> 

## <a name="two-methods-to-drill-down"></a>Twee methoden om in te zoomen
Er zijn twee verschillende manieren voor inzoomen (en uitzoomen) in uw visualisatie.  Beiden worden beschreven in dit artikel. Met beide methoden bereikt u hetzelfde, dus gebruik de methode die u het handigst vindt.

> [!NOTE]
> Open hiervoor het [Voorbeeld van een retailanalyse](sample-datasets.md) in Power BI-service en maak een treemap op basis van **Totaal aantal eenheden dit jaar** (waarden) per **Gebied**, **Plaats**, **Postcode**en **Naam** (Groep).  
> 
> 

## <a name="method-1-for-drill-down"></a>Methode 1 voor inzoomen
Deze methode maakt gebruik van de inzoompictogrammen die in de bovenste hoeken van de visualisatie zelf verschijnen.

1. Open in Power BI een rapport in de [Leesweergave](service-report-open-in-reading-view.md) of [Bewerkweergave](service-reading-view-and-editing-view.md). Voor inzoomen is een visualisatie met een hiërarchie vereist. 
   
   Een hiërarchie wordt weergegeven in de onderstaande animatie.  De visualisatie heeft een hiërarchie die bestaat uit gebied, plaats, postcode en plaatsnaam. Elk gebied heeft één of meer steden, elke stad heeft één of meer postcodes, enzovoort. Standaard geeft de visualisatie alleen de gebiedsgegevens weer, omdat *Gebied* als eerste in de lijst voorkomt.
   
   ![](media/power-bi-visualization-drill-down/power-bi-hierarcy-list.png)
2. Selecteer het pijlpictogram in de rechterbovenhoek van de visualisatie om inzoomen in te schakelen. Wanneer het pictogram donker is, is inzoomen ingeschakeld. Als u inzoomen niet inschakelt, zal het selecteren van een visueel element (zoals een balk of bel) de andere grafieken op de rapportagepagina kruislings filteren.    
   
   ![](media/power-bi-visualization-drill-down/power-bi-drill-icon.png)
3. Als u op ***één veld per keer*** wilt inzoomen, klikt u op één van de elementen in uw visualisatie. In een staafdiagram betekent dit dat u op één van de balken klikt en in een treemap betekent dit klikken op één van de *bladeren*. U ziet dat de titel wordt gewijzigd tijdens het in- en uitzoomen. In deze animatie verandert het van ‘Totaal aantal eenheden dit jaar per gebied’ naar ‘Totaal aantal eenheden dit jaar per gebied en plaats’ naar ‘Totaal aantal eenheden dit jaar per gebied, plaats en postcode’ naar ‘Totaal aantal eenheden dit jaar per gebied, plaats, postcode en naam’. En om weer uit te zoomen, selecteert u het pictogram **Uitzoomen** ![](media/power-bi-visualization-drill-down/power-bi-drill-icon5.png)in de linkerbovenhoek van de visualisatie zoals hieronder wordt weergegeven.
   
   ![](media/power-bi-visualization-drill-down/drill.gif)
4. Als u op ***alle velden in één keer wilt inzoomen***, selecteert u de dubbele pijl in de linkerbovenhoek van de visualisatie.
   
   ![](media/power-bi-visualization-drill-down/pbi_drillall.png)
5. Als u weer wilt uitzoomen, selecteert u de pijl omhoog in de linkerbovenhoek van de visualisatie.
   
   ![](media/power-bi-visualization-drill-down/pbi_drillup2.png)

## <a name="method-2-for-drill-down"></a>Methode 2 voor inzoomen
Deze methode maakt gebruik van de vervolgkeuzelijst **Verkennen** in de bovenste Power BI-menubalk.

1. Open in Power BI een rapport in de [Leesweergave](service-report-open-in-reading-view.md) of [Bewerkweergave](service-reading-view-and-editing-view.md). Voor inzoomen is een visualisatie met een hiërarchie vereist. 
   
   Een hiërarchie wordt weergegeven in de onderstaande afbeelding.  De visualisatie heeft een hiërarchie die bestaat uit gebied, plaats, postcode en plaatsnaam. Elk gebied heeft één of meer steden, elke stad heeft één of meer postcodes, enzovoort. Standaard geeft de visualisatie alleen de gebiedsgegevens weer, omdat *Gebied* als eerste in de lijst voorkomt.
   
   ![](media/power-bi-visualization-drill-down/power-bi-hierarcy-list.png)
2. Als u inzoomen wilt inschakelen, selecteert u een visualisatie om deze actief te maken en vervolgens in de Power BI-menubalk bovenaan **Verkennen** > **Inzoomen**. Het pictogram voor inzoomen in de rechterbovenhoek van de visualisatie verandert in een zwarte achtergrond. ![](media/power-bi-visualization-drill-down/power-bi-drill-icon2.png)  
   
   ![](media/power-bi-visualization-drill-down/power-bi-explore2.png)
3. Eenmaal ingeschakeld kunt u op één veld tegelijk inzoomen door een van de bladeren van de treemap te selecteren. In dit voorbeeld heb ik het gebied met de naam **NC** geselecteerd om het totale aantal verkochte eenheden van dit jaar in North Carolina per plaats te bekijken.
   
   ![](media/power-bi-visualization-drill-down/power-bi-drilldown-1.png)
4. Als u alle velden in één keer wilt inzoomen, selecteer dan **Verkennen** > **Volgend niveau weergeven**.
   
   ![](media/power-bi-visualization-drill-down/power-bi-show-next-level.png)
5. Als u wilt uitzoomen, selecteert u **Verkennen** > **Uitzoomen**.
   
   ![](media/power-bi-visualization-drill-down/power-bi-drill-up2.png)
6. Voor een overzicht van de gegevens die worden gebruikt om het visuele element te maken, selecteert u **Gegevens zien**. De gegevens worden weergegeven in een deelvenster onder het visuele element. Dit deelvenster blijft zichtbaar wanneer u op het visuele element blijft in- en uitzoomen. Zie voor meer informatie [Gegevens weergeven die worden gebruikt voor het maken van het visuele element](service-reports-show-data.md).

## <a name="considerations-and-limitations"></a>Overwegingen en beperkingen
* Als door het toevoegen van een datumveld aan een visualisatie geen hiërarchie wordt gecreëerd, kan het zijn dat het veld Datum niet daadwerkelijk als datum is opgeslagen. Als het uw eigen gegevensset is, opent u het in de weergave *Gegevens* in Power BI Desktop, selecteert u de kolom met de datum en op het tabblad Model maken wijzigt u het **Gegevenstype** naar **Datum** of **Datum/tijd**. Als het rapport met u is gedeeld, neem dan contact op met de eigenaar om de wijziging aan te vragen.  
  
  ![](media/power-bi-visualization-drill-down/power-bi-change-data-type2.png)

## <a name="next-steps"></a>Volgende stappen
[Visualisaties in Power BI-rapporten](power-bi-report-visualizations.md)

[Power BI-rapporten](service-reports.md)

[Power BI - basisconcepten](service-basic-concepts.md)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

