---
title: Matrixvisualisatie in Power BI gebruiken
description: Leer hoe u met matrixvisualisatie stapindelingen en gedetailleerde markeringen in Power BI kunt uitvoeren
author: mihart
manager: kvivek
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 12/05/2018
ms.author: mihart
LocalizationGroup: Create reports
ms.openlocfilehash: acd2ad2afe9b380a8888dee7a4b9d4707d79b41f
ms.sourcegitcommit: c8c126c1b2ab4527a16a4fb8f5208e0f7fa5ff5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2019
ms.locfileid: "54279821"
---
# <a name="use-the-matrix-visual-in-power-bi"></a>Matrixvisualisatie in Power BI gebruiken
Met de visualfunctie **Matrix** kunt u matrixvisuals (ook wel *tabellen* genoemd) maken in **Power BI Desktop-** en **Power BI-service**-rapporten, en elementen in de matrix kruislings markeren met andere visuals. Bovendien kunt u rijen en kolommen selecteren, en zelfs afzonderlijke cellen en kruislings markeren. Afzonderlijke cellen en selecties van meerdere cellen kunnen worden gekopieerd en geplakt in andere toepassingen. En ten slotte ondersteunt de matrixvisualisatie ook een getrapte lay-out, om beter gebruik te maken van de lay-outruimte.

![](media/desktop-matrix-visual/matrix-visual_2a.png)

Er zijn veel functies gekoppeld aan de matrix, en in de volgende secties van dit artikel gaan we die behandelen.

## <a name="report-themes"></a>Rapportthema's
Zowel matrix- als tabelvisualisaties weerspiegelen de stijlen (inclusief kleuren) van het toegepaste **Rapportthema**. Dit zijn mogelijk niet de verwachte kleuren voor uw matrixvisualisatie; u kunt ze wijzigen in de **Rapportthema**-configuratie. Zie [ **Rapportthema's gebruiken in Power BI Desktop** ](../desktop-report-themes.md) voor meer informatie over thema's.

## <a name="understanding-how-power-bi-calculates-totals"></a>Begrijpen hoe Power BI totalen berekent

Voordat u leert hoe u de **Matrix**-visual gebruikt, is het belangrijk om te begrijpen hoe Power BI totale en subtotale waarden in tabellen en matrices berekent. In het geval van totale en subtotale rijen wordt de meting over alle rijen in de onderliggende data geëvalueerd. Het is *geen* eenvoudige optelsom van de waarden in de zichtbare of weergegeven rijen. Dit betekent dat u in de totaalrij andere waarden kunt krijgen dan u had verwacht. 

Bekijk de volgende **Matrix**-visuals. 

![](media/desktop-matrix-visual/matrix-visual_3.png)

In dit voorbeeld geven alle rijen uiterst rechts in de **Matrix**-visual het *Bedrag* weer van elke combinatie van een verkoper/datum. Maar omdat een verkoper in meerdere datums verschijnt kunnen de getallen vaker dan één keer worden weergegeven. Het accurate totaal van de onderliggende gegevens en de eenvoudige optelsom van de zichtbare waarden komen daarom niet overeen. Dit is een algemeen patroon wanneer de waarde die u optelt de één is in een één-op-veelrelatie.

Als u naar de totalen en subtotalen kijkt, moet u onthouden dat die waarden zijn gebaseerd op de onderliggende gegevens en niet enkel op de zichtbare waarden. 

<!-- use Nov blog post video

## Expanding and collapsing row headers
There are two ways you can expand row headers. The first is through the right-click menu. You’ll see options to expand the specific row header you clicked on, the entire level or everything down to the very last level of the hierarchy. You have similar options for collapsing row headers as well.

![](media/desktop-matrix-visual/power-bi-expand1.png)

You can also add +/- buttons to the row headers through the formatting pane under the row headers card. By default, the icons will match the formatting of the row header, but you can customize the icons’ color and size separately if you want. 
Once the icons are turned on, they work similarly to the icons from PivotTables in Excel.

![](media/desktop-matrix-visual/power-bi-expand2.png)

The expansion state of the matrix will save with your report. It can be pinned to dashboards as well, but consumers will need to open up the report to change the state. Conditional formatting will only apply to the inner most visible level of the hierarchy. Note that this expand/collapse experience is not currently supported when connecting to AS servers older than 2016 or MD servers.

![](media/desktop-matrix-visual/power-bi-expand3.png)

Watch the following video to learn more about expand/collapse in the matrix:

-->
## <a name="using-drill-down-with-the-matrix-visual"></a>Inzoomen gebruiken met de Matrix-visualisatie
Met de **Matrix**-visualisatie, kunt u allerlei interessante zoomactiviteiten uitvoeren die vroeger niet beschikbaar waren. Eén hiervan is de mogelijkheid om in te zoomen met behulp van rijen, kolommen en zelfs op afzonderlijke secties en cellen. Laten we eens kijken hoe dat werkt.

### <a name="drill-down-on-row-headers"></a>Inzoomen op rijkoppen
Wanneer u in het deelvenster **Visualisaties** meerdere velden toevoeg in de sectie **Rijen** van de **Velden**-put, maakt u het mogelijk in te zoomen op de rijen van de matrixvisualisatie. Dit is vergelijkbaar met het maken van een hiërarchie, die het vervolgens mogelijk maakt in te zoomen op die hiërarchie (en weer terug te gaan) en de gegevens op elk niveau te analyseren.

In de volgende afbeelding bevat de sectie **Rijen** *Categorie* en *Subcategorie*, waardoor een groepering (of hiërarchie) wordt gemaakt in de rijen waarop we kunnen inzoomen.

![](media/desktop-matrix-visual/matrix-visual_4.png)

Wanneer in de visualisatie een groepering is gemaakt in de sectie **Rijen**, worden in de linkerbovenhoek van de visualisatie zelf de pictogrammen *Inzoomen* en *Uitvouwen* weergegeven.

![](media/desktop-matrix-visual/matrix-visual_5.png)

Net als bij het zoom- en uitvouwgedrag in andere visualisaties, kunnen we met die knoppen inzoomen op (of teruggaan door) de hiërarchie. In dit geval kunnen we vanuit *Categorie* inzoomen op *Subcategorie*, zoals weergegeven in de volgende afbeelding, waar het pictogram voor één niveau inzoomen (de hooivork) is geselecteerd.

![](media/desktop-matrix-visual/matrix-visual_6.png)

U kunt niet alleen die pictogrammen gebruiken, maar ook met de rechtermuisknop op de rijkoppen klikken en inzoomen door een keuze te maken in het weergegeven menu.

![](media/desktop-matrix-visual/matrix-visual_7.png)

Er zijn enkele opties in het menu dat verschijnt die verschillende resultaten genereren:

Door **Inzoomen** te selecteren wordt de matrix voor *dat* rijniveau uitgevouwen; alle andere rijkoppen worden *uitgesloten*, behalve de rijkop waarop u met de rechtermuisknop hebt geklikt. In de volgende afbeelding is met de rechtermuisknop op *Computers* geklikt en **Inzoomen** geselecteerd. U ziet dat andere rijen op het hoogste niveau niet meer in de matrix worden weergegeven. Deze manier van inzoomen is handig, zoals u met name zult zien in de sectie over **kruislings markeren**.

![](media/desktop-matrix-visual/matrix-visual_8.png)

U kunt op het pictogram **Uitzoomen** klikken om terug te gaan naar de vorige weergave op het hoogste niveau. Als u vervolgens **Volgend niveau weergeven** selecteert in het contextmenu, krijgt u een alfabetische lijst met alle items op het volgende niveau (in dit geval het veld *SubCategory*), zonder de hiërarchiecategorisatie op het hogere niveau.

![](media/desktop-matrix-visual/matrix-visual_8a.png)

Wanneer u op het pictogram **Uitzoomen** in de linkerbovenhoek klikt om alle categorieën op het hoogste niveau weer te geven in de matrix, en vervolgens opnieuw met de rechtermuisknop klikt en **Uitbreiden naar het volgende niveau** kiest, ziet u de volgende visual.

![](media/desktop-matrix-visual/matrix-visual_9.png)

U kunt ook de menu-items **Opnemen** en **Uitsluiten** gebruiken om de rij waarop u met de rechtermuisknop klikt (en eventuele subcategorieën) in de matrix te behouden respectievelijk eruit te verwijderen.

### <a name="drill-down-on-column-headers"></a>Inzoomen op kolomkoppen
Vergelijkbaar met de mogelijkheid om in te zoomen op rijen, kunt u ook inzoomen op **kolommen**. In de volgende afbeelding ziet u dat er twee velden in de veldenput **Kolommen** zijn, waardoor een hiërarchie ontstaat die vergelijkbaar is met degene die we eerder in dit artikel voor de rijen hebben gebruikt. De veldenput **Kolommen** bevat *Klasse* en *Kleur*.

![](media/desktop-matrix-visual/matrix-visual_10.png)

Wanneer we in de visualisatie **Matrix** met de rechtermuisknop op een kolom klikken, zien we de optie om in te zoomen. In de volgende afbeelding klikken we met de rechtermuisknop op *Deluxe* en selecteren **Inzoomen**.

![](media/desktop-matrix-visual/matrix-visual_11.png)

Wanneer u **Inzoomen**  selecteert, wordt het volgende niveau van de kolomhiërarchie voor *Deluxe* weergegeven, in dit geval *Kleur*.

![](media/desktop-matrix-visual/matrix-visual_12.png)

De rest van de menu-items in het contextmenu werken voor kolommen op dezelfde manier als voor rijen (zie de vorige sectie **Inzoomen op rijkoppen**). U kunt het **Volgende niveau weergeven**, **Uitbreiden naar het volgende niveau** en kolommen **Opnemen** of **Uitsluiten**, net als met rijen.

> [!NOTE]
> De pictogrammen voor in- en uitzoomen linksboven in de matrixvisual zijn alleen van toepassing op rijen. Als u wilt inzoomen op kolommen, moet u het contextmenu gebruiken.
> 
> 

## <a name="stepped-layout-with-matrix-visuals"></a>Getrapte indeling met matrixvisualisatie
In de visual **Matrix** worden de subcategorieën automatisch ingesprongen in een hiërarchie onder elk bovenliggend item; dit wordt een **indeling met interval** genoemd.

In de *oorspronkelijke* versie van de matrixvisualisatie werden subcategorieën weergegeven in een geheel andere kolom, wat veel meer ruimte kostte in de visualisatie. In de volgende afbeelding wordt de tabel in de oorspronkelijke visual **Matrix** weergegeven; u ziet dat de subcategorieën in een afzonderlijke kolom staan.

![](media/desktop-matrix-visual/matrix-visual_14.png)

In de volgende afbeelding ziet u de visual **Matrix** met een **indeling met interval** in actie. U ziet dat de categorie *Computers* subcategorieën heeft (Computeraccessoires, Desktops, Laptops, Monitors, enzovoort) die enigszins zijn ingesprongen, waardoor de visualisatie er netter en veel compacter uitziet.

![](media/desktop-matrix-visual/matrix-visual_13.png)

U kunt de instellingen van de indeling met interval gemakkelijk aanpassen. Selecteer de **Matrix**-visualisatie en vouw in de sectie **Opmaak** (verfrollerpictogram) van het deelvenster **Visualisaties** de sectie **Rijkoppen** uit. U hebt twee opties: de wisselknop **Getrapte lay-out** (waarmee u dit in- of uitschakelt) en de **Inspringing voor getrapte lay-out** (hiermee geeft u het aantal ingesprongen pixels op).

![](media/desktop-matrix-visual/matrix-visual_15.png)

Als u **Getrapte lay-out** uitschakelt, worden de subcategorieën weergegeven in een aparte kolom in plaats van ingesprongen onder de bovenliggende categorie.

## <a name="subtotals-with-matrix-visuals"></a>Subtotalen met matrixvisualisaties
U kunt subtotalen in- of uitschakelen in matrixvisualisaties, zowel voor rijen als kolommen. In de volgende afbeelding ziet u dat de rijsubtotalen zijn ingesteld op **aan**.

![](media/desktop-matrix-visual/matrix-visual_20.png)

Vouw in de sectie **Opmaak** van het deelvenster **Visualisaties** de kaart **Subtotalen** uit en zet de schuifknop **Rijsubtotalen** op **Uit**. Wanneer u dit doet, worden de subtotalen niet weergegeven.

![](media/desktop-matrix-visual/matrix-visual_21.png)

Hetzelfde geldt voor de kolomsubtotalen.

## <a name="cross-highlighting-with-matrix-visuals"></a>Kruislings markeren met matrixvisualisaties
Met de visual **Matrix** kan elk element in de matrix worden geselecteerd als de basis voor kruislings markeren. Selecteer een kolom in een **Matrix**, en die kolom wordt gemarkeerd, net als andere visualisaties op de rapportpagina. Dit type kruislings markeren was al een algemene functie van andere visualisaties en gegevenspuntselecties, en nu biedt de **matrix**visualisatie dezelfde functionaliteit.

Bovendien werkt Ctrl+klikken ook voor kruislings markeren. In de volgende afbeelding is bijvoorbeeld een verzameling subcategorieën geselecteerd in de **Matrix**visualisatie. U ziet dat items die niet in de visualisatie zijn geselecteerd, lichter zijn gekleurd, en dat de in de **Matrix**-visualisatie gemaakte selecties worden weerspiegeld in de andere visualisaties op de pagina.

![](media/desktop-matrix-visual/matrix-visual_16.png)

## <a name="copying-values-from-power-bi-for-use-in-other-applications"></a>Waarden kopiëren uit Power BI voor gebruik in andere toepassingen

Uw matrix of tabel bevat mogelijk inhoud die u wilt gebruiken in andere toepassingen, bijvoorbeeld Dynamics CRM, Excel of zelfs andere Power BI-rapporten. Met een rechtermuisklik in Power BI kopieert en plakt u een afzonderlijke cel of een selectie cellen naar uw klembord in de andere toepassing.

![kopieeropties](media/desktop-matrix-visual/power-bi-cell-copy.png)

* Kopieer de waarde van een enkele cel, selecteer de cel, klik er met de rechtermuisknop op en kies **Waarde kopiëren**. Als u de onopgemaakte celwaarde naar uw klembord hebt gekopieerd, kunt u deze nu kopiëren in een andere toepassing.

    ![kopieeropties](media/desktop-matrix-visual/power-bi-copy.png)

* Als u meer dan een enkele cel wilt kopiëren, selecteert u een reeks cellen, of gebruikt u CTRL om één of meer cellen te selecteren. De kolomkoppen en rijkoppen zijn opgenomen in de kopie.

    ![plakken in Excel](media/desktop-matrix-visual/power-bi-copy-selection.png)

## <a name="shading-and-font-colors-with-matrix-visuals"></a>Arcering en tekstkleuren met matrixvisualisaties
Met de visual **Matrix** kunt u **voorwaardelijke opmaak** (kleuren en arcering) toepassen op de achtergrond van cellen in de matrix en op de tekst en waarden zelf.

Als u voorwaardelijke opmaak wilt toepassen, kunt u het volgende doen als er een matrixvisualisatie is geselecteerd:

* Klik in het deelvenster **Velden** met de rechtermuisknop op het veld en selecteer **Voorwaardelijke opmaak** in het menu.
  
  ![](media/desktop-matrix-visual/matrix-visual_17.png)
* Of vouw in het deelvenster **Opmaak** de kaart **Voorwaardelijke opmaak** uit en zet de schuifknop van **Achtergrondkleurschalen** of **Tekstkleurschalen** op **Aan**. Door een van deze opties in te schakelen wordt een koppeling weergegeven naar *Geavanceerde besturingselementen*, waarmee u de kleuren en waarden voor de kleurenopmaak kunt aanpassen.
  
  ![](media/desktop-matrix-visual/matrix-visual_18.png)

Beide benaderingen geven hetzelfde resultaat. Door *Geavanceerde besturingselementen* te selecteren wordt het volgende dialoogvenster weergegeven, waarin u aanpassingen kunt doen:

![](media/desktop-matrix-visual/matrix-visual_19.png)

## <a name="next-steps"></a>Volgende stappen

[Spreidingsdiagrammen en bellendiagrammen in Power BI](power-bi-visualization-scatter.md)

[Visualization types in Power BI](power-bi-visualization-types-for-reports-and-q-and-a.md) (Typen visualisaties in Power BI)