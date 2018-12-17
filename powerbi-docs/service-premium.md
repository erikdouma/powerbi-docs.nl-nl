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
ms.date: 10/21/2018
ms.custom: seodec18
LocalizationGroup: Premium
ms.openlocfilehash: cbfee8034639a65517f9adc57cc95dd1271e6044
ms.sourcegitcommit: 72c9d9ec26e17e94fccb9c5a24301028cebcdeb5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/07/2018
ms.locfileid: "53025437"
---
# <a name="what-is-microsoft-power-bi-premium"></a>Wat is Microsoft Power BI Premium?

Microsoft Power BI Premium biedt resources die speciaal zijn ontwikkeld om de Power BI-service voor uw organisatie uit te voeren. Dit resulteert in betrouwbaardere prestaties en u kunt grotere gegevensvolumes verwerken. Premium biedt ook de mogelijkheid tot een wijdverspreide distributie zonder dat u per gebruiker Pro-licenties hoeft te kopen voor inhoudsgebruikers. Zie [Power BI Premium kopen](service-admin-premium-purchase.md) voor meer aankoopinformatie.

<iframe width="560" height="315" src="https://www.youtube.com/embed/lNQDkN0GXzU?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>

## <a name="premium-capacity-and-shared-capacity"></a>Premium-capaciteit en gedeelde capaciteit

U kunt profiteren van Power BI Premium door werkruimten aan een *Premium-capaciteit* toe te wijzen. Premium-capaciteit is een toegewezen resource voor uw organisatie. Werkruimten die niet zijn toegewezen aan een Premium-capaciteit, bevinden zich in een *gedeelde capaciteit*. Met gedeelde capaciteit worden uw workloads uitgevoerd via rekenresources die met andere klanten worden gedeeld.

In de volgende afbeelding wordt de Contoso-organisatie als voorbeeld gebruikt om de relatie tussen de Premium-capaciteit en de gedeelde capaciteit te demonstreren.

![Afbeelding van Power BI Premium](media/service-premium/premium-chart.png)

| Oppervlakte | Beschrijving |
| --- | --- |
| **(1)** Items binnen een Premium-capaciteit | <ul><li>Voor de toegang tot app-werkruimten (als leden of beheerders) en het publiceren van apps is Power BI Pro-licentie vereist.<li>Voor het delen van een app is een Pro-licentie vereist, voor het gebruik van een app niet.<li>Alle ontvangers van het dashboard kunnen gegevensmeldingen instellen, ongeacht de licentie die aan hen is toegewezen.<li>REST-API's voor insluiten maken gebruik van een serviceaccount met een Pro-licentie, in plaats van een gebruikersaccount.</ul> |
| **(2)** Mijn werkruimte in gedeelde capaciteit | <ul><li>Er is een Pro-licentie vereist voor zowel het delen als gebruiken van een app.</ul> |
| **(3)** App-werkruimten in gedeelde capaciteit | <ul><li>Voor het gebruik van de apps is een Pro-licentie vereist.</ul>|
| | |

Bij een gedeelde capaciteit past Power BI meer beperkingen toe voor individuele gebruikers om alle gebruikers een goede ervaring te geven. Uw werkruimte bevindt zich standaard in een gedeelde capaciteit, evenals uw persoonlijke *Mijn werkruimte* en app-werkruimten.

De volgende tabel bevat een overzicht van de verschillen tussen de gedeelde capaciteit en de Premium-capaciteit.

|  | Gedeelde capaciteit | Power BI Premium-capaciteit |
| --- | --- | --- |
| **Vernieuwingsfrequentie** |8 keer per dag |48 keer per dag |
| **Isolatie met toegewezen hardware** |![Niet beschikbaar](media/service-premium/not-available.png) |![Beschikbaar](media/service-premium/available.png) |
| **Enterprise distributie naar** _**alle gebruikers**_ | | |
| Apps en delen |![Niet beschikbaar](media/service-premium/not-available.png) |![Beschikbaar](media/service-premium/available.png) |
| Ingesloten API en besturingselementen |![Niet beschikbaar](media/service-premium/not-available.png) |![Beschikbaar](media/service-premium/available.png)<sup>2</sup> |
| **Power BI-rapporten on-premises publiceren** |![Niet beschikbaar](media/service-premium/not-available.png) |![Beschikbaar](media/service-premium/available.png) |
| | | |

*<sup>1</sup> Zie [Power BI Free vs Pro voor meer informatie](service-features-license-type.md).*  
*<sup>2</sup> Toekomstige verbeteringen voor Power BI Premium.*

Voor meer informatie over het toewijzen van werkruimten aan een premium-capaciteit raadpleegt u [Power BI Premium beheren](service-admin-premium-manage.md).

<a name="premiumskus"/>

### <a name="premium-capacity-nodes"></a>Premium-capaciteitsknooppunten

Power BI Premium is beschikbaar in knooppuntconfiguraties met verschillende v-corecapaciteiten. Zie [Prijzen van Power BI](https://powerbi.microsoft.com/pricing/) voor meer informatie over het specifieke SKU-aanbod en de kosten. Er is ook een [kostencalculator](https://powerbi.microsoft.com/calculator/) beschikbaar. Zie [Technisch document over het plannen van een Power BI Enterprise-implementatie](https://aka.ms/pbienterprisedeploy) voor meer informatie over het plannen van de ingesloten analysecapaciteit. Samenvattend:

* P-knooppunten kunnen worden gebruikt voor ingesloten of service-implementaties.

* EM-knooppunten kunnen alleen worden gebruikt voor ingesloten implementaties. EM-knooppunten hebben geen toegang tot premiummogelijkheden, zoals apps delen met gebruikers die geen Power BI Pro-licentie hebben.

>[!NOTE]
>Koppelingen in deze tabel werken alleen goed voor gebruikers met een globale beheerdersrol voor Office 365. Voor andere gebruikers wordt een 404-fout weergegeven.

| Capaciteitsknooppunt | Totaal aantal v-cores<br/>*(back-end + front-end)* | Back-end-v-cores | Front-end-v-cores | Limieten voor DirectQuery/liveverbindingen | Maximaal aantal paginaweergaven (rendering) tijdens piekuren | Beschikbaarheid |
| --- | --- | --- | --- | --- | --- | --- |
| [EM1 (maandelijks)](https://portal.office.com/SubscriptionDetails?OfferId=4004702D-749C-4F74-BF47-3048F1833780&adminportal=1) |1-v-core |0,5 v-core, 2,5 GB RAM |0,5 v-core |3,75 per seconde |150-300 |Beschikbaar |
| [EM2 (maandelijks)](https://portal.office.com/SubscriptionDetails?OfferId=4004702D-749C-4F74-BF47-3048F1833780&adminportal=1) |2 v-cores |1 v-core, 5 GB RAM |1-v-core |7,5 per seconde |301-600 |Beschikbaar |
| [EM3 (maandelijks)](https://portal.office.com/SubscriptionDetails?OfferId=4004702D-749C-4F74-BF47-3048F1833780&adminportal=1) |4 v-cores |2 v-cores, 10 GB RAM |2 v-cores | |601-1200 |Beschikbaar |
| [P1](https://portal.office.com/SubscriptionDetails?OfferId=b3ec5615-cc11-48de-967d-8d79f7cb0af1&adminportal=1) |8 v-cores |4 v-cores, 25 GB RAM |4 v-cores |30 per seconde |1.201-2.400 |Beschikbaar ([maandelijks](https://portal.office.com/SubscriptionDetails?OfferId=E4C8EDD3-74A1-4D42-A738-C647972FBE81&adminportal=1) is ook beschikbaar) |
| [P2](https://portal.office.com/SubscriptionDetails?OfferId=062F2AA7-B4BC-4B0E-980F-2072102D8605&adminportal=1) |16 v-cores |8 v-cores, 50 GB RAM |8 v-cores |60 per seconde |2.401-4.800 |Beschikbaar |
| [P3](https://portal.office.com/SubscriptionDetails?OfferId=40c7d673-375c-42a1-84ca-f993a524fed0&adminportal=1) |32 v-cores |16 v-cores, 100 GB RAM |16 v-cores |120 per seconde |4.801-9.600 |Beschikbaar |
| | | | | | | |

* De front-end-v-cores zijn verantwoordelijk voor de webservice, het documentbeheer voor dashboards en rapporten, het beheren van de toegangsrechten, de planning, API's, uploaden en downloaden en in het algemeen voor alles met betrekking tot de gebruikerservaring.

* De back-end-v-cores zijn verantwoordelijk voor het zware werk: verwerken van query's, cachebeheer, uitvoeren van R-servers, vernieuwen van gegevens, natuurlijke taalverwerking, realtime feeds en het weergeven van rapporten en afbeeldingen op de server. Voor de back-end-v-cores wordt ook een bepaalde hoeveelheid geheugen gereserveerd. Het is met name belangrijk om voldoende geheugen te hebben wanneer er met grote gegevensmodellen of met een groot aantal actieve gegevenssets wordt gewerkt.

## <a name="workloads-in-premium-capacity"></a>Workloads in Premium-capaciteit

Een workload in Power BI kunt u zien als een van de vele services die u beschikbaar kunt stellen aan gebruikers. De standaardconfiguratie is dat capaciteiten voor  **Power BI Premium** en **Power BI Embedded** alleen de workload ondersteunen die is gekoppeld aan het uitvoeren van Power BI-query's in de cloud.

We bieden nu preview-ondersteuning voor twee extra workloads: **Gepagineerde rapporten** en **Gegevensstromen**. U kunt deze workloads inschakelen in de Power BI-beheerportal of via de REST-API van Power BI. U geeft ook de maximale hoeveelheid geheugen op die elke workload kan gebruiken, zodat u kunt bepalen hoe de verschillende workloads van invloed zijn op elkaar. Zie [Workloads configureren](service-admin-premium-manage.md#configure-workloads) voor meer informatie.

### <a name="default-memory-settings"></a>Standaardinstellingen voor geheugen

In de volgende tabellen ziet u de standaard- en minimumwaarden voor geheugen, op basis van de verschillende [capaciteitsknooppunten](#premium-capacity-nodes) die beschikbaar zijn. Geheugen wordt dynamisch toegewezen aan gegevensstromen, maar in het geval van gepagineerde rapporten betreft het een statische toewijzing. Zie voor meer informatie de volgende sectie, [Overwegingen voor gepagineerde rapporten](#considerations-for-paginated-reports).

#### <a name="microsoft-office-skus-for-software-as-a-service-saas-scenarios"></a>Microsoft Office-SKU's voor SaaS-scenario's (Software as a Service)

|                     | EM3                      | P1                       | P2                      | P3                       |
|---------------------|--------------------------|--------------------------|-------------------------|--------------------------|
| Gepagineerde rapporten | N.v.t. | standaard 20%; minimaal 10% | standaard 20%; minimaal 5% | standaard 20%; minimaal 2,5% |
| Gegevensstromen | standaard 20%; minimaal 8%  | standaard 20%; minimaal 4%  | standaard 20%; minimaal 2% | standaard 20%; minimaal 1%  |
| | | | | |

#### <a name="microsoft-azure-skus-for-platform-as-a-service-paas-scenarios"></a>Microsoft Azure-SKU's voor PaaS-scenario's (Platform as a Service)

|                  | A1                       | A2                       | A3                      | A4                       | A5                      | A6                        |
|-------------------|--------------------------|--------------------------|-------------------------|--------------------------|-------------------------|---------------------------|
| Gepagineerde rapporten | N.v.t.                      | N.v.t.                      | N.v.t.                     | standaard 20%; minimaal 10% | standaard 20%; minimaal 5% | standaard 20%; minimaal 2,5% |
| Gegevensstromen         | standaard 27%; minimaal 27% | standaard 20%; minimaal 16% | standaard 20%; minimaal 8% | standaard 20%; minimaal 4%  | standaard 20%; minimaal 2% | standaard 20%; minimaal 1%   |

### <a name="considerations-for-paginated-reports"></a>Overwegingen voor gepagineerde rapporten

Houd rekening met de volgende punten als u de workload Gepagineerde rapporten gebruikt.

* **Geheugentoewijzing in gepagineerd rapporten**: gepagineerde rapporten ondersteunen het uitvoeren van eigen code bij het weergeven van een rapport (zoals het dynamisch wijzigen van de tekstkleur op basis van inhoud). Gezien dit feit beveiligen we Power BI Premium-capaciteit door gepagineerde rapporten uit te voeren in een afgesloten ruimte binnen de capaciteit. Aan deze ruimte wordt de maximale hoeveelheid geheugen toegewezen die u hebt ingesteld, ongeacht of de workload actief is of niet. Als u Power BI-rapporten of gegevensstromen in dezelfde capaciteit gebruikt, moet u het geheugen voor gepagineerde rapporten laag genoeg instellen, zodat deze workload geen gevolgen heeft voor de andere workloads.

* **Gepagineerde rapporten zijn niet beschikbaar**: in zeldzame gevallen kan het gebeuren dat de workload Gepagineerde rapporten niet beschikbaar is. U ziet dan een foutstatus voor de workload in de beheerportal. Gebruikers zien time-outs als ze rapporten willen weergeven. U kunt dit probleem oplossen door de workload uit te schakelen en vervolgens weer in te schakelen.

## <a name="power-bi-report-server"></a>Power BI Report Server

Met Power BI Premium kunt u Power BI Report Server ook on-premises uitvoeren in uw organisatie. Zie [Aan de slag met Power BI Report Server](report-server/get-started.md) voor meer informatie.

## <a name="next-steps"></a>Volgende stappen

[Veelgestelde vragen over Power BI Premium](service-premium-faq.md)
[Power BI Premium kopen](service-admin-premium-purchase.md)
[Power BI Premium beheren](service-admin-premium-manage.md)
[Whitepaper over Microsoft Power BI Premium](https://aka.ms/pbipremiumwhitepaper)
[Whitepaper: Een Power BI Enterprise-implementatie plannen](https://aka.ms/pbienterprisedeploy)
[Power BI in uw organisatie beheren](service-admin-administering-power-bi-in-your-organization.md)

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](https://community.powerbi.com/)
