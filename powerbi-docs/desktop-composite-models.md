---
title: Samengestelde modellen gebruiken in Power BI Desktop (preview-versie)
description: Lees hoe u in Power BI Desktop gegevensmodellen maakt met meerdere gegevensverbindingen en veel-op-veel-relaties
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 09/17/2018
ms.author: davidi
LocalizationGroup: Transform and shape data
ms.openlocfilehash: 4e7692be8ec78c79076408635a75dbf0ab9080d2
ms.sourcegitcommit: 698b788720282b67d3e22ae5de572b54056f1b6c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/17/2018
ms.locfileid: "45974041"
---
# <a name="composite-models-in-power-bi-desktop-preview"></a>Samengestelde modellen in Power BI Desktop (preview-versie)

Eerder was het zo dat als u in **Power BI Desktop** een DirectQuery gebruikte in een rapport, er geen andere gegevensverbindingen dan DirectQuery of Importeren waren toegestaan voor het rapport. Met **samengestelde modellen** is die beperking weggenomen en kan een rapport naadloos gegevensverbindingen bevatten uit meer dan één DirectQuery of importgegevensverbinding, ook nog eens in elke gewenste combinatie.

![samengestelde modellen in Power BI Desktop](media/desktop-composite-models/composite-models_01.png)

De voorziening **samengestelde modellen** in **Power BI Desktop** bestaat uit drie gerelateerde functies:

* **Samengestelde modellen**: maakt het mogelijk dat een rapport meerdere gegevensverbindingen heeft, inclusief DirectQuery-verbindingen of importverbindingen, in elke gewenste combinatie.
* **Veel-op-veel-relaties**: met **samengestelde modellen** kunt u **veel-op-veel-relaties** instellen tussen tabellen, waardoor de vereisten voor unieke waarden in tabellen worden weggenomen, en er ook geen noodzaak meer is voor eerdere tijdelijke oplossingen zoals het toevoegen van nieuwe tabellen alleen maar om relaties te kunnen opzetten. 
* **Opslagmodus**: u kunt nu opgeven welke visualisaties een query naar de back-end-gegevensbronnen vereisen. Visualisaties waarvoor dit niet nodig is, worden geïmporteerd, zelfs als ze zijn gebaseerd op DirectQuery. Hierdoor kunnen de prestaties worden verbeterd en wordt de back-end minder belast. Eerder was het zo dat zelfs voor eenvoudige visualisaties zoals slicers, er query's werden verzonden naar de back-end-bronnen. 

Deze verzameling van drie gerelateerde functies voor **samengestelde modellen** worden in afzonderlijke artikelen beschreven:

* **Samengestelde modellen** worden in dit artikel beschreven.
* **Veel-op-veel-relaties** worden beschreven in het artikel [Veel-op-veel-relaties in Power BI Desktop (preview-versie)](desktop-many-to-many-relationships.md).
* **Opslagmodus** wordt beschreven in het artikel [Opslagmodus in Power BI Desktop (preview-versie)](desktop-storage-mode.md).

## <a name="enabling-the-composite-models-preview-feature"></a>De preview-versie van samengestelde modellen inschakelen

De voorziening **samengestelde modellen** is nog in preview en moet afzonderlijk worden ingeschakeld in **Power BI Desktop**. U kunt de voorziening **samengestelde modellen** inschakelen door **Bestand > Opties en instellingen > Opties > Preview-functies** te selecteren en vervolgens het selectievakje **Samengestelde modellen** in te schakelen. 

![preview-functies inschakelen](media/desktop-composite-models/composite-models_02.png)

U moet **Power BI Desktop** opnieuw starten om de voorziening in te schakelen.

![opnieuw starten is vereist voor doorvoeren van wijziging](media/desktop-composite-models/composite-models_03.png)


## <a name="using-composite-models"></a>Samengestelde modellen gebruiken

Met behulp van **samengestelde modellen** kunt u verbinding maken met allerlei verschillende gegevensbronnen wanneer u **Power BI Desktop** of de **Power BI-service** gebruikt, en u kunt deze verbindingen op verschillende manieren tot stand brengen. U kunt gegevens importeren in Power BI, wat de meest voorkomende manier is om gegevens te verkrijgen, of u kunt DirectQuery gebruiken om rechtstreeks verbinding te maken met gegevens in de oorspronkelijke opslagplaats. Meer informatie over DirectQuery kunt u lezen in het artikel [DirectQuery gebruiken in Power BI](desktop-directquery-about.md).

Als u DirectQuery gebruikt met **samengestelde modellen**, is het mogelijk om een Power BI-model te maken (zoals een enkel PBIX-bestand van Power BI Desktop) dat het volgende doet:

* gegevens uit een of meer DirectQuery-bronnen combineren en/of
* gegevens uit DirectQuery-bronnen combineren en gegevens importeren

Zo is het met **samengestelde modellen** bijvoorbeeld mogelijk om een model te maken waarin verkoopgegevens uit het datawarehouse van een bedrijf worden gecombineerd met gegevens van verkoopdoelen die zijn opgeslagen in de SQL Server-database van een afdeling, samen met enkele gegevens die worden geïmporteerd uit een spreadsheet. Een model dat gegevens uit meer dan één DirectQuery-bron combineert, of DirectQuery combineert met geïmporteerde gegevens, wordt een *samengesteld model* genoemd.

> [!NOTE]
> Hoewel samengestelde modellen in preview zijn, is het niet mogelijk om samengestelde modellen te publiceren naar de Power BI-service. 

U kunt op de gebruikelijke manier relaties instellen tussen tabellen, zelfs wanneer deze tabellen afkomstig zijn uit verschillende bronnen. Er is echter één beperking waarmee u rekening moet houden: alle relaties die meerdere bronnen gebruiken, moeten worden gedefinieerd met de kardinaliteit **Veel-op-veel**, ongeacht hun werkelijke kardinaliteit. Het gedrag van dergelijke relaties is vervolgens hetzelfde als bij **veel-op-veel**-relaties, zoals wordt beschreven in [Veel-op-veel-relaties in Power BI Desktop (preview-versie)](desktop-many-to-many-relationships.md). Het is belangrijk om te weten dat in de context van samengestelde modellen, alle geïmporteerde tabellen in feite één bron vormen, ongeacht de onderliggende gegevensbron waaruit ze daadwerkelijk worden geïmporteerd.   

## <a name="example-of-using-composite-models"></a>Voorbeeld van het werken met samengestelde modellen

Als voorbeeld van een **samengesteld model** nemen we een rapport dat via DirectQuery is verbonden met een datawarehouse van een bedrijf (in SQL Server), waarbij het datawarehouse gegevens bevat over omzet per land (*Country*), kwartaal (*CalendarQuarter)* en het product fiets (*Bike*), zoals wordt weergegeven in de volgende afbeelding.

![weergave van relaties voor samengestelde modellen](media/desktop-composite-models/composite-models_04.png)

Op basis van deze gegevens kunt u eenvoudige visualisaties bouwen. De volgende visualisatie laat bijvoorbeeld de totale omzet per productnaam (*ProductName*) zien voor een geselecteerd kwartaal. 

![Visualisatie op basis van gegevens](media/desktop-composite-models/composite-models_05.png)

Maar stel dat u ook beschikt over een Excel-spreadsheet met gegevens van de productmanager die aan elk product is toegewezen, samen met de marketingprioriteit. U kunt dan de omzet (*SalesAmount*) uitsplitsen naar productmanager (*Product Manager*), maar het toevoegen van deze lokale gegevens aan het datawarehouse van het bedrijf is waarschijnlijk onhaalbaar of zou in het gunstigste geval maanden duren. Hoewel het misschien mogelijk is om die verkoopgegevens te importeren uit het datawarehouse (in plaats van DirectQuery te gebruiken), waarna de gegevens kunnen worden gecombineerd met gegevens die worden geïmporteerd uit het spreadsheet, is deze aanpak onwenselijk vanwege redenen die ertoe leiden om in eerste instantie te kiezen voor DirectQuery, zoals een combinatie van de beveiligingsregels die in de onderliggende gegevensbron worden afgedwongen, de noodzaak om de meest recente gegevens te kunnen zien en de grote schaal van de gegevens. 

En dat is waar **samengestelde modellen** goed van pas komen. Samengestelde modellen bieden u de mogelijkheid om via DirectQuery verbinding te maken met het datawarehouse, en daarna ook om met GetData aanvullende bronnen te raadplegen. In dit voorbeeld zetten we de DirectQuery-verbinding op met het datawarehouse van het bedrijf, gebruiken we vervolgens GetData en kiezen we Excel, navigeren we naar het spreadsheet met onze lokale gegevens en importeren we het blad met de *ProductNames*, de toegewezen *Product Manager* en *Priority*.  

![Navigator-venster](media/desktop-composite-models/composite-models_06.png)

In de lijst **Velden** zien we nu de oorspronkelijke tabel *Bike* (van SQL Server) en een nieuwe tabel *ProductManagers* (met de gegevens die zijn geïmporteerd uit Excel). 

![Veldweergave van tabellen](media/desktop-composite-models/composite-models_07.png)

Als we naar de **relatieweergave** gaan in **Power BI Desktop**, zien we daar ook een extra tabel met de naam *ProductManagers*. 

![relatieweergave van tabellen](media/desktop-composite-models/composite-models_08.png)

We moeten deze nu koppelen aan de andere tabellen in het model, wat we op de gebruikelijke manier doen, door een relatie op te zetten tussen de tabel *Bike* (in SQL Server) en de tabel *ProductManagers* (die is geïmporteerd ) zoals tussen *Bike [ProductName]* en *ProductManagers [ProductName]*. Zoals eerder is beschreven in dit artikel, moeten alle relaties tussen verschillende bronnen de kardinaliteit **Veel-op-veel** hebben. Om die reden is die kardinaliteit standaard geselecteerd. 

![Dialoogvenster Relatie maken](media/desktop-composite-models/composite-models_09.png)

Nadat deze relatie is gemaakt, wordt deze zoals verwacht weergegeven in de **relatieweergave** in **Power BI Desktop**.

![nieuwe relatieweergave](media/desktop-composite-models/composite-models_10.png)

Nu deze tabelrelaties tot stand zijn gebracht, kunnen we visualisaties maken op basis van de velden in de lijst **Velden**, om zo gegevens uit verschillende bronnen naadloos samen te voegen. In de visualisatie hieronder ziet u bijvoorbeeld de totale omzet (*SalesAmount*) voor elke *productmanager*. 

![visualisatie met het deelvenster Velden weergegeven](media/desktop-composite-models/composite-models_11.png)

In dit voorbeeld zien we een veelgebruikt scenario met een *dimensietabel* (zoals *Product* of *Customer*) die wordt uitgebreid met extra gegevens die worden geïmporteerd uit een andere locatie. Het is ook mogelijk om DirectQuery te gebruiken met tabellen om verbinding te maken met verschillende bronnen. Stel dat we het scenario willen uitbreiden en dat *SalesTargets* per *Country* en *Period* zijn opgeslagen in een afzonderlijke database van de afdeling. U kunt dan met **GetData** op de gebruikelijke manier verbinding maken met die gegevens, zoals wordt weergegeven in de volgende afbeelding. 

![Navigator-venster](media/desktop-composite-models/composite-models_12.png)

We kunnen nu, vergelijkbaar met wat we eerder in dit voorbeeld hebben gedaan, relaties instellen tussen de nieuwe tabel en andere tabellen in het model en vervolgens visualisaties maken om hun gegevens te combineren. Laten we nog eens naar de **relatieweergave** kijken, waaraan nieuwe relaties zijn toegevoegd afkomstig uit ons uitgebreide voorbeeldscenario.

![relatieweergave met meerdere tabellen](media/desktop-composite-models/composite-models_13.png)

Zoals u kunt zien in de volgende afbeelding, die is gebaseerd op de nieuwe gegevens en relaties die we zojuist hebben gemaakt, bevat de visualisatie in de linkerbenedenhoek de totale omzet (*SalesAmount*) versus de prognose (*Target*), waarbij Variance het verschil aangeeft en *SalesAmount* en *Target* afkomstig zijn uit twee verschillende SQL Server-databases. 

![visualisatie met meer gegevens](media/desktop-composite-models/composite-models_14.png)

## <a name="setting-storage-mode"></a>Opslagmodus instellen

Elke tabel in een **samengesteld model** heeft een **opslagmodus** die aangeeft of de tabel is gebaseerd op DirectQuery of importeren. De waarde voor **Opslagmodus** kan worden bekeken en gewijzigd in het deelvenster met **eigenschappen**. Selecteer hiervoor **Eigenschappen** in het contextmenu van de lijst **Velden**. In de volgende afbeelding ziet u de **opslagmodus** (afgekort tot **Opslag...** in de afbeelding, vanwege de breedte van het deelvenster).

![Instelling van opslagmodus](media/desktop-composite-models/composite-models_15.png)

De **opslagmodus** kunt u ook zien in de knopinfo voor elke tabel.

![knopinfo met opslagmodus](media/desktop-composite-models/composite-models_16.png)

Voor een **Power BI Desktop**-bestand (een PBIX-bestand) dat enkele tabellen bevat via DirectQuery en enkele importtabellen, staat op de statusbalk de **opslagmodus** **Gemengd**. Klik op die status om eenvoudig alle tabellen over te zetten naar importeren.

Uitgebreide informatie over **opslagmodus** vindt u in het artikel [Opslagmodus in Power BI Desktop (preview-versie)](desktop-storage-mode.md).  

## <a name="calculated-tables"></a>Berekende tabellen

Berekende tabellen kunnen worden toegevoegd aan een model waarin DirectQuery wordt gebruikt en de DAX met de definitie van de berekende tabel kan verwijzen naar geïmporteerde tabellen, DirectQuery-tabellen of een combinatie hiervan. 

Berekende tabellen worden altijd geïmporteerd en de gegevens in deze tabellen worden vernieuwd wanneer de tabel wordt vernieuwd. Als een berekende tabel verwijst naar een DirectQuery-tabel, bevatten visualisaties die verwijzen naar de DirectQuery-tabel daarom altijd de meest recente waarden uit de onderliggende bron, terwijl visualisaties die verwijzen naar de berekende tabel de waarden bevatten van het moment waarop de berekende tabel voor het laatst is vernieuwd.

## <a name="security-implications"></a>Gevolgen voor de beveiliging 

Samengestelde modellen hebben invloed op de beveiliging. Een query die wordt verzonden naar de ene gegevensbron kan gegevenswaarden bevatten die zijn opgehaald uit een andere bron. In het geval van het voorbeeld dat eerder in dit artikel wordt beschreven, resulteert de visualisatie met omzet (*Sales Amount*) per *productmanager* in een SQL-query die wordt verzonden naar de relationele database **Sales**, waar deze SQL-query de namen van *productmanagers* en de bijbehorende *producten* kan bevatten. 

![script dat gevolgen voor de beveiliging aantoont](media/desktop-composite-models/composite-models_17.png)

Het gevolg is dat gegevens die zijn opgeslagen in de spreadsheet nu worden opgenomen in een query die wordt verzonden naar de relationele database. Als het vertrouwelijke gegevens betreft, moet er een oplossing worden gevonden voor dit beveiligingsprobleem. Houd met name rekening met de volgende scenario's:

* Beheerders van de database die toegang hebben tot traces of auditlogboeken, kunnen deze gegevens inzien, zelfs als ze geen machtiging hebben voor de gegevens in de oorspronkelijke bron (in dit geval machtigingen voor het Excel-bestand).

* De versleutelingsinstellingen voor elke bron vereisen ook aandacht, om te voorkomen dat er gegevens via een versleutelde verbinding worden opgehaald uit de ene bron en deze gegevens vervolgens per ongeluk worden opgenomen in een query die via een niet-versleutelde verbinding wordt verzonden naar een andere bron. 

U ziet in **Power BI Desktop** een waarschuwing wanneer er een actie wordt ondernomen om een samengesteld model te maken, zodat u weet dat dit gevolgen kan hebben voor de beveiliging van uw gegevens.  

Om vergelijkbare redenen moet u zorgvuldig te werk gaan bij het openen van een **Power BI Desktop**-bestand dat is verzonden vanuit een niet-vertrouwde bron. Als dat bestand samengestelde modellen bevat, betekent dit dat gegevens die worden opgehaald uit de ene bron (met behulp van de referenties van de gebruiker die het bestand opent) als onderdeel van de query worden verzonden naar een andere gegevensbron (waar de gegevens mogelijk kunnen worden gezien door de kwaadwillende auteur van het Power BI Desktop-bestand). Om die reden wordt er een waarschuwing weergegeven wanneer u een Power BI Desktop-bestand met meerdere bronnen de eerste keer opent. Deze waarschuwing is vergelijkbaar met de waarschuwing die u ziet bij het openen van een bestand met native SQL-query's.  

## <a name="performance-implications"></a>Gevolgen voor de prestaties  

Als u DirectQuery gebruikt, zijn de prestaties altijd een punt van aandacht. Het is met name belangrijk om ervoor te zorgen dat de back-end-bron voldoende resources heeft om gebruikers een goede ervaring te bieden. Een goede ervaring betekent dat visualisaties binnen maximaal vijf seconden moeten zijn vernieuwd. U moet ook voldoen aan het advies dat wordt gegeven in het artikel [DirectQuery gebruiken in Power BI](desktop-directquery-about.md). Als u kiest voor samengestelde modellen, moet u rekening houden met extra prestatieoverwegingen aangezien één visualisatie kan resulteren in het verzenden van query's naar meerdere bronnen, waarbij de resultaten van een query vaak worden doorgegeven aan een tweede gegevensbron. Deze situatie kan de volgende uitvoeringsscenario's tot gevolg hebben:

* **Een SQL-query met een groot aantal letterlijke waarden**: voor een visualisatie die bijvoorbeeld de totale omzet (*Sales Amount*) uit een SQL-database laat zien voor een set geselecteerde *productmanagers* (uit de gerelateerde tabel die is geïmporteerd uit een spreadsheet), moet eerst worden vastgesteld welke *producten* werden beheerd door deze productmanagers, voordat er een SQL-query wordt verzonden met daarin alle product-id's in een *WHERE*-component.

* **Een SQL-query die op een lager granulatieniveau gegevens opvraagt, waarna de gegevens lokaal worden geaggregeerd**: als we het vorige voorbeeld nemen uit deze lijst, en het aantal *producten* dat voldoet aan het filter voor  *Product Manager* erg groot wordt, is het op een bepaald moment niet meer efficiënt of haalbaar om ze allemaal op te nemen in een *WHERE*-component. In plaats daarvan is het nodig om een query uit te voeren op de relationele bron op het lagere niveau van *Product*, en de resultaten vervolgens lokaal te aggregeren. Als de kardinaliteit van *Products* groter is dan een limiet van 1 miljoen, mislukt de query.

* **Meerdere SQL query's, één per groep op waarde**: wanneer de aggregatie **DistinctCount** gebruikt, gegroepeerd op een kolom uit een andere bron, en als de externe bron geen ondersteuning biedt voor het efficiënt doorgeven van een groot aantal letterlijke waarden die de groepering definiëren, is het nodig om één SQL-query's per groep op waarde te verzenden. Een visualisatie waarin bijvoorbeeld een unieke telling van *CustomerAccountNumber* (uit de SQL Server-tabel) per *productmanager* (uit de gerelateerde tabel die is geïmporteerd uit een spreadsheet) moet worden weergegeven, moet details doorgeven uit de tabel *Product Managers* in de query die is verzonden naar SQL Server. Via andere bronnen, bijvoorbeeld Redshift, is dit niet haalbaar en in plaats daarvan zou er één SQL-query per *Sales Manager* worden verzonden (tot een praktische limiet, waarna de query mislukt). 

Elk van deze scenario's heeft specifieke gevolgen voor de prestaties, waarbij de exacte details verschillen per gegevensbron. Een goede vuistregel is dat wanneer de kardinaliteit van de kolommen die worden gebruikt in de relatie tussen de twee bronnen laag blijft (een paar duizend), de gevolgen voor de prestaties beperkt zijn. Als deze kardinaliteit toeneemt, moet er meer aandacht worden besteed aan de impact op de resulterende prestaties. 

Het gebruik van **veel-op-veel**-relaties betekent bovendien dat afzonderlijke query's moeten worden verzonden naar de onderliggende gegevensbron voor elk totaal-/subtotaalniveau, in plaats van de gedetailleerde waarden lokaal te aggregeren. Het gevolg is dat een eenvoudige tabelvisualisatie met totalen twee SQL-query's zou verzenden, in plaats van één. 

## <a name="limitations-and-considerations"></a>Beperkingen en overwegingen

Er gelden enkele beperkingen voor deze release van **samengestelde modellen**.

De volgende (multidimensionale) Live Connect-bronnen kunnen niet worden gebruikt met **samengestelde modellen**:

* SAP HANA
* SAP Business Warehouse
* SQL Server Analysis Services
* Power BI-gegevenssets
* Azure Analysis Services

Als u met behulp van DirectQuery verbinding maakt met deze multidimensionale bronnen, is het niet mogelijk om ook nog verbinding te maken met een andere DirectQuery-bron. Het is dan evenmin mogelijk om te combineren met geïmporteerde gegevens.

De bestaande beperkingen van het gebruik van DirectQuery gelden nog steeds wanneer u **samengestelde modellen** gebruikt. Veel van deze beperkingen zijn nu per tabel, al naar gelang de **opslagmodus** van de tabel. Zo kan een berekende kolom in een geïmporteerde tabel verwijzen naar andere tabellen, maar kan een berekende kolom in een DirectQuery-tabel nog steeds alleen verwijzen naar kolommen in dezelfde tabel. Andere beperkingen gelden voor het model als geheel, als een van de tabellen in het model DirectQuery gebruikt. De functies **QuickInsights** en **Q&A** zijn bijvoorbeeld niet beschikbaar voor een model als een van de tabellen in het model de **opslagmodus** DirectQuery heeft. 

## <a name="next-steps"></a>Volgende stappen

De volgende artikelen bevatten meer informatie over samengestelde modellen, evenals een gedetailleerde beschrijving van DirectQuery.

* [Veel-op-veel-relaties in Power BI Desktop (preview-versie)](desktop-many-to-many-relationships.md)
* [Opslagmodus in Power BI Desktop (preview-versie)](desktop-storage-mode.md)

DirectQuery-artikelen:

* [DirectQuery gebruiken in Power BI](desktop-directquery-about.md)
* [Gegevensbronnen die worden ondersteund door DirectQuery in Power BI](desktop-directquery-data-sources.md)

