---
title: wat is een dashboard voor gebruikers van de Power BI service?
description: Dashboards zijn een belangrijke functie van de Power BI-service.
author: maggieMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 09/02/2018
ms.author: maggie
LocalizationGroup: Dashboards
ms.openlocfilehash: 2e71f3a1efe60094b9a714e1d03b891aa9da99a6
ms.sourcegitcommit: 07beb155ec0ea1cdcc741085251ed06d7bc8581c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/09/2018
ms.locfileid: "48875003"
---
# <a name="dashboards-in-power-bi-service"></a>Dashboards in de Power BI-service

Een Power BI-***dashboard*** bestaat uit één pagina, ook wel een canvas genoemd, die gebruikmaakt van visualisaties om een verhaal te vertellen. Aangezien het maar één pagina betreft, bevat een goed ontworpen dashboard alleen de belangrijkste elementen van dat verhaal.

![dashboard](media/service-dashboards/power-bi-dashboard2.png)

Dashboards zijn een functie van Power BI-service en zijn niet beschikbaar in Power BI Desktop. Dashboards kunnen niet worden gemaakt op mobiele apparaten, maar ze kunnen daar wel worden [bekeken en gedeeld](mobile-apps-view-dashboard.md).

## <a name="dashboard-creators-and-dashboard-consumers"></a>Auteurs en gebruikers van dashboards
Afhankelijk van uw rol bent u mogelijk iemand die dashboards maakt voor uw eigen gebruik of om te delen met collega's. Uw informatie kan worden gevonden in **Dashboards voor auteurs**. Wanneer u dashboards van anderen ontvangt. U wilt meer informatie over dashboards in het algemeen en hoe u ze gebruikt. Is dit een artikel voor u.


### <a name="if-you-will-be-receiving-and-consuming-dashboards"></a>Als u dashboards ontvangt en gebruikt

De visualisaties die u ziet op het dashboard worden *tegels* genoemd en worden *vastgemaakt* aan het dashboard, vauitn rapporten, door dashboard*auteurs*. Als u geen ervaring hebt met Power BI kunt u een goede basis leggen door de [basisconcepten van Power BI](service-basic-concepts.md) te lezen

> [!IMPORTANT]
> [Power BI Pro](service-free-vs-pro.md) is vereist voor het weergeven van een gedeeld dashboard.

De visualisaties op een dashboard zijn afkomstig uit rapporten en elk rapport is gebaseerd op één gegevensset. Een dashboard kan dan ook worden gezien als een ingang tot de onderliggende rapporten en gegevenssets. Als u een visualisatie selecteert, gaat u naar het rapport (en de gegevensset) die is gebruikt om de visualisatie te maken.

![Diagram met de relatie tussen dashboards, rapporten en gegevenssets](media/service-dashboards/power-bi-diagram.png)



## <a name="advantages-of-dashboards"></a>Voordelen van dashboards
Dashboards zijn een fantastische manier om uw bedrijf te monitoren, te zoeken naar antwoorden en de belangrijkste metrische gegevens in één oogopslag te zien. De visualisaties op een dashboard kunnen afkomstig zijn uit een of meer onderliggende gegevenssets en rapporten. Een dashboard combineert on-premises gegevens en gegevens in de cloud om zo een geconsolideerde weergave te bieden van uw gegevens, ongeacht waar deze zich bevinden.

Een dashboard is niet alleen een mooi plaatje; het is zeer interactief en de tegels worden bijgewerkt wanneer de onderliggende gegevens wijzigen.

## <a name="dashboards-versus-reports"></a>Dashboards versus rapporten
[Rapporten](service-reports.md) worden vaak verward met dashboards omdat dit ook canvassen met visualisaties zijn. Maar er zijn enkele belangrijke verschillen voor gebruikers van Power BI.

| **Mogelijkheid** | **Dashboards** | **Rapporten** |
| --- | --- | --- |
| Pagina's |Eén pagina |Een of meer pagina's |
| Gegevensbronnen |Een of meer rapporten en een of meer gegevenssets per dashboard |Eén gegevensset per rapport |
| Beschikbaar in Power BI Desktop |Nee |Ja, ***auteurs*** kunnen rapporten maken en bekijken in Desktop |
| Abonneren |U kunt zich abonneren op een dashboard |U kunt zich abonneren op een rapportpagina |
| Filteren |U kunt niet filteren of segmenteren |Er zijn verschillende manieren voor filteren, markeren en segmenteren |
| Aanbevolen |U kunt één dashboard instellen als uw aanbevolen dashboard |U kunt geen aanbevolen rapport aanmaken |
| Favoriet | U kunt dashboards instellen als *favorieten* | U kunt rapporten instellen als *favorieten*
| Waarschuwingen instellen |Beschikbaar voor dashboardtegels in bepaalde omstandigheden |Niet beschikbaar in rapporten |
| Query’s in natuurlijke taal |Op dashboard beschikbaar |Niet beschikbaar in rapporten |
| U kunt onderliggende tabellen en velden van de gegevensset bekijken |Nee. U kunt gegevens exporteren maar tabellen en velden niet in het dashboard zelf zien. |Ja. U kunt tabellen en velden en waarden van gegevenssets bekijken. |
| Aanpassen |Nee |In de leesweergave kunt u publiceren, insluiten, filteren, exporteren, downloaden als .pbix, gerelateerde inhoud bekijken, QR-codes genereren, analyseren in Excel en meer.  |

## <a name="next-steps"></a>Volgende stappen
* Maak kennis met dashboards door het bekijken van een van onze [voorbeelddashboards](sample-tutorial-connect-to-the-samples.md).
* Meer informatie over [dashboardtegels](service-dashboard-tiles.md) en wat er gebeurt als u een tegel selecteert.
* Wilt u een bepaalde dashboardtegel monitoren en een e-mail ontvangen wanneer deze een bepaalde drempelwaarde bereikt? [Stel dan een waarschuwing in voor de tegel](service-set-data-alerts.md).
* Vergroot uw kennis door vragen te stellen aan uw dashboard. Ontdek hoe u [Q&A van Power BI](power-bi-tutorial-q-and-a.md) gebruikt om een vraag te stellen over uw gegevens en antwoord krijgt in de vorm van een visualisatie.
