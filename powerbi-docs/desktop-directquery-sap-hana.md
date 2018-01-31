---
title: DirectQuery voor SAP HANA in Power BI
description: Overwegingen bij het gebruik van DirectQuery met SAP HANA
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
ms.date: 01/24/2018
ms.author: davidi
ms.openlocfilehash: 2b2e59371c96928a2b7c6b23bd393a80ecc3041a
ms.sourcegitcommit: 7249ff35c73adc2d25f2e12bc0147afa1f31c232
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/25/2018
---
# <a name="directquery-and-sap-hana"></a>DirectQuery en SAP HANA
Met behulp van **DirectQuery** kunt u rechtstreeks verbinding maken met **SAP HANA**-gegevensbronnen.

Wanneer u **SAP HANA** gebruikt, is het van belang enkele aspecten te kennen van de wijze waarop verbindingen ermee worden behandeld, opdat:

* De resultaten zijn zoals ze worden verwacht als de SAP HANA-weergave niet-additieve metingen bevat (bijvoorbeeld unieke tellingen, of gemiddelden, in plaats van eenvoudige optellingen)
* De resulterende query's efficiënt zijn

Het kan geen kwaad even de tijd te nemen het gedrag uit te leggen van een relationele bron als **SQL Server** als de query die in **Get Data** of **Query-editor** is gedefinieerd, een aggregatie uitvoert. In het volgende voorbeeld retourneert een in **Query-editor** gedefinieerde query de gemiddelde prijs door middel van **ProductID**.

![](media/desktop-directquery-sap-hana/directquery-sap-hana_01.png)

Als de gegevens in Power BI worden geïmporteerd (versus gebruik van DirectQuery), gebeurt er het volgende:

* De gegevens worden geïmporteerd op het aggregatieniveau dat is gedefinieerd door de in **Query-editor** gemaakte query. Bijvoorbeeld gemiddelde prijs per product. Dit leidt tot een tabel met de twee kolommen *ProductID* en *AveragePrice*, die in visuele elementen kunnen worden gebruikt.
* In een visueel element wordt elke volgende samenstelling (zoals *Som*, *Gemiddelde*, *Minus* en overige) uitgevoerd op die geïmporteerde gegevens.  Als bijvoorbeeld *AveragePrice* in een visueel element wordt opgenomen, wordt standaard de samenstelling *Som* gebruikt en wordt de som van *AveragePrice* voor elk *ProductID* geretourneerd, wat in dit geval 13,67 is. Het zelfde geldt voor elke alternatieve samengestelde functie (zoals *Minus*, *Gemiddelde* enzovoort) die voor het visuele element wordt gebruikt. Bijvoorbeeld: het *gemiddelde* van *AveragePrice* retourneert het gemiddelde van 6,66, 4 en 3, wat gelijk is aan 4,56. Het gemiddelde van de *prijs* van de zes records in de onderliggende tabel 5,17) wordt dus *niet* geretourneerd.

Als **DirectQuery** wordt gebruikt in plaats van Importeren, is dezelfde semantiek van toepassing en zouden de resultaten precies dezelfde zijn:

* Gegeven dezelfde query worden logisch gezien exact de dezelfde gegevens aan de rapporterende laag gepresenteerd, hoewel de gegevens niet feitelijk worden geïmporteerd.
* In een visueel element wordt elke volgende samenstelling (*Som*, *Gemiddelde*, *Minus* en overige) opnieuw uitgevoerd voor die logische tabel van de query. En ook hier wordt in een visueel element met een *gemiddelde* van *AveragePrice* de waarde 4,56 geretourneerd.

Laten we nu eens naar **SAP HANA** gaan kijken. Power BI werkt in SAP HANA zowel met *analytische weergaven* als *berekeningsweergaven*. Beide kunnen metingen bevatten. Tegenwoordig volgt de werkwijze voor SAP HANA dezelfde principes als eerder beschreven: de query die wordt gedefinieerd in **Gegevens ophalen** of **Query-editor**, bepaalt de beschikbare gegevens. Vervolgens vindt elke volgende samenstelling in een visueel element van die gegevens plaats. Hetzelfde geldt voor zowel Importeren als DirectQuery.

Gezien de aard van HANA is de query die in het eerste dialoogvenster **Gegevens ophalen** of **Query-editor** is gedefinieerd, echter altijd een combinatiequery. Deze bevat gewoonlijk alle metingen waarbij de feitelijk te gebruiken samenstelling door de HANA-weergave wordt gedefinieerd.

Het equivalent van SQL Server in bovenstaand voorbeeld is dat er een HANA-weergave is die **ID**, **ProductID**, **DepotID**, en metingen bevat, inclusief **AveragePrice**, gedefinieerd in de weergave als **Average of Price**.

![](media/desktop-directquery-sap-hana/directquery-sap-hana_02.png)

Als in **Gegevens ophalen** de gemaakte selecties voor **ProductID** en de meting **AveragePrice** zijn, dan wordt er een query over de weergave gedefinieerd, waarbij die samengestelde gegevens worden gevraagd (in bovenstaand voorbeeld wordt ter verduidelijking pseudo-SQL gebruikt, wat niet overeenkomt met de exacte syntaxis van HANA SQL. Vervolgens aggregeren eventuele verdere samenstellingen die in een visueel element worden gedefinieerd de resultaten van een dergelijke query. Dit is, net zoals hierboven beschreven voor **SQL Server**, opnieuw van toepassing op zowel het geval Importeren als DirectQuery. In het geval van DirectQuery wordt de query uit **Gegevens ophalen** of **Query-editor** gebruikt in een subselectie binnen één query die naar HANA wordt verzonden. Het is dus niet feitelijk zo dat alle gegevens worden ingelezen voordat ze verder worden samengesteld.

Dit leidt tot de volgende belangrijke overwegingen bij het gebruik van DirectQuery over HANA:

* Er moet worden gelet op verdere samenstellingen die in visuele elementen worden uitgevoerd zodra de meting in HANA niet-additief is (bijvoorbeeld geen eenvoudige *Som*, *Minus* of *Max*).
* In **Gegevens ophalen** of **Query-editor** mogen alleen de vereiste kolommen worden opgenomen om de vereiste gegevens op te halen. Dit weerspiegelt het feit dat het resultaat een query is en een redelijke query is die naar HANA kan worden verzonden. Als bijvoorbeeld tientallen kolommen zouden worden geselecteerd (die eventueel nodig kunnen zijn voor verdere visuele elementen), dan houdt een eenvoudig visueel element ook voor DirectQuery in dat de in de subselectie gebruikte combinatiequery tientallen kolommen bevat, die over het algemeen slechte prestaties geven.

We kijken naar een voorbeeld. In het volgende voorbeeld worden naast de meting OrderQuantity vijf kolommen geselecteerd in het dialoogvenster **Gegevens ophalen**: CalendarQuarter, Color, LastName, ProductLine, SalesOrderNumber. Dit betekent dat als er later een eenvoudig visueel element wordt gemaakt met Minus OrderQuantity, dit resulteert in de volgende SQL-query naar HANA. Het gearceerde gedeelte is de subselectie. Deze bevat de query van **Gegevens ophalen** / **Query-editor**. Als de subselectie een resultaat oplevert met zeer hoge kardinaliteit, dan is de prestatie van HANA waarschijnlijk erg slecht.

![](media/desktop-directquery-sap-hana/directquery-sap-hana_03.png)

Daarom wordt het aangeraden dat de in **Gegevens ophalen** of **Query-editor** geselecteerde items moeten worden beperkt tot die items die nodig zijn, terwijl er nog wel een redelijke query voor HANA uitrolt.

### <a name="next-steps"></a>Volgende stappen
Bekijk de volgende bronnen voor meer informatie over DirectQuery:

* [DirectQuery in Power BI](desktop-directquery-about.md)
* [Data sources supported by DirectQuery](desktop-directquery-data-sources.md) (Gegevensbronnen die worden ondersteund door DirectQuery)
* [DirectQuery and SAP BW](desktop-directquery-sap-bw.md) (DirectQuery en SAP BW)
* [On-premises data gateway](service-gateway-onprem.md) (On-premises gegevensgateway)

