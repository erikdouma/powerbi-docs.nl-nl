---
title: Voorwaardelijke tabelopmaak in Power BI Desktop
description: Aangepaste opmaak toepassen op tabellen
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 05/17/2018
ms.author: davidi
LocalizationGroup: Create reports
ms.openlocfilehash: 70aa61d6a02bea1b7058a68b20718008ace1b8c8
ms.sourcegitcommit: 2a7bbb1fa24a49d2278a90cb0c4be543d7267bda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/26/2018
ms.locfileid: "34480883"
---
# <a name="conditional-formatting-in-tables"></a>Voorwaardelijke opmaak in tabellen 
Met voorwaardelijke opmaak voor tabellen kunt u aangepaste celkleuren opgeven op basis van celwaarden of op basis van andere waarden of velden, waaronder het gebruik van kleurovergangen. U kunt ook celwaarden met gegevensbalken weergeven. 

Selecteer voor toegang tot voorwaardelijke opmaak in het venster **Velden** van het deelvenster **Visualisaties** in Power BI Desktop de pijl omlaag naast de waarde in het venster **Waarden** die u wilt opmaken (of klik met de rechtermuisknop op het veld). U kunt voorwaardelijke opmaak alleen beheren voor velden in het gebied **Waarden** van het venster **Velden**.

![Het menu Voorwaardelijke opmaak](media/desktop-conditional-table-formatting/table-formatting-0-popup-menu.png)

In de volgende gedeelten worden deze drie voorwaardelijke opmaakopties behandeld. U kunt een of meer opties combineren in een afzonderlijke tabelkolom.

> [!NOTE]
> Wanneer voorwaardelijke opmaak wordt toegepast op een tabel, worden alle aangepaste tabelstijlen die zijn toegepast op de voorwaardelijk opgemaakte cellen overschreven.

Als u voorwaardelijke opmaak uit een visualisatie wilt verwijderen, klikt u eenvoudigweg opnieuw met de rechtermuisknop op het veld en selecteert u **Voorwaardelijke opmaak verwijderen**. Selecteer vervolgens het type opmaak dat u wilt verwijderen.

![Het menu Voorwaardelijke opmaak verwijderen](media/desktop-conditional-table-formatting/table-formatting-1-remove.png)

## <a name="background-color-scales"></a>Achtergrondkleurschalen

Wanneer u **Voorwaardelijke opmaak** en vervolgens **Achtergrondkleurschalen** selecteert, wordt het volgende dialoogvenster geopend.

![Het dialoogvenster Achtergrondkleurschalen](media/desktop-conditional-table-formatting/table-formatting-1-default-dialog.png)

U kunt een veld selecteren via uw gegevensmodel om daar de kleuren op te baseren door **Kleur gebaseerd op** in te stellen op dat veld. Daarnaast kunt u het aggregatietype opgeven voor het geselecteerde veld met de waarde **Samenvatting**. Het veld dat moet worden ingekleurd, wordt opgegeven in het veld **Kleur toepassen op**, zodat u dit kunt bijhouden. U kunt voorwaardelijke opmaak toepassen op tekst- en datumvelden, zo lang u maar een numerieke waarde als basis van de opmaak kiest.

![Het veld Kleur gebaseerd op](media/desktop-conditional-table-formatting/table-formatting-1-apply-color-to.png)

Als u discrete kleurwaarden wilt gebruiken voor bepaalde waardebereiken, selecteert u **Kleur op regels**. Als u een kleurspectrum wilt gebruiken, laat u de optie **Kleur op regels** uitgeschakeld. 

![Het dialoogvenster Achtergrondkleurschalen](media/desktop-conditional-table-formatting/table-formatting-1-color-by-rules-dialog.png)

### <a name="color-by-rules"></a>Kleur op regels

Wanneer u **Kleur op regels** selecteert, kunt u een of meer waardebereiken invoeren, elk met een ingestelde kleur.  Elk waardebereik begint met een voorwaarde met een *Als-waarde*, een voorwaarde met een *en*-waarde en een kleur.

![Het waardebereik van Kleur op regels](media/desktop-conditional-table-formatting/table-formatting-1-color-by-rules-if-value.png)

Tabelcellen met waarden in elk bereik worden gevuld met de opgegeven kleur. De volgende afbeelding bevat drie regels.

![Voorbeeld van kleur op regels](media/desktop-conditional-table-formatting/table-formatting-1-color-by-rules.png)

De voorbeeldtabel ziet er nu als volgt uit:

![Voorbeeldtabel met kleur op regels](media/desktop-conditional-table-formatting/table-formatting-1-color-by-rules-table.png)


### <a name="color-minimum-to-maximum"></a>Minimum- tot maximumkleur

U kunt de waarden *Minimum* en *Maximum* en de bijbehorende kleuren configureren. Als u het vak **Afwijken** selecteert, kunt u desgewenst ook een waarde voor *Centreren* configureren.

![De knop Afwijken](media/desktop-conditional-table-formatting/table-formatting-1-diverging.png)

De voorbeeldtabel ziet er nu als volgt uit:

![Voorbeeldtabel met afwijkende kleuren](media/desktop-conditional-table-formatting/table-formatting-1-diverging-table.png)

## <a name="font-color-scales"></a>Tekstkleurschalen

Als u **Voorwaardelijke opmaak** en vervolgens **Tekstkleurschalen** selecteert, wordt het volgende dialoogvenster geopend. Dit dialoogvenster is vergelijkbaar met het dialoogvenster**Achtergrondkleurschalen**. Hiermee kunt u echter de tekstkleur wijzigen in plaats van de achtergrondkleur van de cel.

![Het dialoogvenster Tekstkleurschalen](media/desktop-conditional-table-formatting/table-formatting-2-diverging.png)

De voorbeeldtabel ziet er nu als volgt uit:

![Voorbeeldtabel met tekstkleurschalen](media/desktop-conditional-table-formatting/table-formatting-2-table.png)

## <a name="data-bars"></a>Gegevensbalken

Als u **Voorwaardelijke opmaak** en vervolgens **Gegevensbalken** selecteert, wordt het volgende dialoogvenster geopend. 

![Het dialoogvenster Gegevensbalken](media/desktop-conditional-table-formatting/table-formatting-3-default.png)

Standaard is de optie **Alleen balk weergeven** niet ingeschakeld; de tabelcel toont dus zowel de balk als de daadwerkelijke waarde.

![Voorbeeldtabel met gegevensbalken en waarden](media/desktop-conditional-table-formatting/table-formatting-3-default-table.png)

Als de optie **Alleen balk weergeven** is ingeschakeld, toont de tabelcel alleen de balk.

![Voorbeeldtabel met alleen gegevensbalken](media/desktop-conditional-table-formatting/table-formatting-3-default-table-bars.png)
