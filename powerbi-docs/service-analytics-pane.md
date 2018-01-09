---
title: Het deelvenster Analyse in de Power BI-service
description: Dynamische referentielijnen maken voor visuals in de Power BI-service
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
ms.date: 12/21/2017
ms.author: mihart
ms.openlocfilehash: 3750d733967301f952fd092d2d1d0a2b9d1b2238
ms.sourcegitcommit: 6ea8291cbfcb7847a8d7bc4e2b6abce7eddcd0ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/21/2017
---
# <a name="analytics-pane-in-power-bi-service"></a>Het deelvenster Analyse in de Power BI-service
Met het deelvenster **Analyse** in de **Power BI-service** kunt u dynamische *referentielijnen* toevoegen aan visualisaties en de aandacht vestigen op belangrijke trends of inzichten.

![](media/service-analytics-pane/power-bi-analytics-pane.png)

> [!NOTE]
> Het deelvenster **Analyse** wordt alleen weergegeven wanneer u een visueel element op het rapportcanvas selecteert.
> 
> 

## <a name="using-the-analytics-pane"></a>Het deelvenster Analyse gebruiken
Met het deelvenster **Analyse** kunt u de volgende soorten dynamische referentielijnen maken (niet alle lijnen zijn beschikbaar voor alle soorten visuals):

* Constante lijn voor de X-as
* Constante lijn voor de Y-as
* Lijn voor minimum
* Lijn voor maximum
* Lijn voor gemiddelde
* Lijn voor mediaan
* Lijn voor percentiel


Voer de volgende stappen uit als u de beschikbare dynamische referentielijnen voor een visual wilt weergeven:

1. Selecteer of maak een visual en selecteer vervolgens het pictogram **Analyse** in het deelvenster ![](media/service-analytics-pane/power-bi-analytics-icon.png)**Visualisaties**.

2. Selecteer de pijl-omlaag voor het type lijn dat u wilt maken om de bijbehorende opties uit te breiden. In dit geval selecteren we **Lijn voor gemiddelde**.
   
   ![lijn voor gemiddelde toevoegen](media/service-analytics-pane/power-bi-add.png)

3. Als u een nieuwe lijn wilt maken, selecteert u **+ Toevoegen** en bepaalt u de eenheid die wordt gebruikt om de lijn te maken.  De vervolgkeuzelijst **Eenheid** wordt automatisch ingevuld met de beschikbare gegevens uit de geselecteerde visualisatie. Wij gebruiken nu **Aantal open winkels**.

5. U beschikt over allerlei opties voor de lijn, zoals kleur, transparantie, stijl en positie (ten opzichte van de gegevenselementen van het visuele element). Als u de lijn een label wilt geven, geeft u de lijn een titel en verplaatst u de schuifregelaar **Gegevenslabel** naar **Aan**.  In dit geval selecteren we *Gem. aantal open winkels* en passen we enkele van de andere opties toe aan zoals hieronder wordt weergegeven.
   
   ![Analyse voor Lijn voor gemiddelde aanpassen](media/service-analytics-pane/power-bi-average-line2.png)

1. Let op het getal dat naast het item **Lijn voor gemiddelde** in het deelvenster **Analyse** wordt weergegeven. Zo weet u hoeveel dynamische lijnen de visual momenteel bevat en van welk type. Als we een **constante lijn** met een doelaantal van negen winkels toevoegen, ziet u dat het deelvenster **Analyse** dat we nu ook een **Constant constante lijn** als referentielijn hebben toegepast op deze visual.
   
   ![](media/service-analytics-pane/power-bi-reference-lines.png)
   

Er zijn allerlei interessante inzichten die u kunt benadrukken door dynamische referentielijnen te maken met het deelvenster **Analyse**.

## <a name="considerations-and-troubleshooting"></a>Aandachtspunten en probleemoplossing

Als op de visual die u hebt geselecteerd (in dit geval een **kaart**) geen dynamische referentielijnen kunnen worden toegepast, ziet u het volgende wanneer u het deelvenster **Analyse** selecteert.
   
![analyse is niet beschikbaar](media/service-analytics-pane/power-bi-no-lines.png)

De mogelijkheid om dynamische referentielijnen te gebruiken is gebaseerd op het type visual dat wordt gebruikt. In de volgende lijst wordt aangegeven welke dynamische lijnen momenteel beschikbaar zijn voor welke visuele elementen:

Volledig gebruik van dynamische lijnen is beschikbaar voor de volgende visuals:

* Vlakdiagram
* Lijndiagram
* Spreidingsdiagram
* Gegroepeerd kolomdiagram
* Gegroepeerd staafdiagram

De volgende visuals kunnen alleen een *constante lijn* uit het deelvenster **Analyse** gebruiken:

* Gestapeld vlakdiagram
* Gestapeld staafdiagram
* Gestapeld kolomdiagram
* 100% gestapeld staafdiagram
* 100% gestapeld kolomdiagram

Voor de volgende visuals is een *trendlijn* momenteel de enige optie:

* Niet-gestapeld lijndiagram
* Gegroepeerd kolomdiagram

Tot slot kunnen voor niet-Cartesische visuals momenteel geen dynamische lijnen uit het deelvenster **Analyse** worden toegepast, zoals:

* Matrix
* Cirkeldiagram
* Ringdiagram
* Tabel

## <a name="next-steps"></a>Volgende stappen
[Het deelvenster Analyse in Power BI Desktop](desktop-analytics-pane.md)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

