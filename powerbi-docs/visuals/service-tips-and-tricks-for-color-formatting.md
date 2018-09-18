---
title: Tips en trucs voor het gebruik van kleuren in Power BI
description: Tips en trucs voor het gebruik van kleuren in Power BI
author: davidiseminger
manager: kvivek
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 07/19/2018
ms.author: davidi
LocalizationGroup: Visualizations
ms.openlocfilehash: c134592cabda6148d0bc50ee22f7501e60aef919
ms.sourcegitcommit: 67336b077668ab332e04fa670b0e9afd0a0c6489
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/12/2018
ms.locfileid: "44732877"
---
# <a name="tips-and-tricks-for-color-formatting-in-power-bi"></a>Tips en trucs voor het gebruik van kleuren in Power BI
Power BI biedt veel verschillende manieren voor het aanpassen van uw dashboards en rapporten. In dit artikel vindt u een verzameling tips die ervoor kunnen zorgen dat uw Power BI-visualisaties boeiend, interessant en afgestemd op uw behoeften zijn.

De volgende tips worden gegeven. Hebt u nog een goede tip? Mooi! Stuur de tip naar ons en we zullen kijken of deze aan de lijst kan worden toegevoegd.

* De kleur van één gegevenspunt wijzigen
* De kleuren van een grafiek baseren op een numerieke waarde
* De kleur van gegevenspunten baseren op een veldwaarde
* Kleuren in de kleurenschaal aanpassen
* Uiteenlopende kleurenschalen gebruiken
* Hoe kunt u iets ongedaan maken in Power BI?

Als u wijzigingen wilt aanbrengen, moet u een rapport bewerken: selecteer uw **Rapport** in het deelvenster **Mijn werkruimte** en selecteer **Rapport bewerken** in het menu bovenaan, zoals op de volgende afbeelding.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_1.png)

Wanneer het deelvenster **Visualisaties** wordt weergegeven aan de rechterkant van het **rapportcanvas**, kunt u beginnen met aanpassen.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_2.png)

## <a name="change-the-color-of-a-single-data-point"></a>De kleur van één gegevenspunt wijzigen
Soms wilt u een bepaald gegevenspunt markeren. Misschien zijn het verkoopcijfers voor de lancering van een nieuw product, of hogere kwaliteitsscores na de lancering van een nieuw programma. Met Power BI kunt u een gegevenspunt markeren door de kleur ervan te wijzigen.

In de volgende visualisatie worden kosten van levensonderhoud gerangschikt. 

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_3.png)

Stel, u wilt snel laten zien waar Washington in die ranglijst staat door het gebruik van kleur. Dit zijn de stappen:

Vouw de sectie **Gegevenskleuren** uit. Het volgende verschijnt.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_4.png)

Stel **Alles weergeven** in op **Aan**. Hiermee worden de kleuren voor elk gegevenselement in de visualisatie weergegeven. Wanneer u met de muisaanwijzer over de gegevenspunten beweegt, is schuiven ingeschakeld zodat u alle gegevenspunten kunt wijzigen.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_5.png)

In dit geval gaan we **Washington** wijzigen naar groen. Schuif omlaag naar **Washington** en selecteer de pijl omlaag in het kleurvak. Het venster kleurselectie verschijnt.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_6.png)

Eenmaal geselecteerd, heeft het gegevenspunt **Washington** een mooie groene tint en valt zeker op.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_7.png)

Zelfs als u het visualisatietype wijzigt en vervolgens terugkeert, onthoudt Power BI uw selectie en blijft **Washington** groen.

U kunt de kleur van een gegevenspunt ook voor meer dan één gegevenselement wijzigen. In de volgende afbeelding is **Arizona** rood en is **Washington** nog steeds groen.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_8.png)

Er zijn veel verschillende dingen die u met kleuren kunt doen. In de volgende sectie gaan we in op kleurovergangen.

## <a name="base-the-colors-of-a-chart-on-a-numeric-value"></a>De kleuren van een grafiek baseren op een numerieke waarde
Grafieken profiteren vaak van dynamisch ingestelde kleuren op basis van de numerieke waarde van een veld. Hiermee kunt u een andere waarde laten zien dan wat u gewend bent voor de grootte van een balk en twee waarden in één grafiek weergeven. Of u kunt dit gebruiken om gegevenspunten boven (of onder) een bepaalde waarde te markeren - misschien om gebieden met een lage winstgevendheid te accentueren.

In de volgende secties worden verschillende manieren beschreven om kleur te baseren op een numerieke waarde.

## <a name="base-the-color-of-data-points-on-a-value"></a>De kleur van gegevenspunten baseren op een waarde
Als u de kleur wilt wijzigen op basis van een waarde, sleept u het veld waarop u de kleur wilt baseren, naar het gebied **Kleurverzadiging** in het deelvenster **Veld**. In de volgende afbeelding is **Winst voor belasting** naar **Kleurverzadiging** gesleept. U ziet dat **Velo** weliswaar een hogere **Brutoverkoop** heeft (de kolom is hoger), maar **Amarilla** heeft een grotere **Winst voor belasting** (de kolom heeft meer kleurverzadiging).

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_9.png)

## <a name="customize-the-colors-used-in-the-color-scale"></a>De kleuren in de kleurenschaal aanpassen
U kunt de kleuren in de kleurenschaal ook aanpassen. Vouw **Gegevenskleuren** uit en u ziet een kleurovergang van de kleuren die worden gebruikt voor het visualiseren van uw gegevens. Standaard wordt de laagste waarde in uw gegevens toegewezen aan de minst verzadigde kleur en de hoogste waarde aan de meest verzadigde kleur.

Het kleurbereik wordt weergegeven in een kleurenbalk met het spectrum tussen de kleurwaarden **Minimum** en **Maximum** met **Minimum** aan de linkerzijde en  **Maximum**helemaal rechts.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_10.png)

Als u de schaal wilt wijzigen om een ander kleurbereik te gebruiken, selecteert u de keuzelijst met kleuren naast **Minimum** of **Maximum**en selecteert u een kleur. In de volgende afbeelding is de kleur **Maximum** gewijzigd in zwart en de kleurenbalk geeft het nieuwe kleurenspectrum aan tussen **Minimum** en **Maximum**.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_11.png)

U kunt ook de manier wijzigen waarop de waarden aan deze kleuren worden toegewezen. In de volgende afbeelding zijn de kleuren voor **Minimum** en **Maximum** ingesteld op respectievelijk oranje en groen.

In deze eerste afbeelding ziet u hoe de balken in de grafiek het kleurverloop in de balk weergeven; de hoogste waarde is groen, de laagste is oranje en elke balk ertussen is gekleurd met een tint uit het spectrum tussen groen en oranje.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_12.png)

Nu gaan we kijken wat er gebeurt als wij numerieke waarden opgeven in de vakken **Minimum** en **Maximum** onder de kleurenkiezers **Minimum** en **Maximum** (zie volgende afbeelding). Stel **Minimum** in op 20.000.000 en **Maximum** in op 20.000.001.

Door het instellen van deze waarden wordt het verloop niet langer toegepast op de waarden in de grafiek die onder **Minimum** of boven **Maximum** liggen; een balk met een waarde boven **Maximum** is groen en een balk met een waarde onder **Minimum** is rood.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_13.png)

## <a name="use-diverging-color-scales"></a>Uiteenlopende kleurenschalen gebruiken
Soms kunnen uw gegevens van nature verschillen. Een temperatuurbereik heeft bijvoorbeeld een natuurlijk midden op het vriespunt en een rentabiliteitsscore heeft een natuurlijk middelpunt (nul).

Voor het gebruik van uiteenlopende kleurenschalen schuift u de schuifregelaar **Afwijken** naar **Aan**. Wanneer **Afwijken** is ingeschakeld, verschijnen een extra kleurenkiezer en waardevak, beiden **Midden** genoemd (zie de volgende afbeelding).

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_14.png)

Wanneer de schuifregelaar **Afwijken** is ingeschakeld, kunt u de kleuren afzonderlijk instellen voor **Minimum**, **Maximum** en **Midden**. In de volgende afbeelding is **Midden** ingesteld op één, dus balken met waarden boven één zijn een kleurtint van groen en balken onder één zijn tinten van rood.

## <a name="how-to-undo-in-power-bi"></a>Hoe kunt u iets ongedaan maken in Power BI?
Net als in veel andere services en software van Microsoft, biedt Power BI een eenvoudige manier om de laatst uitgevoerde opdracht ongedaan te maken. Laten we bijvoorbeeld zeggen dat u de kleur van een gegevenspunt of een reeks gegevenspunten wijzigt en dat de weergegeven kleur in de visualisatie u niet bevalt. U weet niet precies welke kleur het eerder was, maar u weet wel dat u die kleur terug wilt!

Als u uw laatste actie of acties **ongedaan wilt maken** , doet u het volgende:

- Typ CTRL+Z

## <a name="feedback"></a>Feedback
Hebt u een tip die u wilt delen? Stuur de tip naar ons en we zullen kijken of we deze kunnen toevoegen.

>[!NOTE]
>Deze aanpassingen van kleur, assen en overige aanpassingen die beschikbaar zijn wanneer het pictogram **Opmaak** is geselecteerd, zijn ook beschikbaar in Power BI Desktop.

## <a name="next-steps"></a>Volgende stappen
[Aan de slag met de kleuropmaak en de eigenschappen van assen](service-getting-started-with-color-formatting-and-axis-properties.md)

