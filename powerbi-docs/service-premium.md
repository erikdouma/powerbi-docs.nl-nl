---
title: Wat is Microsoft Power BI Premium?
description: Power BI Premium is toegewezen capaciteit voor uw organisatie of team om u betrouwbaardere prestaties en grotere gegevensvolumes te kunnen bieden, zonder dat u voor iedere gebruiker een licentie hoeft te kopen.
author: mgblythe
ms.author: mblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-admin
ms.topic: conceptual
ms.date: 09/11/2018
LocalizationGroup: Premium
ms.openlocfilehash: 0723ddb57131fed499d4ac86666b3cd6d8bcbd2d
ms.sourcegitcommit: 833cf1252807721fb1b3000487bd032bfd6c8c98
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/04/2018
ms.locfileid: "48271803"
---
# <a name="what-is-microsoft-power-bi-premium"></a>Wat is Microsoft Power BI Premium?

Microsoft Power BI Premium biedt resources die speciaal zijn ontwikkeld om de Power BI-service voor uw organisatie of team uit te voeren. Dit resulteert in betrouwbaardere prestaties en u kunt grotere gegevensvolumes verwerken. Premium biedt ook de mogelijkheid tot een wijdverspreide distributie zonder dat u per gebruiker Pro-licenties hoeft te kopen voor viewers.

U kunt profiteren van Power BI Premium door werkruimten aan een *Premium-capaciteit* toe te wijzen. Premium-capaciteit is een toegewezen resource voor uw organisatie. Werkruimten die niet zijn toegewezen aan een Premium-capaciteit, bevinden zich in een *gedeelde capaciteit*. Met gedeelde capaciteit worden uw workloads uitgevoerd via rekenresources die met andere klanten worden gedeeld. 

Bij een gedeelde capaciteit past Power BI meer beperkingen toe voor individuele gebruikers om alle gebruikers een goede ervaring te geven. Uw werkruimte bevindt zich standaard in een gedeelde capaciteit, evenals uw persoonlijke *Mijn werkruimte* en app-werkruimten.

[!INCLUDE [powerbi-premium-illustration](./includes/powerbi-premium-illustration.md)]

<iframe width="560" height="315" src="https://www.youtube.com/embed/lNQDkN0GXzU?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>

## <a name="capacity-tiers"></a>Capaciteitslagen

Hier volgt een overzicht van de verschillen tussen gedeelde capaciteit en Premium-capaciteit.

|  | Gedeelde capaciteit | Power BI Premium-capaciteit |
| --- | --- | --- |
| **Vernieuwingsfrequentie** |8 keer per dag |48 keer per dag |
| **Isolatie met toegewezen hardware** |![](media/service-premium/not-available.png "Niet beschikbaar") |![](media/service-premium/available.png "Beschikbaar") |
| **Enterprise distributie** naar ***alle gebruikers*** | | |
| Apps en delen |![](media/service-premium/not-available.png "Niet beschikbaar") |![](media/service-premium/available.png "Beschikbaar")<sup>1</sup> |
| Ingesloten API en besturingselementen |![](media/service-premium/not-available.png "Niet beschikbaar") |![](media/service-premium/available.png "Beschikbaar")<sup>2</sup> |
| **Power BI-rapporten on-premises publiceren** |![](media/service-premium/not-available.png "Niet beschikbaar") |![](media/service-premium/available.png "Beschikbaar") |

*<sup>1</sup> Zie [Power BI Free vs Pro voor meer informatie](service-features-license-type.md).*  
*<sup>2</sup> Toekomstige verbeteringen voor Power BI Premium.*

Als u een Power BI Premium-capaciteit wilt gebruiken, wijst u een werkruimte toe aan een capaciteit. Wanneer premium-capaciteit een back-up maakt van een werkruimte, krijgt u:

* **Geplande vernieuwingen**: met gedeelde capaciteit wordt het aantal geplande vernieuwingen voor geïmporteerde modelgegevenssets beperkt tot acht per dag. Voor gegevenssets in Premium-werkruimten, kunt u maximaal 48 keer per dag vernieuwingen plannen. Het vernieuwen van de DirectQuery-cache is nog steeds beperkt tot acht keer per dag in Premium-capaciteit.

* **Isolatie met toegewezen hardware**: in gedeelde capaciteit kunnen de resourcevereisten van andere werkbelastingen invloed hebben op de prestaties van uw rapporten en dashboards. Premium-capaciteit biedt daarentegen meer consistente, betrouwbaardere prestaties voor uw werkbelastingen door deze te isoleren van niet-gerelateerde werkbelastingen.

Als een app wordt ondersteund door Premium-capaciteit (oftewel de app is gepubliceerd vanuit een app-werkruimte die momenteel is toegewezen aan Premium), kan de gepubliceerde app worden gebruikt door iedere gebruiker in uw organisatie, ongeacht de toegewezen licenties.

Voor meer informatie over het toewijzen van werkruimten aan een premium-capaciteit raadpleegt u [Power BI Premium beheren](service-admin-premium-manage.md).

<a name="premiumskus"/>

### <a name="premium-capacity-nodes"></a>Premium-capaciteitsknooppunten

Power BI Premium is beschikbaar in knooppuntconfiguraties met verschillende v-corecapaciteiten. Zie [Prijzen van Power BI](https://powerbi.microsoft.com/pricing/) voor meer informatie over het specifieke SKU-aanbod en de kosten. Er is ook een [kostencalculator](https://powerbi.microsoft.com/calculator/) beschikbaar. Zie [Technisch document over het plannen van een Power BI Enterprise-implementatie](https://aka.ms/pbienterprisedeploy) voor meer informatie over het plannen van de ingesloten analysecapaciteit.

* P-knooppunten kunnen worden gebruikt voor ingesloten of service-implementaties.

* EM-knooppunten kunnen alleen worden gebruikt voor ingesloten implementaties. EM-knooppunten hebben geen toegang tot premiummogelijkheden, zoals apps delen met gebruikers die geen Power BI Pro-licentie hebben.

>[!NOTE]
>Koppelingen in deze tabel werken alleen goed voor gebruikers die globale beheerders van Office 365 zijn. Voor andere gebruikers wordt een 404-fout weergegeven.

| Capaciteitsknooppunt | Totaal aantal v-cores<br/>*(back-end + front-end)* | Back-end-v-cores | Front-end-v-cores | Limieten voor DirectQuery/liveverbindingen | Maximaal aantal paginaweergaven (rendering) tijdens piekuren | Beschikbaarheid |
| --- | --- | --- | --- | --- | --- | --- |
| [EM1 (maandelijks)](https://portal.office.com/SubscriptionDetails?OfferId=4004702D-749C-4F74-BF47-3048F1833780&adminportal=1) |1-v-core |0,5 v-core, 2,5 GB RAM |0,5 v-core |3,75 per seconde |150-300 |Beschikbaar |
| [EM2 (maandelijks)](https://portal.office.com/SubscriptionDetails?OfferId=4004702D-749C-4F74-BF47-3048F1833780&adminportal=1) |2 v-cores |1 v-core, 5 GB RAM |1-v-core |7,5 per seconde |301-600 |Beschikbaar |
| [EM3 (maandelijks)](https://portal.office.com/SubscriptionDetails?OfferId=4004702D-749C-4F74-BF47-3048F1833780&adminportal=1) |4 v-cores |2 v-cores, 10 GB RAM |2 v-cores | |601-1200 |Beschikbaar |
| [P1](https://portal.office.com/SubscriptionDetails?OfferId=b3ec5615-cc11-48de-967d-8d79f7cb0af1&adminportal=1) |8 v-cores |4 v-cores, 25 GB RAM |4 v-cores |30 per seconde |1.201-2.400 |Beschikbaar ([maandelijks](https://portal.office.com/SubscriptionDetails?OfferId=E4C8EDD3-74A1-4D42-A738-C647972FBE81&adminportal=1) is ook beschikbaar) |
| [P2](https://portal.office.com/SubscriptionDetails?OfferId=062F2AA7-B4BC-4B0E-980F-2072102D8605&adminportal=1) |16 v-cores |8 v-cores, 50 GB RAM |8 v-cores |60 per seconde |2.401-4.800 |Beschikbaar |
| [P3](https://portal.office.com/SubscriptionDetails?OfferId=40c7d673-375c-42a1-84ca-f993a524fed0&adminportal=1) |32 v-cores |16 v-cores, 100 GB RAM |16 v-cores |120 per seconde |4.801-9.600 |Beschikbaar |

* De front-end-v-cores zijn verantwoordelijk voor de webservice, het documentbeheer voor dashboards en rapporten, het beheren van de toegangsrechten, de planning, API's, uploaden en downloaden en in het algemeen voor alles met betrekking tot de gebruikerservaring.

* De back-end-v-cores zijn verantwoordelijk voor het zware werk: verwerken van query's, cachebeheer, uitvoeren van R-servers, vernieuwen van gegevens, natuurlijke taalverwerking, realtime feeds en het weergeven van rapporten en afbeeldingen op de server. Voor de back-end-v-cores wordt ook een bepaalde hoeveelheid geheugen gereserveerd. Het is met name belangrijk om voldoende geheugen te hebben wanneer er met grote gegevensmodellen of met een groot aantal actieve gegevenssets wordt gewerkt.

## <a name="power-bi-report-server"></a>Power BI Report Server
Met Power BI Premium kunt u Power BI Report Server ook on-premises uitvoeren in uw organisatie. Zie [Aan de slag met Power BI Report Server](report-server/get-started.md) voor meer informatie.

## <a name="next-steps"></a>Volgende stappen
[Veelgestelde vragen over Power BI Premium](service-premium-faq.md)  
[Releaseopmerkingen bij Power BI Premium](service-premium-release-notes.md)  
[Power BI Premium aanschaffen](service-admin-premium-purchase.md)  
[Power BI Premium beheren](service-admin-premium-manage.md)  
[Technisch document over Microsoft Power BI Premium](https://aka.ms/pbipremiumwhitepaper)  
[Een technisch document over een Power BI-implementatie voor de onderneming plannen](https://aka.ms/pbienterprisedeploy)  
[Power BI in uw organisatie beheren](service-admin-administering-power-bi-in-your-organization.md)  

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](https://community.powerbi.com/)
