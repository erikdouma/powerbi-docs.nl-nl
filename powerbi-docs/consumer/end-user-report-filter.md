---
title: Overzicht van het deelvenster Filters van Power BI voor klanten
description: Overzicht van het deelvenster Rapportfilters in Power BI-service
author: mihart
manager: kvivek
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 09/25/2018
ms.author: mihart
LocalizationGroup: Reports
ms.openlocfilehash: c49e075bd7fbe2debb0b577a1ce2771491d5fac4
ms.sourcegitcommit: 52ac456bf2ac025b22ea634c28482f22e1cc19ac
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2018
ms.locfileid: "48908274"
---
# <a name="take-a-tour-of-the-report-filters-pane"></a>Rondleiding door het deelvenster Filters van het rapport
In dit artikel wordt het rapportvenster Filters in Power BI-service besproken.

Er zijn veel verschillende manieren om gegevens te filteren in Power BI. Wij raden u aan om te beginnen met het lezen van [Filters en markeren](../power-bi-reports-filters-and-highlighting.md).

![rapport in browser](media/end-user-report-filter/power-bi-browser.png)

## <a name="working-with-the-report-filters-pane"></a>Het deelvenster Filters van het rapport gebruiken
Als een collega een rapport met u deelt, bekijk dan het deelvenster **Filters**. Het wordt soms samengevouwen aan de rechterzijde van het rapport. Selecteer het om het uit te breiden.   

![rapport in browser](media/end-user-report-filter/power-bi-expanded.png)

Het deelvenster Filters bevat filters die aan het rapport zijn toegevoegd door de *rapportontwerper*. *Gebruikers* als uzelf kunnen de filters gebruiken en uw wijzigingen opslaan, maar geen nieuwe filters aan het rapport toevoegen.

In de Power BI-service worden wijzigingen die u aanbrengt in het deelvenster Filters bewaard en deze wijzigingen worden doorgevoerd in de mobiele versie van het rapport. Als u de standaardinstellingen die de ontwerper heeft geconfigureerd voor het deelvenster Filters wilt herstellen, selecteert u **Standaardinstellingen herstellen** in de bovenste menubalk.     

## <a name="open-the-filters-pane"></a>Het deelvenster Filters openen
Wanneer een rapport is geopend, wordt het deelvenster Filters aan de rechterkant van het rapportcanvas weergegeven. Als u het deelvenster niet ziet, selecteert u de pijl in de rechterbovenhoek om het uit te vouwen.  

In dit voorbeeld hebben we een visualisatie met 6 filters geselecteerd. De rapportagepagina heeft ook filters, onder de kop **Filters op paginaniveau**. Er is één [Drillthrough-filter](../power-bi-report-add-filter.md) en het hele rapport heeft ook een filter: **FiscalYear** (Boekjaar) is 2013 of 2014.

![lijst met filters](media/end-user-report-filter/power-bi-filter-list.png)

Naast sommige filters staat het woord **Alle**, wat betekent dat alle waarden in het filter worden opgenomen.  Zo zien we aan **Chain (All)** (Keten (Alle)) in onderstaande schermafbeelding dat deze rapportpagina gegevens bevat over alle winkelketens.  Aan de andere kant blijkt uit het filter op rapportniveau **FiscalYear is 2013 or 2014** (Boekjaar is 2013 of 2014) dat het rapport alleen gegevens voor de boekjaren 2013 en 2014 bevat.

Iedereen die dit rapport bekijkt, kan met deze filters werken.

* Bekijk de details van het filter door de pijl naast het filter aan te wijzen en te selecteren.
  
   ![geeft Lindseys geselecteerd weer](media/end-user-report-filter/power-bi-expan-filter.png)
* Wijzig het filter, bijvoorbeeld door **Lindseys** te wijzigen in **Fashions Direct**.
  
     ![geeft Fashions Direct geselecteerd weer](media/end-user-report-filter/power-bi-filter-chain.png)

* Herstel de oorspronkelijke staat van de filters door **Standaardinstellingen herstellen** in de bovenste menubalk te selecteren.    
    ![standaardinstelling herstellen](media/end-user-report-filter/power-bi-reset-to-default.png)
    
* Verwijder het filter door de **x** naast de filternaam te selecteren.
  
  Het verwijderen van een filter verwijdert het uit de lijst, maar verwijdert de gegevens niet uit het rapport.  Als u bijvoorbeeld het filter **FiscalYear is 2013 or 2014** (Boekjaar is 2013 of 2014) verwijdert, blijven de boekjaargegevens in het rapport staan. De gegevens worden niet meer gefilterd, zodat nu niet alleen de gegevens voor 2013 en 2014, maar voor alle belastingjaren die voorkomen in de gegevens worden weergegeven.  Als u het filter eenmaal hebt verwijderd kunt u het echter niet meer wijzigen, omdat het uit de lijst is verwijderd. Een betere optie is het filter te wissen door het ![gumpictogram](media/end-user-report-filter/power-bi-eraser-icon.png) te selecteren.
  
  ![met x gemarkeerd](media/end-user-report-filter/power-bi-delete-filter.png)



## <a name="clear-a-filter"></a>Een filter wissen
 Selecteer in de geavanceerde modus of standaardfiltermodus het gumpictogram  ![gumpictogram](media/end-user-report-filter/pbi_erasericon.jpg) om het filter te wissen. 


## <a name="types-of-filters-text-field-filters"></a>Typen filters: tekstveldfilters
### <a name="list-mode"></a>Lijstmodus
Als u een selectievakje aanvinkt, selecteert of deselecteert u de waarde. Het selectievakje **Alle** kan worden gebruikt om alle selectievakjes in of uit te schakelen. De selectievakjes geven alle beschikbare waarden voor dat veld weer.  Terwijl u het filter aanpast, wordt de herformulering aangepast aan uw keuzes. 

![lijstmodusfilter](media/end-user-report-filter/pbi_restatement.png)

U ziet dat de herformulering nu luidt:"is Amarilla of Carretera"

### <a name="advanced-mode"></a>Geavanceerde modus
Selecteer **Geavanceerd filteren** om over te schakelen naar de geavanceerde modus. Gebruik de vervolgkeuzelijsten en tekstvakken om aan te geven welke velden u wilt opnemen. Door te kiezen tussen **En** en **Of**, kunt u complexe filterexpressies maken. Selecteer de knop **Filter toepassen** wanneer u de gewenste waarden hebt ingesteld.  

![geavanceerde modus](media/end-user-report-filter/aboutfilters.png)

## <a name="types-of-filters-numeric-field-filters"></a>Typen filters: numerieke veldfilters
### <a name="list-mode"></a>Lijstmodus
Als er een eindig aantal waarden is, wordt er een lijst weergegeven als u de veldnaam selecteert.  Zie **Tekstveldfilters** &gt; **Lijstmodus** hierboven voor hulp bij het gebruik van selectievakjes.   

### <a name="advanced-mode"></a>Geavanceerde modus
Als het aantal waarden oneindig is of als de waarden een bereik aangeven, wordt de geavanceerde filtermodus geopend als u de veldnaam selecteert. Gebruik de vervolgkeuzelijst en tekstvakken om een bereik met waarden aan te geven dat u wilt zien. 

![geavanceerd filteren](media/end-user-report-filter/pbi_dropdown-and-text.png)

Door te kiezen tussen **En** en **Of**, kunt u complexe filterexpressies maken. Selecteer de knop **Filter toepassen** wanneer u de gewenste waarden hebt ingesteld.

## <a name="types-of-filters-date-and-time"></a>Typen filters: datum en tijd
### <a name="list-mode"></a>Lijstmodus
Als er een eindig aantal waarden is, wordt er een lijst weergegeven als u de veldnaam selecteert.  Zie **Tekstveldfilters** &gt; **Lijstmodus** hierboven voor hulp bij het gebruik van selectievakjes.   

### <a name="advanced-mode"></a>Geavanceerde modus
Als de veldwaarden datums of tijden vertegenwoordigen, kunt u een begin-/eindtijd opgeven wanneer u datum-/tijdfilters gebruikt.  

![datum/tijd-filter](media/end-user-report-filter/pbi_date-time-filters.png)


## <a name="next-steps"></a>Volgende stappen
[Leer hoe en waarom visuals elkaar in een rapport kruislings filteren en markeren](end-user-interactions.md)