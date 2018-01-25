---
title: Tips en trucs voor het stellen van vragen met de Q&A-functie in Power BI
description: Tips en trucs voor het stellen van vragen met de Q&A-functie in Power BI
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
ms.date: 01/18/2018
ms.author: jastru
ms.openlocfilehash: 5d9b65448fced78bf3eb4ed02c84e1561d2d209a
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/19/2018
---
# <a name="tips-for-asking-questions-in-power-bi-qa"></a>Tips voor het stellen van vragen met de Q&A-functie van Power BI
## <a name="words-and-terminology-that-qa-recognizes"></a>Woorden en terminologie die door Q&A worden herkend
Deze lijst met trefwoorden is niet volledig.  U kunt het beste controleren of een trefwoord door Power BI wordt herkend, door het woord in het vragenvak te typen.  Als het woord of de term grijs wordt weergegeven, wordt deze niet door Power BI herkend of wordt het woord of de term niet herkend in de huidige context.

In de onderstaande lijst wordt de tegenwoordige tijd gebruikt, maar aanwezig tijd gebruikt, maar doorgaans worden alle tijdsvormen herkend. Het woord 'is' omvat bijvoorbeeld ook zijn, was, waren, worden, hebben, heeft, had, zal zijn, zijn wezen.  En 'sorteren' omvat ook gesorteerd en sorteren.  Bovendien herkend en bevat PowerBI de enkel- en meervoudsvorm van een woord. Power BI herkent bijvoorbeeld 'jaar' en 'jaren'.

> [!NOTE]
> Q&A is ook beschikbaar in de [Microsoft Power BI-app voor iOS op iPads, iPhones en iPod Touch-apparaten](mobile-apps-ios-qna.md).
> 
> 

Als u de eigenaar van een gegevensset bent, kunt u frasen en synoniemen toevoegen om de Q&A-resultaten voor uw klanten te verbeteren.

**Statistische functies**: totaal, som, bedrag, aantal, hoeveelheid, gemiddelde, meeste, minste, grootste, kleinste, hoogste, maximum, max., laagste, minimum, min.

**Lidwoorden**: een, de, het

**Leeg en Booleaanse waarde**: leeg, leeg, null, met het voorvoegsel 'niet' of 'niet-', lege tekenreeks, lege tekst, true, t, waar, false, f, onwaar

**Vergelijkingen**: vs, versus, in vergelijking tot, vergeleken met

**Voegwoorden**: en, of, elke, met versus, &, maar, noch, behalve, naast

**Samentrekkingen**: Q&A herkent bijna alle samentrekkingen. Probeer het maar eens uit.  Hier volgen enkele voorbeelden: im- en export, lucht- en ruimtevaarttechniek.

**Datums**: Power BI herkent de meeste datumtermen (dag, week, maand, jaar, kwartaal, decennium, enzovoort...) en verschillende datumnotaties (zie hieronder). Power BI herkent ook de volgende trefwoorden: MaandNaam, 1-31 dagen, decennium.

Voorbeelden: 3e januari van 1995, 3 januari 1995, 03 jan 1995, jan 03 1995, de 3e van januari, januari 1995, 1995 januari, 01-1995, 01/1995, namen van maanden.

**Relatieve datums**: vandaag, nu, huidige tijd, gisteren, morgen, de huidige, volgende, de komende, afgelopen, vorige, geleden, vóór vandaag, eerder dan, na, later dan, vanaf, op, voortaan, vanaf vandaag, in de toekomst, aanstaande, binnen, over, N dagen geleden, over N dagen, vervolgens, één keer, twee keer.

Bijvoorbeeld: aantal orders in de afgelopen 6 dagen.

**Gelijkheid (bereik)**: in, gelijk aan, =, na, is meer dan, in, tussen, vóór

Voorbeelden: Orderjaar is vóór 2012? Prijs ligt tussen 10 en 20? Ligt de leeftijd van John boven de 40? Totale verkoop in 200 en 300?

**Gelijkheid (waarde)**: is, gelijk, is gelijk aan, in, van, voor, ligt binnen, is op

Voorbeelden: Welke producten zijn groen? Orderdatum is gelijk aan 2012. Is de leeftijd van John 40? Totale verkoop is niet gelijk aan 200? Orderdatum 1-1-2016. 10 in prijs? Groen voor kleur? 10 in prijs?

**Namen**: als een kolom in de gegevensset de frase 'naam' bevat (bijvoorbeeld NaamWerknemer), begrijpt Q&A dat de waarden in die kolom namen zijn en vragen stellen zoals: "welke werknemers heten robert?".

**Voornaamwoorden**: hij, hem, zelf, zijn, zij, haarzelf, haar, van haar, het, zichzelf, ze, hun, zij zelf, hun, dit,deze, dat, die

**Queryopdrachten**: gesorteerd, sorteren op, richting, groeperen, groeperen op, op, weergeven, vermelden, weergeven, ik wil, naam, alleen, uitsluitend, schikken, rangschikken, vergelijken, met, alfabetisch, oplopende, aflopende, volgorde

**Bereik**: groter, meer, hoger, boven, >, minder, kleiner, lager, onder, <, ten minste, niet minder dan >=, maximaal, niet meer dan, <=, in, tussen, in het bereik van, van , later, eerder, vroeger, nadat, op, later dan, na sinds, begint met, vanaf, eindigt met

**Tijden**: ben 's ochtends, na de middag 's middags, 's avonds, uur, tussen de middag, middernacht, uur, minuut, seconde, uu mm:ss

Voorbeelden: 10 uur 's ochtends, 10:35 uur 's avonds, 10:35:15, 10 uur , uur, tussen de middag, middernacht, uur, minuut, seconde.

**Eerste N** (volgorde, rangschikking): bovenste, onderste, hoogste, laagste, eerste, laatste, volgende, vroegste, nieuwste, oudste, laatste, meest recente

**Typen visuals**: alle typen visuals zijn systeemeigen Power BI-visuals.  Opties die beschikbaar zijn in het deelvenster Visualisaties, kunt u opnemen in uw vraag.  De uitzondering hierop vormen [aangepaste visuals](power-bi-custom-visuals.md) die u handmatig hebt toegevoegd aan het deelvenster Visualisaties.

Voorbeeld: gebieden per maand weergeven en het verkooptotaal weergeven als staafdiagram

**Wh (relatie, gekwalificeerd)**: wanneer, waar, welke, wie, wiens, hoeveel, hoeveel keer, hoe vaak, hoe frequent, bedrag, aantal, hoeveelheid, hoelang, wat

## <a name="qa-helps-you-phrase-the-question"></a>Q&A helpt u bij het formuleren van de vraag
Er wordt geprobeerd om de vraag die u in Q&A stelt, zo nauwkeurig mogelijk te beantwoorden. Dit gebeurt op verschillende manieren. Voor alle onderstaande methoden geldt dat u de actie volledig, gedeeltelijk of helemaal niet kunt accepteren. Wanneer u de vraag in Q&A typt, gebeurt het volgende:

* Woorden en vragen worden automatisch aangevuld. Er worden verschillende strategieën gehanteerd, inclusief het aanvullen van herkenbare woorden, populaire vragen voor de onderliggende werkmappen en eerder gestelde vragen die een geldige respons hebben opgeleverd. Als er meerdere opties voor automatisch aanvullen beschikbaar zijn, worden deze weergegeven in een vervolgkeuzelijst.
* Spelfouten worden gecorrigeerd.
* Er wordt een voorbeeld van het antwoord gegeven in de vorm van een visualisatie. De visualisatie wordt bijgewerkt terwijl u typt en de vraag bewerkt (er wordt niet gewacht totdat u op Enter hebt gedrukt).
* Er worden automatisch vervangende termen uit een of meer onderliggende gegevenssets voorgesteld wanneer u de muisaanwijzer in het vragenvak naar achteren verplaatst.
* De vraag wordt op basis van de gegevens in een of meer onderliggende gegevenssets opnieuw geformuleerd. Dit is om te controleren of Q&A uw vraag heeft begrepen, aangezien de woorden die u hebt gebruikt, worden vervangen door synoniemen uit een of meer onderliggende gegevenssets.
* Woorden die niet worden herkend, worden weergegeven in een lichtere kleur.

## <a name="combine-results-from-more-than-one-dataset"></a>Resultaten van meerdere gegevenssets combineren
Een van de krachtigste functies van Power BI is de mogelijkheid om gegevens uit verschillende gegevenssets te combineren.  Beperk uw vragen dus niet tot één gegevensset. Stel vragen waarmee u gegevens uit meerdere gegevenssets ophaalt. Als mijn dashboard bijvoorbeeld bevat uit het voorbeeld van een retailanalyse en een gegevensset met informatie over de populatie van de provinciën, kan ik het volgende vragen: *geef in aflopende volgorde het aantal winkels op basis van de provinciebevolking weer in een staafdiagram*.

## <a name="dont-stop-now"></a>Stop nog niet
Nadat Q&A de resultaten heeft weergegeven, kunt u nog meer acties uitvoeren. Met de interactieve functies van de visualisatie en van Q&A kunt u nog meer inzichten te verwerven

## <a name="next-steps"></a>Volgende stappen
Terug naar [Q&A in Power BI](power-bi-q-and-a.md)  

[Power BI - basisconcepten](service-basic-concepts.md)  

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

