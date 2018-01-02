---
title: De grootte van een rapportpagina wijzigen (zelfstudie)
description: 'Zelfstudie: De weergave-instellingen voor een pagina in een Power BI-rapport wijzigen'
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: modifying
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/25/2017
ms.author: mihart
ms.openlocfilehash: a5cc05e26012f88e889612788d4479a370063d4f
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2017
---
# <a name="change-the-size-of-a-report-page-tutorial"></a>De grootte van een rapportpagina wijzigen (zelfstudie)
In het [vorige artikel en de video](power-bi-report-display-settings.md) hebt u twee verschillende manieren gezien om de paginaweergave in Power BI-rapporten te bepalen: **Weergave** en **Paginagrootte**. Nu gaan we het zelf proberen.

## <a name="first-lets-change-the-page-view-setting"></a>Laten we eerst de pagina Weergave-instelling wijzigen
1. Open een rapport in de lees- of bewerkingsweergave. In dit voorbeeld wordt de pagina 'Nieuwe winkels' van het [Voorbeeld van een retailanalyse](sample-retail-analysis.md) gebruikt.  Deze pagina wordt weergegeven met behulp van de instelling **Passend op pagina**.  In dit geval geeft Passend op pagina de rapportpagina weer zonder schuifbalken, maar sommige details en titels zijn te klein om te lezen.
   
   ![](media/power-bi-change-report-display-settings/pbi_fit_to_page.png)
2. Zorg dat er geen visualisaties zijn ingeschakeld op het canvas. Selecteer **Weergave** en bekijk de weergaveopties.

* In de Leesweergave ziet u dit.
  
     ![](media/power-bi-change-report-display-settings/power-bi-page-view-menu-new.png)
* In de Bewerkweergave ziet u dit.
  
    ![](media/power-bi-change-report-display-settings/power-bi-view-editing-view.png)

1. Laten we kijken hoe de pagina eruit ziet met de instelling **Ware grootte** .
   
   ![](media/power-bi-change-report-display-settings/power-bi-actal-size2.png)
   
   Niet geweldig, het dashboard heeft nu dubbele schuifbalken.
2. Schakel over naar **Aan breedte aanpassen**.
   
   ![](media/power-bi-change-report-display-settings/pbi_fit_to_width.png)
   
   Het ziet er beter uit nu we schuifbalken hebben, is het makkelijker om de details te lezen.

## <a name="change-the-default-view-for-a-report-page"></a>De standaardweergave voor een rapportpagina wijzigen
Alle Power BI-rapporten zijn standaard ingesteld op de weergave **Passend op pagina**. Maar wat gebeurt er als u wilt dat deze rapportpagina altijd worden geopend in de weergave **Ware grootte**?

1. Op de pagina **Nieuwe winkels** van het rapport gaat u terug naar de weergave **Ware grootte**.
   
   ![](media/power-bi-change-report-display-settings/power-bi-actual-size.png)
2. Sla het rapport met een andere naam op door het selecteren van **Bestand > Opslaan als**. U hebt nu 2 exemplaren van dit rapport; in het oorspronkelijke rapport wordt **New Stores** nog steeds geopend in de standaardweergave, maar in het nieuwe rapport wordt het geopend in de weergave **Ware grootte**. Laten we eens kijken.
   
   ![](media/power-bi-change-report-display-settings/power-bi-save-as.png)
3. Selecteer de naam van de huidige werkruimte in de bovenste navigatiebalk om terug te keren naar deze werkruimte.  
   
   ![](media/power-bi-change-report-display-settings/power-bi-my-workspace.png)
4. Selecteer het tabblad **Rapporten** en kies het nieuwe rapport dat u zojuist hebt gemaakt (met een geel sterretje).
   
    ![](media/power-bi-change-report-display-settings/power-bi-new-report2.png)
5. Het rapport wordt geopend de weergave **Ware grootte**!
   
   ![](media/power-bi-change-report-display-settings/power-bi-actal-size2.png)

## <a name="now-lets-explore-the-page-size-setting"></a>Nu gaan we de instelling *Paginaformaat* bekijken
De instellingen voor paginaformaat zijn alleen beschikbaar in [Bewerkweergave](service-interact-with-a-report-in-editing-view.md). Als u een rapport wilt openen in de bewerkweergave moet u eigenaarsmachtigingen hebben voor het rapport. Als u verbonden bent met een van onze [voorbeelden](sample-datasets.md), dan hebt eigenaarsmachtigingen voor deze rapporten.

1. Open de pagina Maandelijkse verkoop per district van het [Voorbeeld van een retailanalyse](sample-retail-analysis.md) in de bewerkweergave.
2. Zorg dat er geen visualisaties zijn ingeschakeld op het canvas.  Selecteer in het deelvenster **Visualisaties** het pictogram van de verfroller ![](media/power-bi-change-report-display-settings/power-bi-paintroller.png).
3. Selecteer **Paginaformaat** &gt; **Type** om de opties voor paginaformaat weer te geven.
   
   ![](media/power-bi-change-report-display-settings/power-bi-page-size-menu-new.png)
4. Selecteer **Letter**.  Op het canvas blijft alleen de inhoud die binnen 816 x 1056 pixels (lettergrootte) op het witte gedeelte van het canvas past zichtbaar.
   
   ![](media/power-bi-change-report-display-settings/power-bi-letter-new.png)
5. Als we **Weergave** wijzigen naar Passend in breedte wordt op ons canvas alleen de pagina-inhoud weergegeven die in de lettergrootte past.
   
   ![](media/power-bi-change-report-display-settings/power-bi-fit-to-width-new.png)
6. Selecteer **Paginaformaat** **16:9**-verhouding.
   
   ![](media/power-bi-change-report-display-settings/power-bi-16-to-9-new.png)
   
   De rapportpagina wordt weergegeven met een verhouding van 16 breed bij 9 hoog. Om de werkelijke pixelgrootte te zien die wordt gebruikt, kijkt u naar de velden met een grijze achtergrond Breedte en Hoogte (1280x720). Er is veel lege ruimte rond het rapportcanvas. Dit komt omdat we eerder de **Weergave** op Passend in breedte hebben ingesteld.
7. Ga verder met het verkennen van de opties voor **Paginaformaat**.

## <a name="using-page-view-and-page-size-together"></a>Paginaweergave en paginaformaat samen gebruiken
Gebruik Paginaweergave en Paginaformaat samen om een rapport te maken dat het beste wordt weergegeven wanneer het in een andere toepassing wordt opgenomen.

In deze oefening maakt u een rapportpagina die wordt weergegeven in een toepassing die ruimte heeft voor 500 pixels breed bij 750 pixels hoog.

Vergeet niet dat u in de vorige stap hebt gezien dat onze rapportpagina momenteel wordt weergegeven op 1280 breed bij 720 hoog. We weten dus dat we heel wat moeten vergroten/verkleinen en herschikken als we willen dat al onze visuele elementen passen.

1. Vergroot of verklein de visuele elementen zodat ze in minder dan de helft van het huidige tekengebied passen.
   
    ![](media/power-bi-change-report-display-settings/power-bi-custom-view.gif)
2. Selecteer **Paginaformaat** &gt; **Aangepast**.
3. Stel de breedte in op 500 en de hoogte op 750.
   
    ![](media/power-bi-change-report-display-settings/power-bi-custom-new.png)
4. Wijzig de rapportagepagina totdat deze er het beste uitziet. Schakel tussen **Weergave > Ware grootte** en **Weergave > Passend op pagina** om wijzigingen door te voeren.
   
    ![](media/power-bi-change-report-display-settings/power-bi-final-new.png)

## <a name="next-steps"></a>Volgende stappen
[Rapporten voor Cortana maken](service-cortana-answer-cards.md)

Terug naar [Instellingen voor de paginaweergave in een Power BI-rapport](power-bi-report-display-settings.md)

Lees meer over [rapporten in Power BI](service-reports.md)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

