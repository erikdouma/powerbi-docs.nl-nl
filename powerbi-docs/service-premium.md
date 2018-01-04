---
title: Wat is Power BI Premium?
description: Power BI Premium is toegewezen capaciteit voor uw organisatie of team om u betrouwbaardere prestaties en grotere gegevensvolumes te kunnen bieden, zonder dat u voor iedere gebruiker een licentie hoeft te kopen.
services: powerbi
documentationcenter: 
author: guyinacube
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: get-started-article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 12/05/2017
ms.author: asaxton
ms.openlocfilehash: 7c1536693490252029d51ddc619eaa7266095403
ms.sourcegitcommit: d91436de68a0e833ecff18d976de9d9431bc4121
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/06/2017
---
# <a name="power-bi-premium---what-is-it"></a>Wat is Power BI Premium?
Power BI Premium bevat toegewezen resources om de Power BI-service voor uw organisatie of een team uit te voeren, wat resulteert in betrouwbaardere prestaties en grotere gegevensvolumes. Premium biedt de mogelijkheid tot een wijd verspreide distributie zonder dat u gebruikerslicentie hoeft aan te schaffen voor viewers.

U kunt profiteren van Power BI Premium door werkruimten aan een Premium-capaciteit toe te wijzen. *Premium-capaciteit* is een toegewezen resource voor uw organisatie. Werkruimten die niet zijn toegewezen aan een premium-capaciteit, bevinden zich in een gedeelde capaciteit.

*Gedeelde capaciteit* is de ervaring zoals u die gewend bent met Power BI, waar uw workloads worden uitgevoerd op calculatiebronnen die worden gedeeld met andere klanten. Bij een gedeelde capaciteit gelden er meer beperkingen voor de individuele gebruikers om een goede ervaring voor alle gebruikers te waarborgen.

[!INCLUDE [powerbi-premium-illustration](./includes/powerbi-premium-illustration.md)]

<iframe width="560" height="315" src="https://www.youtube.com/embed/lNQDkN0GXzU?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>

## <a name="capacity-tiers"></a>Capaciteitslagen
Er zijn twee typen capaciteit in Power BI. Gedeelde capaciteit en Power BI Premium-capaciteit. Hier volgt een overzicht van de verschillen tussen beide.

|  | Gedeelde capaciteit | Power BI Premium-capaciteit |
| --- | --- | --- |
| **Vernieuwingsfrequentie** |8 keer per dag |Niet beperkt |
| **Isolatie met toegewezen hardware** |![](media/service-premium/not-available.png "Niet beschikbaar") |![](media/service-premium/available.png "Beschikbaar") |
| **Enterprise distributie** naar ***alle gebruikers*** | | |
| Apps |![](media/service-premium/not-available.png "Niet beschikbaar") |![](media/service-premium/available.png "Beschikbaar")<sup>1</sup> |
| Ingesloten API en besturingselementen |![](media/service-premium/not-available.png "Niet beschikbaar") |![](media/service-premium/available.png "Beschikbaar")<sup>2</sup> |
| **Power BI-rapporten on-premises publiceren** |![](media/service-premium/not-available.png "Niet beschikbaar") |![](media/service-premium/available.png "Beschikbaar") |

*<sup>1</sup> Gratis gebruik door gebruiker in apps omvat onder meer het weergeven van inhoud op internet en op mobiele apparaten, het gebruik van Q&A, Snelle inzichten, Cortana, exporteren naar CSV, Excel en PowerPoint.*  
*<sup>2</sup> Toekomstige verbeteringen voor Power BI Premium nadat Power BI algemeen beschikbaar is gemaakt.*

### <a name="premium-capacity"></a>Premium-capaciteit
Als u een Power BI Premium-capaciteit wilt gebruiken, moet u een werkruimte toewijzen aan een capaciteit. Zie [Power BI Premium beheren](service-admin-premium-manage.md) voor meer informatie over het toewijzen van een werkruimte aan een premium-capaciteit.

Wanneer een werkruimte wordt ondersteund door een premium-capaciteit, kunt profiteren van de voordelen van Power BI Premium.

* Geplande vernieuwingen: voorheen konden geïmporteerde modellen slechts 8x per dag volgens schema worden vernieuwd. Deze beperking geldt niet voor gegevenssets in Premium-werkruimten. Dit is niet van toepassing op de geplande cachevernieuwingsinstellingen voor DirectQuery. Deze zijn hetzelfde voor de Premium-capaciteit en de gedeelde capaciteit.
* Isolatie met toegewezen hardware: gezien de aard van de gedeelde capaciteit, kunnen de prestaties van uw rapporten en dashboards worden beïnvloed door de resourcevereisten van andere workloads in de capaciteit, ondanks dat we dit zoveel mogelijk proberen te voorkomen. Premium biedt daarentegen een consistentere, betrouwbaardere prestaties voor uw workloads door deze te isoleren van niet-gerelateerde workloads.

Als een app wordt ondersteund door een premium-capaciteit (oftewel de app is gepubliceerd vanuit een app-werkruimte die momenteel is toegewezen aan Premium), kan de gepubliceerde app worden gebruikt door iedere gebruiker in uw organisatie, ongeacht de toegewezen licenties. Dit betekent dat zelfs gebruikers van de gratis versie van Power BI deze gepubliceerde apps kunnen gebruiken.

### <a name="shared-capacity"></a>Gedeelde capaciteit
Uw werkruimte bevindt zich standaard in de gedeelde capaciteit. Dit geldt ook voor uw persoonlijke *Mijn werkruimte* en app-werkruimten. Een gedeelde capaciteit is de ervaring zoals u die gewend bent met Power BI, waar uw workloads worden uitgevoerd op calculatiebronnen die worden gedeeld met andere klanten.

<a name="premiumskus"/>

### <a name="premium-capacity-nodes"></a>Premium-capaciteitsknooppunten
Power BI Premium is beschikbaar in knooppuntconfiguraties met verschillende v-corecapaciteiten. Zie [Prijzen van Power BI](https://powerbi.microsoft.com/pricing/) voor meer informatie over het specifieke SKU-aanbod en de kosten. Er is ook een [kostencalculator](https://powerbi.microsoft.com/calculator/) beschikbaar. Zie [Technisch document over het plannen van een Power BI Enterprise-implementatie](https://aka.ms/pbienterprisedeploy) voor meer informatie over het plannen van de ingesloten analysecapaciteit.

* P-knooppunten kunnen worden gebruikt voor ingesloten implementaties of service-implementaties
* EM-knooppunten kunnen alleen worden gebruikt voor ingesloten implementaties
* EM1 en EM2 
* Koppelingen in deze tabel werken alleen goed voor gebruikers die globale beheerders zijn voor Office 365. Voor andere gebruikers wordt een 404-fout weergegeven. 

| Capaciteitsknooppunt | Totaal aantal cores<br/>*(back-end + front-end)* | Back-endcores | Front-endcores | Limieten voor DirectQuery/liveverbindingen | Maximaal aantal paginaweergaven (rendering) tijdens piekuren | Beschikbaarheid |
| --- | --- | --- | --- | --- | --- | --- |
| [EM1 (maandelijks)](https://portal.office.com/SubscriptionDetails?OfferId=4004702D-749C-4F74-BF47-3048F1833780&adminportal=1) |1-v-core |.5 kernen, 2,5 GB RAM-geheugen |0,5 core |3,75 per seconde |150-300 |Beschikbaar |
| [EM2 (maandelijks)](https://portal.office.com/SubscriptionDetails?OfferId=4004702D-749C-4F74-BF47-3048F1833780&adminportal=1) |2 v-cores |1 core, 5 GB RAM |1 core |7,5 per seconde |301-600 |Beschikbaar |
| [EM3 (maandelijks)](https://portal.office.com/SubscriptionDetails?OfferId=4004702D-749C-4F74-BF47-3048F1833780&adminportal=1) |4 v-cores |2 cores, 10 GB RAM |2 cores | |601-1,200 |Beschikbaar |
| [P1](https://portal.office.com/SubscriptionDetails?OfferId=b3ec5615-cc11-48de-967d-8d79f7cb0af1&adminportal=1) |8 v-cores |4 cores, 25 GB RAM |4 cores |30 per seconde |1.201-2.400 |Beschikbaar ([maandelijks](https://portal.office.com/SubscriptionDetails?OfferId=E4C8EDD3-74A1-4D42-A738-C647972FBE81&adminportal=1) is ook beschikbaar) |
| [P2](https://portal.office.com/SubscriptionDetails?OfferId=062F2AA7-B4BC-4B0E-980F-2072102D8605&adminportal=1) |16 v-cores |8 cores, 50 GB RAM |8 cores |60 per seconde |2.401-4.800 |Beschikbaar |
| [P3](https://portal.office.com/SubscriptionDetails?OfferId=40c7d673-375c-42a1-84ca-f993a524fed0&adminportal=1) |32 v-cores |16 cores, 100 GB RAM |16 cores |120 per seconde |4.801-9.600 |Beschikbaar |

* De front-endcores zijn verantwoordelijk voor de webservice, het documentbeheer voor dashboards en rapporten, het beheren van de toegangsrechten, de planning, API's, uploaden en downloaden en in het algemeen voor alles met betrekking tot de gebruikerservaring.
* De back-endcores zijn verantwoordelijk voor het zware werk: verwerken van query's, cachebeheer, uitvoeren van R-servers, vernieuwen van gegevens, natuurlijke taalverwerking, realtime feeds en het weergeven van rapporten en afbeeldingen op de server. Voor de back-endcores wordt ook een bepaalde hoeveelheid geheugen gereserveerd. Het is met name belangrijk om voldoende geheugen te hebben wanneer er met grote gegevensmodellen of met een groot aantal actieve gegevenssets wordt gewerkt.

## <a name="power-bi-report-server"></a>Power BI Report Server
Power BI Premium biedt het recht om Power BI Report Server on-premises uit te voeren. Zie [Aan de slag met Power BI Report Server](report-server/get-started.md) voor meer informatie.

## <a name="next-steps"></a>Volgende stappen
[Veelgestelde vragen over Power BI Premium](service-premium-faq.md)  
[Releaseopmerkingen bij Power BI Premium](service-premium-release-notes.md)  
[Power BI Premium aanschaffen](service-admin-premium-purchase.md)  
[Power BI Premium beheren](service-admin-premium-manage.md)  
[Technisch document over Microsoft Power BI Premium](https://aka.ms/pbipremiumwhitepaper)  
[Een technisch document over een Power BI-implementatie voor de onderneming plannen](https://aka.ms/pbienterprisedeploy)  
[Power BI in uw organisatie beheren](service-admin-administering-power-bi-in-your-organization.md)  

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](https://community.powerbi.com/)

