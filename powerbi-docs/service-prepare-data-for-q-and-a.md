---
title: Uw gegevens geschikt maken voor Q&A in Power BI
description: Uw gegevens geschikt maken voor Q&A in Power BI
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
ms.date: 09/26/2017
ms.author: mihart
ms.openlocfilehash: 499c3beca9046af9336de6dfec96994004050986
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/15/2017
---
# <a name="make-your-data-work-well-with-qa-in-power-bi"></a>Uw gegevens geschikt maken voor Q&A in Power BI
Lees verder als u gegevensmodellen maakt of Excel-werkmappen bouwt die worden gebruikt in Power BI.

De Q&A-functie in Power BI zoekt gestructureerde gegevens en kiest de juiste visualisatie voor uw vraag. Dit is precies waar het zo'n aantrekkelijke hulpprogramma is om te gebruiken.   

Q&A kan worden gebruikt voor elk geüpload Excel-bestand dat tabellen, bereiken of een PowerPivot-model bevat, maar hoe meer optimalisaties u uitvoert en gegevens u opschoont, hoe robuuster de prestaties Q&A levert. 

## <a name="how-qa-works"></a>Hoe Q&A werkt
Q&A biedt u een reeks natuurlijke taalverwerkingsmogelijkheden die kunnen worden gebruikt voor al uw gegevens. U kunt contextafhankelijke trefwoorden zoeken in uw Excel-tabel, -kolom en namen van berekende velden. Ten tweede beschikt de functie over ingebouwde kennis op basis waarvan uw gegevens kunnen worden gefilterd, gesorteerd, geaggregeerd, gegroepeerd en weergegeven. 

Als u bijvoorbeeld een Excel-tabel met de naam Verkopen hebt die de kolommen Product, Maand, Verkochte eenheden, Brutoverkoop en Winst bevat, kunt u over elk van deze entiteiten vragen stellen.  U kunt bijvoorbeeld vragen om het aantal verkopen of de totale winst per maand weer te geven of om de producten te sorteren op basis van de verkochte eenheden. Meer informatie over de [soorten vragen die u kunt stellen](http://blogs.msdn.com/b/powerbi/archive/2014/02/27/demystifying-power-bi-q-amp-a-part-1.aspx), [het stellen van vragen op basis van een vragensjabloon](service-q-and-a.md) en over [de typen visualisaties die u kunt opgeven in een Q&A-query](power-bi-visualization-types-for-reports-and-q-and-a.md).

## <a name="prepare-a-workbook-for-qa"></a>Een werkmap voorbereiden voor Q&A
Q&A is afhankelijk van de namen van tabellen, kolommen en berekende velden om gegevensspecifieke vragen te kunnen beantwoorden. De entiteiten in u werkmap spelen dus een belangrijke rol.

Hier volgen enkele tips optimaal gebruik van Q&A te maken in uw werkmap.

* Zorg ervoor dat uw gegevens in een Excel-tabel staan. U kunt als volgt [een Excel-tabel maken](https://support.office.com/article/Create-an-Excel-table-in-a-worksheet-e81aa349-b006-4f8a-9806-5af9df0ac664?ui=en-US&rs=en-US&ad=US).
* Zorg ervoor dat de namen van de tabellen, kolommen en het berekende veld een logische naam hebben.
  
  Als u bijvoorbeeld een tabel met verkoopgegevens hebt, geeft u de tabel de naam Verkoop. Kolomnamen zoals Jaar, Product, Vertegenwoordiger en Bedrag werken uitstekend in Q&A.

> [!NOTE]
> Als uw werkmap een Power Pivot-gegevensmodel bevat, kunt u nog meer optimalisaties uitvoeren. Lees [Ontrafelen van Power BI Q&A deel 2](http://blogs.msdn.com/b/powerbi/archive/2014/02/27/demystifying-power-bi-q-amp-a-part-2.aspx) van ons interne team van experts op het gebied van natuurlijk taalgebruik.
> 
> 

## <a name="next-steps"></a>Volgende stappen
[Q&A in Power BI](service-q-and-a.md)  
[Zelfstudie: Inleiding tot Q&A in Power BI](power-bi-visualization-introduction-to-q-and-a.md)  
[Gegevens ophalen (voor Power BI)](service-get-data.md)  
[Power BI - basisconcepten](service-basic-concepts.md)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

