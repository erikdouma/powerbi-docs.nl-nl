---
title: 'Voorbeeld van een inkoopanalyse: rondleiding'
description: 'Voorbeeld van een inkoopanalyse voor Power BI: een rondleiding'
services: powerbi
documentationcenter: 
author: mihart
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
ms.date: 10/28/2017
ms.author: mihart
ms.openlocfilehash: 576ddfbbf52a2738dd32597479ffd03d554a5256
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2017
---
# <a name="procurement-analysis-sample-for-power-bi-take-a-tour"></a>Voorbeeld van een inkoopanalyse voor Power BI: een rondleiding
In dit voorbeelddashboard met bedrijfsgegevens en in het onderliggende rapport worden de uitgaven van een productiebedrijf aan leveranciers geanalyseerd op categorie en locatie. In het voorbeeld verkennen we deze gebieden:

* Wie de belangrijkste leveranciers zijn
* Aan welke categorieën we het meeste besteden
* Welke leveranciers de meeste korting geven en wanneer

Dit voorbeeld is onderdeel van een serie die laat zien hoe u Power BI kunt gebruiken met bedrijfsgegevens, -rapporten en -dashboards. Dit zijn echte gegevens die afkomstig zijn van obviEnce ([www.obvience.com)](http://www.obvience.com/) die zijn geanonimiseerd.

![](media/sample-procurement/procurement1.png)

Doet u mee? Ga in [Power BI-service](https://powerbi.com) naar **Gegevens ophalen > Voorbeelden > Voorbeeld van een inkoopanalyse > Verbinden** voor uw eigen kopie van het voorbeeld.

U kunt ook [alleen de gegevensset (Excel-werkmap)](http://go.microsoft.com/fwlink/?LinkId=529784) voor dit voorbeeld downloaden.

## <a name="spending-trends"></a>Bestedingstrends
Laten we eerst zoeken naar bestedingstrends op categorie en locatie.  

1. Open in uw werkruimte het tabblad **Dashboards** en selecteer het dashboard Inkoopanalyse.
2. Selecteer de dashboardtegel **Totaal aan facturen per land/regio**. Deze wordt geopend op de pagina Bestedingsoverzicht van het rapport Voorbeeld van een inkoopanalyse.
   
    ![](media/sample-procurement/procurement2.png)

U ziet een aantal dingen:

* In het lijndiagram **Totaal aan facturen per maand en categorie**: de categorie **Direct** heeft behoorlijk consistente uitgaven **Logistiek** heeft een piek in december en  **Overige** heeft een piek in februari.
* Op de kaart **Totaal aan facturen per land/regio**: het grootste deel van onze uitgaven is in de Verenigde Staten.
* In het kolomdiagram **Totaal aan facturen per subcategorie**: **Hardware** en **Indirecte goederen en services** zijn de grootste bestedingscategorieën.
* In het staafdiagram Totaal aan facturen per laag: wij doen het meeste zaken met onze leveranciers van laag 1 (top 10). Dit helpt bij een beter relatiebeheer van onze leveranciers.

## <a name="spending-in-mexico"></a>Uitgaven in Mexico
Laten we de bestedingsgebieden in Mexico bekijken.

1. Selecteer in het cirkeldiagram de bel **Mexico** op de kaart. U ziet dat in het kolomdiagram Totaal aan facturen op subcategorie het meeste in de subcategorie **Indirecte goederen en services** staat.
   
   ![](media/sample-procurement/pbi_procsample_spendmexico.png)
2. Inzoomen op de kolom **Indirecte goederen en services**:
   
   * Selecteer de pijl voor inzoomen ![](media/sample-procurement/pbi_drilldown_icon.png) in de rechterbovenhoek van de grafiek.
   * Selecteer de kolom **Indirecte goederen & Services**.
     
      Tot nu toe is Verkoop en marketing verreweg de grootste uitgavenpost in deze categorie.
   * Selecteer nogmaals **Mexico** op de kaart.
     
      De grootste uitgaven in deze categorie in Mexico zijn de uitgaven voor Onderhoud en reparatie.
     
      ![](media/sample-procurement/pbi_procsample_drill_mexico.png)
3. Selecteer de pijl omhoog in de linkerbovenhoek van de grafiek om weer uit te zoomen.
4. Selecteer de pijl opnieuw om inzoomen uit te schakelen.  
5. Selecteer **Power BI** in de bovenste navigatiebalk om terug te keren naar uw werkruimte.

## <a name="evaluate-different-cities"></a>Verschillende steden evalueren
U kunt markeren gebruiken om verschillende steden te evalueren.

1. Selecteer de dashboardtegel **Totaal aan facturen, kortingspercentage per maand**. Het rapport wordt geopend op de pagina Kortingsanalyse.
2. Selecteer de verschillende steden in de treemap **Totaal aan facturen per stad** om te zien hoe deze zich verhouden. Bijna alle facturen van Miami zijn van leveranciers van laag 1.
   
   ![](media/sample-procurement/pbi_procsample_miamitreemap2.png)

## <a name="vendor-discounts"></a>Leverancierskortingen
Laten we kijken naar de beschikbare kortingen van leveranciers en de perioden waarin de meeste korting wordt gegeven. 

![](media/sample-procurement/procurement4.png)

Stel de volgende vragen:

* Zijn de kortingen verschillend per maand of worden elke maand dezelfde kortingen gegeven?
* Krijg sommige steden meer kortingen dan andere?

### <a name="discount-by-month"></a>Korting per maand
Als wij kijken naar de combinatiegrafiek **Totaal aan facturen en kortingspercentage per maand**, zien we dat **februari** de drukste maand en **september** de minst drukke maand is. Bekijk nu het kortingspercentage tijdens deze maanden.
Als het volume toeneemt, wordt de korting minder en als het volume laag is, neemt de korting toe. Hoe meer we de korting nodig hebben, des te slechter de deal zal zijn.

![](media/sample-procurement/procurement5.png)

### <a name="discount-by-city"></a>Korting per stad
Een ander aspect om te verkennen, is de korting per stad. Selecteer elke plaats in de treemap en kijk hoe de andere grafieken wijzigen. 

* St. Louis, MO had een grote piek in het totaal aan facturen in februari en een grote dip in de kortingsbesparingen in april.
* Mexico-Stad, Mexico heeft het hoogste kortingspercentage (11,05%) en Atlanta, GA het laagste (0,08%).

![](media/sample-procurement/procurement6.png)

### <a name="edit-the-report"></a>Het rapport bewerken
Selecteer **Rapport bewerken** in de linkerbovenhoek en bekijk deze optie in de Bewerkingsweergave.

* Zie hoe de pagina's zijn gemaakt
* Pagina's en grafieken op basis van dezelfde gegevens toevoegen
* Het visualisatietype voor een grafiek wijzigen, bijvoorbeeld van de treemap naar een ringdiagram
* Vastmaken aan uw dashboard

Dit is een veilige omgeving om in te spelen. U kunt er altijd voor kiezen om de wijzigingen niet op te slaan. Als u deze wel opslaat, kunt u altijd naar **Gegevens ophalen** gaan voor een nieuwe kopie van dit voorbeeld.

## <a name="next-steps-connect-to-your-data"></a>Volgende stappen: koppelen aan uw gegevens
We hopen dat deze rondleiding heeft geleerd hoe u met Power BI-dashboards en rapporten inzicht kunt krijgen in inkoopgegevens. Nu is het uw beurt: aan uw eigen gegevens koppelen. Met Power BI kunt u koppelen aan een groot aantal gegevensbronnen. Meer informatie over [Aan de slag met Power BI](service-get-started.md).

