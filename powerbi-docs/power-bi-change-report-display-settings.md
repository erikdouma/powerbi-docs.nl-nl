---
title: De grootte van een rapportpagina wijzigen
description: De weergave-instellingen voor een pagina in een Power BI-rapport wijzigen
author: mihart
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 01/24/2018
ms.author: mihart
LocalizationGroup: Reports
ms.openlocfilehash: e4ffc542a9564ba3893245ef637b3edd01c38640
ms.sourcegitcommit: 127df71c357127cca1b3caf5684489b19ff61493
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/03/2018
ms.locfileid: "37598750"
---
# <a name="change-the-size-of-a-report-page"></a>De grootte van een rapportpagina wijzigen
In het [vorige artikel en de video](power-bi-report-display-settings.md) hebt u twee verschillende manieren gezien om de paginaweergave in Power BI-rapporten te bepalen: **Weergave** en **Paginagrootte**. Paginaweergave en paginagrootte zijn beschikbaar in Power BI-service en Power BI Desktop, welke bijna identiek zijn qua uiterlijk en functioneren, maar voor deze zelfstudie maken we gebruik van Power BI-service.

### <a name="prerequisites"></a>Vereisten
- Power BI-service   
- [Voorbeeld van een retailanalyse](sample-retail-analysis.md)

## <a name="first-lets-change-the-page-view-setting"></a>Laten we eerst de pagina Weergave-instelling wijzigen

1. Open het rapport in de lees- of bewerkweergave en selecteer het rapporttabblad voor **Nieuwe winkels**. Deze rapportpagina wordt standaard weergegeven met behulp van de instelling **Passend op pagina**.  In dit geval geeft Passend op pagina de rapportpagina weer zonder schuifbalken, maar sommige details en titels zijn te klein om te lezen.

   ![](media/power-bi-change-report-display-settings/pbi_fit_to_page.png)
2. Zorg dat er geen visualisaties zijn ingeschakeld op het canvas. Selecteer **Weergave** en bekijk de weergaveopties.

   * In de Leesweergave ziet u dit.

     ![](media/power-bi-change-report-display-settings/power-bi-page-view-menu-new.png)
   * In de Bewerkweergave ziet u dit.

     ![](media/power-bi-change-report-display-settings/power-bi-view-editing-view.png)

3. Laten we kijken hoe de pagina eruit ziet met de instelling **Ware grootte** .

   ![](media/power-bi-change-report-display-settings/power-bi-actal-size2.png)

   Niet geweldig, het dashboard heeft nu dubbele schuifbalken.
4. Schakel over naar **Aan breedte aanpassen**.

   ![](media/power-bi-change-report-display-settings/pbi_fit_to_width.png)

   Het ziet er beter uit nu we schuifbalken hebben, is het makkelijker om de details te lezen.

## <a name="change-the-default-view-for-a-report-page"></a>De standaardweergave voor een rapportpagina wijzigen
Als u *auteur* van het rapport bent, kunt u de standaardweergave voor uw rapportpagina’s wijzigen. Wanneer u het rapport met anderen deelt, worden de rapportpagina's geopend met behulp van de weergave die u hebt ingesteld. *Gebruikers* van het rapport kunnen de weergave wijzigen, maar kunnen hun wijzigingen niet opslaan als ze het rapport afsluiten.

1. Op de pagina **Nieuwe winkels** van het rapport gaat u terug naar de weergave **Ware grootte**.

   ![](media/power-bi-change-report-display-settings/power-bi-actual-size.png)

2. Stel op de rapportpagina **Maandelijkse verkoop per district** de weergave in op **Passend in breedte**.

3. Laat op de rapportpagina **Overzicht** de standaardinstelling voor de weergave ongewijzigd.

4. Sla nu het rapport op door **Bestand > Opslaan** te selecteren. De volgende keer dat u dit rapport opent worden de pagina's weergegeven met de nieuwe weergave-instellingen. Laten we eens kijken.

   ![](media/power-bi-change-report-display-settings/power-bi-save.png)
3. Selecteer de naam van de huidige werkruimte in de bovenste navigatiebalk om terug te keren naar deze werkruimte.  

   ![](media/power-bi-change-report-display-settings/power-bi-my-workspace.png)
4. Selecteer het tabblad **Rapporten** en kies hetzelfde rapport (Voorbeeld van een retailanalyse).

    ![](media/power-bi-change-report-display-settings/power-bi-new-report2.png)
5. Open een pagina van het rapport om de nieuwe instellingen te bekijken.

   ![](media/power-bi-change-report-display-settings/power-bi-page-view.gif)

## <a name="now-lets-explore-the-page-size-setting"></a>Nu gaan we de instelling *Paginaformaat* bekijken
De instellingen voor paginagrootte zijn alleen beschikbaar in de [bewerkweergave](service-interact-with-a-report-in-editing-view.md), dus moet u (*auteurs-* of) bewerkmachtigingen voor het rapport te wijzigen van de instellingen voor paginagrootte. Als u verbonden bent met een van onze [voorbeelden](sample-datasets.md), dan hebt u *auteursmachtigingen* voor deze rapporten.

1. Open de pagina Maandelijkse verkoop per district van het [Voorbeeld van een retailanalyse](sample-retail-analysis.md) in de bewerkweergave.
2. Zorg dat er geen visualisaties zijn ingeschakeld op het canvas.  Selecteer in het deelvenster **Visualisaties** het pictogram van de verfroller ![](media/power-bi-change-report-display-settings/power-bi-paintroller.png).
3. Selecteer **Paginaformaat** &gt; **Type** om de opties voor paginaformaat weer te geven.

   ![](media/power-bi-change-report-display-settings/power-bi-page-size-menu-new.png)
4. Selecteer **Letter**.  Op het canvas blijft alleen de inhoud die binnen 816 x 1056 pixels (lettergrootte) op het witte gedeelte van het canvas past zichtbaar.

   ![](media/power-bi-change-report-display-settings/power-bi-letter-new.png)
5. Selecteer **Paginaformaat** **16:9**-verhouding.

   ![](media/power-bi-change-report-display-settings/power-bi-16-to-9-new.png)

   De rapportpagina wordt weergegeven met een verhouding van 16 breed bij 9 hoog. Om de werkelijke pixelgrootte te zien die wordt gebruikt, kijkt u naar de velden met een grijze achtergrond Breedte en Hoogte (1280x720). Er is veel lege ruimte rond het rapportcanvas. Dit komt omdat we eerder de **Weergave** op Passend in breedte hebben ingesteld.
7. Ga verder met het verkennen van de opties voor **Paginaformaat**.

## <a name="use-page-view-and-page-size-together"></a>Paginaweergave en paginagrootte samen gebruiken
Gebruik Paginaweergave en Paginagrootte samen om een rapport te maken dat het beste wordt weergegeven wanneer deze wordt gedeeld met collega’s of in een andere toepassing wordt opgenomen.

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

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)
