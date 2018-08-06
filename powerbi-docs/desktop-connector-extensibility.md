---
title: Uitbreidbaarheid van connectors in Power BI
description: Uitbreidingsmogelijkheden voor connectors, kenmerken, beveiligingsinstellingen en gecertificeerde connectors
author: cpopell
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 07/25/2018
ms.author: gepopell
LocalizationGroup: Connect to data
ms.openlocfilehash: c63357df043ff6a646562d398a07d8042dd5a0ee
ms.sourcegitcommit: 7fb0b68203877ff01f29724f0d1761d023075445
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/26/2018
ms.locfileid: "39256548"
---
# <a name="connector-extensibility-in-power-bi"></a>Uitbreidbaarheid van connectors in Power BI

In Power BI kunnen klanten en ontwikkelaars de gegevensbronnen waarmee ze verbinding maken op tal van manieren uitbreiden, door bijvoorbeeld bestaande connectors en algemene gegevensbronnen te gebruiken (zoals ODBC, OData, Oledb, Web, CSV, XML en JSON). Hiernaast kunnen ontwikkelaars ook gegevensextensies maken (ook wel **aangepaste connectors** genoemd) en connectors certificeren zodat het **gecertificeerde connectors** worden.

In eerdere versies van Power BI werd de mogelijkheid om **aangepaste connectors** te gebruiken ingeschakeld met een functieschakelaar. Er is nu een menu waarmee u veilig kunt bepalen welk niveau aan aangepaste code u wilt kunnen laten uitvoeren in uw systeem: alle aangepaste connectors of alleen connectors die zijn gecertificeerd en die door Microsoft worden gedistribueerd via het dialoogvenster **Gegevens ophalen**.

## <a name="custom-connectors"></a>Aangepaste connectors

**Aangepaste connectors** kunnen vele verschillende zaken omvatten, van kleine API's die van groot belang zijn voor uw bedrijf tot grote, branchespecifieke services die Microsoft niet heeft geïmplementeerd. De meeste van deze connectors worden door de leverancier zelf gedistribueerd. Als u een specifieke gegevensconnector nodig hebt, moet u contact opnemen met een leverancier.

Als u een **aangepaste connector** wilt gebruiken, plaatst u deze in de map *\[Documenten\\Power BI Desktop\\Aangepaste connectors*. Pas de beveiligingsinstellingen aan zoals wordt beschreven in het volgende gedeelte.

U hoeft de beveiligingsinstellingen niet aan te passen als u **gecertificeerde connectors** wilt gebruiken.

## <a name="data-extension-security"></a>Beveiliging van gegevensextensies

Als u de beveiligingsinstellingen van een gegevensextensie wilt wijzigen, gaat u naar **Power BI Desktop** en selecteert u **Bestand > Opties en instellingen > Opties > Beveiliging**.

![Bepalen of u aangepaste connectors wilt kunnen laden met de beveiligingsopties voor gegevensextensies](media/desktop-connector-extensibility/data-extension-security-1.png)

Bij **Gegevensextensies** kunt u uit twee beveiligingsniveaus kiezen:

* (Aanbevolen) Toestaan dat alleen gecertificeerde extensies worden geladen
* (Niet aanbevolen) Toestaan dat een extensie wordt geladen zonder waarschuwing

Als u van plan bent om **aangepaste connectors**, zelf ontwikkelde connectors of connectors van een derden te gebruiken, moet u **(Niet aanbevolen) Toestaan dat een extensie wordt geladen zonder waarschuwing** selecteren. Het wordt afgeraden om die beveiligingsinstelling te gebruiken, tenzij u van plan bent om **aangepaste connectors** te gaan gebruiken.

Met de **aanbevolen** beveiligingsinstelling wordt een foutmelding weergegeven waarin wordt beschreven welke connectors niet kunnen worden geladen vanwege de beveiliging (als er aangepaste connectors aanwezig zijn in uw systeem).

![Er wordt een dialoogvenster weergegeven met de aangepaste connectors die niet kunnen worden geladen vanwege de beveiligingsinstellingen (in dit geval TripPin)](media/desktop-connector-extensibility/data-extension-security-2.png)

Als u deze fout wilt verhelpen en u de connectors wilt gebruiken, moet u de beveiligingsinstellingen wijzigen zodat de eerder beschreven instelling **niet aanbevolen** wordt gebruikt. Start vervolgens **Power BI Desktop** opnieuw op.

## <a name="certified-connectors"></a>Gecertificeerde connectors

Een beperkte subset gegevensextensies wordt beschouwd als **gecertificeerd**. Gecertificeerde connectors zijn beschikbaar via het dialoogvenster **Gegevens ophalen**. De partij die verantwoordelijk is voor onderhoud en ondersteuning blijft de externe ontwikkelaar die de connector heeft gemaakt. Microsoft distribueert deze wel, maar kan niet verantwoordelijk worden gehouden voor de prestaties of de functionaliteit op de lange termijn.

Als u een aangepaste connector wilt laten certificeren, laat u uw leverancier contact opnemen met Microsoft.
