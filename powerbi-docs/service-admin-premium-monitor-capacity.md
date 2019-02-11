---
title: Bewaak Power BI Premium-capaciteiten met de Premium Capacity Metrics-app.
description: De Power BI-beheerportal en de app Power BI Premium Capacity Metrics gebruiken
author: minewiskan
ms.author: owend
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 02/05/2019
LocalizationGroup: Premium
ms.openlocfilehash: c4e919de95c86051257ddc38b65c4dfda78dfc03
ms.sourcegitcommit: 54d44deb6e03e518ad6378656c769b06f2a0b6dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/07/2019
ms.locfileid: "55794620"
---
# <a name="monitor-premium-capacities-with-the-app"></a>Premium-capaciteiten bewaken met de app

Bewaking van uw capaciteiten is essentieel voor het nemen van gefundeerde beslissingen over hoe u uw Premium-capaciteitsresources het beste kunt gebruiken. U kunt de capaciteiten bewaken in de beheerportal of met de **Power BI Premium Capacity Metrics**-app. In dit artikel wordt het gebruik van de Premium Capacity Metrics-app beschreven. De app biedt de meest uitgebreide informatie over hoe uw capaciteiten presteren. Voor een algemener overzicht van de metrische gegevens over het gemiddelde gebruik in de afgelopen zeven dagen, kunt u de beheerportal gebruiken. Zie [Premium-capaciteiten bewaken in de beheerportal](service-admin-premium-monitor-portal.md) voor meer informatie over het bewaken in de portal.

De app wordt regelmatig bijgewerkt met nieuwe functies en functionaliteit. Zorg ervoor dat u de meest recente versie gebruikt.
**De meest recente versie van de app is 1.10.1.1 (5 februari 2019)**.   
Als er al een eerdere versie van de app is geïnstalleerd, is het raadzaam deze uit uw apps te verwijderen en vervolgens op CTRL+F5 te drukken om te vernieuwen. 

## <a name="install-the-app"></a>De app installeren

U kunt rechtstreeks naar [Premium Capacity Metrics-app](https://app.powerbi.com/groups/me/getapps/services/capacitymetrics) gaan of deze net als andere apps in Power BI installeren.


1. Klik in Power BI op **Apps**.   
    ![Ga naar Apps](media/service-admin-premium-monitor-capacity/apps.png)

2. Klik aan de rechterkant op **Apps downloaden**.
3. Zoek in de categorie **Apps** naar **Power BI Premium Capacity Metrics-app**.
4. Meld u aan om de app te installeren.

Een ogenblik geduld. Het duurt een paar minuten om te installeren en metrische gegevens te vernieuwen. Als u in de app lege metrische gegevens ziet, drukt u op F5 om uw browser te vernieuwen.


## <a name="get-app-refresh-history"></a>Vernieuwingsgeschiedenis van app ophalen

Als u wilt controleren wanneer de Premium Capacity Metrics-app voor het laatst is vernieuwd, klikt u op **Instellingen** > **Gegevenssets** > **Power BI Premium Capacity Metrics** > **Vernieuwingsgeschiedenis**. 

![Vernieuwingsgeschiedenis in Instellingen](media/settings-refresh-history.png)

De laatste vernieuwing wordt weergegeven. U kunt ook op **Vernieuwingsgeschiedenis** klikken om geplande vernieuwingen en vernieuwingen op aanvraag weer te geven.

![Laatste vernieuwing](media/service-admin-premium-monitor-capacity/settings-last-refresh.png)

## <a name="monitor-a-capacity-with-the-app"></a>Een capaciteit bewaken met de app

Als de app is geïnstalleerd, kunt u metrische gegevens voor de capaciteiten in uw organisatie zien. Laten we eens kijken naar enkele belangrijke metrische gegevens die beschikbaar zijn.

### <a name="metrics-dashboard"></a>Dashboard met metrische gegevens

Als u de app opent, ziet u eerst een dashboard met een overzicht van alle capaciteiten waarvoor u beheerdersrechten bezit.

![App-dashboard met metrische gegevens](media/service-admin-premium-monitor-capacity/app-dashboard.png)

Het dashboard bevat de volgende metrische gegevens:

| **Rapportsectie** | **Metrische gegevens** |
| --- | --- |
| **Systeemoverzicht** |  Versie van de toepassing<br>  Aantal capaciteiten waarvan u beheerder bent<br>  Aantal werkruimten in de capaciteiten waarvoor metrische gegevens worden gerapporteerd<br>  Gemiddeld geheugengebruik in GB gedurende de afgelopen zeven dagen<br>  Maximaal geheugengebruik in GB gedurende de afgelopen zeven dagen<br>  Lokaal tijdstip waarop het maximale geheugengebruik is opgetreden<br>  Aantal keren dat de CPU 80% van de drempelwaarden overschreed gedurende de afgelopen zeven dagen, gesplitst in buckets van drie minuten<br>  Tijden waarop de CPU de 80% meestal overschreed gedurende de afgelopen zeven dagen, gesplitst in buckets van één uur<br>  Lokaal tijdstip waarop de CPU de 80% het vaakst in één uur heeft overschreden |
| **Overzicht gegevensset** |  Totaal aantal gegevenssets in alle werkruimten in uw capaciteiten<br>  Aantal keren dat DirectQuery/live-verbindingen 80% van de drempelwaarden overschreed gedurende de afgelopen zeven dagen, gesplitst in buckets van drie minuten<br>  Tijden waarop DirectQuery/live-verbindingen de 80% meestal overschreed gedurende de afgelopen zeven dagen, gesplitst in buckets van één uur<br>  Lokaal tijdstip waarop DirectQuery/live-verbindingen de 80% het vaakst in één uur heeft overschreden<br>  Totaal aantal vernieuwingen gedurende de afgelopen zeven dagen<br>  Gemiddelde wachttijd voor vernieuwen: de gemiddelde vertraging tussen de geplande tijd en het daadwerkelijke vernieuwen, in minuten<br>  Gemiddelde vernieuwingsduur: de tijd om het vernieuwen te voltooien, in minuten<br>  Totaal aantal uitgevoerde query's gedurende de afgelopen zeven dagen<br>  Gemiddelde querywachttijd: de tijd dat een query heeft gewacht op systeemresources alvorens aan de uitvoering te beginnen, in milliseconden<br>  Gemiddelde queryduur: de tijd om de query uit te voeren, in milliseconden<br>  Totaal aantal modellen dat wegens geheugendruk is verwijderd<br>  Gemiddelde grootte van gegevenssets <br>  Gemiddeld aantal gegevenssets dat in het geheugen is geladen |
| **Overzicht gegevensstroom** |  Totaal aantal gegevensstromen in alle werkruimten in uw capaciteiten<br>  Totaal aantal vernieuwingen gedurende de afgelopen zeven dagen<br>  Gemiddelde wachttijd voor vernieuwen: de gemiddelde vertraging tussen de geplande tijd en het daadwerkelijke vernieuwen, in minuten<br>  Gemiddelde vernieuwingsduur: de tijd om het vernieuwen te voltooien, in minuten |
| **Overzicht gepagineerde rapporten** |  Totaal aantal gepagineerde rapporten in alle werkruimten in uw capaciteiten<br>  Totaal aantal keren dat alle rapporten door gebruikers zijn bekeken<br>  Totaal aantal rijen gegevens in alle rapporten<br>  Totale tijd die nodig is voor alle fasen van alle rapporten (gegevens ophalen, verwerken en weergeven), in milliseconden |
|  |  |

### <a name="metrics-report"></a>Rapport voor metrische gegevens

Klik op het dashboard om naar het onderliggende rapport te gaan. Aan de onderkant van het rapport vindt u vijf tabsbladen:

* [**Gegevenssets**](#datasets): gedetailleerde metrische gegevens over de status van de Power BI-gegevenssets in de capaciteiten.

* [**Gepagineerde rapporten**](#paginated-reports): gedetailleerde metrische gegevens over de status van de gepagineerde rapporten in de capaciteiten.

* [**Gegevensstromen**](#dataflows): gedetailleerde metrische vernieuwingsgegevens voor gegevensstromen in de capaciteiten.

* [**Resourceverbruik**](#resource-consumption): metrische gegevens over de totale capaciteit, inclusief hoog geheugen- en CPU-verbruik.

* [**Id's en info**](#ids-and-info): namen, id's en eigenaren van capaciteiten, werkruimten en workloads.

U kunt op elk tabblad de metrische gegevens filteren op basis van capaciteit en datumbereik. Als u er geen filters zijn geselecteerd, worden in het rapport alleen de metrische gegevens van afgelopen week weergegeven voor alle capaciteiten waarvoor metrische gegevens worden gerapporteerd. 

#### <a name="datasets"></a>Gegevenssets

Gebruik de knoppen bovenaan het tabblad **Gegevenssets** om naar andere gedeelten te navigeren: **Vernieuwingen**, **Queryduur**, **Wachten op query** en **Gegevenssets**.

##### <a name="refreshes-area"></a>Vernieuwingengebied

Het **Vernieuwingengebied** bevat de volgende metrische gegevens.

| **Rapportsectie** | **Metrische gegevens** |
| --- | --- |
| **Betrouwbaarheid van vernieuwen** |  Totaal aantal: het totale aantal vernieuwingen voor elke gegevensset<br>  Betrouwbaarheid: het percentage vernieuwingen dat is voltooid voor elke gegevensset<br>  Gemiddelde wachttijd: de gemiddelde vertraging tussen de geplande tijd en het begin van een vernieuwing voor de gegevensset, in minuten<br>  Maximale wachttijd: de maximale wachttijd voor de gegevensset, in minuten <br>  Gemiddelde duur: de gemiddelde duur van een vernieuwing voor de gegevensset, in minuten<br>  Maximale duur: de duur van de langst lopende vernieuwing voor de gegevensset, in minuten |
| **Belangrijkste 5 gegevenssets op Gemiddelde vernieuwingsduur** |  De vijf gegevenssets met de langste gemiddelde vernieuwingsduur, in minuten |
| **Belangrijkste 5 gegevenssets op Gemiddelde wachttijd** |  De vijf gegevenssets met de langste gemiddelde wachttijd, in minuten |
| **Gemiddelde wachttijden voor vernieuwen per uur** |  De gemiddelde wachttijd voor vernieuwen, opgesplitst in buckets van één uur, vermeld in de lokale tijd. Meerdere pieken met een lange wachttijd duiden erop dat de limiet van de capaciteit wordt bereikt. |
| **Aantal vernieuwingen en geheugenverbruik per uur** |  Geslaagde en mislukte pogingen, en geheugenverbruik, opgesplitst in buckets van één uur, vermeld in de lokale tijd |
|  |  |

##### <a name="query-durations-area"></a>Het gebied Queryduur

Het gebied **Queryduur** bevat de volgende metrische gegevens.

| **Rapportsectie** | **Metrische gegevens** |
| --- | --- |
| **Queryduur** |  Gegevens in deze sectie zijn opgedeeld in gegevenssets, werkruimten en buckets van één uur, in de afgelopen zeven dagen<br>  Totaal: het totale aantal query's dat wordt uitgevoerd voor de gegevensset<br>  Gemiddeld: de gemiddelde queryduur voor de gegevensset, in milliseconden<br>  Maximaal: de duur van de langst lopende query in de gegevensset, in milliseconden|
| **Queryduurdistributie** |  Het histogram voor de queryduur wordt verzameld per queryduur (in milliseconden) in de volgende categorieën: intervallen van <= 30 ms, 30 - 100 ms, 100 - 300 ms, 300 ms - 1 sec, 1 sec - 3 sec, 3 sec - 10 sec, 10 sec - 30 sec en > 30 seconden. Een lange queryduur en lange wachttijden geven aan dat de capaciteit overbelast raakt. Het kan ook betekenen dat een enkele gegevensset problemen veroorzaakt en dat verder onderzoek nodig is. |
| **Belangrijkste 5 gegevenssets op Gemiddelde duur** |  De vijf gegevenssets met de langste gemiddelde queryduur, in minuten |
| **DirectQuery/liveverbindingen (gebruik > 80%)** |  Het aantal keren dat een DirectQuery of liveverbinding het CPU-gebruik van 80% heeft overschreden, opgesplitst in buckets van één uur, vermeld in de lokale tijd |
| **Queryduurdistributies per uur** |  Aantal query's en gemiddelde duur (in milliseconden) in vergelijking met het geheugenverbruik in GB, opgesplitst in buckets van één uur, vermeld in de lokale tijd |
|  |  |

##### <a name="query-waits-area"></a>Het gebied Querywachttijden

Het gebied **Querywachttijden** bevat de volgende metrische gegevens.

| **Rapportsectie** | **Metrische gegevens** |
| --- | --- |
| **Querywachttijden** |  Gegevens in deze sectie zijn opgedeeld in gegevenssets, werkruimten en buckets van één uur, in de afgelopen zeven dagen<br>  Totaal: het totale aantal query's dat wordt uitgevoerd voor de gegevensset<br>  Aantal in wachtrij: het aantal query's in de gegevensset dat, vóór uitvoering, moest wachten op systeemresources <br>  Gemiddeld: de gemiddelde querywachtduur voor de gegevensset, in milliseconden<br>  Maximaal: de duur van de langst wachtende query in de gegevensset, in milliseconden|
| **Wachttijddistributie** |  Het histogram voor de queryduur wordt verzameld per queryduur (in milliseconden) in de volgende categorieën: intervallen van <= 50 ms, 50 - 100 ms, 100 - 200 ms, 200 - 400 ms, 400 ms - 1 sec, 1 sec - 5 sec en  > 5 seconden |
| **Belangrijkste 5 gegevenssets op Gemiddelde wachttijd** |  De vijf gegevenssets met de langste gemiddelde wachttijd voor het uitvoeren van een query, in milliseconden |
| **Aantal wachtquery's en tijden per uur** |  Aantal wachtquery's en gemiddelde duur (in milliseconden) in vergelijking met het geheugenverbruik in GB, opgesplitst in buckets van één uur, vermeld in de lokale tijd |
|  |  |

##### <a name="datasets-area"></a>Het gebied gegevenssets

Het gebied **Gegevenssets** bevat de volgende metrische gegevens.

| **Rapportsectie** | **Metrische gegevens** |
| --- | --- |
| **Aantal verwijderingen van gegevenssets** |  Totaal: het totale aantal *verwijderingen* van gegevenssets voor elke capaciteit. Wanneer een capaciteit geheugendruk ervaart, worden via het knooppunt een of meer gegevenssets uit het geheugen verwijderd. Gegevenssets die niet actief zijn (waarvoor op dat moment geen query- of vernieuwingsbewerkingen worden uitgevoerd) worden het eerst verwijderd. Vervolgens wordt de volgorde van verwijderen gebaseerd op een meting van 'minst recentelijk gebruikt' (least recently used, LRU).|
| **Verwijderingen en geheugenverbruik van gegevenssets per uur** |  Verwijderingen van gegevenssets versus geheugenverbruik in GB, opgesplitst in buckets van één uur, vermeld in de lokale tijd |
| **Aantal gegevenssets dat per uur wordt geladen** |  Aantal gegevenssets dat in het geheugen wordt geladen versus geheugenverbruik in GB, opgesplitst in buckets van één uur, vermeld in de lokale tijd |
| **Percentages gebruikt geheugen** |  Totaal aantal actieve gegevenssets in het geheugen als percentage van het totale geheugen. Met het verschil tussen Actief en Alle wordt bepaald welke gegevenssets kunnen worden verwijderd. Per uur weergegeven, voor de afgelopen zeven dagen. |
| **Gegevensgrootten**  |  Maximale grootte: de maximale grootte van de gegevensset in MB voor de periode die wordt weergegeven |
|  |  |

#### <a name="paginated-reports"></a>Gepagineerde rapporten

Op het tabblad **Gepagineerde rapporten** worden gedetailleerde metrische gegevens weergegeven over de status van de gepagineerde rapporten in uw capaciteiten.

| **Rapportsectie** | **Metrische gegevens** |
| --- | --- |
| **Algemene gebruik** |  Totaal aantal weergaven: het aantal keer dat een rapport is bekeken door gebruikers<br>  Aantal rijen: het aantal rijen met gegevens in het rapport<br>  Ophalen (gemiddelde): de gemiddelde tijd die het kost om gegevens voor het rapport op te halen, in milliseconden. Als dit lang duurt, kan dit duiden op langzame query's of andere problemen met gegevensbronnen. <br>  Verwerken (gemiddelde): de gemiddelde tijd die het kost om gegevens voor een rapport te verwerken, in milliseconden<br> Weergeven (gemiddelde): de gemiddelde tijd die het kost om een rapport weer te geven in de browser, in milliseconden<br>  Totale tijd: de tijd die het kost om alle fasen van een rapport te doorlopen, in milliseconden|
| **Belangrijkste 5 rapporten op Gemiddelde tijd voor gegevens ophalen** |  De vijf rapporten met de langste gemiddelde tijd voor gegevens ophalen, in milliseconden |
| **Belangrijkste 5 rapporten op Gemiddelde verwerkingstijd voor rapport** |  De vijf rapporten met de langste gemiddelde verwerkingstijd voor het rapport, in milliseconden |
| **Duur per uur** |  Ophalen van gegevens versus de tijd voor verwerken en weergeven, gesplitst in buckets van één uur, vermeld in de lokale tijd |
| **Resultaten per uur** |  Geslaagde en mislukte pogingen, en geheugenverbruik, opgesplitst in buckets van één uur, vermeld in de lokale tijd |
|  |  |

#### <a name="dataflows"></a>Gegevensstromen

Op het tabblad **Gegevensstromen** worden gedetailleerde metrische gegevens weergegeven voor gegevensstromen in uw capaciteiten.

| **Rapportsectie** | **Metrische gegevens** |
| --- | --- |
| **Vernieuwen** |  Totaal: totaal aantal vernieuwingen voor elke gegevensstroom<br>  Betrouwbaarheid: het percentage vernieuwingen dat is voltooid voor elke gegevensstroom<br>  Gemiddelde wachttijd: de gemiddelde vertraging tussen de geplande tijd en het begin van een vernieuwing voor de gegevensstroom, in minuten<br>  Maximale wachttijd: de maximale wachttijd voor de gegevensstroom, in minuten <br>  Gemiddelde duur: de gemiddelde duur van een vernieuwing voor de gegevensstroom, in minuten<br>  Maximale duur: de duur van de langst lopende vernieuwing voor de gegevensstroom, in minuten |
| **Belangrijkste 5 gegevensstromen op Gemiddelde vernieuwingsduur** |  De vijf gegevensstromen met de langste gemiddelde vernieuwingsduur, in minuten |
| **Belangrijkste 5 gegevensstromen op Gemiddelde wachttijd** |  De vijf gegevensstromen met de langste gemiddelde wachttijd, in minuten |
| **Gemiddelde wachttijden voor vernieuwen per uur** |  De gemiddelde wachttijd voor vernieuwen, opgesplitst in buckets van één uur, vermeld in de lokale tijd. Meerdere pieken met een lange wachttijd duiden erop dat de limiet van de capaciteit wordt bereikt. |
| **Aantal vernieuwingen en geheugenverbruik per uur** |  Geslaagde en mislukte pogingen, en geheugenverbruik, opgesplitst in buckets van één uur, vermeld in de lokale tijd |
|  |  |

#### <a name="resource-consumption"></a>Resourceverbruik

Op het tabblad **Resourceverbruik** worden het CPU- en geheugenverbruik weergegeven van alle capaciteiten en workloads.

| **Rapportsectie** | **Metrische gegevens** |
| --- | --- |
| **CPU-verbruik** |  Gebruik per workload als een percentage van de totale CPU-capaciteit. Per uur weergegeven, voor de afgelopen zeven dagen. |
| **Geheugenverbruik** |  Geheugengebruik in GB per workload (ononderbroken lijnen) overlapt met de workloadlimieten (stippellijn). Per uur weergegeven, voor de afgelopen zeven dagen. |
|  |  |

#### <a name="ids-and-info"></a>Id's en info

Het tabblad **Id's en info** bevat de namen, id's en eigenaren van de capaciteiten, werkruimten en workloads.


## <a name="monitor-power-bi-embedded-capacity"></a>Power BI Embedded-capaciteit bewaken

U kunt de Power BI Premium Capacity Metrics-app gebruiken om *A SKU*-capaciteiten in Power BI Embedded te bewaken. Deze capaciteiten worden in het rapport weergegeven als u een beheerder van de capaciteit bent. U kunt het rapport echter niet vernieuwen, tenzij u bepaalde machtigingen verleent aan Power BI op uw A SKU's:

1. Open uw capaciteit in de Azure-portal.

1. Klik op **Toegangsbeheer (IAM)** en voeg de app Power BI Premium aan de lezersrol toe. Als u de app niet op naam kunt vinden, kunt u deze ook op client-id toevoegen: cb4dc29f-0bf4-402a-8b30-7511498ed654.

    ![Machtigingen voor Power BI Embedded](media/service-admin-premium-monitor-capacity/embedded-permissions.png)

> [!NOTE]
> U kunt capaciteitsgebruik van Power BI Embedded bewaken met de app of in de Azure-portal, maar niet in de Power BI-beheerportal.


## <a name="next-steps"></a>Volgende stappen

> [!div class="nextstepaction"]
> [Resourcebeheer en optimalisatie van Power BI Premium-capaciteit](service-premium-understand-how-it-works.md)
