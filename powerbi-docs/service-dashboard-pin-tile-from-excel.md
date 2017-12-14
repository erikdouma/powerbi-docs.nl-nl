---
title: Vanuit Excel een tegel vastmaken aan een Power BI-dashboard
description: Vanuit Excel op OneDrive voor Bedrijven een tegel vastmaken aan een Power BI-dashboard. Bereiken, grafieken, tabellen vastmaken
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: l8JoB7w0zJA
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 09/26/2017
ms.author: mihart
ms.openlocfilehash: 855ecbe74fa4bf4ab1b1f81f22f2bab278adddb9
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2017
---
# <a name="pin-a-tile-to-a-power-bi-dashboard-from-excel"></a>Vanuit Excel een tegel vastmaken aan een Power BI-dashboard
Voordat u een tegel uit uw Excel-werkmap vastmaakt, koppelt u de werkmap aan de Power BI-service (app.powerbi.com). Met het koppelen van een werkmap wordt een gekoppelde alleen-lezen versie van die werkmap naar Power BI-service overgebracht. Zo kunt u bereiken aan dashboards koppelen. U kunt zelfs een volledig werkblad aan een dashboard vastmaken.  
Als een werkmap met u is gedeeld, kunt u de tegels die zijn vastgemaakt door de eigenaar bekijken, maar zelf geen dashboardtegels maken. 

Zie [Gegevens ophalen uit Excel-werkmappen](http://go.microsoft.com/fwlink/?LinkID=521962) voor gedetailleerde informatie over de manier waarop Excel en Power BI samenwerken.

Kijk hoe Will verschillende manieren demonstreert om gegevens te importeren uit en verbinding te maken met Excel-werkmappen.

<iframe width="560" height="315" src="https://www.youtube.com/embed/l8JoB7w0zJA" frameborder="0" allowfullscreen></iframe>

## <a name="connect-your-excel-workbook-from-onedrive-for-business-to-power-bi"></a>Uw Excel-werkmap in OneDrive voor Bedrijven koppelen aan Power BI
Wanneer u de optie **Verbinden** kiest, wordt uw werkmap weergegeven in Power BI, precies zoals in Excel Online. Maar anders dan in Excel Online hebt u een aantal handige functies waarmee u elementen uit uw werkbladen direct aan uw dashboards kunt vastmaken.

U kunt uw werkmap niet in Power BI bewerken. Maar als u wijzigingen wilt aanbrengen, kunt u het potloodpictogram op het tabblad **Werkmappen** in uw werkruimte selecteren en uw werkmap vervolgens bewerken in Excel Online of openen in Excel op uw computer. Eventuele wijzigingen worden opgeslagen in de werkmap op OneDrive.

1. Upload uw werkmap naar uw OneDrive voor Bedrijven.
2. Maak vanuit Power BI [verbinding met die werkmap](service-excel-workbook-files.md).
3. De werkmap wordt in Power BI toegevoegd aan het tabblad **Werkmappen** van uw werkruimte.  Het pictogram ![](media/service-dashboard-pin-tile-from-excel/pbi_workbookicon.png) geeft aan dat dit een Excel-werkmap is en een geel sterretje geeft aan dat de werkmap nieuw is.
   
    Wijzigingen in de werkmap in Power BI worden niet opgeslagen en hebben geen invloed op de oorspronkelijke werkmap in OneDrive voor Bedrijven. Als u waarden in Power BI sorteert, filtert of wijzigt, kunnen deze wijzigingen niet worden opgeslagen of vastgemaakt. Selecteer het potloodpictogram om de werkmap in Excel Online te openen en bij te werken. Het duurt enkele minuten voordat wijzigingen in de werkmap in Excel Online in de tegels worden bijgewerkt.     
   
   ![](media/service-dashboard-pin-tile-from-excel/power-bi-workbooks.png)
4. Open de werkmap in Power BI door de werkmapnaam te selecteren.
   
   ![](media/service-dashboard-pin-tile-from-excel/power-bi-opened.png)

## <a name="pin-a-range-of-cells-to-a-dashboard"></a>Een bereik van cellen aan een dashboard vastmaken
U kunt een nieuwe [dashboardtegel](service-dashboard-tiles.md) onder meer toevoegen vanuit een Excel-werkmap in Power BI. Bereiken kunnen worden vastgemaakt vanuit Excel-werkmappen die zijn opgeslagen in uw OneDrive voor bedrijven of een andere in groepen gedeelde documentbibliotheek. De bereiken kunnen gegevens, grafieken, tabellen, draaitabellen, draaigrafieken en andere onderdelen van Excel bevatten.

1. Markeer de cellen die u wilt vastmaken aan een dashboard.
   
    ![](media/service-dashboard-pin-tile-from-excel/pbi_selectrange.png)
2. Selecteer het speldpictogram ![](media/service-dashboard-pin-tile-from-excel/pbi_pintile_small.png). 
3. Maak de tegel vast aan een bestaand dashboard of aan een nieuw dashboard. 
   
   * Bestaand dashboard: selecteer de naam van het dashboard in de vervolgkeuzelijst.
   * Nieuw dashboard: typ de naam van het nieuwe dashboard.
   
   ![](media/service-dashboard-pin-tile-from-excel/pbi_dashdialog1.png)
4. Selecteer **Vastmaken**. Een bericht (rechts bovenin) laat u weten dat het bereik als tegel aan uw dashboard is toegevoegd. 
   
    ![](media/service-dashboard-pin-tile-from-excel/power-bi-go-to-dashboard.png)
5. Selecteer **Naar het dashboard gaan**. Hier kunt u de vastgemaakte visualisatie [hernoemen, vergroten of verkleinen, koppelen en verplaatsen](service-dashboard-edit-tile.md). Standaard wordt de werkmap in Power BI geopend als de vastgemaakte tegel wordt geselecteerd.

## <a name="pin-an-entire-table-or-pivot-chart-to-a-dashboard"></a>Een hele tabel of draaigrafiek aan een dashboard vastmaken
Volg de bovenstaande stappen maar selecteer in plaats van een celbereik een hele tabel of draaitabel.

Als u een tabel wilt vastmaken, selecteert u het volledige bereik van de tabel inclusief koppen.  Als u een draaitabel wilt vastmaken, moet u elk zichtbare gedeelte van de draaitabel opnemen, inclusief eventuele filters.

 ![](media/service-dashboard-pin-tile-from-excel/pbi_selecttable.png)

Als een tegel is gemaakt op basis van een tabel of draaitabel, wordt de hele tabel weergeven.  Als u rijen of kolommen in de originele werkmap toevoegt/verwijdert/filtert, worden deze ook in de tegel toegevoegd/verwijderd/gefilterd.

## <a name="view-the-workbook-linked-to-the-tile"></a>De werkmap die aan de tegel is gekoppeld bekijken
Als een tegelwerkmap wordt geselecteerd, wordt de gekoppelde werkmap in Power BI geopend. Omdat het werkmapbestand is opgeslagen op OneDrive voor Bedrijven, moet u voor de weergave van de werkmap leesmachtigingen voor de werkmap hebben. Als u geen machtiging hebt, krijgt u een foutbericht.  

## <a name="considerations-and-troubleshooting"></a>Overwegingen en probleemoplossing
Niet-ondersteunde functies: Power BI maakt gebruik van Excel Services om de werkmaptegels op te halen. Omdat sommige functies van Excel niet worden ondersteund in de Excel Services REST API, zijn ze niet zichtbaar in de tegels in Power BI. Bijvoorbeeld: Sparklines, voorwaardelijke opmaak van pictogrammenset en tijdslicers. Zie [Niet-ondersteunde functies in Excel Services REST API](http://msdn.microsoft.com/library/office/ff394477.aspx) voor een volledige lijst met niet-ondersteunde functies.

## <a name="next-steps"></a>Volgende stappen
[Een dashboard met koppelingen naar een Excel-werkmap delen](service-share-dashboard-that-links-to-excel-onedrive.md)

[Gegevens ophalen uit Excel-werkmappen](service-excel-workbook-files.md)

[Dashboards in Power BI](service-dashboards.md)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

