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
ms.date: 02/26/2018
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: fb834c92953c2cafcbca77bc1b3828b385755bca
ms.sourcegitcommit: 743e44fc8730fea0f7149916080b0c6d7eb6359d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2018
---
# <a name="drill-down-in-a-visualization-in-power-bi"></a>Inzoomen op een visualisatie in Power BI
## <a name="drill-down-requires-a-hierarchy"></a>Voor inzoomen is een hiërarchie vereist
Wanneer een visueel element een hiërarchie heeft, kunt u inzoomen om extra details te onthullen. U kunt bijvoorbeeld een visualisatie hebben die kijkt naar het aantal Olympische medailles door een hiërarchie bestaande uit sport, discipline en gebeurtenis. Standaard zou de visualisatie het aantal medailles weergeven per sport (gymnastiek, skiën, watersport, enzovoort). Maar omdat deze een hiërarchie bevat, zou het selecteren van één van de visuele elementen (zoals een balk, lijn of bel) een steeds gedetailleerder beeld weergeven. Selecteer het element **Watersport** om de gegevens voor zwemmen, duiken en waterpolo te bekijken.  Selecteer het element **Duiken** om de details voor duikplank, platform en gesynchroniseerde duikgebeurtenissen te bekijken.

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
U kunt op twee manieren inzoomen (en uitzoomen) in uw visualisatie.  Beiden worden beschreven in dit artikel. Met beide methoden bereikt u hetzelfde, dus gebruik de methode die u het handigst vindt.

> [!NOTE]
> Open hiervoor het [Voorbeeld van een retailanalyse](sample-datasets.md) in Power BI-service en maak een treemap op basis van **Totaal aantal eenheden dit jaar** (waarden) per **Gebied**, **Plaats**, **Postcode**en **Naam** (Groep).  
> 
> 

## <a name="method-one-for-drill-down"></a>Methode één voor inzoomen
Deze methode maakt gebruik van de inzoompictogrammen die in de bovenste hoeken van de visualisatie zelf verschijnen.

1. Open in Power BI een rapport in de [Leesweergave of Bewerkweergave](service-reading-view-and-editing-view.md). Voor inzoomen is een visualisatie met een hiërarchie vereist. 
   
   Een hiërarchie wordt weergegeven in de onderstaande animatie.  De visualisatie heeft een hiërarchie die bestaat uit gebied, plaats, postcode en plaatsnaam. Elk gebied heeft één of meer plaatsen, elke plaats heeft één of meer postcodes, enzovoort. Standaard geeft de visualisatie alleen de gebiedsgegevens weer, omdat *Gebied* als eerste in de lijst voorkomt.
   
   ![](media/power-bi-visualization-drill-down/power-bi-hierarcy-list.png)
2. Selecteer het pijlpictogram in de rechterbovenhoek van de visualisatie om inzoomen in te schakelen. Wanneer het pictogram donker is, is inzoomen ingeschakeld. Als u inzoomen niet inschakelt, zal het selecteren van een visueel element (zoals een balk of bel) de andere grafieken op de rapportagepagina kruislings filteren.    
   
   ![](media/power-bi-visualization-drill-down/power-bi-drill-icon.png)
3. Als u op **één veld tegelijk** wilt inzoomen, selecteert u een van de elementen in uw visualisatie. In een staafdiagram betekent dit dat u op een van de staven moet klikken. In een treemap betekent dit dat u op een van de **bladeren** moet klikken. U ziet dat de titel wordt gewijzigd tijdens het in- en uitzoomen. In deze animatie wijzigt de titel van Totaal aantal eenheden dit jaar per gebied in Totaal aantal eenheden dit jaar per gebied en plaats en vervolgens in Totaal aantal eenheden dit jaar per gebied, plaats en postcode en in Totaal aantal eenheden dit jaar per gebied, plaats, postcode en naam. Als u weer wilt uitzoomen, selecteert u het pictogram **Uitzoomen** ![](media/power-bi-visualization-drill-down/power-bi-drill-icon5.png) in de linkerbovenhoek van de visualisatie zoals hieronder wordt weergegeven.
   
   ![](media/power-bi-visualization-drill-down/drill.gif)
4. Als u op ***alle velden tegelijk*** wilt inzoomen, selecteert u de dubbele pijl in de linkerbovenhoek van de visualisatie.
   
   ![](media/power-bi-visualization-drill-down/pbi_drillall.png)
5. Als u weer wilt uitzoomen, selecteert u de pijl omhoog in de linkerbovenhoek van de visualisatie.
   
   ![](media/power-bi-visualization-drill-down/pbi_drillup2.png)

## <a name="method-two-for-drill-down"></a>Methode twee voor inzoomen
Voor deze methode wordt gebruikgemaakt van de vervolgkeuzelijst **Verkennen** in de bovenste Power BI-menubalk.

1. Open in Power BI een rapport in de [Leesweergave of Bewerkweergave](service-reading-view-and-editing-view.md). Voor inzoomen is een visualisatie met een hiërarchie vereist. 
   
   Een hiërarchie wordt weergegeven in de onderstaande afbeelding.  De visualisatie heeft een hiërarchie die bestaat uit gebied, plaats, postcode en plaatsnaam. Elk gebied heeft één of meer plaatsen, elke plaats heeft één of meer postcodes, enzovoort. Standaard geeft de visualisatie alleen de gebiedsgegevens weer, omdat *Gebied* als eerste in de lijst voorkomt.
   
   ![](media/power-bi-visualization-drill-down/power-bi-hierarcy-list.png)
2. Als u de functie voor inzoomen wilt inschakelen, selecteert u een visualisatie om deze te activeren en selecteert u vervolgens in de Power BI-menubalk bovenaan **Verkennen** > **Inzoomen**. Het pictogram voor inzoomen in de rechterbovenhoek van de visualisatie verandert in een zwarte achtergrond. ![](media/power-bi-visualization-drill-down/power-bi-drill-icon2.png)  
   
   ![](media/power-bi-visualization-drill-down/power-bi-explore2.png)
3. Eenmaal ingeschakeld kunt u op één veld tegelijk inzoomen door een van de bladeren van de treemap te selecteren. In dit voorbeeld is het gebied met de naam **NC** geselecteerd om het totale aantal verkochte eenheden van dit jaar in North Carolina per plaats te bekijken.
   
   ![](media/power-bi-visualization-drill-down/power-bi-drilldown-1.png)
4. Als u alle velden in één keer wilt inzoomen, selecteer dan **Verkennen** > **Volgend niveau weergeven**.
   
   ![](media/power-bi-visualization-drill-down/power-bi-show-next-level.png)
5. Als u wilt uitzoomen, selecteert u **Verkennen** > **Uitzoomen**.
   
   ![](media/power-bi-visualization-drill-down/power-bi-drill-up2.png)

6. Als u de gegevens wilt zien die worden gebruikt om de visual te maken, selecteert u **Gegevens bekijken**. De gegevens worden weergegeven in een deelvenster onder de visual. Dit deelvenster blijft zichtbaar wanneer u op het visuele element blijft in- en uitzoomen. Zie voor meer informatie [Gegevens weergeven die worden gebruikt voor het maken van het visuele element](service-reports-show-data.md).

## <a name="understanding-the-hierarchy-axis-and-hierarchy-group"></a>Informatie over de hiërarchie-as en de hiërarchiegroep
De hiërarchie-as en de hiërarchiegroep kunt u zien als mechanismen voor het verhogen en verlagen van de granulatie van de gegevens die u wilt weergeven. Alle gegevens die kunnen worden ingedeeld in categorieën en subcategorieën, worden gezien als gegevens met een hiërarchie. Ook datums en tijden vallen hieronder.

U kunt in Power BI aangeven dat een visualisatie over een hiërarchie moet beschikken. Hiervoor selecteert u een of meer gegevensvelden die u aan de bron **As** of aan de bron **Groep** wilt toevoegen, samen met de gegevens die u als gegevensvelden wilt onderzoeken in de bron **Waarden**. Gegevens zijn hiërarchisch als in de linker- en rechterbovenhoek van uw visualisatie de pictogrammen voor de inzoommodus worden weergegeven. 

Er zijn in feite twee typen hiërarchische gegevens:
- Datum- en tijdgegevens: Als u een gegevensveld met gegevenstype Datum/tijd hebt, hebt u al hiërarchische gegevens. Voor elk gegevensveld waarvan de waarden kunnen worden geparseerd in een [datum-/tijd](https://msdn.microsoft.com/library/system.datetime.aspx) structuur, wordt in Power BI automatisch een hiërarchie gemaakt. U hoeft hiervoor alleen een datum-/tijdveld aan de bron **As** of **Groep** toe te voegen.
- Categorische gegevens: Als uw gegevens zijn afgeleid van verzamelingen die subverzamelingen bevatten, of op een andere manier rijen met gegevens bevatten die gemeenschappelijke waarden delen, hebt u hiërarchische gegevens.

In Power BI kunt u de gegevens uitvouwen op basis van een of alle subsets. U kunt inzoomen op uw gegevens om op elk niveau één subset weer te geven, of om op elk niveau alle subsets tegelijkertijd weer te geven. U kunt bijvoorbeeld inzoomen op een bepaald jaar of alle resultaten voor elk jaar weergeven wanneer u inzoomt op de hiërarchie. Op dezelfde manier kunt u ook uitzoomen.

In de volgende secties wordt beschreven hoe u kunt inzoomen vanuit de weergave op het hoogste niveau, de weergave op het middelste niveau en de weergave op het laagste niveau.

### <a name="hierarchical-data-and-time-data"></a>Hiërarchische gegevens en tijdsgegevens
Voor dit voorbeeld volgen we het [voorbeeld van een retailanayse](sample-datasets.md) en maakt u een visualisatie van een gestapeld kolomdiagram waarmee wordt gekeken naar **Maand** (as) op basis van **Totaalomzet** (waarden).  

Hoewel **Maand** het gegevensveld voor de as is, wordt ook de categorie **Jaar** in de bron **As** gemaakt. Dit komt doordat Power BI de volledige structuur datum-/tijdstructuur biedt voor alle waarden die worden gelezen. Boven in de hiërarchie worden gegevens voor het jaar weergegeven.

![](media\power-bi-visualization-drill-down/power-bi-hierarchical-axis-datetime-1.png)

Klik in de inzoommodus op de balk in het diagram om één niveau omlaag te gaan in de hiërarchie. U ziet drie balken voor de gegevens van de beschikbare kwartalen. Kies in de pictogrammen in de linkerbovenhoek **Alles één niveau in de hiërarchie omlaag uitvouwen**. Voer deze actie nogmaals uit om naar het laagste niveau van de hiërarchie te gaan, waarin de resultaten voor elke maand worden weergegeven.

![](media\power-bi-visualization-drill-down/power-bi-hierarchical-axis-datetime-2.png)

Naast de visualisatie ziet u de hiërarchie in de gegevens die voor elk rapport worden weergegeven. In de volgende tabel ziet u de resultaten van **Gegevens weergeven** in een rapport waarin u inzoomt vanuit één maand of vanuit alle maanden. 

U ziet dat de gegevens voor de kwartaal- en jaarrapporten identiek zijn. Wanneer u inzoomt op het detailniveau dat voor **Waarden** is opgegeven, ziet u hoe het rapport voor één maand minder en specifiekere gegevens bevat en het rapport voor alle maanden meer gegevens bevat.


|Modus voor uitgevouwen gegevens|Jaar|Kwartaal|Maand|Dag|
| ---|:---:|:---:|:---:|---|
|Enkel|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-year.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-quarter.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-one-month.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-one-day.png)|
|Alle|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-year.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-quarter.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-all-month.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-all-day.png)|


### <a name="hierarchical-category-data"></a>Hiërarchische categoriegegevens
Gegevens die zijn gemodelleerd op basis van verzamelingen en subverzamelingen, noemen we hiërarchische gegevens. Een goed voorbeeld hiervan zijn locatiegegevens. Stel dat u een tabel hebt in een gegevensbron met de kolommen Land, Provincie, Plaats en Postcode. Gegevens die hetzelfde land, dezelfde provincie en dezelfde plaats delen, zijn hiërarchische gegevens.

Voor dit voorbeeld volgen we het [voorbeeld van een retailanalyse](sample-datasets.md). Maak een visualisatie van een gestapeld kolomdiagram waarin wordt gekeken naar **Totale eenheden dit jaar** (waarden) op basis van **Gebied**, **Plaats**, **Postcode** en **Naam** (groep).  

![](media\power-bi-visualization-drill-down/power-bi-hierarchical-axis-category-1.png)

Kies in de linkerbovenhoek van de inzoommodus drie keer het pictogram **Alles één niveau in de hiërarchie omlaag uitvouwen**.
U moet zich op het laagste niveau van de hiërarchie bevinden, waarin de resultaten voor Gebied, Plaats en Postcode worden weergegeven.

![](media\power-bi-visualization-drill-down/power-bi-hierarchical-axis-category-2.png)

Naast de visualisatie ziet u de hiërarchie in de gegevens die voor elk rapport worden weergegeven. In de volgende tabel ziet u de resultaten van **Gegevens weergeven** in een rapport waarin u inzoomt voor één gebied of voor alle gebieden. Tijdens het inzoomen ziet u hoe het rapport voor één gebied minder en specifiekere gegevens bevat en het rapport voor alle gebieden meer gegevens bevat.


| Modus voor uitgevouwen gegevens|Gebied|Plaats|Postcode|Naam|
| ---|:---:|:---:|:---:|---|
|Enkel|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-territory.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-one-territory-city.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-one-territory-city-postal.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-one-territory-city-postal-name.png)|
|Alle|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-territory.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-all-territory-city.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-all-territory-city-postal.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-all-territory-city-postal-name.png)|


## <a name="considerations-and-limitations"></a>Overwegingen en beperkingen
* Als door het toevoegen van een datumveld aan een visualisatie geen hiërarchie wordt gecreëerd, kan het zijn dat het veld Datum niet daadwerkelijk als datum is opgeslagen. Als het uw eigen gegevensset is, opent u het in de weergave *Gegevens* in Power BI Desktop, selecteert u de kolom met de datum en wijzigt u het **gegevenstype** in **Datum** of **Datum/tijd** op het tabblad Model maken. Als het rapport met u is gedeeld, neem dan contact op met de eigenaar om de wijziging aan te vragen.  
  
  ![](media/power-bi-visualization-drill-down/power-bi-change-data-type2.png)

## <a name="next-steps"></a>Volgende stappen
[Visualisaties in Power BI-rapporten](power-bi-report-visualizations.md)

[Power BI-rapporten](service-reports.md)

[Power BI - basisconcepten](service-basic-concepts.md)

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

