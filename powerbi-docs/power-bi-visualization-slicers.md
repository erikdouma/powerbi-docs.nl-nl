---
title: Slicers in Power BI (zelfstudie)
description: 'Zelfstudie: Slicers in Power BI'
services: powerbi
documentationcenter: ''
author: mihart
manager: kfile
backup: ''
editor: ''
tags: ''
featuredvideoid: zIZPA0UrJyA
qualityfocus: monitoring
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 03/05/2018
ms.author: v-thepet
LocalizationGroup: Visualizations
ms.openlocfilehash: cfa4c0f17c67a036b7d01744da1b5247345c493a
ms.sourcegitcommit: 4217430c3419046c3a90819c34f133ec7905b6e7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2018
---
# <a name="slicers-in-power-bi-tutorial"></a>Slicers in Power BI (zelfstudie)
Een adjunct-directeur van Verkoop wil verschillende metrische gegevens kunnen inzien, voor de gehele afdeling en voor elke afzonderlijke District Manager. Ze kan voor elke manager een apart rapport maken, of ze kan een slicer gebruiken. Een slicer beperkt het gedeelte van de gegevensset dat wordt weergegeven in andere visualisaties in een rapport. Slicers bieden een alternatieve manier voor filteren.

In deze zelfstudie wordt gebruikgemaakt van de gratis [Voorbeeld van een retailanalyse](sample-retail-analysis.md) om u te helpen u bij het maken en opmaken van een slicer en hoe u deze kunt gebruiken om een rapport te filteren. Ontdek manieren om slicers op te maken en te gebruiken. 

![slicer](media/power-bi-visualization-slicers/slicer2.gif)

## <a name="when-to-use-a-slicer"></a>Een slicer gebruiken
Slicers zijn een goede keuze als u:

* veelgebruikte of belangrijke filters op het rapportcanvas wilt weergeven voor een eenvoudigere toegang;
* de huidige gefilterde status gemakkelijker wilt bekijken zonder dat u een vervolgkeuzelijst hoeft te openen; 
* wilt filteren op kolommen die niet nodig zijn en verborgen zitten in de gegevenstabellen;
* meer gerichte rapporten wilt maken door slicers naast belangrijke visuele elementen te zetten.

Slicers van Power BI hebben de volgende beperkingen:

- Slicers bieden geen ondersteuning voor invoervelden.
- Slicers kunnen niet worden vastgemaakt aan een dashboard.
- Detailweergave wordt niet ondersteund voor slicers.
- Slicers bieden geen ondersteuning voor filters op niveau van visuele elementen.

## <a name="create-a-slicer"></a>Een slicer maken

In deze zelfstudie wordt gebruikgemaakt van een lijstslicer. Voor de gegevenstypen Numeriek en Datum/tijd kunt u bereikslicers gebruiken. Zie [De slicer voor numeriek bereik gebruiken in Power BI Desktop](desktop-slicer-numeric-range.md) of de volgende video voor meer informatie over het maken en gebruiken van bereikslicers.
<iframe width="560" height="315" src="https://www.youtube.com/embed/zIZPA0UrJyA" frameborder="0" allowfullscreen></iframe>

1. Open in Power BI Desktop of de Power BI-service het [Voorbeeld van een retailanalyse](sample-retail-analysis.md) in de [Bewerkweergave](service-interact-with-a-report-in-editing-view.md) en [voeg een nieuwe rapportpagina toe](power-bi-report-add-page.md).
2. Selecteer in het deelvenster Velden onder District **District Manager** voor het maken van een nieuwe visualisatie.
    
    ![nieuwe grafiek](media/power-bi-visualization-slicers/1-new-vis.png)
    
3. Selecteer het pictogram **Slicer** ![Slicer-pictogram](media/power-bi-visualization-slicers/slicer-icon.png) in het deelvenster Visualisaties om de nieuwe visualisatie te converteren naar een slicer. 
    
    ![converteren naar slicer](media/power-bi-visualization-slicers/2-slicer.png)

U kunt ook het pictogram Slicer selecteren om een nieuwe slicer te maken en vervolgens een gegevensveld selecteren of het naar het vak Veld slepen om het vak hiermee te vullen.

>[!TIP]
>U kunt items van de lijstslicer sorteren op gegevenswaarden. Als u sliceritems in omgekeerde alfabetische volgorde wilt sorteren, selecteert u de weglatingstekens (...) in de rechterbovenhoek van de slicer en kiest u **Sorteren op District Manager**. De instelling is standaard alfabetisch oplopend, maar schakelen tussen oplopende of aflopende volgorde is mogelijk. 

## <a name="format-the-slicer"></a>De slicer opmaken
Pas visuele opmaak toe op de District Manager-slicer.
1. Selecteer, terwijl de slicer is geselecteerd, in het deelvenster Visualisaties het pictogram Opmaak ![](media/power-bi-visualization-slicers/power-bi-paintroller.png) om de besturingselementen voor opmaken weer te geven. 
    
    ![opmaak](media/power-bi-visualization-slicers/3-format.png)
    
2. Klik op de vervolgkeuzelijstpijlen naast elke categorie om de opties weer te geven en te bewerken. 

### <a name="general-options"></a>Algemene opties
1. Selecteer rood bij de **kleur van omtrek** en wijzig **de dikte van omtrek** in '2'. Dit stelt de kleur en de dikte in van de omtrekken of onderstrepingen van kopteksten en items, wanneer deze zijn ingeschakeld. 
2. Bij Stand is verticaal de standaardinstelling, waarmee een slicer voor verticale lijsten wordt gemaakt met selectievakjes vóór de items. Selecteer **Horizontaal** voor het produceren van een slicer met horizontaal gerangschikte items. De horizontale stand kan diverse rankschikkingsmogelijkheden opleveren voor tekst, knoppen of tegels, afhankelijk van de slicergrootte en -vorm en de opmaak van het item. 
    
    ![horizontaal](media/power-bi-visualization-slicers/4-horizontal.png)
    
3. Schakel de lay-out **Responsief** in, waarin de grootte en de rangschikking van de horizontale sliceritems zo wordt gewijzigd dat deze overeenkomen met de afmeting en vorm van de slicer. In een zeer klein formaat wordt de slicer een filterpictogram. 
    
    ![responsief](media/power-bi-visualization-slicers/5-responsive.png)
    
    >[!NOTE]
    >Wijzigingen in de responsieve lay-out kunnen specifieke, door u ingestelde opmaak van kopteksten en items opmaak overschrijven. 
    
4. Stel de positie en grootte van de slicer in met numerieke precisie onder **X-positie**, **Y-positie**, **Breedte**, en **Hoogte**, of verplaats en wijzig de grootte van de slicer rechtstreeks op het canvas, wat verschillende groottes en rangschikkingen van items oplevert, zoals een horizontale rij knoppen. 

    ![horizontale knoppen](media/power-bi-visualization-slicers/6-buttons.png)

Zie [Een responsieve slicer maken waarvan u de grootte kunt wijzigen in Power BI](power-bi-slicer-filter-responsive.md) voor meer informatie over de horizontale stand en responsieve opmaak.

### <a name="selection-controls-options"></a>Opties voor selectiebesturingselementen
1. Alles selecteren weergeven is standaard uitgeschakeld. Zet deze op **Aan** om het item Alles selecteren aan de slicer toe te voegen waarin alle items worden geselecteerd of gedeselecteerd wanneer u omschakelt. Wanneer alle items zijn geselecteerd, wordt één item gedeselecteerd als u erop klikt, zodat u een 'is-niet'-type filter krijgt. 
    
    ![alles selecteren](media/power-bi-visualization-slicers/7-select-all.png)
    
2. Eén selecteren is standaard ingeschakeld. U selecteert een item door erop te klikken, en u selecteert meerdere items wanneer u bij het klikken de CTRL-toets ingedrukt houdt. Zet Eén selecteren op **Uit** zodat u meerdere items kunt selecteren zonder de CTRL-toets ingedrukt te hoeven houden. U deselecteert een item door opnieuw erop te klikken. 

### <a name="header-options"></a>Opties voor Kopteksten
De koptekst is standaard ingeschakeld, waarin de naam van het gegevensveld aan de bovenkant van de slicer wordt weergegeven. 
1. Maak de koptekst zo op dat de **tekstkleur** rood, de **tekengrootte** 14 pt en **lettertypefamilie** Arial Black is. 
2. Kies onder Omtrek **Alleen onder** om een onderstreping te krijgen met de grootte en de kleur die u hebt ingesteld onder algemene opties. 

### <a name="item-options"></a>Opties voor items
1. Maak de tekst en de achtergrond van items zo op dat de **tekstkleur** zwart, de **achtergrond** lichtrood, de **tekengrootte** 10 pt en de **lettertypefamilie** Arial is. 
2. Kies onder Omtrek **Kader** om een rand om elk item te tekenen met de grootte en de kleur die u bij algemene opties hebt ingesteld. 
    
    ![opgemaakt](media/power-bi-visualization-slicers/8-formatted.png)
    
    >[!TIP]
    >- Gedeselecteerde items tonen bij een horizontale stand de gekozen tekst- en achtergrondkleuren, terwijl de geselecteerde items gebruikmaken van de systeemstandaard, doorgaans een zwarte achtergrond met witte tekst. 
    >- Bij een verticale stand tonen items altijd de ingestelde kleuren, en selectievakjes zijn altijd zwart wanneer deze zijn geselecteerd. 

### <a name="other-formatting-options"></a>Overige opmaakopties
De overige opmaakopties zijn standaard uitgeschakeld. Indien **ingeschakeld**: 
- **Titel:** Hiermee wordt een titel toegevoegd en opgemaakt (naast en onafhankelijk van de koptekst) aan de bovenkant van de slicer. 
- **Achtergrond:** Hiermee wordt een achtergrondkleur toegevoegd aan de algehele slicer en wordt de transparantie ingesteld.
- **Aspect vergrendelen:** Hiermee wordt de vorm van de slicer behouden als de grootte ervan wordt gewijzigd.
- **Rand:** Hiermee wordt een rand van 1-pixel rondom de slicer toegevoegd en wordt de kleur ervan ingesteld. (Deze slicerrand valt niet onder en wordt niet beïnvloed door de algemene omtrekinstellingen.) 

## <a name="sync-and-use-the-slicer-on-other-pages"></a>De slicer synchroniseren en op andere pagina's gebruiken
Met ingang van de Power BI-update van februari 2018 kunt u een slicer synchroniseren en deze op een of alle pagina's in een rapport gebruiken. 
1. Selecteer, terwijl u de District Manager-slicer hebt geselecteerd, in het menu Weergave **Slicers synchroniseren** in Power BI Desktop of schakel het deelvenster **Slicers synchroniseren** in bij Power BI-service. Het deelvenster Slicers synchroniseren wordt weergegeven. 
    
    ![slicers synchroniseren](media/power-bi-visualization-slicers/9-sync-slicers.png)
    
2. Selecteer in de eerste kolom **Overzicht** en andere pagina's waarmee u wilt de slicer wilt laten synchroniseren, of klik op **Toevoegen aan alle** waarmee u de slicer laat synchroniseren met alle rapportpagina's.  
3. Selecteer in de volgende kolom **Overzicht** en alle andere pagina's waarop de slicer zichtbaar moet zijn. 
4. Schakel over naar de pagina **Overzicht** en observeer de slicer en welk effect deze heeft op de andere visuele elementen op de pagina. 
    - Maak en verwijder verschillende selecties van items, en observeer hoe de andere visuele elementen op de pagina zich dienovereenkomstig wijzigen. De selectie van items op een pagina wordt op alle gesynchroniseerde pagina's weergegeven.
    - De grootte, vorm, positie en/of opmaak wijzigen van de slicer op de pagina Overzicht. De opmaak van de slicer op andere gesynchroniseerde pagina's wordt niet gewijzigd. 

### <a name="control-which-page-visuals-are-affected-by-the-slicer"></a>Regelen welke visuele elementen op de pagina worden beïnvloed door de slicer
Standaard is een slicer op een rapportpagina van invloed op alle andere visualisaties op die pagina. Gebruik **Visuele interacties** om te voorkomen dat bepaalde visualisaties op de pagina worden beïnvloed.

1. Wanneer op de pagina **Overzicht** de slicer is geselecteerd:
    - Klik in Power BI Desktop op het menu Opmaak onder Visual Tools en selecteer **Interacties bewerken**.
    - Kies in de Power BI-service **Visual interacties** in de menubalk en schakel **Interacties bewerken** in. 
    
    De besturingselementen voor filteren verschijnen boven alle andere visuele elementen op de pagina. ![besturingselementen voor filteren](media/power-bi-visualization-slicers/filter-controls.png)
    
2. Selecteer het pictogram **Geen** boven een visueel element om de slicer te laten stoppen met filteren. Selecteer het pictogram **Filteren** om ervoor te zorgen dat de slicer het visuele element opnieuw gaat filteren. 

Zie [Visuele interacties in een Power BI-rapport](service-reports-visual-interactions.md) voor meer informatie over het bewerken van interacties.

## <a name="next-steps"></a>Volgende stappen
[Probeer het uit - het is gratis.](https://powerbi.com/)

Hebt u ideeën voor het verbeteren van Power BI? [Een idee verzenden](https://ideas.powerbi.com/forums/265200-power-bi-ideas).

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

[Een visualisatie toevoegen aan een rapport](power-bi-report-add-visualizations-i.md)

[Typen visualisaties in Power BI](power-bi-visualization-types-for-reports-and-q-and-a.md)

[Power BI - basisconcepten](service-basic-concepts.md)

