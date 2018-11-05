---
title: Capaciteiten van Power BI Premium in uw organisatie bewaken
description: De Power BI-beheerportal en de app Power BI Premium Capacity Metrics gebruiken
author: mgblythe
ms.author: mblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-admin
ms.topic: conceptual
ms.date: 10/09/2018
LocalizationGroup: Premium
ms.openlocfilehash: 2623dd3280636583d5dd6d6e3f57518550032193
ms.sourcegitcommit: 42475ac398358d2725f98228247b78aedb8cbc4f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/25/2018
ms.locfileid: "50003197"
---
# <a name="monitor-power-bi-premium-and-power-bi-embedded-capacities"></a>Power BI Premium en Power BI Embedded-capaciteiten bewaken

In dit artikel vindt u een overzicht van het bewaken van de metrische gegevens voor uw Power BI Premium-capaciteiten. Het bewaken van het capaciteitsgebruik biedt een geïnformeerde benadering voor het beheren van uw capaciteiten.

U kunt de capaciteit bewaken met de app Power BI Premium Capacity Metrics of via de beheerportal. We raden de app aan omdat deze meer detail biedt. Dit artikel behandelt echte beide opties.

<iframe width="560" height="315" src="https://www.youtube.com/embed/UgsjMbhi_Bk?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>

## <a name="install-the-premium-capacity-metrics-app"></a>De app Premium Capacity Metrics installeren

U kunt rechtstreeks naar de [app Premium Capacity Metrics](https://app.powerbi.com/groups/me/getapps/services/capacitymetrics) gaan of deze net als andere apps in Power BI installeren.

1. Klik in Power BI op **Apps**.

    ![Ga naar Apps](media/service-admin-premium-monitor-capacity/apps.png)

2. Klik aan de rechterkant op **Apps downloaden**.

3. Zoek in de categorie **Apps** naar **Power BI Premium Capacity Metrics-app**.

4. Meld u aan om de app te installeren.

Als de app is geïnstalleerd, kunt u metrische gegevens over de capaciteiten in uw organisatie zien. Laten we eens kijken naar enkele belangrijke metrische gegevens die beschikbaar zijn.

## <a name="use-the-metrics-app"></a>De Metrics-app gebruiken

Als u de app opent, ziet u eerst een dashboard met een overzicht van alle capaciteiten waarvoor u beheerdersrechten bezit.

![App-dashboard met metrische gegevens](media/service-admin-premium-monitor-capacity/app-dashboard.png)

Het rapport heeft drie tabbladen die we in de volgende secties met meer detail beschrijven.

* **Filters die zijn toegepast op alle pagina's**: zorgen ervoor dat u de andere pagina's in het rapport kunt filteren op een specifieke capaciteit.
* **Gegevenssets**: bieden gedetailleerde metrische gegevens over de status van de gegevenssets binnen uw capaciteiten.
* **Systeem**: geeft de metrische gegevens van de totale capaciteit weer, inclusief hoog geheugen- en CPU-verbruik. 

### <a name="filters-applied-to-all-pages-tab"></a>Filters die op alle paginatabbladen zijn toegepast

Op het tabblad **Filters op alle pagina's toegepast** kunt u een capaciteit, een gegevensset en een gegevensbereik binnen de afgelopen zeven dagen selecteren. Filters worden vervolgens toegepast op alle relevante pagina's en tegels in het rapport. Als u er geen filters zijn geselecteerd, worden in het rapport alleen de metrische gegevens getoond van elke capaciteit waarvan u de eigenaar bent.

![Tabblad Filters](media/service-admin-premium-monitor-capacity/filters-tab.png)

### <a name="datasets-tab"></a>Tabblad Gegevenssets

Het tabblad **Gegevenssets** biedt het grootste deel van metrische gegevens in de app. Gebruik de knoppen bovenaan het tabblad om door de verschillende gebieden te navigeren: **Samenvatting**, **Vernieuwingen**, **Queryduur**, **Querywachttijden** en **Gegevenssets**.

![Tabblad Gegevenssets](media/service-admin-premium-monitor-capacity/datasets-tab.png)

#### <a name="summary-area"></a>Overzichtsgebied

In het **Samenvattingsgebied** wordt een weergave van uw capaciteiten op basis van entiteiten, systeemresources en werkbelastingen van gegevenssets weergegeven.

| | **Metrische gegevens** |
| --- | --- |
| **Entiteiten** | * Het aantal capaciteiten waarvan u eigenaar bent<br> * Het verschillende aantal gegevenssets in uw capaciteit<br> * Het verschillende aantal werkruimten in uw capaciteit |
| **Systeem** | * Het gemiddelde geheugengebruik in GB gedurende de afgelopen zeven dagen<br> * Het hoogste geheugengebruik in GB gedurende de afgelopen zeven dagen en de lokale tijd waarop dit plaatsvond<br> * Het aantal keren waarop de CPU 80% van de drempelwaarden overschreed gedurende de afgelopen zeven dagen, gesplitst in buckets van drie minuten<br> * De tijden waarop de CPU de 80% meestal overschreed gedurende de afgelopen zeven dagen, gesplitst in buckets van één uur, en de lokale tijd waarop dit plaatsvond<br> * Het aantal keren dat DirectQuery/Live-verbindingen 80% van de drempelwaarden overschreed gedurende de afgelopen zeven dagen, gesplitst in buckets van drie minuten<br> * De tijden waarop DirectQuery/Live-verbindingen de 80% meestal overschreed gedurende de afgelopen zeven dagen, gesplitst in buckets van één uur, en de lokale tijd waarop dit plaatsvond |
| **Workloads van gegevenssets** | * Het totale aantal vernieuwingen gedurende de afgelopen zeven dagen<br> * Het totale aantal geslaagde vernieuwingen gedurende de afgelopen zeven dagen<br> * Het totale aantal mislukte vernieuwingen gedurende de afgelopen zeven dagen<br> * Het totale aantal mislukte vernieuwingen wegens onvoldoende geheugen<br> * De gemiddelde vernieuwingsduur wordt gemeten in minuten, de tijd om de bewerking te voltooien<br> * De gemiddelde wachttijd voor het vernieuwen wordt gemeten in minuten, de gemiddelde vertraging tussen de geplande tijd en het begin van de bewerking<br> * Het totale aantal uitgevoerde query's gedurende de afgelopen zeven dagen<br> * Het totale aantal geslaagde query's gedurende de afgelopen zeven dagen<br> * Het totale aantal mislukte query's gedurende de afgelopen zeven dagen<br> * De gemiddelde duur van de query's wordt gemeten in minuten, de tijd om de bewerking te voltooien<br> * Het totale aantal modellen dat wegens geheugendruk is verwijderd |
|  |  |

#### <a name="refreshes-area"></a>Vernieuwingengebied

In het gebied **Vernieuwingen** vindt u de voltooide vernieuwingen, de geslaagde vernieuwingen, de gemiddelde/maximale wachttijd en de gemiddelde/maximale vernieuwingsduur gedurende de afgelopen zeven dagen, gesegmenteerd in gegevenssets. De onderste twee diagrammen tonen de vernieuwingen versus het geheugenverbruik in GB en de gemiddelde wachttijden, gesplitst in buckets van één uur en weergegeven in de lokale tijd. De bovenste staafdiagrammen tonen de gemiddelde tijd voor het vernieuwen van de gegevensset (vernieuwingsduur) en de gemiddelde duur van de wachttijden. Meerdere pieken met een lange wachttijd duiden erop dat de capaciteit aan zijn maximum zit.

#### <a name="query-durations-area"></a>Het gebied Queryduur

In het gebied **Queryduur** wordt het totaalaantal uitvoeringen van query's vermeld en de gemiddelde/maximale duur in milliseconden. Deze gegevens zijn opgedeeld in gegevenssets, werkruimten en buckets per uur in de afgelopen zeven dagen. De onderste grafiek geeft het aantal query's weer, evenals de gemiddelde duur (in milliseconden) in vergelijking met het geheugenverbruik in GB, opgesplitst in buckets per uur en vermeld in lokale tijd.

De bovenste grafiek geeft een histogram van de distributie van de queryduur weer. Het histogram is gebucket per queryduur, dat in milliseconden in de volgende categorieën wordt vermeld: intervallen van <= 30 ms, 30 - 100 ms, 100 - 300 ms, 300 ms - 1 sec, 1 sec - 3 sec, 3 sec - 10 sec, 10 sec - 30 sec en > 30 seconden.

De grafiek rechtsonder vermeldt de top vijf gegevenssets per gemiddelde queryduur voordat de query's waren voltooid.

Een lange queryduur en lange wachttijden geven aan dat de capaciteit overbelast raakt. Het kan ook betekenen dat een enkele gegevensset problemen veroorzaakt en dat verder onderzoek nodig is.

#### <a name="query-waits-area"></a>Het gebied Querywachttijden

In het gebied **Querywachttijden** wordt het totaalaantal uitgevoerde query's vermeld, evenals het totaalaantal wachtende query's voor Livequery/DirectQuery en de gemiddelde/maximale wachttijd, uitgedrukt in milliseconden. Deze gegevens zijn opgedeeld in gegevenssets, werkruimten en buckets per uur in de afgelopen zeven dagen. De onderste grafiek geeft het aantal querywachttijden weer, evenals de gemiddelde wachttijd (in milliseconden) in vergelijking met het geheugenverbruik in GB, opgesplitst in buckets per uur en vermeld in lokale tijd.

De bovenste grafiek geeft een histogram van de distributie van de querywachttijd weer. Het histogram is gebucket per queryduur, dat in milliseconden in de volgende categorieën wordt vermeld: intervallen van <= 50 ms, 50 - 100 ms, 100 - 200 ms, 200 - 400 ms, 400 ms - 1 sec, 1 sec - 5 sec en  > 5 seconden.

De grafiek rechtsonder vermeldt de top vijf gegevenssets per gemiddelde querywachttijd voordat de query's waren gestart.

#### <a name="datasets-area"></a>Het gebied gegevenssets

In het gebied **Gegevenssets** vindt u de volledige gegevenssets die zijn verwijderd vanwege geheugendruk (per uur).

### <a name="system-tab"></a>Tabblad Systeem

In het tabblad **Systeem** vindt u de tijden van hoog CPU-gebruik (aantal keren dat de drempelwaarde van 80% is overschreden), hoog gebruik van DirectQuery/Live-verbindingen en het geheugengebruik.

![Rapport Premium-systeem](media/service-admin-premium-monitor-capacity/system-tab.png)

## <a name="monitor-power-bi-embedded-capacity"></a>Power BI Embedded-capaciteit bewaken

U kunt ook de app Power BI Premium Capacity Metrics gebruiken om *A SKU*-capaciteiten in Power BI Embedded te bewaken. Deze capaciteiten worden in het rapport weergegeven als u een beheerder van de capaciteit bent. U kunt het rapport echter niet vernieuwen, tenzij u bepaalde machtigingen verleent aan Power BI op uw A SKU's:

1. Open uw capaciteit in de Azure-portal.
1. Klik op **Toegangsbeheer (IAM)** en voeg de app Power BI Premium aan de lezersrol toe. Als u de app niet op naam kunt vinden, kunt u deze ook op client-id toevoegen: cb4dc29f-0bf4-402a-8b30-7511498ed654.

    ![Machtigingen voor Power BI Embedded](media/service-admin-premium-monitor-capacity/embedded-permissions.png)

> [!NOTE]
> U kunt capaciteitsgebruik van Power BI Embedded bewaken met de app of in de Azure-portal, maar niet in de Power BI-beheerportal.

## <a name="basic-monitoring-in-the-admin-portal"></a>Eenvoudige bewaking in de beheerportal

Het gebied **Capaciteitsinstellingen** van de beheerportal bevat vier meters waarmee de geplaatste belastingen en de door uw capaciteit gebruikte resources gedurende de afgelopen zeven dagen worden gemeten. Deze vier tegels werken volgens met tijdvensters van een uur, waarin wordt aangegeven hoeveel uren gedurende de afgelopen zeven dagen de desbetreffende meting meer dan 80% aangaf. Deze meting geeft en potentiële afname van de eindgebruikerservaring aan.

![Gebruik over zeven dagen](media/service-admin-premium-monitor-capacity/usage-in-days.png)

| **Meting** | **Beschrijving** |
| --- | --- |
| CPU |Aantal keer dat CPU-gebruik 80% of meer was. |
| Geheugenthrashing |De geheugendruk van uw back-endkernen. Met deze gegevens wordt aangegeven hoe vaak gegevenssets uit het geheugen zijn verwijderd vanwege de geheugendruk door het gebruik van meerdere gegevenssets. |
| Memory Usage |Gemiddeld geheugengebruik, in gigabytes (GB). |
| DQ/s | Aantal keer dat het aantal DirectQuery- en liveverbindingen 80% van de limiet heeft overschreden. <br> * We beperken het totale aantal query's per seconde voor DirectQuery en live-verbindingen. * De grenswaarden zijn 30/s voor P1, 60/s voor P2 en 120/s voor P3. * De query's voor DirectQuery en liveverbindingen tellen beide een zwaar voor de bovenstaande limiet. Als u gedurende één seconde bijvoorbeeld 15 DirectQuery's en 15 live-verbindingen hebt, is de grenswaarde bereikt<br>* Dit geldt ook voor on-premises- en cloudverbindingen. |
|  |  |

Metrische gegevens geven het gebruik van de afgelopen week aan.  Als u een weergave met meer details wilt zien van de metrische gegevens, klikt u hiervoor op een van de samenvattingstegels.  Hiermee gaat u naar de gedetailleerde diagrammen voor elk van de metrische gegevens voor uw Premium-capaciteit. In het volgende diagram worden de details voor de CPU-meting getoond.

![Gedetailleerde gebruiksgrafiek CPU](media/service-admin-premium-monitor-capacity/premium-usage-detailed-chart-cpu.png)

Deze grafieken worden voor de afgelopen week per uur samengevat en kunnen helpen bij het isoleren wanneer u mogelijk specifieke, prestatiegerelateerde evenementen hebt gehad in uw Premium-capaciteit.

U kunt ook de onderliggende gegevens voor elk van de metrische gegevens exporteren naar een csv-bestand.  Deze export biedt u gedetailleerde informatie voor elke dag van de afgelopen week, in stappen van drie minuten.

## <a name="next-steps"></a>Volgende stappen

U hebt geleerd hoe u Power BI Premium-capaciteiten kunt bewaken. U kunt nu meer leren over het optimaliseren van capaciteiten.

> [!div class="nextstepaction"]
> [Resourcebeheer en optimalisatie van Power BI Premium-capaciteit](service-premium-understand-how-it-works.md)
