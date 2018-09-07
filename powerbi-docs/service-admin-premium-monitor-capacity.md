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
ms.date: 08/29/2018
LocalizationGroup: Premium
ms.openlocfilehash: 8e19bc596bef3862dca79ac92ffbd74954a9c756
ms.sourcegitcommit: 6be2c54f2703f307457360baef32aee16f338067
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/30/2018
ms.locfileid: "43300156"
---
# <a name="monitor-power-bi-premium-capacities-in-your-organization"></a>Capaciteiten van Power BI Premium in uw organisatie bewaken

In dit artikel vindt u een overzicht van het bewaken van de metrische gegevens voor uw Power BI Premium-capaciteiten. Het bewaken van het capaciteitsgebruik biedt een geïnformeerde benadering voor het beheren van uw capaciteiten. 

U kunt de capaciteit bewaken met de app Power BI Premium Capacity Metrics of via de beheerportal. We raden de app aan omdat deze meer detail biedt. Dit artikel behandelt echte beide opties.

## <a name="install-the-premium-capacity-metrics-app"></a>De app Premium Capacity Metrics installeren

U kunt rechtstreeks naar de [app Premium Capacity Metrics](https://app.powerbi.com/groups/me/getapps/services/capacitymetrics) gaan of deze net als andere apps in Power BI installeren.

> [!IMPORTANT]
> Als u de app wilt installeren en gebruiken, moet u een capaciteitsbeheerder voor ten minste één capaciteit zijn. Een Power BI-beheerder heeft hiervoor onvoldoende rechten. 

1. Klik in Power BI op **Apps**.

    ![Ga naar Apps](media/service-admin-premium-monitor-capacity/apps.png)

2. Klik aan de rechterkant op **Apps downloaden**.

3. Zoek in de categorie **Apps** naar **Power BI Premium Capacity Metrics-app**.

4. Meld u aan om de app te installeren.

Als de app is geïnstalleerd, kunt u metrische gegevens over de capaciteiten in uw organisatie zien. Laten we eens kijken naar enkele belangrijke metrische gegevens die beschikbaar zijn.

## <a name="use-the-metrics-app"></a>De Metrics-app gebruiken 
Als u de app opent, ziet u eerst een dashboard met een overzicht van alle capaciteiten waarvoor u beheerdersrechten bezit.

![Overzicht Premium-rapport](media/service-admin-premium-monitor-capacity/app-dashboard.png)

### <a name="filtering"></a>Filteren

Op het tabblad **Filters op alle pagina's toegepast** kunt u een capaciteit, een gegevensset en/of een gegevensbereik binnen de afgelopen zeven dagen selecteren. Met deze filters wordt de selectie toegepast op alle relevante pagina's en tegels in dit rapport. Als u niets selecteert, worden in het rapport alleen de metrische gegevens getoond van elke capaciteit waarvan u de eigenaar bent.

![Overzicht Premium-rapport](media/service-admin-premium-monitor-capacity/premium-report-overview.png)

### <a name="summary-tab"></a>Tabblad Samenvatting

Op het tabblad **Samenvatting** wordt een weergave getoond van de capaciteit op basis van entiteiten, het systeem en gegevenssets.

![Filters die op alle pagina's van toepassing zijn](media/service-admin-premium-monitor-capacity/premium-summary-report.png)

| **Gebied** | **Metrische gegevens** |
| --- | --- |
| **Entiteiten** | * Het aantal capaciteiten waarvan u eigenaar bent<br> * Het verschillende aantal gegevenssets in uw capaciteit<br> * Het verschillende aantal werkruimten in uw capaciteit |
| **Systeem** | * Het gemiddelde geheugengebruik in GB gedurende de afgelopen zeven dagen<br> * Het hoogste geheugengebruik in GB gedurende de afgelopen zeven dagen en de lokale tijd waarop dit plaatsvond<br> * Het aantal keren waarop de CPU 80% van de drempelwaarden overschreed gedurende de afgelopen zeven dagen, gesplitst in buckets van drie minuten<br> * De tijden waarop de CPU de 80% meestal overschreed gedurende de afgelopen zeven dagen, gesplitst in buckets van één uur, en de lokale tijd waarop dit plaatsvond<br> * Het aantal keren dat DirectQuery/Live-verbindingen 80% van de drempelwaarden overschreed gedurende de afgelopen zeven dagen, gesplitst in buckets van drie minuten<br> * De tijden waarop DirectQuery/Live-verbindingen de 80% meestal overschreed gedurende de afgelopen zeven dagen, gesplitst in buckets van één uur, en de lokale tijd waarop dit plaatsvond |
| **Workloads van gegevenssets** | * Het totale aantal vernieuwingen gedurende de afgelopen zeven dagen<br> * Het totale aantal geslaagde vernieuwingen gedurende de afgelopen zeven dagen<br> * Het totale aantal mislukte vernieuwingen gedurende de afgelopen zeven dagen<br> * Het totale aantal mislukte vernieuwingen wegens onvoldoende geheugen<br> * De gemiddelde vernieuwingsduur wordt gemeten in minuten, de tijd om de bewerking te voltooien<br> * De gemiddelde wachttijd voor het vernieuwen wordt gemeten in minuten, de gemiddelde vertraging tussen de geplande tijd en het begin van de bewerking<br> * Het totale aantal uitgevoerde query's gedurende de afgelopen zeven dagen<br> * Het totale aantal geslaagde query's gedurende de afgelopen zeven dagen<br> * Het totale aantal mislukte query's gedurende de afgelopen zeven dagen<br> * De gemiddelde duur van de query's wordt gemeten in minuten, de tijd om de bewerking te voltooien<br> * Het totale aantal modellen dat wegens geheugendruk is verwijderd |
|  |  |

### <a name="refreshes-tab"></a>Tabblad Vernieuwingen

Op het tabblad **Vernieuwingen** vindt u de voltooide vernieuwingen, de geslaagde vernieuwingen, de gemiddelde/maximale wachttijd en de gemiddelde/maximale vernieuwingsduur gedurende de afgelopen zeven dagen, gesegmenteerd in gegevenssets. De onderste twee diagrammen tonen de vernieuwingen versus het geheugenverbruik in GB en de gemiddelde wachttijden, gesplitst in buckets van één uur en weergegeven in de lokale tijd. De bovenste staafdiagrammen tonen de gegevenssets met de langste tijden voor het vernieuwen van de gegevensset (vernieuwingsduur) en de maximale duur van de wachttijden. Meerdere pieken met een lange wachttijd duiden erop dat de capaciteit aan zijn maximum zit.

![Rapport Premium-vernieuwing](media/service-admin-premium-monitor-capacity/premium-refresh-report.png)

### <a name="datasets-tab"></a>Tabblad Gegevenssets

Op het tabblad **Gegevenssets** vindt u de volledige gegevenssets die zijn verwijderd vanwege geheugendruk (per uur).

![Rapport Premium-gegevenssets](media/service-admin-premium-monitor-capacity/premium-datasets-report.png)

### <a name="system-tab"></a>Tabblad Systeem

Op het tabblad **Systeem** vindt u het hoog CPU-gebruik (aantal keren dat de drempelwaarde van 80% is overschreden), hoog gebruik van DirectQuery/Live-verbindingen en het geheugengebruik.

![Rapport Premium-systeem](media/service-admin-premium-monitor-capacity/premium-system-report.png)

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
