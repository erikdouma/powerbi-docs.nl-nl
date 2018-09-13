---
title: Gegevens uit een Power BI-visualisatie exporteren
description: Exporteer gegevens uit een rapportvisualisatie en dashboardvisualisatie en bekijk ze in Excel.
author: mihart
manager: kvivek
ms.reviewer: ''
featuredvideoid: jtlLGRKBvXY
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 09/06/2018
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: 55fe4a2e8b3121431567309e935e9fa4a15cd31b
ms.sourcegitcommit: fe03f2a80f2df82219b8e026085f93a8453201df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/08/2018
ms.locfileid: "44168038"
---
# <a name="export-data-from-visualizations"></a>Gegevens uit visualisaties exporteren
Als u de gegevens wilt zien die gebruikt worden om een visualisatie te maken, kunt u die [gegevens weergeven in Power BI](service-reports-show-data.md) of exporteren naar Excel als .xlsx- of .csv-bestand.   

Kijk hoe Will de gegevens van een van de visualisaties in zijn rapport exporteert, opslaat als .xlsx-bestand en opent in Excel. Volg vervolgens de stapsgewijze instructies onder de video om het zelf te proberen.

<iframe width="560" height="315" src="https://www.youtube.com/embed/KjheMTGjDXw" frameborder="0" allowfullscreen></iframe>

## <a name="from-a-visualization-on-a-power-bi-dashboard"></a>Vanuit een visualisatie in een Power BI-dashboard
1. Selecteer het beletselteken in de rechterbovenhoek van de visualisatie.

    ![](media/power-bi-visualization-export-data/pbi-export-tile3.png)
2. Kies het pictogram **Gegevens exporteren**.

    ![](media/power-bi-visualization-export-data/pbi_export_dash.png)
3. De gegevens worden geëxporteerd naar een .csv-bestand. Als de visualisatie is gefilterd, worden de gedownloade gegevens ook gefilterd.    
4. U wordt gevraagd het bestand op te slaan.  Nadat het is opgeslagen, opent u het .csv-bestand in Excel.

    ![](media/power-bi-visualization-export-data/pbi-export-to-excel.png)

## <a name="from-a-visualization-in-a-report"></a>Vanuit een visualisatie in een rapport
Als u mee wit doen, opent u het rapport [Procurement analysis sample](sample-procurement.md) (Voorbeeld van een inkoopanalyse) in de [Bewerkingsweergave](service-reading-view-and-editing-view.md). [Voeg een nieuwe, lege rapportpagina toe](power-bi-report-add-page.md). Volg vervolgens onderstaande stappen om een aggregatie en een filter op visualisatieniveau toe te voegen.

1. Maak een nieuw kolomdiagram.  Selecteer in het deelvenster Velden **Locatie > Plaats** en **Factuur > Kortingspercentage**.  Mogelijk moet u **Kortingspercentage** verplaatsen naar de Waarde-put. 

    ![](media/power-bi-visualization-export-data/power-bi-export-data3.png)
2. Wijzig de aggregatie voor **Kortingspercentage** van **Aantal** in **Gemiddelde**. Selecteer in de Waarde-put de pijl rechts van **Kortingspercentage** (er staat mogelijk **Aantal kortingspercentage**) en kies **Gemiddelde**.

    ![](media/power-bi-visualization-export-data/power-bi-export-data6.png)
3. Voeg een filter toe aan **Plaats** om **Atlanta** te verwijderen.

   ![](media/power-bi-visualization-export-data/power-bi-export-data4.png)

   Nu zijn we klaar om beide opties voor het exporteren van gegevens uit te proberen. 

4. Selecteer het beletselteken in de rechterbovenhoek van de visualisatie. Kies **Gegevens exporteren**.

   ![](media/power-bi-visualization-export-data/power-bi-export-data2.png)
5. Als uw visualisatie in Power BI Online een statistische functie heeft (een voorbeeld zou zijn als u **Aantal** wijzigt in *Gemiddelde*, **Som** of *Minimum*), hebt u twee opties: **Samengevatte gegevens** en **Onderliggende gegevens**. In Power BI Desktop kunt u alleen **Samengevatte gegevens** kiezen. Zie [Statistische functies in Power BI](service-aggregates.md) voor hulp bij statistische functies in Power BI.

    ![](media/power-bi-visualization-export-data/power-bi-export-data5.png)
6. Selecteer **Samengevatte gegevens** > **Exporteren** en kies .xlsx- of .csv. Power BI exporteert de gegevens.  Als u filters op de visualisatie hebt toegepast, worden de geëxporteerde gegevens geëxporteerd als gefilterd. Wanneer u **Exporteren** selecteert, wordt u gevraagd het bestand op te slaan. Nadat het is opgeslagen, opent u het bestand in Excel.

   **Samengevatte gegevens**: selecteer deze optie als u gegevens wilt exporteren voor wat u ziet in de visual.  Bij dit type uitvoer ziet u alleen de gegevens (kolommen en metingen) die u hebt gekozen om de visual te maken.  Als de visual een statistische functie bevat, exporteert u hiermee statistische gegevens. Als u bijvoorbeeld een staafdiagram met 4 balken hebt, krijgt u 4 rijen gegevens. Samengevatte gegevens zijn beschikbaar als .xlsx en .csv.

   In dit voorbeeld bevat onze Excel-export één totaal voor elke plaats. Omdat we Atlanta uitgefilterd hebben, is deze plaats niet opgenomen in de resultaten.  In de eerste rij van onze werkblad ziet u de filters die zijn gebruikt bij het extraheren van de gegevens uit Power BI.

   ![](media/power-bi-visualization-export-data/power-bi-export-data7.png)
7. Selecteer nu  **Onderliggende gegevens** > **Export** en kies .xlsx. Power BI exporteert de gegevens. Als u filters op de visualisatie had toegepast, worden de geëxporteerde gegevens geëxporteerd als gefilterd. Wanneer u **Exporteren** selecteert, wordt u gevraagd het bestand op te slaan. Nadat het is opgeslagen, opent u het bestand in Excel.

   >[!WARNING]
   >Door onderliggende gegevens te exporteren, kunnen gebruikers alle gedetailleerde gegevens zien: elke kolom in de gegevens. Power BI-servicebeheerders kunnen dit uitschakelen voor hun organisatie. Als u de eigenaar van een gegevensset bent, kunt u eigen kolommen instellen als ‘verborgen’, zodat ze niet worden weergegeven in de veldenlijst in Desktop of Power BI-service.


   **Onderliggende gegevens**: selecteer deze optie als u de gegevens in de visual ***en*** aanvullende gegevens uit het model wilt weergeven (bekijk de onderstaande grafiek voor meer informatie).  Als uw visualisatie een statistische functie bevat, wordt de statistische functie verwijderd als u *Onderliggende gegevens* selecteert. Wanneer u **Exporteren** selecteert, worden de gegevens geëxporteerd naar een .xlsx-bestand en wordt u gevraagd het bestand op te slaan. Nadat het is opgeslagen, opent u het bestand in Excel.

   In dit voorbeeld toont onze Excel-export één rij voor elke Plaats-rij in onze gegevensset, en het kortingspercentage voor dat ene item. Met andere woorden, de gegevens worden afgevlakt en niet geaggregeerd. In de eerste rij van onze werkblad ziet u de filters die zijn gebruikt bij het extraheren van de gegevens uit Power BI.  

   ![](media/power-bi-visualization-export-data/power-bi-export-data8.png)

## <a name="export-underlying-data-details"></a>Details van de onderliggende gegevens exporteren
Wat u ziet wanneer u **Onderliggende gegevens** selecteert, varieert. Vraag uw beheerder of IT-afdeling voor meer informatie over deze details. In Power BI Desktop of de Power BI-service wordt in de rapportweergave een *meting* in de lijst Velden weergegeven met een rekenmachinepictogram ![pictogram weergeven](media/power-bi-visualization-export-data/power-bi-calculator-icon.png). Metingen worden gedaan in Power BI Desktop, niet in Power BI-service.


| De visual bevat |                                                                              Wat u ziet in het exportbestand                                                                              |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Statistische functies    |                                                 de *eerste* statistische functie en niet-verborgen gegevens uit de hele tabel voor die combinatie                                                  |
|   Statistische functies    | gerelateerde gegevens - als gegevens uit andere gegevenstabellen worden gebruikt voor de visuals die *\*\*gerelateerd*\* zijn aan de gegevenstabel met de statistische functie (zolang deze relatie \*:1 of 1:1 is) |
|    Metingen     |                                      Alle metingen in de visual *en* alle metingen uit gegevenstabellen die een meting bevatten die in de visual wordt gebruikt                                      |
|    Metingen     |                                       Alle niet-verborgen gegevens uit tabellen die deze meting bevatten (zolang deze relatie \*:1 of 1:1 is)                                       |
|    Metingen     |                                      Alle gegevens van alle tabellen die zijn gerelateerd aan tabellen met de metingen via een keten van \*:1 van 1:1                                      |
|  Alleen metingen  |                                                   Alle niet-verborgen kolommen van alle gerelateerde tabellen (om de meting te kunnen uitbreiden)                                                   |
|  Alleen metingen  |                                                             Samengevatte gegevens voor alle dubbele rijen voor modelmetingen.                                                              |

## <a name="limitations-and-considerations"></a>Beperkingen en overwegingen
* Het maximum aantal rijen dat uit **Power BI Desktop** en de **Power BI-service** naar .csv kan worden geëxporteerd, is 30.000.
* Het maximum aantal rijen dat naar .xlsx kan worden geëxporteerd, is 150.000.
* Exporteren met behulp van *onderliggende gegevens* werkt niet als de gegevensbron een liveverbinding met Analysis Services is en de versie ouder is dan 2016 is en de tabellen in het model niet over een unieke sleutel beschikken.  
* Exporteren met behulp van *onderliggende gegevens* werkt niet als de optie *Items zonder gegevens weergeven* is ingeschakeld voor de visualisatie die wordt geëxporteerd.
* Bij gebruik van DirectQuery is de maximale hoeveelheid gegevens die geëxporteerd kan worden 16 MB. Dit kan ertoe leiden dat minder dan het maximum aantal rijen wordt geëxporteerd, vooral als er veel kolommen zijn, gegevens die moeilijk te comprimeren zijn en andere factoren die de bestandsgrootte vergroten en het aantal geëxporteerde rijen verminderen.
* Als de visual gebruikmaakt van gegevens uit meer dan één gegevenstabel en er geen relatie bestaat voor deze tabellen in het gegevensmodel, worden alleen gegevens voor de eerste tabel geëxporteerd. 
* Aangepaste visuals en R-visuals worden momenteel niet ondersteund.
* Het exporteren van gegevens is niet beschikbaar voor gebruikers buiten uw organisatie die een dashboard gebruiken dat met ze is gedeeld. 
* In Power BI kunt u de naam van een veld (kolom) wijzigen door te dubbelklikken op het veld en een nieuwe naam in te voeren.  Deze nieuwe naam wordt een *alias* genoemd. Het is mogelijk dat een Power BI-rapport hierdoor dubbele veldnamen bevat, maar duplicaten zijn niet toegestaan in Excel.  Wanneer de gegevens naar Excel worden geëxporteerd, worden voor de veldaliassen weer hun oorspronkelijke veld-/kolomnamen gebruikt.  
* Als er unicode-tekens in het .csv-bestand staan, wordt de tekst in Excel mogelijk niet correct weergegeven. Het werkt wel goed als u het bestand opent in Kladblok. Voorbeelden van unicode-tekens zijn valutasymbolen en woorden in vreemde talen. U kunt dit probleem vermijden door het .csv-bestand in Excel te importeren in plaats van het rechtstreeks te openen. Ga als volgt te werk:

  1. Open Excel
  2. Selecteer op het tabblad **Gegevens** **Externe gegevens ophalen** > **Uit tekst**.
* Power BI-beheerders hebben de mogelijkheid het exporteren van gegevens uit te schakelen.

## <a name="next-steps"></a>Volgende stappen
[Dashboards in Power BI](service-dashboards.md)  
[Rapporten in Power BI](service-reports.md)  
[Power BI - basisconcepten](service-basic-concepts.md)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

