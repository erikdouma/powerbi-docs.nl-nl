---
title: Statistische functies (som, gemiddelde, maximum, enzovoort) in Power BI
description: De aggregatie in een grafiek (som, gemiddelde, maximum, enz.) in Power BI wijzigen
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
ms.date: 09/23/2017
ms.author: mihart
ms.openlocfilehash: c1b926e129e8d82edd9c329a51623908c4e7c9e0
ms.sourcegitcommit: 8f72ce6b35aa25979090a05e3827d4937dce6a0d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/27/2017
---
# <a name="aggregates-in-power-bi"></a>Statistische functies in Power BI
## <a name="what-is-an-aggregate"></a>Wat is een statistische functie?
Soms wilt u de waarden van rijen rekenkundig combineren in een kolom. De rekenkundige bewerking kan de som, het gemiddelde, het maximum, het aantal, enzovoort zijn. Het combineren van de waarde van gegevens in rijen in een kolom wordt aggregeren genoemd. Het resultaat van die rekenkundige bewerking is een *aggregatie*. 

Een numeriek veld is een waarde die worden geaggregeerd (som of een gemiddelde, bijvoorbeeld) in een categorische veld.  Bijvoorbeeld de omzet per product en het aantal fouten per regio. Numeriek velden worden ook vaak **metingen** genoemd. In de lijst met velden worden metingen weergegeven met het symbool ∑. Ga naar [De rapporteditor... een rondleiding](service-the-report-editor-take-a-tour.md) voor meer informatie.

Soms is een *meting* eigenlijk een *berekende meting*. Berekende metingen in Power BI worden geïmporteerd samen met de gegevens (die zijn gedefinieerd in het gegevensmodel waarop uw rapport is gebaseerd). Elk berekende meting heeft een eigen in code vastgelegde formule. U kunt de gebruikte aggregatie niet wijzigen; als de aggregatie bijvoorbeeld een som is, kan deze alleen een som zijn. *Berekende metingen* worden in de lijst Velden weergegeven met het calculatorsymbool. Zie [Metingen in Power BI Desktop](desktop-measures.md) voor meer informatie over hoe berekende metingen worden gemaakt.

Categorische velden zijn geen numerieke velden, maar kunnen wel worden samengevoegd.  Wanneer categorische velden in een bucket met *alleen numerieke waarden* worden geplaatst, zoals **Waarden** of **Tooltips**, kan Power BI tellen hoeveel keer elke categorie voorkomt of het aantal unieke instanties van een categorie tellen.  Voor tekenreeksen en datums beschikt u in Power BI over nog een aantal aggregatieopties : vroegste, meest recent, eerste en laatste.  

## <a name="why-dont-aggregates-work-the-way-i-want-them-to"></a>Waarom werken de statische functies niet zoals ik wil?
Wanneer u met statische functies in Power BI werkt, kan dit wel eens verwarrend zijn. Mogelijk hebt u een numeriek veld en kunt u de statische functie niet wijzigen in Power BI. Of misschien hebt u een veld, zoals een jaar, en wilt u dit niet aggregeren, omdat u alleen wilt tellen hoe vaak het jaar voorkomt.

De oorzaak van het probleem ligt meestal in de manier waarop het veld is gecategoriseerd in de Power BI-gegevensset. Mogelijk is het veld is gecategoriseerd als tekst en kan het daarom niet worden opgeteld of kan er geen gemiddelde worden berekend. Helaas kan [alleen de eigenaar van de gegevensset wijzigen hoe een veld is gecategoriseerd](desktop-measures.md).  

Aan het eind van dit artikel is een speciale sectie, **Tips en probleemoplossing**, toegevoegd om de verwarring weg te nemen.  Als hier geen antwoord op uw vraag kunt vinden, stelt u de vraag in het [Power BI Community-forum](http://community.powerbi.com) voor een snelle, rechtstreekse reactie van het Power BI-team.

## <a name="change-how-a-numeric-field-is-aggregated"></a>Wijzigen hoe een numeriek veld wordt samengevoegd
Stel u hebt een diagram waarin de totale omzet voor de verschillende regio's wordt opgesomd, maar u liever het gemiddelde weergeeft. 

1. Voeg in de bewerkingsweergave voor het rapport de meting toe aan een visualisatie.
2. Zoek het desbetreffende veld in het deelvenster Visualisaties, klik met de rechtermuisknop en selecteer het type statistische functie dat u nodig hebt. Als u de gewenste statistische functie niet wordt weergegeven, neemt u contact op met de eigenaar van de gegevensset. Mogelijk is er een probleem met de manier waarop het veld door de eigenaar is gecategoriseerd.  
   
   ![](media/service-aggregates/aggregate_new.png)
   
   > [!NOTE]
   > De beschikbare opties in de vervolgkeuzelijst variëren, afhankelijk van 1) het geselecteerde veld en 2) de wijze waarop het veld door de eigenaar van de gegevensset is gecategoriseerd.
   > 
   > 

Enkele opties die beschikbaar zijn voor de aggregatie van een veld:

* **Niet samenvatten**. Wanneer u deze optie kiest, wordt elke waarde in dat veld afzonderlijk verwerkt en niet samengevat. Dit wordt vaak gebruikt als er een numerieke kolom bevatten die niet mogen worden opgeteld.
* **Som**. Hiermee worden alle waarden in het veld opgeteld.
* **Gemiddelde**. Hiermee wordt het rekenkundige gemiddelde van de waarden berekend.
* **Minimum**. Geeft de kleinste waarde.
* **Maximum**. Geeft de grootste waarde.
* **Aantal (niet leeg)**. Hiermee wordt het aantal (niet-lege) waarden in het veld geteld.
* **Aantal (uniek)**. Hiermee wordt het aantal verschillende waarden in het veld geteld.
* **Standaarddeviatie**.
* **Afwijking**.
* **Mediaan**.  Hiermee wordt de mediaanwaarde (middelste waarde) weergegeven. Dit is de waarde met hetzelfde aantal boven- als onderliggende items.  Als er 2 medianen zijn, wordt het gemiddelde hiervan genomen in Power BI.

Neem bijvoorbeeld de volgende gegevens:

| Land | Bedrag |
|:--- |:--- |
| VS |100 |
| VK |150 |
| Canada |100 |
| Duitsland |125 |
| Frankrijk | |
| Japan |125 |
| Australië |150 |

Dit voorbeeld geeft de volgende resultaten:

* **Niet samenvatten**: elke waarde wordt afzonderlijk weergegeven
* **Som**: 750
* **Gemiddelde**: 125
* **Maximum**:  150
* **Minimum**: 100
* **Aantal (niet leeg)**: 6
* **Aantal (uniek)**: 4
* **Standaarddeviatie** 20,4124145...
* **Afwijking**: 416,666...
* **Mediaan**: 125

## <a name="use-a-non-aggregated-field-as-a-numeric-field"></a>Een niet-geaggregeerd veld als numeriek veld gebruiken
U kunt ook een niet-geaggregeerd veld als numeriek veld gebruiken. Als u bijvoorbeeld het veld Productnaam hebt, kunt u dit toevoegen als een waarde en vervolgens instellen op **Aantal** of **Uniek aantal**. 

1. U selecteert bijvoorbeeld **Winkel > Keten**.
   
   ![](media/service-aggregates/count-of-chain-do_not_summarize.png)
2. En als u de aggregatie van de standaardwaarde wijzigt **Niet samenvatten** wijzigt in **Aantal (uniek)**, wordt het aantal verschillende ketens in Power BI geteld. In dit geval zijn dat er twee: Fashions Direct en Lindseys.
   
   ![](media/service-aggregates/aggregates_count.png)
3. En als u wijzigt de aggregatie wijzigt in **Aantal**, wordt het totale aantal in Power BI geteld. In dit geval zijn er 104 vermeldingen voor **Keten**. Door **Keten** toe te voegen als filter, ziet u dat er 37 rijen voor Fashions Direct en 67 rijen voor Lindseys zijn.  
   
   ![](media/service-aggregates/count_of_chain_104.png)

## <a name="tips-and-troubleshooting"></a>Tips en probleemoplossing
V: Waarom beschik ik niet over de optie **Niet samenvatten**?

A: Het veld dat u hebt geselecteerd, is waarschijnlijk een berekende meting. Onthoud dat elke berekende meting een eigen in code vastgelegde formule heeft. U kunt de berekening niet wijzigen.

V: Mijn veld **is** numeriek, waarom kan ik alleen kiezen uit **Aantal** en **Uniek aantal**?

A: Waarschijnlijk heeft de eigenaar van de gegevensset het veld per ongeluk of bewust *niet* geclassificeerd als een getal. Als een gegevensset bijvoorbeeld het veld **Jaar** bevat, kan de eigenaar van de gegevensset dat veld categoriseren als tekst, omdat het veld **Jaar** naar alle waarschijnlijkheid eerder wordt geteld (bijvoorbeeld het aantal mensen dat geboren is in 1974) dan dat het veld wordt opgeteld of dat er een gemiddelde van wordt genomen. Als u de eigenaar bent, kunt u de gegevensset openen in Power BI Desktop en het tabblad **Model maken** gebruiken om het gegevenstype te wijzigen.  

A: Een andere mogelijkheid is dat u het veld in een *bucket* hebt geplaatst waarin allee alleen categorische waarden zijn toegestaan.  In dat geval beschikt u alleen over de opties Aantal en Uniek aantal.

A: En een derde mogelijkheid is dat u het veld gebruikt voor een as. Er wordt in Power BI bijvoorbeeld één staaf voor elke afzonderlijke waarde weergegeven op de as van een staafdiagram. De veldwaarden worden niet samengevoegd. 

>[!NOTE]
>Spreidingsdiagrammen vormen een uitzondering op deze regel. Deze diagrammen *vereisen* geaggregeerde waarden voor de x- en y-as.


V: Ik heb een spreidingsdiagram en ik wil *niet* dat mijn veld wordt geaggregeerd.  Hoe doe ik dit?

A: Voeg het veld toe aan de bucket **Details** en niet aan de bucket van de x- of y-as.

V: Wanneer ik een numeriek veld aan een visualisatie toevoeg, wordt meestal de som weergegeven, maar soms wordt ook het gemiddelde, het aantal of een andere aggregatie weergegeven.  Waarom is de standaardaggregatie niet altijd hetzelfde?

A: Eigenaren van gegevenssets hebben de mogelijkheid om de standaardsamenvatting voor elk veld in te stellen. Als u eigenaar van een gegevensset bent, kunt u de standaardsamenvatting wijzigen op het tabblad **Modelleren** van Power BI Desktop.

V: Mijn veld **is** numeriek, waarom worden er geen aggregatieopties weergegeven in de vervolgkeuzelijst?

A: Als er een rekenmachinepictogram voor het veld wordt weergegeven, betekent dit dat het veld een *berekende meting* bevat en elke berekende meting heeft een eigen in code vastgelegde formule. Deze kan niet in de Power BI-service worden gewijzigd. De berekening die wordt gebruikt, is mogelijk een eenvoudige aggregatie zoals een gemiddelde of som, maar er kunnen ook complexe berekeningen worden gebruikt. zoals een percentage voor de bijdrage aan de bovenliggende categorie of het voorlopige totaal vanaf het begin van het jaar. De resultaten worden niet opgeteld of gemiddeld in Power BI. In plaats daarvan wordt elk gegevenspunt opnieuw berekend (aan de hand van de in code vastgelegde formule).

V: Ik ben de eigenaar van een gegevensset en ik wil er voor zorgen dat een veld nooit wordt samengevoegd.

A: In Power BI Desktop kunt u op het tabblad **Modelleren** de optie **Gegevenstype** instellen op **Tekst**.

V: De optie **Niet samenvatten** wordt niet weergegeven in de vervolgkeuzelijst.

A: Verwijder het veld en voeg het vervolgens opnieuw toe.

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

