---
title: Overzicht van het deelvenster Filters van Power BI
description: Overzicht van het deelvenster Rapportfilters in Power BI-service en Power BI-dashboard
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: monitoring
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 01/22/2018
ms.author: mihart
ms.openlocfilehash: 14aa2a2813484c3af814332736906c2aae0e0230
ms.sourcegitcommit: be5223b62e9a5d57c52f8588d4e539d814751dd6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2018
---
# <a name="take-a-tour-of-the-report-filters-pane"></a>Rondleiding door het deelvenster Filters van het rapport
In dit artikel wordt het rapportvenster Filters diepgaand besproken. U ziet het deelvenster in de [bewerkweergave en leesweergave van Power BI-service](service-reading-view-and-editing-view.md) en in de [rapportweergave van Power BI Desktop](desktop-report-view.md).

Er zijn veel verschillende manieren om gegevens te filteren in Power BI. Wij raden u aan om te beginnen met het lezen van [Filters en markeren](power-bi-reports-filters-and-highlighting.md).

## <a name="working-with-filters"></a>Werken met filters
Rapporten kunnen worden geopend in de [Bewerkweergave of Leesweergave](service-reading-view-and-editing-view.md). In de Bewerkweergave kunnen rapporteigenaren [ filters toevoegen aan een rapport](power-bi-report-add-filter.md), en deze filters worden opgeslagen bij het rapport. Mensen die het rapport bekijken in de Leesweergave kunnen de filters gebruiken, maar kunnen wijzigingen in de filters niet opslaan in het rapport.

## <a name="filters-in-reading-view"></a>Filters in Leesweergave
Wanneer een rapport is geopend in de leesweergave, wordt het deelvenster Filters aan de rechterkant van het rapportcanvas weergegeven. Als u het deelvenster niet ziet, selecteert u de pijl in de rechterbovenhoek om het uit te vouwen.

In dit voorbeeld hebben we een visualisatie met 6 filters geselecteerd. De rapportagepagina heeft ook filters, onder de kop **Filters op paginaniveau**. Er is één [Drillthrough-filter](power-bi-report-add-filter.md) en het hele rapport heeft ook een filter: **FiscalYear** (Boekjaar) is 2013 of 2014.

![](media/power-bi-how-to-report-filter/power-bi-filter-list.png)

Naast sommige filters staat het woord **Alle**, wat betekent dat alle waarden in het filter worden opgenomen.  Zo zien we aan **Chain (All)** (Keten (Alle)) in onderstaande schermafbeelding dat deze rapportpagina gegevens bevat over alle winkelketens.  Aan de andere kant blijkt uit het filter op rapportniveau **FiscalYear is 2013 or 2014** (Boekjaar is 2013 of 2014) dat het rapport alleen gegevens voor de boekjaren 2013 en 2014 bevat.

Iedereen die dit rapport bekijkt, kan met deze filters werken.

* Bekijk de details van het filter door de pijl naast het filter aan te wijzen en te selecteren.
  
   ![](media/power-bi-how-to-report-filter/power-bi-expan-filter.png)
* Wijzig het filter, bijvoorbeeld door **Lindseys** te wijzigen in **Fashions Direct**.
  
     ![](media/power-bi-how-to-report-filter/power-bi-filter-chain.png)
* Verwijder het filter door de **x** naast de naam van het filter te selecteren.
  
  Het verwijderen van een filter verwijdert het uit de lijst, maar verwijdert de gegevens niet uit het rapport.  Als u bijvoorbeeld het filter van **FiscalYear is 2013 or 2014** (Boekjaar is 2013 of 2014) verwijdert, blijven de boekjaargegevens in het rapport staan, maar worden ze niet langer gefilterd om alleen 2013 en 2014 weer te geven, en worden alle belastingjaren weergegeven die voorkomen in de gegevens.  Als u het filter eenmaal hebt verwijderd kunt u het echter niet meer wijzigen, omdat het uit de lijst is verwijderd. Een betere optie is het filter te wissen door het gumpictogram ![](media/power-bi-how-to-report-filter/power-bi-eraser-icon.png) te selecteren.
  
  ![](media/power-bi-how-to-report-filter/power-bi-delete-filter.png)

## <a name="filters-in-editing-view"></a>Filters in de Bewerkweergave
Wanneer een rapport is geopend in de Bewerkweergave, wordt het deelvenster Filters rechts van het rapportcanvas weergegeven, in het onderste deel van het **Visualisatiedeelvenster**. Als u het deelvenster niet ziet, selecteert u de pijl in de rechterbovenhoek om het uit te vouwen.

![](media/power-bi-how-to-report-filter/power-bi-all-filters.png).  

Als er geen visualisatie is geselecteerd in het canvas, worden in het deelvenster Filters alleen de filters weergegeven die van toepassing zijn op de gehele rapportpagina of het volledige rapport, en eventuele drillthrough-filters (als die zijn ingesteld). In het onderstaande voorbeeld is er geen visualisatie geselecteerd en zijn er geen filters op paginaniveau of drillthrough-filters, maar wel een filter op rapportniveau.  

![](media/power-bi-how-to-report-filter/power-bi-no-visual.png)  

Als er een visualisatie is geselecteerd in het canvas, ziet u ook de filters die alleen van toepassing zijn op die visualisatie:   

![](media/power-bi-how-to-report-filter/power-bi-visual-filters.png)

Als u opties voor een bepaald filter wilt weergeven, selecteert u de pijl omlaag naast de filternaam.  In onderstaand voorbeeld is het rapportniveaufilter ingesteld op 2013 en 2014. Dit is een voorbeeld van het toepassen van **standaardfilters**.  Als u de geavanceerde opties wilt weergeven, selecteert u **Geavanceerd filteren**.

![](media/power-bi-how-to-report-filter/pbi_filterlistdropdown.jpg)

## <a name="clear-a-filter"></a>Een filter wissen
 Selecteer in de geavanceerde of standaardfiltermodus het gumpictogram ![](media/power-bi-how-to-report-filter/pbi_erasericon.jpg) om het filter opnieuw in te stellen. 

## <a name="add-a-filter"></a>Een filter toevoegen
* Voeg in de bewerkingsweergave een filter toe aan een visueel element, pagina, drillthrough of rapport door een veld uit het deelvenster Velden te selecteren en het naar de juiste filterbucket te slepen, waar u de woorden **Sleep velden hierheen** ziet. Nadat een veld als filter is toegevoegd, kunt u het verfijnen met behulp van de besturingselementen Standaardfilters toepassen en Geavanceerd filteren (zie hieronder).

- **Door een nieuw veld naar het filtergebied op niveau van visuele elementen te slepen, wordt dat veld niet aan het visuele element toegevoegd** maar kunt u wel filteren op dit visuele element met het nieuwe veld. In onderstaand voorbeeld wordt **Chain** (Keten) aan de visualisatie toegevoegd als nieuw filter. Merk op dat het toevoegen van **Chain** als filter de visualisatie niet verandert, totdat u het besturingselement Standaardfilters toepassen of Geavanceerd filteren gebruikt.

    ![](media/power-bi-how-to-report-filter/power-bi-visual-filter.gif)

* Alle velden die worden gebruikt om een visualisatie te maken, zijn ook beschikbaar als filters. Selecteer eerst een visueel element om het te activeren. De velden die in de visualisatie worden gebruikt, worden vermeld in het deelvenster Visualisaties (als u de Bewerkweergave gebruikt) en in het deelvenster Filters onder het kopje **Filters op niveau van visuele elementen**.
  
   ![](media/power-bi-how-to-report-filter/power-bi-visual-filter.png)  
  
   U kunt elk van deze velden verfijnen met behulp van de besturingselementen Standaardfilters toepassen en Geavanceerd filteren (zie hieronder).

## <a name="types-of-filters-text-field-filters"></a>Typen filters: tekstveldfilters
### <a name="list-mode"></a>Lijstmodus
Als u een selectievakje aanvinkt, selecteert of deselecteert u de waarde. Het selectievakje **Alle** kan worden gebruikt om alle selectievakjes in of uit te schakelen. De selectievakjes geven alle beschikbare waarden voor dat veld weer.  Terwijl u het filter aanpast, wordt de herformulering aangepast aan uw keuzes. 

![](media/power-bi-how-to-report-filter/pbi_restatement.png)

U ziet dat de herformulering nu luidt:"is Amarilla of Carretera"

### <a name="advanced-mode"></a>Geavanceerde modus
Selecteer **Geavanceerd filteren** om over te schakelen naar de geavanceerde modus. Gebruik de vervolgkeuzelijsten en tekstvakken om aan te geven welke velden u wilt opnemen. Door te kiezen tussen **En** en **Of**, kunt u complexe filterexpressies maken. Selecteer de knop **Filter toepassen** wanneer u de gewenste waarden hebt ingesteld.  

![](media/power-bi-how-to-report-filter/aboutfilters.png)

## <a name="types-of-filters-numeric-field-filters"></a>Typen filters: numerieke veldfilters
### <a name="list-mode"></a>Lijstmodus
Als er een eindig aantal waarden is, wordt er een lijst weergegeven als u de veldnaam selecteert.  Zie **Tekstveldfilters** &gt; **Lijstmodus** hierboven voor hulp bij het gebruik van selectievakjes.   

### <a name="advanced-mode"></a>Geavanceerde modus
Als het aantal waarden oneindig is of als de waarden een bereik aangeven, wordt de geavanceerde filtermodus geopend als u de veldnaam selecteert. Gebruik de vervolgkeuzelijst en tekstvakken om een bereik met waarden aan te geven dat u wilt zien. 

![](media/power-bi-how-to-report-filter/pbi_dropdown-and-text.png)

Door te kiezen tussen **En** en **Of**, kunt u complexe filterexpressies maken. Selecteer de knop **Filter toepassen** wanneer u de gewenste waarden hebt ingesteld.

## <a name="types-of-filters-date-and-time"></a>Typen filters: datum en tijd
### <a name="list-mode"></a>Lijstmodus
Als er een eindig aantal waarden is, wordt er een lijst weergegeven als u de veldnaam selecteert.  Zie **Tekstveldfilters** &gt; **Lijstmodus** hierboven voor hulp bij het gebruik van selectievakjes.   

### <a name="advanced-mode"></a>Geavanceerde modus
Als de veldwaarden datums of tijden vertegenwoordigen, kunt u een begin-/eindtijd opgeven wanneer u datum-/tijdfilters gebruikt.  

![](media/power-bi-how-to-report-filter/pbi_date-time-filters.png)

## <a name="next-steps"></a>Volgende stappen
[Filters en markeren in rapporten](power-bi-reports-filters-and-highlighting.md)  
[Interact with filters and highlighting in report Reading View](service-reading-view-and-editing-view.md) (Werken met filters en markeringen in de leesweergave voor rapporten)  
[Filters maken in de Bewerkweergave van rapporten](power-bi-report-add-filter.md)  
[Change how report visuals cross-filter and cross-highlight each other](service-reports-visual-interactions.md) (Wijzigen hoe visuele rapportelementen elkaar kruislings filteren en markeren)

Lees meer over [rapporten in Power BI](service-reports.md)  
[Power BI - basisconcepten](service-basic-concepts.md)

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

