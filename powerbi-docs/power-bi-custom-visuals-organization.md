---
title: Aangepaste visuals voor organisaties gebruiken in Power BI
description: Gebruik, beheer en maak aangepaste visuals voor organisaties in Power BI
services: powerbi
documentationcenter: 
author: markingmyname
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
ms.date: 02/06/2018
ms.author: maghan
LocalizationGroup: Visualizations
ms.openlocfilehash: 6f7827f7804fcd52e7d922ebc8ffad5a8036b33c
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/24/2018
---
# <a name="using-organization-custom-visuals-in-power-bi-preview"></a>Aangepaste visuals voor organisaties gebruiken in Power BI (preview)

U kunt aangepaste visuals gebruiken in Power BI om een uniek soort visual te maken die op u is aangepast, of op de gegevensinzichten die u naar voren wilt brengen. Deze aangepaste visuals worden vaak door ontwikkelaars gemaakt, wanneer het grote aantal visuals in Power BI niet helemaal aan de behoefte voldoet. 

In sommige organisaties zijn aangepaste visuals nog belangrijker. Ze kunnen nodig zijn om bepaalde gegevens of inzichten die uniek zijn voor de organisatie naar voren te brengen, hebben misschien speciale vereisten voor gegevens of kunnen unieke methoden van het bedrijf onderstrepen. Zulke organisaties moeten aangepaste visuals ontwikkelen, die in de hele organisatie delen en ervoor zorgen dat ze goed worden onderhouden. Met aangepaste visuals van Power BI (nu als preview-versie beschikbaar) kunnen organisaties precies dat doen. 

De volgende afbeelding toont het proces waardoor aangepaste visuals voor organisaties (preview) in Power BI vanaf de beheerder, via ontwikkeling en onderhoud, ten slotte allemaal bij de gegevensanalist aankomen.

![](media/power-bi-custom-visuals-organizational/custom-visual-org-01.jpg)

## <a name="how-to-enable-organizational-custom-visuals-preview"></a>Aangepaste visuals voor organisaties inschakelen (preview)

Aangepaste visuals voor organisaties zijn momenteel beschikbaar in de preview-versie. Daarom moet u de functie inschakelen in Power BI Desktop. Als u deze preview-functie wilt inschakelen, selecteert u Bestand > Opties en instellingen > Opties op het lint. Vervolgens selecteert u Preview-functies in het deelvenster aan de linkerkant en daarna vinkt u het selectievakje aan naast Aangepaste visuele elementen van mijn organisatie, zoals dat in de volgende afbeelding wordt weergegeven.

![](media/power-bi-custom-visuals-organizational/custom-visual-org-02.jpg)

Visuals voor organisaties worden door de Power BI-beheerder geïmplementeerd en beheerd vanuit de beheerportal. Zodra de visuals in de opslagplaats van de organisatie zijn geïmplementeerd, kunnen gebruikers in de organisatie de visuals eenvoudig vinden en de aangepaste visuals voor organisaties direct vanuit Power BI Desktop in hun rapporten importeren.

## <a name="using-organizational-custom-visuals"></a>Aangepaste visuals voor organisaties gebruiken

Raadpleeg [dit artikel](power-bi-custom-visuals.md) voor meer informatie over het gebruik van aangepaste visuals voor organisaties in rapporten die u hebt gemaakt.
 
## <a name="administering-organizational-custom-visuals"></a>Aangepaste visuals voor organisaties beheren

Raadpleeg [dit artikel](https://go.microsoft.com/fwlink/?linkid=866790) voor meer informatie over het beheren en implementeren van aangepaste visuals voor organisaties.

> [!WARNING]
> Een aangepaste visual kan code bevatten met beveiligings- of privacyrisico's. Ga na of u de auteur en de bron van een aangepaste visual vertrouwt voordat u deze implementeert in de opslagplaats van de organisatie. 
> 

## <a name="considerations-and-limitations"></a>Overwegingen en beperkingen
 
Aangezien aangepaste visuals voor organisaties beschikbaar is in de preview-versie, zijn er verschillende overwegingen en beperkingen waarvan u zich bewust moet zijn en waar u rekening mee moet houden.
 
Beheerder:

* Verouderde aangepaste visuals (zoals aangepaste visuals die niet op de nieuwe API-versies zijn gebouwd) worden niet ondersteund

* In-place updates worden nog niet ondersteund. U moet een nieuwe versie van de visual in de opslagplaats van de organisatie uploaden om een visual bij te werken (zorg er ook voor dat deze dezelfde visual-id heeft als in het PBIVIZ-bestand). Auteurs van rapporten kunnen de nieuwe versie dan in hun rapport importeren en hun huidige versie van de visual ter plaatse in het rapport vervagen.

* Als een aangepaste visual uit de opslagplaats wordt verwijderd, zullen de bestanden die de verwijderde visual gebruiken, de rendering stoppen. De verwijderingsbewerking vanuit de opslagplaats is niet omkeerbaar.
 
Eindgebruiker:

* Het gebruik van dezelfde visual (met dezelfde visual-id) uit de openbare marketplace (AppSource) en uit de opslagplaats van de organisatie wordt niet ondersteund. In dat geval wordt de laatst geïmporteerde visual gebruikt.

* Het extern delen van visuals voor organisaties in dashboards en rapporten wordt niet ondersteund. Gebruikers van buiten de organisatie die een dashboard met een aangepaste visual voor organisaties bekijken, zullen een blanco visual te zien krijgen. 

* Power BI-werkruimteverzameling wordt niet ondersteund voor visuals voor organisaties.

* Aangepaste visuals voor organisaties in rapporten die niet online zijn gepubliceerd, zullen niet worden weergegeven.

* De Visio-visual, PowerApps-visual en de GlobeMap-visual uit de AppSource-marketplace worden niet weergegeven als ze worden geïmplementeerd via de opslagplaats van de organisatie.

* Als de beheerder een aangepaste visual verwijdert uit de opslagplaats en die visual wordt gebruikt in een rapport, dan zal de visual niet meer worden weergegeven en moet die uit het rapport worden verwijderd, zodat het rapport kan worden opgeslagen.