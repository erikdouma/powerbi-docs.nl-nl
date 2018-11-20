---
title: Gebruik en optimalisatie van Power BI Premium-geheugencapaciteit
description: Informatie over beheer en optimalisatie van Power BI Premium-geheugencapaciteit.
ms.date: 10/18/2018
ms.topic: conceptual
ms.service: powerbi
ms.component: powerbi-admin
ms.author: mblythe
ms.reviewer: mblythe
author: mgblythe
manager: kfile
ms.openlocfilehash: 534c06c66d561a04dbffc04412095d6924c92781
ms.sourcegitcommit: b23fdcc0ceff5acd2e4d52b15b310068236cf8c7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/07/2018
ms.locfileid: "51266065"
---
# <a name="microsoft-power-bi-premium-capacity-resource-management-and-optimization"></a>Resourcebeheer en optimalisatie van Microsoft Power BI Premium-capaciteit

In dit artikel wordt beschreven hoe resources worden beheerd door Power BI Premium. Dit artikel bevat ook voorbeelden en suggesties voor probleemoplossing. Zie [Wat is Power BI Premium?](service-premium.md) voor een overzicht.

## <a name="premium-capacity-memory-management"></a>Beheer van Premium-geheugencapaciteit

 Premium-geheugencapaciteit wordt verbruikt door:

* De gegevenssets die in het geheugen worden geladen
* Het vernieuwen van gegevenssets (zowel gepland als op aanvraag)
* Workloads die worden ondersteund voor de capaciteit
* Rapportquery's

Wanneer een aanvraag wordt gedaan op basis van een gepubliceerde gegevensset in uw capaciteit, wordt die gegevensset vanuit de permanente opslag (dit wordt ook wel 'image laden' genoemd) in het geheugen geladen. Door de gegevensset in het geheugen geladen te houden, kunnen toekomstige query’s op deze gegevensset snel worden uitgevoerd. Naast de hoeveelheid geheugen die nodig is om de gegevensset in het geheugen geladen te houden, verbruiken rapportquery's en het vernieuwen van gegevenssets extra geheugen.

### <a name="dataset-memory-estimation"></a>Geheugengebruik gegevensset schatten

Wanneer u probeert een gegevensset in het geheugen te laden, maakt Power BI een schatting van de hoeveelheid geheugen die de gegevensset nodig heeft om de aangevraagde opdracht te voltooien. Gegevenssets in het geheugen zijn meestal groter dan wanneer ze zijn opgeslagen op schijf. Tijdens het vernieuwen van een gegevensset vereist Power BI minstens de dubbele hoeveelheid geheugen ten opzichte van wanneer de gegevensset niet actief is.

### <a name="overcommitting-capacity-eviction-and-reloading-of-datasets"></a>Te veel capaciteit toewijzen, gegevenssets verwijderen en opnieuw laden

Power BI Premium biedt het voordeel dat u *te veel* capaciteit kunt toewijzen. U kunt bijvoorbeeld meer gegevenssets publiceren dan uw capaciteit kan bevatten. Als de gepubliceerde gegevenssets meer geheugen nodig hebben dan beschikbaar is in de capaciteit, wordt een aantal van de gegevenssets afzonderlijk opgeslagen in permanente opslag. De permanente opslag maakt deel uit van de 100 TB aan opslag die is gekoppeld aan elk van uw capaciteiten.

Welke gegevenssets blijven dan in het geheugen en wat gebeurt er met de andere gegevenssets? Zoals eerder beschreven, wanneer een aanvraag wordt gedaan voor een gegevensset, wordt deze in het geheugen geladen (image laden). De aanvraag kan een rapportquery of vernieuwingsbewerking zijn. Omdat u echter te veel capaciteit kunt toewijzen, kan de capaciteit ook geheugendruk ervaren. Wanneer een capaciteit geheugendruk ervaart, *verwijdert* het knooppunt een of meer gegevenssets uit het geheugen. Gegevenssets die niet actief zijn (waarvoor op dat moment geen query- of vernieuwingsbewerkingen worden uitgevoerd) worden het eerst verwijderd. Vervolgens wordt de volgorde van verwijderen gebaseerd op een meting van 'minst recentelijk gebruikt' (least recently used, LRU). Als er nieuwe opdrachten worden verstrekt aan de verwijderde gegevensset, probeert de service de gegevensset opnieuw te laden in het geheugen, waarbij andere gegevenssets mogelijk worden verwijderd. Op deze manier wordt het gebruik efficiënter doordat de capaciteit veel meer gegevenssets kan afhandelen dan het geheugen kan bevatten.

Het laden van een gegevensset in het geheugen is vrij kostbaar. Afhankelijk van de grootte van de gegevensset kan dit van een paar seconden voor kleine gegevenssets tot tientallen seconden of zelfs minuten duren voor gegevenssets van aanzienlijke grootte, zoals gegevenssets van ongeveer 10 GB of meer. Premium-capaciteit probeert het aantal keren dat de capaciteit moet worden geladen te beperken door de minst recent gebruikte gegevenssets zo lang mogelijk in het geheugen te houden. Wanneer extra geheugen nodig is, moeten sommige gegevenssets worden verwijderd en wordt geprobeerd om de gegevenssets te kiezen die de minste impact op de gebruikerservaring hebben. Wanneer extra geheugen nodig is, moeten sommige gegevenssets worden verwijderd en wordt geprobeerd om de gegevenssets te kiezen die de minste impact op de gebruikerservaring hebben. Het systeem probeert bijvoorbeeld te voorkomen dat er gegevenssets worden verwijderd die de laatste paar minuten actief zijn gebruikt. De kans is namelijk groot dat er snel opnieuw query’s worden uitgevoerd op deze gegevenssets.

Het verwijderen zelf verloopt snel. Als de gegevensset niet actief wordt gebruikt op het moment van verwijderen, merkt de gebruiker nauwelijks iets van de verwijdering. Als er echter te veel gegevenssets tegelijkertijd actief worden gebruikt en er onvoldoende geheugen is om ze allemaal te bevatten, kunnen er veel verwijderingen plaatsvinden. De aanwezigheid van te veel actieve gegevenssets kan leiden tot een 'thrashing’-situatie. Hierbij worden gegevenssets voortdurend verwijderd en opnieuw geladen, en kunnen gebruikers een merkbare afname in reactietijden en prestaties ervaren.

### <a name="dataset-refresh-memory-requirement-competing-with-an-active-dataset-memory-requirement"></a>Geheugenvereiste voor vernieuwen gegevensset concurreert met geheugenvereiste voor een actieve gegevensset

Gegevenssets kunnen worden vernieuwd volgen een planning of op aanvraag door gebruikers. Zoals eerder beschreven, is het vereiste geheugen voor volledige vernieuwingen ten minste tweemaal de geheugengrootte van de geladen en niet-actieve gegevenssets. Voordat het vernieuwen wordt gestart, wordt een geheugenvereiste voor het vernieuwen geschat. Als het totale vereiste geheugen groter is dan het beschikbare geheugen in de capaciteit, worden sommige gegevenssets verwijderd. De verwijdering vindt weer plaats op basis van LRU.

Als het vereiste geheugen ondanks verwijdering niet beschikbaar is, wordt de vernieuwing in de wachtrij geplaatst voor een nieuwe poging later. De service blijft pogingen doen tot het is gelukt of een nieuwe vernieuwingsactie begint.

Als een interactieve query wordt uitgevoerd op een gegevensset in de capaciteit en er onvoldoende geheugen beschikbaar is vanwege een lopende vernieuwing is, mislukt deze aanvraag en moet deze opnieuw worden geprobeerd door de gebruiker.

### <a name="workloads"></a>Workloads

De standaardconfiguratie is dat capaciteiten voor  **Power BI Premium** en **Power BI Embedded** alleen de workload ondersteunen die is gekoppeld aan het uitvoeren van Power BI-query's in de cloud. We bieden nu preview-ondersteuning voor twee extra workloads: **Gepagineerde rapporten** en **Gegevensstromen**. Indien ingeschakeld kunnen deze workloads het geheugengebruik in de capaciteit beïnvloeden. Zie [Workloads configureren](service-admin-premium-manage.md#configure-workloads) voor meer informatie.

## <a name="cpu-resource-management-in-premium-capacity"></a>CPU-bronbeheer in premium-capaciteit

Er zijn twee primaire verbruikers van CPU-bronnen:

* Query's van rapporten
* Vernieuwen (verwerking)

### <a name="queries-from-reports"></a>Query's van rapporten

Rapportquery's verbruiken CPU-resources in uw capaciteit. Rapporten met inefficiënte query's of veel gelijktijdige gebruikers kunnen veel CPU-resources verbruiken. Uw bestaande capaciteit is mogelijk niet voldoende om de lading te verwerken.

### <a name="refresh-parallelization-policy"></a>Beleid voor parallel vernieuwen

Geheugen is niet de enige resource die het vernieuwen van gegevenssets kan beperken. Het aantal v-cores op een server kan ook een factor zijn. Omdat voor elke vernieuwingsbewerking een bepaald aantal v-cores is vereist, is er een limiet voor het aantal vernieuwingen die parallel kunnen worden uitgevoerd. De limiet per SKU wordt vermeld in de volgende tabel. Aanvullende vernieuwingen die buiten deze limiet vallen, worden in de wachtrij geplaatst.

 | SKU | Back-end-v-cores | Model voor parallelle vernieuwing |
 | --- | --- | --- |
 | A1  | 0,5  | 1  |
 | A2  | 1  | 2  |
 | A3  | 2  | 3  |
 | A4  | 4  | 6  |
 | A5  | 8  | 12  |
 | A6  | 16  | 24  |
 | EM1  | 0,5  | 1  |
 | EM2  | 1  | 2  |
 | EM3  | 2  | 3  |
 | P1  | 4  | 6  |
 | P2  | 8  | 12  |
 | P3  | 16  | 24  |
 | P4  | 32  | 48  |
 | P5  | 64  | 96  |

 > [!TIP]
> Als uw vernieuwingen vertraging ondervinden, controleert u het aantal parallelle vernieuwingen dat door uw capaciteit wordt ondersteund.

## <a name="example-scenarios"></a>Voorbeeldscenario's

Hier volgen enkele algemene scenario's en de acties die door de service worden ondernomen:

**Twintig geplande vernieuwingen die allemaal tegelijk zijn ingediend**. Power BI probeert tegelijkertijd te beginnen met de eerste *x* vernieuwingen. De waarde voor *x* wordt bepaald door het beleid voor parallel vernieuwen voor deze SKU. Als Power BI niet voldoende geheugen kan verkrijgen door inactieve gegevenssets (gegevenssets die niet recent zijn gebruikt) te verwijderen, starten niet alle *x* vernieuwingen op hetzelfde moment. Vernieuwingen die niet kunnen worden gestart, worden in de wachtrij geplaatst totdat deze kunnen worden gestart.

**Er worden twee vernieuwingen tegelijkertijd uitgevoerd en er is alleen voldoende geheugen om er één te voltooien**. De vernieuwing die kan worden voltooid, wordt gestart. De andere wordt later opnieuw geprobeerd.

**Er worden query’s uitgevoerd op een groot aantal gegevenssets terwijl er meerdere gegevenssets worden vernieuwd**. Als er onvoldoende geheugen beschikbaar is, probeert Power BI actieve vernieuwingen te stoppen om prioriteit te geven aan interactieve query's. Hierdoor nemen de prestaties voor vernieuwingsbewerkingen af.

**De gegevensset vereist te veel geheugen om te worden vernieuwd met de huidige capaciteitsgrootte**. Het vernieuwen mislukt. Er wordt niet geprobeerd meer geheugen op te halen door middel van verwijdering.

**Er wordt één gegevensset vernieuwd met een grote piek in het geheugen**. Als de piek groter is dan de hoeveelheid geheugen die kan worden verkregen door inactieve gegevenssets te verwijderen, wordt de vernieuwingsbewerking later opnieuw geprobeerd totdat er voldoende geheugen is om de piek af te handelen.

**Er wordt een query uitgevoerd voor een gegevensset waarvoor niet voldoende geheugen kan worden verkregen door verwijdering van alle inactieve gegevenssets en vernieuwingen**. Deze query's mislukken. Voor dit soort workloadvereisten moet hogere capaciteit worden aangeschaft.

## <a name="troubleshooting-and-testing"></a>Probleemoplossing en testen

Als rapporten traag zijn of niet reageren, begint u met testen voor slechts één gebruiker in uw rapport. Verhoog vervolgens de belasting van het gelijktijdig aantal gebruikers om de limiet te vinden. In veel gevallen kunt u de prestaties van uw rapporten aanzienlijk verbeteren door uw DAX-query’s af te stemmen. Met de queryafstemming vergroot u ook het aantal gelijktijdige gebruikers dat door uw capaciteit wordt ondersteund. [Controleer uw capaciteit](service-admin-premium-monitor-capacity.md) om mogelijke prestatieproblemen te identificeren.

Gebruik Power BI Embedded-capaciteit in Azure om verschillende SKU's te testen en de beste Premium-SKU voor uw verwachte workload te bepalen. De Power BI Embedded A4-SKU is gelijk aan de P1, A5 = P2 en A6 = P3. In Azure kunt u eenvoudig schakelen tussen SKU's door de schaal te vergroten en te verkleinen in Azure Portal. Wanneer u de SKU hebt gevonden die het beste werkt voor uw workload en klaar bent met testen, kunt u de SKU verwijderen.

In sommige gevallen kan het openen van een PBIX-bestand (Power BI Desktop) van het model op uw computer en het controleren van het geheugen- en CPU-verbruik veel over het probleem aangeven. Dit helpt niet voor zeer grote modellen, maar voor sommige kleinere modellen kunt u proberen om het model te openen, te vernieuwen en er een query op uit te voeren vanaf uw computer. Controleer de modelgrootte, het geheugen- en CPU-verbruik wanneer u het model opent. Probeer te vernieuwen en een query uit te voeren. Gebruik Taakbeheer om het CPU- en geheugenverbruik te controleren voor het lokale bestand. Soms blijkt uit deze metrische gegevens op uw computer dat een lagere Premium-capaciteit, zoals P1/P2, niet werkt voor uw oplossing.

## <a name="next-steps"></a>Volgende stappen

[Capaciteiten in Power BI Premium en Power BI Embedded beheren](service-admin-premium-manage.md)