---
title: Aangepaste visuals voor organisaties gebruiken in Power BI
description: Gebruik, beheer en maak aangepaste visuals voor organisaties in Power BI
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 02/06/2018
ms.author: maghan
LocalizationGroup: Visualizations
ms.openlocfilehash: bc4dcc26ac2007e482b396139d572018c8a3acd3
ms.sourcegitcommit: 638de55f996d177063561b36d95c8c71ea7af3ed
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/17/2018
ms.locfileid: "34291898"
---
# <a name="using-organization-custom-visuals-in-power-bi"></a>Aangepaste visuals voor organisaties gebruiken in Power BI

U kunt aangepaste visuals gebruiken in Power BI om een uniek soort visual te maken die op u is aangepast, of op de gegevensinzichten die u naar voren wilt brengen. Deze aangepaste visuals worden vaak door ontwikkelaars gemaakt, wanneer het grote aantal visuals in Power BI niet helemaal aan de behoefte voldoet. 

In sommige organisaties zijn aangepaste visuals nog belangrijker. Ze kunnen nodig zijn om bepaalde gegevens of inzichten die uniek zijn voor de organisatie naar voren te brengen, hebben misschien speciale vereisten voor gegevens of kunnen unieke methoden van het bedrijf onderstrepen. Zulke organisaties moeten aangepaste visuals ontwikkelen, die in de hele organisatie delen en ervoor zorgen dat ze goed worden onderhouden. Met aangepaste visuals van Power BI kunnen organisaties precies dat doen.

De volgende afbeelding toont via welk proces aangepaste visuals voor organisaties in Power BI vanaf de beheerder, via ontwikkeling en onderhoud, ten slotte allemaal bij de gegevensanalist aankomen.

![](media/power-bi-custom-visuals-organizational/custom-visual-org-01.jpg)

Visuals voor organisaties worden door de Power BI-beheerder geïmplementeerd en beheerd vanuit de beheerportal. Zodra de visuals in de opslagplaats van de organisatie zijn geïmplementeerd, kunnen gebruikers in de organisatie de visuals eenvoudig vinden en de aangepaste visuals voor organisaties direct vanuit Power BI Desktop in hun rapporten importeren.

## <a name="using-organizational-custom-visuals"></a>Aangepaste visuals voor organisaties gebruiken

Raadpleeg [dit artikel](power-bi-custom-visuals.md) voor meer informatie over het gebruik van aangepaste visuals voor organisaties in rapporten die u hebt gemaakt.
 
## <a name="administering-organizational-custom-visuals"></a>Aangepaste visuals voor organisaties beheren

Raadpleeg [dit artikel](https://go.microsoft.com/fwlink/?linkid=866790) voor meer informatie over het beheren en implementeren van aangepaste visuals voor organisaties.

> [!WARNING]
> Een aangepaste visual kan code bevatten met beveiligings- of privacyrisico's. Ga na of u de auteur en de bron van een aangepaste visual vertrouwt voordat u deze implementeert in de opslagplaats van de organisatie. 
> 

## <a name="considerations-and-limitations"></a>Overwegingen en beperkingen
 
Er zijn enkele overwegingen en beperkingen waarmee u rekening moet houden.
 
Beheerder:

* Verouderde aangepaste visuals (zoals aangepaste visuals die niet op de nieuwe API-versies zijn gebouwd) worden niet ondersteund

* Als een aangepaste visual uit de opslagplaats wordt verwijderd, zullen de bestanden die de verwijderde visual gebruiken, de rendering stoppen. De verwijderingsbewerking vanuit de opslagplaats is niet omkeerbaar. Als u een aangepast visueel element tijdelijk moet uitschakelen, gebruikt u de functie ‘Uitschakelen’.
 
Eindgebruiker:

* Power BI-werkruimteverzameling wordt niet ondersteund voor visuals voor organisaties.

* De Visio-visual, PowerApps-visual en de GlobeMap-visual uit de AppSource-marketplace worden niet weergegeven als ze worden geïmplementeerd via de opslagplaats van de organisatie.
