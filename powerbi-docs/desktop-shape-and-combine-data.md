---
title: Gegevens vormgeven en combineren in Power BI Desktop
description: Gegevens vormgeven en combineren in Power BI Desktop
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
ms.date: 01/30/2018
ms.author: davidi
LocalizationGroup: Transform and shape data
ms.openlocfilehash: c8f2419ae2898a59907763392eb86b4877b4fd75
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/24/2018
---
# <a name="shape-and-combine-data-in-power-bi-desktop"></a>Gegevens vormgeven en combineren in Power BI Desktop
Met **Power BI Desktop** kunt u verbinding maken met veel verschillende soorten gegevensbronnen en vervolgens de gegevens vormgeven om aan uw behoeften te voldoen. Het *vormgeven* van gegevens betekent het omzetten van de gegevens, zoals de naam wijzigen van kolommen of tabellen, het wijzigen van tekst in getallen, het verwijderen van rijen, het instellen van de eerste rij als koptekst, enzovoort. Het *combineren* van gegevens betekent verbinding maken met twee of meer gegevensbronnen, deze naar wens vormgeven en ze samenvoegen tot één handige query.

Dit document laat zien hoe u een query kunt vormgeven met Power BI Desktop, waarbij enkele van de meest algemene taken nader worden toegelicht. De hier gebruikte query wordt uitvoeriger beschreven, waaronder het maken van een volledig nieuwe query, in [Aan de slag met Power BI Desktop](desktop-getting-started.md).

Het is handig om te weten dat de **Query-editor** in Power BI Desktop op ruime schaal gebruikmaakt van contextmenu's, samen met het lint. Het meeste van wat u kunt selecteren in het lint **Transformeren** is ook beschikbaar door met de rechtermuisknop op een item (zoals een kolom) te klikken en een keuze te maken in het menu dat verschijnt.

## <a name="shape-data"></a>Gegevens vormgeven
Wanneer u gegevens in de Query-editor vormgeeft, geeft u stapsgewijze instructies (die de Query-editor voor u uitvoert) om de gegevens aan te passen terwijl Query-editor de gegevens laadt en presenteert. De oorspronkelijke gegevensbron wordt daardoor niet beïnvloed; alleen deze specifieke weergave van de gegevens wordt aangepast, ofwel *vormgegeven*.

De stappen die u opgeeft (zoals de naam van een tabel wijzigen, een gegevenstype transformeren of kolommen verwijderen), worden vastgelegd door de Query-editor en elke keer dat deze query verbinding maakt met de gegevensbron, worden die stappen uitgevoerd zodat de gegevens altijd op de door u bepaalde manier worden vormgegeven. Dit proces vindt plaats wanneer u de Query-editor van Power BI Desktop gebruikt, maar vindt ook plaats voor iedereen die gebruikmaakt van de door u gedeelde query, zoals in de **Power BI**-service. Deze stappen worden in volgorde vastgelegd in het deelvenster **Query-instellingen** onder **Toegepaste stappen**.

De volgende afbeelding toont het deelvenster **Query-instellingen** voor een query die is vormgegeven. In de volgende alinea’s bekijken we elk van deze stappen.

![](media/desktop-shape-and-combine-data/shapecombine_querysettingsfinished.png)

Met behulp van de pensioneringsgegevens uit [Aan de slag met Power BI Desktop](https://powerbi.uservoice.com/knowledgebase/articles/471664), die we hebben gevonden door verbinding te maken met een gegevensbron op internet, gaan we die gegevens vormgeven op basis van onze behoeften.

Om te beginnen werden de cijfers van één kolom niet automatisch omgezet van tekst naar getallen toen Query-editor de tabel laadde, dus we moeten daarvan alsnog getallen maken. Geen probleem: we hoeven alleen met de rechtermuisknop op de kolomkop te klikken en **Type wijzigen \> Geheel getal** selecteren om de tekst te wijzigen. Als u meer dan één kolom wilt selecteren, selecteert u eerst een kolom en houdt u **SHIFT** ingedrukt, selecteert u extra aangrenzende kolommen en klikt u vervolgens met de rechtermuisknop op een kolomkop om alle geselecteerde kolommen te wijzigen. U kunt ook de **CTRL**-toets gebruiken om niet-aaneengesloten kolommen te selecteren.

![](media/desktop-shape-and-combine-data/shapecombine_changetype.png)

U kunt die kolommen ook *transformeren* van tekst naar koptekst met behulp van het lint **Transformeren**. Hier ziet u het lint **Transformeren**, met een pijl die wijst naar de knop **Gegevenstype**, waarmee u het huidige gegevenstype in een ander gegevenstype kunt omzetten.

![](media/desktop-shape-and-combine-data/queryoverview_transformribbonarrow.png)

De optie **Toegepaste stappen** in **Query-instellingen** laat alle vormgevingsstappen zien die op de gegevens worden toegepast. Als ik een stap uit het vormgevingsproces wil verwijderen, selecteer ik gewoon de **X** links van de stap. In de volgende afbeelding geeft **Toegepaste stappen** de tot nu toe uitgevoerde stappen aan: verbinding maken met de website (**Bron**); de tabel selecteren (**Navigatie**); en tijdens het laden van de tabel heeft Query-editor kolommen op tekstbasis automatisch gewijzigd van *Tekst* in *Geheel getal* (**Type gewijzigd**). Een kolom met classificaties werd niet automatisch gewijzigd in een getaltype en in de eerstvolgende alinea’s zullen we zien hoe dat komt.

![](media/desktop-shape-and-combine-data/shapecombine_appliedstepsearly.png)

Voordat we met deze query kunnen werken, moeten we enkele wijzigingen aanbrengen om de bijbehorende gegevens te krijgen zoals we willen:

* *Verwijder de eerste kolom*: we hebben deze niet nodig, want de kolom bevat alleen redundante rijen met de tekst 'Check out how your state ranks for retirement', wat is overgenomen uit deze gegevensbron die de vorm van een webgebaseerde tabel heeft.
* *Corrigeer enkele fouten*: een van de kolommen, **Health care quality**, bevat enkele problemen in de classificatie van staten, die op de website werden aangegeven met de tekst *(tie)* na de getallen. Dat werkt prima op de website, maar het is wel nodig dat we de kolom handmatig omzetten van tekst naar getallen. Dat is gemakkelijk op te lossen met behulp van Power BI Desktop, waarmee een handige functie van **Toegepaste stappen** in Query wordt gedemonstreerd
* *Wijzig de naam van de tabel*: **Table 0** is niet handig als beschrijving, maar dat kan eenvoudig worden gewijzigd

Voor het verwijderen van de eerste kolom selecteert u de kolom en selecteert u het tabblad **Start** op het lint, gevolgd door **Kolommen verwijderen** zoals weergegeven in de volgende afbeelding.

![](media/desktop-shape-and-combine-data/shapecombine_removecolumnsretirement.png)

Vervolgens moeten we de tekstkolom aanpakken en de tekst omzetten in getallen. In eerste instantie lijkt het logisch dat we het type van de kolom **Health care quality** gewoon kunnen wijzigen van tekst in getallen (zoals *Geheel getal* of *Decimaal getal*). Maar wanneer we het type wijzigen van **Tekst** in **Geheel getal** en vervolgens de waarden in die kolom doorzoeken, zullen we zien dat Query-editor enkele fouten meldt.

![](media/desktop-shape-and-combine-data/shapecombine_error.png)

Er zijn enkele manieren om meer informatie over elke fout te krijgen. U kunt de cel selecteren (zonder te klikken op het woord **Fout**) of rechtstreeks klikken op het woord **Fout**. Als u de cel selecteert *zonder* rechtstreeks op het woord **Fout** te klikken, geeft Query-editor de foutinformatie weer aan de onderkant van het venster.

![](media/desktop-shape-and-combine-data/shapecombine_errorinfo.png)

Als u rechtstreeks op het woord *Fout* klikt, maakt Query een **Toegepaste stap** in het deelvenster **Query-instellingen** en wordt er informatie over de fout weergegeven.

![](media/desktop-shape-and-combine-data/shapecombine_errorselect.png)

Als u terug wilt gaan naar de Query-editor, moet u die stap verwijderen door de **X** ernaast te selecteren.

Wanneer we de meest recent **Toegepaste stap** selecteren, verschijnt de zojuist beschreven fout, zoals wordt weergegeven in de volgende afbeelding.

![](media/desktop-shape-and-combine-data/shapecombine_querystep1.png)

Omdat de Query-editor stappen sequentieel registreert, kunnen we in **Toegepaste stappen** de stap selecteren voordat het type wordt gewijzigd en zien wat de waarde van die cel is voorafgaand aan de transformatie, zoals weergegeven in de volgende afbeelding.

![](media/desktop-shape-and-combine-data/shapecombine_querystep2.png)

Prima, nu kunnen we deze waarden herstellen en *vervolgens* het type wijzigen. Omdat de Query-editor de stappen sequentieel registreert, weliswaar onafhankelijk van elkaar, kunt u elke **Toegepaste stap** hoger of lager in de reeks zetten. Klik met de rechtermuisknop op een stap en de Query-editor laat een menu zien waarmee u het volgende kunt doen: **Naam wijzigen**, **Verwijderen**, **Verwijderen** **tot aan het einde** (verwijder de huidige stap, samen met alle verdere stappen), **Omhoog** of **Omlaag**.

![](media/desktop-shape-and-combine-data/shapecombine_querystepreorder.png)

Bovendien kunt u een **Toegepaste stap** overal in de lijst selecteren en doorgaan met het vormgeven van de gegevens op dat punt in de reeks. De Query-editor voegt automatisch een nieuwe stap in, onmiddellijk na de geselecteerde **Toegepaste stap**. Laten we dat eens proberen.

We selecteren eerst de **Toegepaste stap** voordat we het type van de kolom **Health care quality** gaan wijzigen. Vervolgens vervangen we de waarden die '(tie)' als tekst in de cel hebben, zodat alleen het nummer achterblijft. Klik met de rechtermuisknop op de cel met '35 (tie)' en selecteer *Waarden vervangen...*  in het menu. Onthoud welke **Toegepaste stap** momenteel is geselecteerd (de stap voorafgaand aan het wijzigen van het type).

![](media/desktop-shape-and-combine-data/shapecombine_replacevalues.png)

Omdat we een stap invoegen, geeft de Query-editor daarvoor een waarschuwing: de daaropvolgende stappen zouden de query kunnen verbreken. Daarom moeten we zorgvuldig en doordacht te werk gaan. Aangezien dit een zelfstudie is en we een heel handige functie van de Query-editor bespreken om te laten zien hoe u stappen kunt maken, verwijderen, invoegen en anders kunt rangschikken, gaan we verder en selecteren we **Invoegen**.

![](media/desktop-shape-and-combine-data/shapecombine_insertstep.png)

Er zijn drie ties en we gaan de waarde van elk daarvan vervangen. Wanneer u een nieuwe toegepaste stap maakt, geeft de Query-editor deze een naam op basis van de actie, in dit geval **Waarde vervangen**. Wanneer de query meer dan één stap met dezelfde naam bevat, voegt de Query-editor aan elke volgende **Toegepaste stap** een getal toe (in oplopende volgorde) om ze van elkaar te onderscheiden.

Het volgende scherm toont de drie stappen voor **Waarde vervangen** in **Query-instellingen**, maar er is ook iets anders te zien dat nog interessanter is: aangezien we elk exemplaar van de tekst '(tie)' hebben verwijderd uit de kolom **Health care quality**, wordt de stap **Type gewijzigd** nu *zonder fouten* uitgevoerd.

![](media/desktop-shape-and-combine-data/shapecombine_replacedvaluesok.png)

> [!NOTE]
> U kunt ook **Fouten verwijderen** (met het lint of het snelmenu), waardoor alle rijen met fouten worden verwijderd. In dit geval zouden alle staten met '*(tie)*' uit onze gegevens worden verwijderd, maar dat is niet wat we wilden: we vinden alle staten prima en willen die in de tabel houden.

Hoe het ook zij, dit is een goed voorbeeld van hoe krachtig en veelzijdig Query-editor kan zijn.

Tot slot willen we de naam van de tabel meer beschrijvend maken. Wanneer u rapporten gaat maken, is het bijzonder handig om beschrijvende tabelnamen te hebben, vooral wanneer er verbinding met meerdere gegevensbronnen wordt gemaakt en deze allemaal worden weergegeven in het deelvenster **Velden** van de **Rapport**weergave.

De tabelnaam kan eenvoudig worden gewijzigd: typ in het deelvenster **Query-instellingen**, onder **Eigenschappen**, de nieuwe naam van de tabel, zoals weergegeven in de volgende afbeelding, en druk op **Enter**. Laten we deze tabel *RetirementStats* noemen.

![](media/desktop-shape-and-combine-data/shapecombine_renametable.png)

Goed, we hebben die gegevens vormgegeven voor zover dat nodig was. Laten we nu verbinding maken met een andere gegevensbron en gegevens gaan combineren.

## <a name="combine-data"></a>Gegevens combineren
De informatie over de verschillende staten is best interessant en handig voor extra analyses en query's. Maar er is wel één probleem: de meeste van die gegevens gebruiken de tweeletterige afkorting als code voor staten, niet de volledige naam van de staat. We hebben een manier nodig om namen van staten te koppelen aan hun afkortingen.

Maar gelukkig is er een andere openbare gegevensbron die precies dat doet, maar er moet dan wel eerst aardig wat worden aangepast voordat die bron aan de pensioneringstabel kan worden gekoppeld. Hier is de webbron voor staatafkortingen:

<http://en.wikipedia.org/wiki/List_of_U.S._state_abbreviations>

Op het **Start**lint van de Query-editor selecteren we **Nieuwe bron \> Web** en typen we het adres. We klikken op OK en de Navigator laat zien wat er op die webpagina werd gevonden.

 ![](media/desktop-shape-and-combine-data/designer_gsg_usstateabbreviationsnavigator.png)

We selecteren **Tabel [bewerken]** omdat hierin de gewenste gegevens zijn opgenomen, maar het kost wel wat werk om de gegevens uit die tabel op de juiste manier aan te passen.

> [!TIP]
> Is er een snellere of gemakkelijkere manier om de onderstaande stappen uit te voeren? Jazeker, we zouden een *relatie* tussen de twee tabellen kunnen maken en de gegevens vormgeven op basis van die relatie. De volgende stappen zijn nog steeds prima geschikt voor het werken met tabellen, maar denk er wel aan dat u met relaties snel gegevens uit meerdere tabellen kunt gebruiken.
> 
> 

We voeren de volgende stappen uit om deze gegevens vorm te geven:

* Verwijder de eerste twee rijen. Deze zijn een resultaat van de manier waarop de tabel van die webpagina werd gemaakt en we hebben die rijen niet nodig. Op het **Start**lint selecteren we **Minder rijen \> Minder rijen \> Bovenste rijen verwijderen**.

![](media/desktop-shape-and-combine-data/shapecombine_removetoprows.png)

Het venster **Bovenste rijen verwijderen** wordt weergegeven, waarin u kunt opgeven hoeveel rijen u wilt verwijderen.

* Verwijder de onderste 26 rijen; dat zijn alle territoriale gebieden en die hebben we nu niet nodig. Op het **Start**lint selecteren we **Minder rijen \> Minder rijen \> Onderste rijen verwijderen**.

![](media/desktop-shape-and-combine-data/shapecombine_removebottomrows.png)

* Omdat de tabel RetirementStats geen informatie voor Washington DC bevat, moeten we dat uit onze lijst filteren. Klik op de vervolgkeuzepijl naast de kolom Region Status en schakel het selectievakje naast **Federal district** uit.

![](media/desktop-shape-and-combine-data/shapecombine_filterdc.png)

* Verwijder enkele overbodige kolommen. We hebben alleen de koppeling van een staat met de officiële afkorting van twee letters nodig, dus kunnen we de volgende kolommen verwijderen: **Kolom2**, **Kolom3** en vervolgens **Kolom5**  tot en met **Kolom10**. Selecteer eerst Kolom2, houd de **CTRL**-toets ingedrukt en selecteer de andere kolommen die moeten worden verwijderd (op deze manier kunt u meerdere niet-aaneengesloten kolommen selecteren). Selecteer op het tabblad Start van het lint de optie **Kolommen verwijderen \> Kolommen verwijderen**.

![](media/desktop-shape-and-combine-data/shapecombine_removecolumns.png)

* Gebruik de eerste rij voor de kopnamen. Omdat we de drie bovenste rijen hebben verwijderd, bevat de huidige bovenste rij de gewenste koptekst. U kunt **De eerste rij als veldnamen gebruiken** op het tabblad **Start** of op het tabblad **Transformeren** op het lint selecteren.

![](media/desktop-shape-and-combine-data/shapecombine_usefirstrowasheaders.png)

>[!NOTE]
>Dit is een goed moment om te vermelden dat de *reeks* toegepaste stappen in de Query-editor belangrijk is en van invloed kan zijn op hoe de gegevens worden vormgegeven. Het is ook belangrijk om na te gaan hoe de ene stap van invloed kan zijn op een volgende stap. Als u een stap uit de Toegepaste stappen verwijdert, werken daarop volgende stappen mogelijk niet meer zoals oorspronkelijk beoogd vanwege de impact van de reeks stappen van de query.

>[!NOTE]
>Wanneer u het venster van Query-editor smaller maakt, worden enkele items op het lint verkleind om de zichtbare ruimte zo goed mogelijk te benutten. Wanneer u het venster van Query-editor breder maakt, worden de items op het lint vergroot om de extra ruimte voor het lint zo goed mogelijk te benutten.

* Wijzig de naam van de kolommen en van de tabel zelf. Zoals gewoonlijk zijn er een aantal manieren om de naam van een kolom te wijzigen; selecteer eerst de kolom en selecteer vervolgens **Naam wijzigen** op het tabblad **Transformeren** op het lint, of klik met de rechtermuisknop en selecteer **Naam wijzigen...** in het snelmenu. De volgende afbeelding laat pijlen zien die beide opties aanwijzen; u hoeft er maar één te kiezen.

![](media/desktop-shape-and-combine-data/shapecombine_rename.png)

Laten we de naam wijzigen in *State Name* en *State Code*. U wijzigt de naam van de tabel door de naam te typen in het vak **Naam** van het deelvenster **Query-instellingen**. Laten we deze tabel *StateCodes* noemen.

Nu we de tabel StateCodes de gewenste vorm hebben gegeven, gaan we deze twee tabellen, of query's, samenvoegen in één tabel. Omdat de tabellen die we nu hebben, het resultaat zijn van de query's die we op de gegevens hebben toegepast, worden ze vaak aangeduid als *query's*.

Er zijn twee manieren om query's te combineren: *samenvoegen* en *toevoegen*.

Wanneer u een of meer kolommen hebt die u wilt toevoegen aan een andere query gaat u de query’s **samenvoegen**. Wanneer u extra rijen met gegevens hebt die u aan een bestaande query wilt toevoegen, gaat u de query **toevoegen**.

In dit geval gaan we query's samenvoegen. Als eerste selecteren we in het linkerdeelvenster van de Query-editor de query *waarin* we de andere query willen samenvoegen, in dit geval is dat *RetirementStats*. Selecteer vervolgens **Combineren \> Query's samenvoegen** op het tabblad **Start** van het lint.

![](media/desktop-shape-and-combine-data/shapecombine_mergequeries.png)

U wordt mogelijk gevraagd de privacyniveaus in te stellen om te controleren of de gegevens worden gecombineerd zonder dat er gegevens worden opgenomen of overgedragen waarvan u niet wilt dat ze worden overgedragen.

![](media/desktop-shape-and-combine-data/shapecombine_mergequeriesb.png)

Het venster **Samenvoegen** wordt weergegeven, waarin wordt gevraagd welke tabel er in de geselecteerde tabel moet worden samengevoegd, gevolgd door de overeenkomende kolommen die worden gebruikt voor het samenvoegen. Selecteer State in de *RetirementStats*-tabel (query) en selecteer de query *StateCodes* (eenvoudig in dit geval, omdat er maar één andere query is – wanneer u verbinding met veel gegevensbronnen maakt, zijn er veel query's waaruit u kunt kiezen). Wanneer we de juiste overeenkomende kolommen selecteren – **State** uit *RetirementStats* en **State Name** uit *StateCodes* – ziet het venster **Samenvoegen** er als volgt uit en is de knop **OK** ingeschakeld.

![](media/desktop-shape-and-combine-data/shapecombine_merge.png)

Er wordt een **NewColumn** aan het einde van de query gemaakt, met daarin de inhoud van de tabel (query) die met de bestaande query is samengevoegd. Alle kolommen uit de samengevoegde query zijn samengevoegd in de **NewColumn**, maar u kunt ervoor kiezen de tabel **uit te breiden** om elke gewenste kolom op te nemen.

![](media/desktop-shape-and-combine-data/shapecombine_mergenewcolumn.png)

Als u de samengevoegde tabel wilt uitvouwen en wilt aangeven welke kolommen u wilt opnemen, selecteert u het uitvouwpictogram (![Uitvouwen](media/desktop-shape-and-combine-data/icon.png)). Het venster **Uitvouwen** wordt weergegeven.

![](media/desktop-shape-and-combine-data/shapecombine_mergeexpand.png)

In dit geval hebben we alleen de kolom **State Code** nodig. Daarom selecteren we alleen die kolom en vervolgens **OK**. We schakelen het selectievakje ‘Oorspronkelijke kolomnaam gebruiken als voorvoegsel’ uit omdat we die niet nodig hebben en ook niet willen. Als we het selectievakje ingeschakeld zouden laten, krijgt de samengevoegde kolom de naam **NewColumn.State Code** (de naam van de oorspronkelijke kolom, ofwel **NewColumn**, gevolgd door een punt, gevolgd door de naam van de kolom die in de query wordt opgenomen).

>[!NOTE]
>Wilt u uitproberen hoe u die **NewColumn**-tabel kunt opzetten? U kunt wat experimenteren en als de resultaten u niet bevallen, kunt u die stap gewoon verwijderen uit de lijst **Toegepaste stappen** in het deelvenster **Query-instellingen**. De query krijgt dan weer de status die gold voordat de stap **Uitbreiden** werd toegepast. U kunt de stap zo vaak uitvoeren als u wilt, totdat u met het uitbreidproces het gewenste resultaat hebt bereikt.

We hebben nu één query (tabel) waarin twee gegevensbronnen zijn samengevoegd, die elk volgens onze behoeften zijn vormgegeven. Deze query kan fungeren als basis voor een groot aantal extra, interessante gegevensverbindingen, zoals statistieken voor huisvestingskosten, demografische gegevens of werkgelegenheid in een staat.

Als u wijzigingen wilt toepassen en de Query-editor wilt sluiten, selecteert u Sluiten en toepassen op het tabblad **Start** op het lint. De getransformeerde gegevensset wordt weergegeven in Power BI Desktop en is klaar voor het maken van rapporten.

![](media/desktop-shape-and-combine-data/shapecombine_closeandapply.png)

## <a name="next-steps"></a>Volgende stappen
U kunt allerlei handelingen uitvoeren met Power BI Desktop. Bekijk de volgende bronnen voor meer informatie over de vele mogelijkheden:

* [Getting Started with Power BI Desktop](desktop-getting-started.md) (Aan de slag met Power BI Desktop)
* [Query Overview with Power BI Desktop](desktop-query-overview.md) (Queryoverzicht met Power BI Desktop)
* [Data Sources in Power BI Desktop](desktop-data-sources.md) (Gegevensbronnen in Power BI Desktop)
* [Verbinding maken met gegevens in Power BI Desktop](desktop-connect-to-data.md)
* [Algemene querytaken in Power BI Desktop](desktop-common-query-tasks.md)   

