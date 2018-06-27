---
title: Gebruik en optimalisatie van Power BI Premium-geheugencapaciteit
description: Informatie over beheer en optimalisatie van Power BI Premium-geheugencapaciteit.
ms.date: 04/30/2018
ms.topic: conceptual
ms.service: powerbi
ms.component: powerbi-admin
ms.author: susuresh
ms.reviewer: susuresh
author: suds001
manager: kfile
ms.openlocfilehash: 03c5e56c5f516bb1f09f51463d4c533185fbb63c
ms.sourcegitcommit: 2a7bbb1fa24a49d2278a90cb0c4be543d7267bda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/26/2018
ms.locfileid: "34298453"
---
# <a name="power-bi-premium-capacity-resource-management-and-optimization"></a>Resourcebeheer en optimalisatie van Power BI Premium-capaciteit

In dit artikel wordt beschreven hoe de Power BI Premium-service resources beheert en tips biedt voor het plannen en optimaliseren van uw oplossing.

## <a name="premium-capacity-memory-management"></a>Beheer van Premium-geheugencapaciteit

 Premium-geheugencapaciteit wordt verbruikt door:

* Geheugen dat wordt gebruikt door de geladen gegevenssets
* Geheugen dat wordt gebruikt door het vernieuwen van gegevenssets (gepland en op aanvraag)
* Geheugen dat wordt gebruikt door rapportquery's

Wanneer een aanvraag wordt gedaan op basis van een gepubliceerde gegevensset in uw capaciteit, wordt die gegevensset vanuit de permanente opslag (dit wordt ook wel 'image laden' genoemd) in het geheugen geladen. Door de gegevensset in het geheugen geladen te houden, kunnen toekomstige query’s op deze gegevensset snel worden uitgevoerd. Naast de hoeveelheid geheugen die nodig is om de gegevensset in het geheugen geladen te houden, verbruiken rapportquery's en het vernieuwen van gegevenssets ook extra geheugen.

### <a name="dataset-memory-estimation"></a>Geheugengebruik gegevensset schatten

Wanneer u probeert een gegevensset in het geheugen te laden, maakt Power BI een schatting van de hoeveelheid geheugen die de gegevensset nodig heeft om de aangevraagde opdracht te voltooien. Gegevenssets in het geheugen zijn meestal groter dan als ze zijn opgeslagen op schijf. Tijdens het vernieuwen van een gegevensset is minstens de dubbele hoeveelheid geheugen vereist dan wanneer een gegevensset niet actief is.

### <a name="overcommitting-capacity-eviction-and-reloading-of-datasets"></a>Te veel capaciteit toewijzen, gegevenssets verwijderen en opnieuw laden

Power BI Premium biedt u het voordeel te veel capaciteit te kunnen toewijzen. U kunt bijvoorbeeld meer gegevenssets publiceren dan de geheugencapaciteit kan bevatten. Als de gepubliceerde gegevenssets in uw capaciteit meer geheugen nodig hebben dan in de capaciteit past, wordt een aantal van de gegevenssets afzonderlijk opgeslagen in een permanente opslag. De permanente opslag maakt deel uit van 100 TB-opslag die is gekoppeld aan elk van uw capaciteiten.

Welke gegevenssets blijven dan in het geheugen en wat gebeurt er met de andere gegevenssets? Zoals eerder beschreven, wanneer een aanvraag wordt gedaan voor een gegevensset, wordt deze in het geheugen geladen (image laden). De aanvraag kan een rapportquery of vernieuwingsbewerking zijn.

Omdat u te veel capaciteit kunt toewijzen, kan uw capaciteit ook geheugendruk ervaren. Wanneer capaciteit te maken krijgt met geheugendruk bespreekt (omdat een nieuwe gegevensset moet worden geladen of de query's op sommige geladen gegevenssets het geheugenvereiste verhogen), *verwijdert het knooppunt een of meer gegevenssets* die de geheugencapaciteit in beslag nemen. Gegevenssets die inactief zijn (ofwel er wordt momenteel geen query of vernieuwingsbewerking op uitgevoerd) worden het eerst verwijderd en de volgorde van de verwijdering is 'minst recentelijk gebruikt'. Als nieuwe opdrachten worden verstrekt aan de verwijderde gegevensset, probeert de service deze opnieuw te laden in het geheugen, waarbij andere gegevenssets mogelijk worden verwijderd. Op deze manier wordt het gebruik efficiënter doordat de capaciteit veel meer gegevenssets kan afhandelen dan het geheugen kan bevatten.

Het laden van een gegevensset in het geheugen is vrij kostbaar. Afhankelijk van de grootte van de gegevensset kan dit van een paar seconden voor kleine gegevenssets tot tientallen seconden of zelfs minuten duren voor grote gegevenssets, zoals gegevenssets van 10 GB of meer. Premium-capaciteit probeert het aantal keren dat de capaciteit moet worden geladen te beperken door de minst recent gebruikte gegevenssets zo lang mogelijk in het geheugen te houden. Wanneer extra geheugen nodig is, moeten sommige gegevenssets worden verwijderd en wordt geprobeerd om de gegevenssets te kiezen die de minste impact op de gebruikerservaring hebben. Wanneer extra geheugen nodig is, moeten sommige gegevenssets worden verwijderd en wordt geprobeerd om de gegevenssets te kiezen die de minste impact op de gebruikerservaring hebben. Het systeem vermijdt bijvoorbeeld gegevenssets te verwijderen die de laatste paar minuten actief zijn gebruikt, omdat ze mogelijk zeer snel opnieuw worden opgevraagd.

Het verwijderen zelf verloopt snel. Als de gegevensset niet actief wordt gebruikt op het moment van verwijderen, merkt de gebruiker nauwelijks iets van de verwijdering. Als er echter te veel gegevenssets tegelijkertijd actief worden gebruikt en er onvoldoende geheugen is om ze allemaal geladen te hebben, kan een groot aantal verwijderingen optreden. Dit kan leiden tot een 'thrashingsituatie', waarbij gegevenssets voortdurend worden verwijderd en opnieuw worden geladen, en waarbij gebruikers een merkbare afname in reactietijden en prestaties kunnen zien.

### <a name="dataset-refresh-memory-requirement-competing-with-an-active-dataset-memory-requirement"></a>Geheugenvereiste voor vernieuwen gegevensset concurreert met geheugenvereiste voor een actieve gegevensset

Gegevenssets kunnen worden vernieuwd volgen een planning of op aanvraag door gebruikers. Zoals eerder beschreven, is het vereiste geheugen voor volledige vernieuwingen ten minste tweemaal de geheugengrootte van de geladen en niet-actieve gegevenssets. Voordat het vernieuwen wordt gestart, wordt een geheugenvereiste voor het vernieuwen geschat. Als het totale vereiste geheugen groter is dan het beschikbare geheugen in de capaciteit, worden sommige gegevenssets verwijderd. Kandidaten voor verwijdering zijn geselecteerd in de volgorde van minst recent gebruikte gegevenssets. Dit wil zeggen dat de service zoveel mogelijk recent gebruikte gegevenssets in het geheugen probeert te houden.

Als het vereiste geheugen ondanks verwijdering niet beschikbaar is, wordt de vernieuwing in de wachtrij geplaatst voor een nieuwe poging later. De service blijft pogingen doen tot het is gelukt of een nieuwe vernieuwingsactie begint.

Als een interactieve query wordt uitgevoerd op een gegevensset in de capaciteit en er onvoldoende geheugen beschikbaar is vanwege een lopende vernieuwing is, mislukt deze aanvraag en moet deze opnieuw worden geprobeerd door de gebruiker.

## <a name="cpu-resource-management-in-premium-capacity"></a>CPU-bronbeheer in premium-capaciteit

Er zijn twee primaire verbruikers van CPU-bronnen:

- Query's van rapporten
- Vernieuwen (verwerking)

### <a name="queries-from-reports"></a>Query's van rapporten

Rapportquery's verbruiken CPU-bronnen van uw capaciteit. Als uw rapport enkele query's bevat die inefficiënt zijn of als er veel gelijktijdige gebruikers zijn, verbruikt dit veel CPU-bronnen en is uw bestaande capaciteit mogelijk niet voldoende om de belasting te verwerken.

### <a name="refresh-parallelization-policy"></a>Beleid voor parallel vernieuwen

Geheugen is niet de enige bron die het vernieuwen van gegevenssets kan beperken. Het aantal v-cores op een server kan ook een factor zijn. Omdat elke vernieuwingsbewerking een bepaald aantal v-cores vereist, is er een limiet voor het aantal vernieuwingen dat parallel kan worden uitgevoerd. De limiet per SKU wordt vermeld in de volgende tabel. Aanvullende vernieuwingen die verdergaan dan deze limiet worden in de wachtrij geplaatst.

 | SKU  | Back-end-v-cores  | Model voor parallelle vernieuwing   |
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

Hieronder worden enkele algemene scenario's beschreven en de acties die door de service worden genomen:

 **Er worden twintig vernieuwingen allemaal op hetzelfde moment verzonden**: Power BI probeert de eerste *x* vernieuwingen op hetzelfde moment te starten. De waarde voor *x* wordt bepaald door het beleid voor parallel vernieuwen voor deze SKU. Als Power BI niet voldoende geheugen kan verkrijgen door inactieve gegevenssets (gegevenssets die niet recent zijn gebruikt) te verwijderen, starten niet alle *x* vernieuwingen op hetzelfde moment. Vernieuwingen die niet kunnen worden gestart, worden in de wachtrij geplaatst totdat deze kunnen worden gestart.

 **Er worden twee vernieuwingen tegelijkertijd uitgevoerd en er is alleen voldoende geheugen om er één te voltooien**: de vernieuwing die kan worden voltooid, wordt gestart. De andere wordt later opnieuw geprobeerd.

 **Op een groot aantal gegevenssets wordt een query uitgevoerd terwijl verschillende gegevenssets worden vernieuwd**: als er onvoldoende geheugen beschikbaar is, probeert Power BI om actieve vernieuwingen te stoppen om prioriteit te geven aan interactieve query's. Hierdoor nemen de prestaties voor vernieuwingsbewerkingen af.

 **Gegevensset vereist te veel geheugen om te worden vernieuwd met de huidige capaciteitsgrootte**: het vernieuwen mislukt. Er wordt niet geprobeerd meer geheugen op te halen door middel van verwijdering.

 **Er wordt één gegevensset vernieuwd met een grote piek in het geheugen**: als de piek groter is dan de hoeveelheid geheugen die kan worden verkregen door inactieve gegevenssets te verwijderen, wordt de vernieuwingsbewerking later opnieuw geprobeerd totdat er voldoende geheugen is om de piek af te handelen.

 **Query wordt uitgevoerd voor een gegevensset die niet voldoende geheugen kan verkrijgen door alle inactieve gegevenssets en vernieuwingen te verwijderen**: deze query's mislukken. Voor dit soort workloadvereisten moet hogere capaciteit worden aangeschaft.

## <a name="troubleshooting-and-testing"></a>Probleemoplossing en testen

Als rapporten traag zijn of niet reageren, begint u met testen voor slechts één gebruiker in uw rapport. Verhoog vervolgens de belasting van het gelijktijdig aantal gebruikers om de limiet te vinden. In veel gevallen kan het afstemmen van uw DAX (rapportquery's) de prestaties van uw rapporten drastisch wijzigen (en het aantal gelijktijdige gebruikers dat wordt ondersteund door uw capaciteit verhogen).

Gebruik Power BI Embedded-capaciteit in Azure om verschillende SKU's te testen en de beste Premium-SKU voor uw verwachte workload te bepalen. De Power BI Embedded A4-SKU is gelijk aan de P1, A5 = P2 en A6 = P3. In Azure kunt u eenvoudig schakelen tussen SKU's door de schaal te vergroten en te verkleinen in Azure Portal. Wanneer u de SKU hebt gevonden die het beste werkt voor uw workload en klaar bent met testen, kunt u de SKU verwijderen.

In sommige gevallen kan het openen van een PBIX-bestand van het model op uw computer en het controleren van geheugen- en CPU-verbruik veel over het probleem vertellen. Dit helpt niet voor zeer grote modellen, maar voor sommige kleinere modellen kunt u proberen om het model te openen, te vernieuwen en er een query op uit te voeren vanaf uw computer. Controleer de modelgrootte, het geheugen- en CPU-verbruik wanneer u het model opent. Probeer te vernieuwen en een query uit te voeren. Gebruik Taakbeheer om het CPU- en geheugenverbruik te controleren voor het lokale PBIX-bestand. Soms blijkt uit deze metrische gegevens op uw computer dat een lagere Premium-capaciteit, zoals P1/P2, niet werkt voor uw oplossing.
