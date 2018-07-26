---
title: Aan de slag met Power BI Q&A
description: Aan de slag met Q&A in de Power BI-service met een retailanalyse als voorbeeld
author: mihart
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 01/16/2018
ms.author: mihart
LocalizationGroup: Ask questions of your data
ms.openlocfilehash: c567921b765f03fbaa11f2b98724cea1a1ce1905
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2018
ms.locfileid: "34240980"
---
# <a name="get-started-with-power-bi-qa"></a>Aan de slag met Power BI Q&A
## <a name="use-power-bi-qa-with-the-retail-analysis-sample"></a>De Q&A-functie van Power BI gebruiken met een retailanalyse als voorbeeld
Soms krijgt u het snelst een antwoord uit uw gegevens wanneer u een vraag stelt in natuurlijke taal.  In deze snelstartgids bekijken we twee verschillende manieren om dezelfde visualisatie te maken: eerst samenstellen in een rapport en daarna een vraag stellen met Q&A. We doen dit met behulp van Power BI-service, maar het proces is bijna identiek aan als u dit doet met behulp van Power BI Desktop.

Als u dit wilt volgen, moet u een rapport gebruiken dat u kunt bewerken. Daarom maken we gebruik van een van de voorbeelden die beschikbaar zijn met Power BI.

## <a name="method-1-using-the-report-editor"></a>Methode 1: met behulp van de rapporteditor
1. Selecteer in de Power BI-werkruimte **Gegevens ophalen** \> **Voorbeelden** \> **Voorbeeld van een retailanalyse**  >  **Verbinding maken**.
   
    ![](media/power-bi-visualization-introduction-to-q-and-a/power-bi-dashboard.png)
2. Het dashboard bevat een diagramtegel voor de omzet van het afgelopen jaar en de omzet van dit jaar.  Selecteer deze tegel. 
   
   * Als deze tegel is gemaakt met Q&A en u de tegel selecteert, wordt Q&A geopend. 
   * Deze tegel is echter gemaakt in een rapport, waardoor het rapport wordt geopend op de pagina met deze visualisatie.
3. Open het rapport in de bewerkingsweergave en selecteer **Rapport bewerken**.  Als u niet de eigenaar van een rapport bent, kunt u het rapport niet openen in de bewerkingsweergave.
   
    ![](media/power-bi-visualization-introduction-to-q-and-a/power-bi-edit-report.png)
4. Selecteer het vlakdiagram en controleer de instellingen in het deelvenster **Velden**.  De maker van het rapport heeft dit diagram samengesteld door deze drie waarden (**Tijd > FiscalMonth**, **Verkoop > Omzet van dit jaar**, **Verkoop > Omzet van afgelopen jaar > Waarde**) te selecteren en ze te ordenen in de bronnen **As** en **Waarden**.
   
    ![](media/power-bi-visualization-introduction-to-q-and-a/gnatutorial_3-new.png)

## <a name="method-2-using-qa"></a>Methode 2: Q&A gebruiken
Hoe zouden we hetzelfde lijndiagram maken met Q&A?

![](media/power-bi-visualization-introduction-to-q-and-a/power-bi-qna.png)

1. Navigeer terug naar het dashboard Voorbeeld van een retailanalyse.
2. Typ iets als het volgende in het vragenvak in natuurlijke taal:
   
   **Wat was de omzet van dit jaar en vorig jaar, per maand als vlakdiagram**
   
   Als u een vraag typt, kiest de Q&A-functie de beste visualisatie om uw antwoord weer te geven. De visualisatie wordt dynamisch gewijzigd als u de vraag wijzigt. Q&A helpt u ook om uw vraag te formuleren door suggesties te bieden, de vraag automatisch aan te vullen en spellingcorrecties toe te passen.
   
   Als u de vraag hebt getypt, resulteert dit in exact hetzelfde diagram als in het rapport.  Maar op deze manier is het diagram veel sneller gemaakt.
   
   ![](media/power-bi-visualization-introduction-to-q-and-a/powerbi-qna-areachart.png)
3. Net als wanneer u met rapporten werkt, hebt u in Q&A toegang tot de deelvensters Visualisaties, Filters en Velden.  Open deze deelvensters om uw visual verder te verkennen en te wijzigen.
4. Selecteer het speldpictogram ![](media/power-bi-visualization-introduction-to-q-and-a/pinnooutline.png) om uw diagram aan het dashboard vast te maken.

## <a name="next-steps"></a>Volgende stappen
[Q&A in Power BI](power-bi-q-and-a.md)

[Uw gegevens geschikt maken voor Q&A in Power BI](service-prepare-data-for-q-and-a.md)

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

