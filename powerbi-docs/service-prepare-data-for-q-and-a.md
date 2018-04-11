---
title: Uw Excel-gegevens geschikt maken voor Q&A in Power BI
description: Uw gegevens geschikt maken voor Q&A in Power BI
services: powerbi
documentationcenter: ''
author: mihart
manager: kfile
backup: ''
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 03/01/2018
ms.author: mihart
LocalizationGroup: Ask questions of your data
ms.openlocfilehash: b45c259cf90668fea878c220670f3efa76b482fd
ms.sourcegitcommit: 5e1f7d2673efe25c47b9b9f315011055bfe92c8f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2018
---
# <a name="how-to-make-your-excel-data-work-well-with-qa-in-power-bi"></a>Uw Excel-gegevens geschikt maken voor Q&A in Power BI
Lees verder als u gegevensmodellen maakt of Excel-werkmappen bouwt die worden gebruikt in Power BI.

De Q&A-functie in Power BI zoekt gestructureerde gegevens en kiest de juiste visualisatie voor uw vraag. Dit is precies waar het zo'n aantrekkelijke hulpprogramma is om te gebruiken.   

Q&A kan worden gebruikt voor elk geüpload Excel-bestand dat tabellen, bereiken of een PowerPivot-model bevat, maar hoe meer optimalisaties u uitvoert en gegevens u opschoont, hoe robuuster de prestaties Q&A levert.  Als u rapporten en dashboards op basis van uw gegevensset wilt delen, kunt u beter uw collega's vragen u ruim de tijd te geven om vragen te stellen en antwoorden van kwaliteit te krijgen.

### <a name="how-qa-works-with-excel"></a>Hoe Q&A met Excel samenwerkt
Q&A biedt u een reeks natuurlijke taalverwerkingsmogelijkheden die kunnen worden gebruikt voor al uw gegevens. U kunt contextafhankelijke trefwoorden zoeken in uw Excel-tabel, -kolom en namen van berekende velden. Tevens beschikt de functie over ingebouwde kennis op basis waarvan uw gegevens kunnen worden gefilterd, gesorteerd, geaggregeerd, gegroepeerd en weergegeven. 

Als u bijvoorbeeld een Excel-tabel met de naam Verkopen hebt die de kolommen Product, Maand, Verkochte eenheden, Brutoverkoop en Winst bevat, kunt u over elk van deze entiteiten vragen stellen.  U kunt bijvoorbeeld vragen om het aantal verkopen of de totale winst per maand weer te geven of om de producten te sorteren op basis van de verkochte eenheden. Meer informatie over de [soorten vragen die u kunt stellen](power-bi-q-and-a.md) en [de typen visualisaties die u kunt opgeven in een Q&A-query](power-bi-visualization-types-for-reports-and-q-and-a.md).

### <a name="prepare-an-excel-dataset-for-qa"></a>Een Excel-gegevensset voorbereiden voor Q&A
Q&A is afhankelijk van de namen van tabellen, kolommen en berekende velden om gegevensspecifieke vragen te kunnen beantwoorden. De entiteiten in u werkmap spelen dus een belangrijke rol.

Hier volgen enkele tips optimaal gebruik van Q&A te maken in uw werkmap.

* Zorg ervoor dat uw gegevens in een Excel-tabel staan. U kunt als volgt [een Excel-tabel maken](https://support.office.com/article/Create-an-Excel-table-in-a-worksheet-e81aa349-b006-4f8a-9806-5af9df0ac664?ui=en-US&rs=en-US&ad=US).
* Zorg ervoor dat de namen van tabellen, kolommen en het berekende veld logische klinken in natuurlijke taal.
  
  Als u bijvoorbeeld een tabel met verkoopgegevens hebt, geeft u de tabel de naam Verkoop. Kolomnamen zoals Jaar, Product, Vertegenwoordiger en Bedrag werken uitstekend in Q&A.

* Als uw werkmap een Power Pivot-gegevensmodel bevat, kunt u nog meer optimalisaties uitvoeren. Lees [Ontrafelen van Power BI Q&A deel 2](http://blogs.msdn.com/b/powerbi/archive/2014/02/27/demystifying-power-bi-q-amp-a-part-2.aspx) van ons interne team van experts op het gebied van natuurlijk taalgebruik.

* Open de gegevensset in Power BI Desktop openen en maak nieuwe kolommen, maak berekende eenheden en voeg velden samen om unieke waarden samen te stellen, classificeer gegevens op type (bijvoorbeeld datums, tekenreeksen, geografie, afbeeldingen of URL's), en meer.

## <a name="next-steps"></a>Volgende stappen
Terug naar [Q&A in Power BI](power-bi-q-and-a.md)  
[On-premises gegevenssets voorbereiden voor Q&A](service-q-and-a-direct-query.md)   
[Snelstartgids Q&A](power-bi-visualization-introduction-to-q-and-a.md)  
[Gegevens ophalen (voor Power BI)](service-get-data.md)  

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

