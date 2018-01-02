---
title: 'Zelfstudie: Berekende kolommen in Power BI Desktop maken'
description: 'Zelfstudie: Berekende kolommen in Power BI Desktop maken'
services: powerbi
documentationcenter: 
author: davidiseminger
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
ms.date: 12/06/2017
ms.author: davidi
ms.openlocfilehash: 9ea93980a095ca4e626b6f8071d044448af59635
ms.sourcegitcommit: d91436de68a0e833ecff18d976de9d9431bc4121
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/06/2017
---
# <a name="tutorial-create-calculated-columns-in-power-bi-desktop"></a>Zelfstudie: Berekende kolommen in Power BI Desktop maken
De gegevens die u analyseert bevatten soms niet een bepaald veld dat u nodig hebt om de gewenste resultaten te krijgen. In dergelijke gevallen bieden berekende kolommen uitkomst. Berekende kolommen gebruiken DAX-formules (Data Analysis Expressions) om de waarden in een kolom te definiëren. Die waarden kunnen bijna van alles zijn, of het nu gaat om het samenstellen van tekstwaarden uit een aantal verschillende kolommen elders in het model of om het berekenen van een numerieke waarde op basis van andere waarden. Stel uw gegevens bevatten een kolom Plaats en een kolom Staat (als velden in de lijst Velden), maar u wilt één veld Locatie waarin beide waarden als één waarde zijn opgenomen, zoals Miami, FL. En dat is precies waarvoor berekende kolommen bedoeld zijn.

Berekende kolommen zijn vergelijkbaar met metingen in die zin dat beide gebaseerd zijn op een DAX-formule, maar van elkaar verschillen in de manier waarop ze worden gebruikt. Metingen worden het vaakst gebruikt in het gebied Waarden van een visualisatie om resultaten te berekenen op basis van andere velden in een rij in een tabel of op een as, in een legenda of groep van een visualisatie. Anderzijds worden berekende kolommen gebruikt wanneer u de resultaten van de kolom in die rij in de tabel of op de as, in de legenda of groep wilt.

Deze zelfstudie bevat uitleg en een stapsgewijze procedure voor het maken van enkele berekende kolommen in Power BI Desktop. De zelfstudie is bedoeld voor Power BI-gebruikers die al bekend zijn met het gebruik van Power BI Desktop en eraan toe zijn om geavanceerdere modellen te maken. U dient al te weten hoe u Query gebruikt om gegevens te importeren, hoe u werkt met meerdere verwante tabellen en hoe u velden toevoegt aan het rapportcanvas. Raadpleeg [Aan de slag met Power BI Desktop](desktop-getting-started.md) als u nog geen ervaring hebt met het gebruik van Power BI Desktop.

Om de stappen in deze zelfstudie te voltooien, moet u het bestand [Contoso-verkoopvoorbeeld voor Power BI Desktop](http://download.microsoft.com/download/4/6/A/46AB5E74-50F6-4761-8EDB-5AE077FD603C/Contoso%20Sales%20Sample%20for%20Power%20BI%20Desktop.zip) downloaden. Dit is hetzelfde voorbeeldbestand dat wordt gebruikt in de zelfstudie [Uw eigen metingen maken in Power BI Desktop](desktop-tutorial-create-measures.md). Het bestand bevat al verkoopgegevens van het fictieve bedrijf Contoso, Inc. Omdat de gegevens in het bestand zijn geïmporteerd uit een database, kunt u geen verbinding maken met de gegevensbron en ook geen gegevens weergeven in Query-editor. Nadat u het bestand hebt gedownload naar uw computer, opent u het in Power BI Desktop.

## <a name="lets-create-a-calculated-column"></a>We gaan een berekende kolom maken
Stel dat we productcategorieën willen weergeven samen met subcategorieën van producten in één enkele waarde in rijen, zoals Mobiele telefoons – accessoires, Mobiele telefoons – smartphones & PDA's, enzovoort. Als we in de Rapport- en Gegevensweergave (we gebruiken hier de Rapportweergave) naar onze producttabellen in de lijst met velden kijken, is er blijkbaar geen veld met informatie die we nodig hebben. We hebben echter wel een veld ProductCategory en een veld ProductSubcategory, elk in hun eigen tabel.

 ![](media/desktop-tutorial-create-calculated-columns/calccol_fileds_nonewcol.png)

We maken een nieuwe berekende kolom om waarden uit deze twee kolommen te combineren naar nieuwe waarden voor de nieuwe kolom. Opmerkelijk genoeg moeten we gegevens uit twee verschillende tabellen combineren in één kolom. Omdat we DAX gaan gebruiken om de nieuwe kolom te maken, kunnen we gebruikmaken van alle mogelijkheden van het model dat we al hebben, inclusief de relaties tussen verschillende tabellen die al bestaan.

### <a name="to-create-a-productfullcategory-column"></a>Een ProductFullCategory-kolom maken
1.  Klik met de rechtermuisknop op (of klik op de pijl-omlaag bij) de tabel **ProductSubcategory** in de lijst met velden en klik vervolgens op **New Column**. Hiermee zorgt u ervoor dat de nieuwe kolom wordt toegevoegd aan de tabel ProductSubcategory.
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_fileds_newcolumn.png)
    
    De formulebalk wordt weergegeven aan de bovenkant van het rapportcanvas of het gegevensraster. Hier kunnen we de naam van de kolom wijzigen en een DAX-formule invoeren.
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_fileds_newcolumnformula.png)
    
    Een nieuwe berekende kolom heet standaard gewoon Column. Als we de naam niet wijzigen en we een nieuwe kolom maken, krijgt die de naam Column 2, Column 3, enzovoort. We willen de kolommen herkenbaarder maken, dus geven we de nieuwe kolom een nieuwe naam.
    
2.  Aangezien de naam **Column** al in de formulebalk is gemarkeerd, typt u **ProductFullCategory**.
    
    Nu kunnen we de formule gaan invoeren. We willen de waarden in de nieuwe kolom laten beginnen met de ProductCategory-naam uit de tabel ProductCategory. Omdat deze kolom in een andere, maar wel gerelateerde tabel staat, gaan we daarvoor de functie [RELATED](https://msdn.microsoft.com/library/ee634202.aspx) gebruiken.
    
3.  Typ na het gelijkteken een **R**. In een vervolgkeuzelijst wordt een lijst met suggesties weergegeven met alle DAX-functies die beginnen met de letter R. Hoe meer u typt, hoe korter de lijst met suggesties wordt. Ga door tot u de gewenste functie hebt gevonden. Naast de functie ziet u een beschrijving van de functie. Selecteer **RELATED** door omlaag te schuiven en druk vervolgens op Enter.
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_fileds_pfc_1.png)
    
    Er wordt een haakje openen weergegeven en een andere lijst met suggesties, ditmaal voor alle beschikbare kolommen die kunnen worden doorgegeven in de functie RELATED. Er wordt ook een beschrijving weergegeven, samen met informatie over welke parameters worden verwacht.
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_fileds_pfc_2.png)
    
    Een expressie wordt altijd wordt weergegeven tussen een haakje openen en een haakje sluiten. In dit geval bevat onze expressie één argument die wordt doorgegeven aan de functie RELATED; een gerelateerde kolom waaruit waarden worden geretourneerd. De lijst met kolommen wordt automatisch verkleind zodat alleen de gerelateerde kolommen worden weergegeven. In dit geval willen we de kolom ProductCategory opnemen in de tabel ProductCategory.
    
    Selecteer **ProductCategory[ProductCategory]** en typ een haakje sluiten.
    
    > [!TIP]
    > Syntaxisfouten zijn meestal te wijten aan een ontbrekend of verkeerd geplaatst haakje sluiten. Maar Power BI Desktop zal dat in veel gevallen automatisch toevoegen, mocht u het vergeten.
    > 
    > 
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_fileds_pfc_3.png)
    
4. We willen een koppeltekensymbool toevoegen om de waarden van elkaar te scheiden. Typ daarom na het haakje sluiten van de eerste expressie een spatie, een en-teken (&), een aanhalingsteken, een spatie, een koppelteken (-), nog een spatie, een aanhalingsteken sluiten en tot slot nog een en-teken. De formule moet er nu zo uitzien:
    
    **ProductFullCategory = RELATED(ProductCategory[ProductCategory]) & " - " &**
    
    > [!TIP]
    > Klik op de dubbele pijl-omlaag rechts van de formulebalk om de formule-editor uit te vouwen. Druk op Alt en Enter om een regel omlaag te gaan en op Tab om items te verplaatsen.
    > 
    > 
    
5.  Typ tot slot nog een haakje openen en selecteer de kolom **[ProductSubcategory]** om de formule te voltooien. De formule moet er nu zo uitzien:
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_fileds_pfc_5.png)
    
    U ziet dat we geen andere RELATED-functie hebben gebruikt in de tweede expressie voor het aanroepen van de kolom ProductSubcategory. Dat komt omdat deze kolom al in dezelfde tabel staat waarin we de nieuwe kolom maken. We kunnen [ProductCategory] invoeren met de tabelnaam (volledig gekwalificeerde naam) of zonder de tabelnaam (niet-gekwalificeerde naam).
    
6.  Voltooi de formule door op Enter te drukken of op het vinkje in de formulebalk te klikken. De formule wordt gevalideerd en toegevoegd aan de lijst met velden in de tabel **ProductSubcategory**.
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_fileds_pfc_6.png)
    
    Zoals u ziet, krijgen berekende kolommen een speciaal pictogram in de lijst met velden. Dat geeft aan dat ze een formule bevatten. Zo worden ze alleen in Power BI Desktop weergegeven. Het is in de Power BI-service (uw Power BI-site) niet mogelijk om een formule te wijzigen en daarom heeft een veld met een berekende kolom geen pictogram.
    
## <a name="lets-add-our-new-column-to-a-report"></a>Laten we onze nieuwe kolom toevoegen aan een rapport
We kunnen nu de nieuwe ProductFullCategory-kolom toevoegen aan het rapportcanvas. Laten we SalesAmount bekijken op basis van ProductFullCategory.

Sleep de kolom **ProductFullCategory** uit de tabel **ProductSubcategory** naar het rapportcanvas en sleep het veld **SalesAmount**uit de tabel **Sales** naar de grafiek.

![](media/desktop-tutorial-create-calculated-columns/calccol_fileds_report_1.png)

## <a name="lets-create-another"></a>Laten we nog een kolom maken
Nu u weet hoe u een berekende kolom kunt maken, maken we er nog een.

Het Contoso Sales Sample for Power BI Desktop-model bevat verkoopgegevens voor zowel actieve als inactieve winkels. We willen duidelijk laten zien dat de gegevens voor inactieve winkels ook als zodanig worden aangeduid. Daarom gaan we een veld met de naam Active StoreName maken. Daarvoor maken we een andere kolom. Wanneer, zoals in dit geval, een winkel niet actief is, willen we dat de nieuwe Active StoreName-kolom (als een veld) de naam van de winkel weergeeft als 'Inactief', maar wel de echte naam van de winkel laat zien als deze actief is.

Gelukkig heeft de tabel Stores een kolom Status, met de waarde On voor actieve winkels en Off voor inactieve winkels. We kunnen waarden voor elke rij in de kolom Status testen om nieuwe waarden in de nieuwe kolom te maken.

### <a name="to-create-an-active-storename-column"></a>Een Active StoreName-kolom maken
1.  Maak een nieuwe berekende kolom met de naam **Active StoreName** in de tabel **Stores**.
    
    Voor deze kolom gaat onze DAX-formule de status van elke kolom controleren. Als de status van een winkel On is, wordt de naam van de winkel door de formule geretourneerd. Is de status Off, dan is de naam 'Inactive'. Daarvoor gebruiken we de logische functie [IF](https://msdn.microsoft.com/library/ee634824.aspx) om de winkelstatus te testen en een bepaalde waarde te retourneren als het resultaat waar of onwaar is.
    
2.  Begin **IF** te typen. In de lijst met suggesties wordt weergegeven wat we kunnen toevoegen. Selecteer **IF**.
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_activestore_1.png)
    
    Het eerste argument voor IF is een logische test. We willen testen of een winkel de status 'On' heeft.
    
3.  Typ een haakje openen **[**, zodat we kolommen uit de tabel Stores kunnen selecteren. Selecteer **[Status]**.
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_activestore_2.png)
    
4.  Direct achter **[Status]** typt u **="On"** en typt u een komma (**,**) om het tweede argument in te voeren. De knopinfo stelt voor de waarde toe te voegen als het resultaat waar is.
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_activestore_3.png)
    
5.  Als de winkel de status ’On’ heeft, willen we de naam van de winkel laten zien. Typ een haakje openen **[**, selecteer de kolom **[StoreName]** en typ nog een komma zodat we het derde argument kunnen invoeren.
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_activestore_step5.png)
    
6.  We moeten een waarde toevoegen voor wanneer het resultaat onwaar is, en in dit geval moet de waarde **‘Inactive’** zijn.
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_activestore_step6.png)
    
7.  Voltooi de formule door op Enter te drukken of op het vinkje in de formulebalk te klikken. De formule wordt gevalideerd en toegevoegd aan de lijst met velden in de tabel Stores.
    
    We kunnen de nieuwe Active StoreName-kolom in visualisaties gebruiken, net zoals elk ander veld. In dit diagram worden winkels met de status ‘On’ afzonderlijk weergegeven op naam, maar winkels met de status ‘Off’ worden gegroepeerd en weergegeven als ‘Inactive’. 
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_activestore_viz.png)
    
## <a name="what-weve-learned"></a>Wat hebben we geleerd
Berekende kolommen kunnen onze gegevens duidelijker maken. We hebben geleerd hoe berekende kolommen worden gemaakt met behulp van de formulebalk, hoe de lijst met suggesties wordt gebruikt en wat de beste manier is om de nieuwe kolommen een naam te geven.

## <a name="next-steps"></a>Volgende stappen
Zie [Standaard DAX-bewerkingen in Power BI Desktop](desktop-quickstart-learn-dax-basics.md) voor meer informatie over DAX-formules en voor het maken van berekende kolommen met geavanceerdere DAX-formules. Dit artikel is voornamelijk gericht op de grondbeginselen van DAX, zoals de syntaxis en functies. Daarnaast gaan we iets dieper in op het begrip context.

Voeg [Naslaginformatie over Data Analysis Expressions (DAX)](https://msdn.microsoft.com/library/gg413422.aspx) toe aan uw favorieten. Hier vindt u gedetailleerde informatie over de syntaxis, operators en meer dan 200 functies van DAX.

