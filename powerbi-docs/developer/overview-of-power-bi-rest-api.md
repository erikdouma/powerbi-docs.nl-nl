---
title: Wat kan ik doen met de Power BI-API
description: Wat kan ik doen met de Power BI-API
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-developer
ms.topic: conceptual
ms.date: 05/25/2018
ms.author: maghan
ms.openlocfilehash: 3b19740616e7b9a390a883fde2fd96320de7b94a
ms.sourcegitcommit: 698b788720282b67d3e22ae5de572b54056f1b6c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/17/2018
ms.locfileid: "45973581"
---
# <a name="what-can-developers-do-with-the-power-bi-api"></a>Wat kunnen ontwikkelaars doen met de Power BI-API?

Power BI geeft dashboards weer die interactief zijn en in realtime kunnen worden gemaakt en bijgewerkt via vele verschillende gegevensbronnen. Met behulp van elke programmeertaal die REST-aanroepen ondersteunt, kunt u apps maken die in realtime met een Power BI-dashboard kunnen worden geïntegreerd. U kunt ook Power BI-tegels en -rapporten integreren met apps.

Ontwikkelaars kunnen ook hun eigen gegevensvisualisaties bouwen die in interactieve rapporten en dashboards kunnen worden gebruikt.

Hier volgen enkele dingen die u kunt doen met de Power BI-API‘s.

| **Om dit te doen** | **Gaat u hierheen** |
| --- | --- |
| Dashboards, rapporten en tegels insluiten voor Power BI-gebruikers en niet-Power BI-gebruikers (app is eigenaar van gegevens) |[Dashboards, rapporten en tegels van Power BI insluiten](embedding-content.md) |
| Een bestaande zakelijke werkstroom uitbreiden om belangrijke gegevens naar een Power BI-dashboard te pushen. |[Gegevens in een dashboard pushen](walkthrough-push-data.md) |
| Verifiëren bij Power BI. |[Verifiëren bij Power BI](get-azuread-access-token.md) |
| Een aangepast visueel element maken. |[Aangepaste visuele elementen maken met behulp van ontwikkelhulpprogramma's](../service-custom-visuals-getting-started-with-developer-tools.md) |

> [!NOTE]
> In de Power BI-API's worden app-werkruimten nog steeds groepen genoemd. Als er wordt verwezen naar groepen, werkt u in feite met app-werkruimten.

## <a name="power-bi-developer-samples"></a>Voorbeelden voor Power BI-ontwikkelaars

De voorbeelden voor Power BI-ontwikkelaars omvatten items voor het insluiten van dashboards, rapporten en tegels.

[Voorbeelden voor Power BI-ontwikkelaars](https://github.com/Microsoft/PowerBI-Developer-Samples)

* Voorbeelden in **App is eigenaar van gegevens** zijn bestemd voor insluiten met niet-Power BI-gebruikers.
* Voorbeelden in **Gebruiker is eigenaar van gegevens** zijn bestemd voor insluiten met Power BI-gebruikers.

## <a name="github-repositories"></a>GitHub-opslagplaatsen

* [.NET SDK](https://github.com/Microsoft/PowerBI-CSharp)
* [JavaScript-API](https://github.com/Microsoft/PowerBI-JavaScript)
* [Aangepaste visuele elementen](https://github.com/Microsoft/PowerBI-visuals)

## <a name="developer-tools"></a>Ontwikkelhulpprogramma's

Hieronder volgen hulpprogramma‘s die u kunt gebruiken bij het ontwikkelen van Power BI-items.

U kunt het [instelprogramma voor insluiten](https://aka.ms/embedsetup) uitvoeren om snel aan de slag te gaan en een voorbeeldtoepassing voor het insluiten van Power BI-inhoud te downloaden.

Kies de oplossing die het beste bij u past:

* [Door inhoud voor uw klanten in te sluiten](embedding.md#embedding-for-your-customers) kunt u dashboards en rapporten insluiten voor gebruikers die geen account voor Power BI hebben. Voer de oplossing [Insluiten voor uw klanten](https://aka.ms/embedsetup/AppOwnsData) uit.

* [Met het insluiten van inhoud voor uw organisatie](embedding.md#embedding-for-your-organization) kunt u Power BI-service uitbreiden. Voer de oplossing [Insluiten voor uw organisatie](https://aka.ms/embedsetup/UserOwnsData) uit.

Voor een volledig voorbeeld van het gebruik van de JavaScript-API kunt u het [hulpprogramma Playground](https://microsoft.github.io/PowerBI-JavaScript/demo) gebruiken. Met dit hulpprogramma kunt u op een snelle manier verschillende typen Power BI Embedded-voorbeelden proberen. Op de [wikipagina voor Power BI JavaScript](https://github.com/Microsoft/powerbi-javascript/wiki) vindt u ook meer informatie over de JavaScript-API.

## <a name="push-data-into-power-bi"></a>Gegevens pushen naar Power BI

U kunt de Power BI-API gebruiken om gegevens naar een gegevensset te pushen. Met deze functie kunt u een rij aan een tabel in een gegevensset toevoegen. De nieuwe gegevens kunnen vervolgens worden weergegeven in tegels op een dashboard en in visuele elementen binnen uw rapport.

![Voorbeeld van pushen van gegevens](media/what-can-you-do/powerbi-push-data.png)

## <a name="next-steps"></a>Volgende stappen

[Gegevens naar een gegevensset pushen](walkthrough-push-data.md)  
[Aan de slag met ontwikkelhulpprogramma's voor aangepaste visuele elementen](../service-custom-visuals-getting-started-with-developer-tools.md)  
[Power BI REST API reference](https://docs.microsoft.com/rest/api/power-bi/) (Naslag voor REST-API voor Power BI)  

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)
