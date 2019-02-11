---
title: Power BI Premium-capaciteiten bewaken met behulp van de beheerportal
description: Gebruik de Power BI-beheerportal om uw Premium-capaciteiten te bewaken.
author: minewiskan
ms.author: owend
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 02/05/2019
LocalizationGroup: Premium
ms.openlocfilehash: 59097c07719e4bb8db188e8a86db377076aea7a9
ms.sourcegitcommit: 54d44deb6e03e518ad6378656c769b06f2a0b6dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/07/2019
ms.locfileid: "55794104"
---
# <a name="monitor-capacities-in-the-admin-portal"></a>Capaciteiten bewaken in de beheerportal

In dit artikel wordt beschreven hoe u het gebied Instellingen voor capaciteit in de beheerportal kunt gebruiken voor een snel overzicht van de prestaties van uw capaciteit.  Als u de meest uitgebreide metrische gegevens over uw capaciteit wilt, is het raadzaam de [Power BI Premium Capacity Metrics](service-admin-premium-monitor-capacity.md)-app te gebruiken.

## <a name="capacity-metrics"></a>Metrische capaciteitsgegevens

Het gebied **Capaciteitsinstellingen** van de beheerportal bevat vier meters waarmee de geplaatste belastingen en de door uw capaciteit gebruikte resources gedurende de afgelopen zeven dagen worden gemeten. Deze vier tegels werken volgens met tijdvensters van een uur, waarin wordt aangegeven hoeveel uren gedurende de afgelopen zeven dagen de desbetreffende meting meer dan 80% aangaf. Deze meting geeft en potentiële afname van de eindgebruikerservaring aan.

![Gebruik over zeven dagen](media/service-admin-premium-monitor-capacity/usage-in-days.png)

| **Meting** | **Beschrijving** |
| --- | --- |
| CPU |Aantal keer dat CPU-gebruik 80% of meer was. |
| Geheugenthrashing |De geheugendruk van uw back-endkernen. Met deze gegevens wordt aangegeven hoe vaak gegevenssets uit het geheugen zijn verwijderd vanwege de geheugendruk door het gebruik van meerdere gegevenssets. |
| Geheugengebruik |Gemiddeld geheugengebruik, in gigabytes (GB). |
| DQ/s | Aantal keer dat het aantal DirectQuery- en liveverbindingen 80% van de limiet heeft overschreden. <br>  Het totale aantal query's per seconde voor DirectQuery en liveverbindingen is beperkt. De limieten zijn 30/s voor P1, 60/s voor P2 en 120/s voor P3.  De query's voor DirectQuery en liveverbindingen tellen beide even zwaar voor de bovenstaande limiet. Als u gedurende één seconde bijvoorbeeld 15 DirectQuery's en 15 live-verbindingen hebt, is de grenswaarde bereikt<br> Dit geldt ook voor on-premises en cloudverbindingen. |
|  |  |

Metrische gegevens geven het gebruik van de afgelopen week aan.  Als u een weergave met meer details wilt zien van de metrische gegevens, klikt u hiervoor op een van de samenvattingstegels.  Hiermee gaat u naar de gedetailleerde diagrammen voor elk van de metrische gegevens voor uw Premium-capaciteit. In het volgende diagram worden de details voor de CPU-meting getoond.

![Gedetailleerde gebruiksgrafiek CPU](media/service-admin-premium-monitor-capacity/premium-usage-detailed-chart-cpu.png)

Deze grafieken worden voor de afgelopen week per uur samengevat en kunnen helpen bij het isoleren wanneer u mogelijk specifieke, prestatiegerelateerde evenementen hebt gehad in uw Premium-capaciteit.

U kunt ook de onderliggende gegevens voor elk van de metrische gegevens exporteren naar een csv-bestand.  Deze export biedt u gedetailleerde informatie voor elke dag van de afgelopen week, in stappen van drie minuten.

## <a name="next-steps"></a>Volgende stappen

U hebt geleerd hoe u Power BI Premium-capaciteiten kunt bewaken. U kunt nu meer leren over het optimaliseren van capaciteiten.

> [!div class="nextstepaction"]
> [Resourcebeheer en optimalisatie van Power BI Premium-capaciteit](service-premium-understand-how-it-works.md)
