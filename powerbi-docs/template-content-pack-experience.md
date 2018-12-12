---
title: Ervaringen met sjablooninhoudspakketten in Power BI
description: Ervaringen met sjablooninhoudspakketten
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 10/09/2017
ms.author: maggies
ms.openlocfilehash: 23a8875479197f1d200a9f086fcfd27d483faf40
ms.sourcegitcommit: b03912343a5a214c6bb972aaa6aa051c2a5f4332
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2018
ms.locfileid: "52900216"
---
# <a name="template-content-pack-experiences-in-power-bi"></a>Ervaringen met sjablooninhoudspakketten in Power BI
In deze sectie wordt een typische ervaring voor een gebruiker beschreven die verbinding maakt met een ISV [inhoudspakket](service-connect-to-services.md).

Probeer het verbindingsproces zelf uit door te verbinden met een uitgebracht inhoudspakket op https://app.powerbi.com/getdata/services (zoals het [GitHub-inhoudspakket](https://app.powerbi.com/getdata/services/github) dat hieronder wordt beschreven).

## <a name="connect"></a>Verbinden
Om te beginnen, bladert een gebruiker door de galerie voor inhoudspakketten en selecteert een inhoudspakket om verbinding mee te maken. Het inhoudspakketitem bevat een naam, een pictogram en een beschrijvende tekst die meer informatie biedt voor de gebruiker.

![verbinding maken](media/template-content-pack-experience/github_data.png)

![verbinding maken](media/template-content-pack-experience/github_connect.png)

## <a name="parameters"></a>Parameters
Nadat de gebruiker zijn selectie heeft gemaakt, wordt hem gevraagd om parameters op te geven (indien vereist). Het parametersdialoogvenster wordt tijdens het maken van het inhoudspakket declaratief verstrekt door de auteur.

Momenteel is de gebruikersinterface voor parameters zeer eenvoudig: er is geen manier om vervolgkeuzelijsten te inventariseren en validatie voor gegevensinvoer is beperkt tot regex.

![parameters](media/template-content-pack-experience/github_params.png)

## <a name="credentials"></a>Referenties
Na het opgeven van de parameters, wordt de gebruiker gevraagd om zich aan te melden.  Als de bron meerdere typen verificatie ondersteunt, wordt de gebruiker gevraagd de juiste optie kiezen. Als de bron OAuth vereist, wordt de gebruikersinterface voor het aanmelden bij de service weergegeven wanneer de gebruiker op Aanmelden drukt.  Anders kan de gebruiker zijn referenties invoeren in het weergegeven dialoogvenster.

![Referenties](media/template-content-pack-experience/github_login.png)

![verbinding maken](media/template-content-pack-experience/github_creds2.png)

## <a name="instantiation"></a>Instantiëring
Wanneer de aanmelding is geslaagd, worden de artefacten die zijn opgenomen in het inhoudspakket (model, rapporten en dashboard) weergegeven in de navigatiebalk.  Deze artefacten worden toegevoegd aan elk gebruikersaccount.  De gegevens laden asynchroon om de gegevensset (model) te vullen.  De gebruiker kan vervolgens het dashboard, de rapporten en het model gebruiken.

Standaard wordt er een dagelijks vernieuwingsschema geconfigureerd voor de gebruiker. Hiermee worden de query's in het model opnieuw geëvalueerd.  Met de referenties die de gebruiker heeft ontvangen, kan hij de gegevens vernieuwen zonder hiervoor aanwezig te zijn.

![Instantiëring](media/template-content-pack-experience/github_dashboard.png)

## <a name="exploration-and-monitoring"></a>Verkennen en bewaken
Zodra het inhoudspakket is gemigreerd naar het account van de gebruiker kan hij de gegevens/inzichten verkennen en bewaken.

Dit omvat doorgaans:

* Het dashboard bekijken en aanpassen.
* Het rapport bekijken en aanpassen.
* In natuurlijke taal vragen stellen over uw gegevens
* De gegevens in het gegevensmodel verkennen met behulp van het verkencanvas

Voeg modellen voor natuurlijke taalverwerking (synoniemen) en een begrijpelijk modelschema toe om de ervaring bij het verkennen te verbeteren.

