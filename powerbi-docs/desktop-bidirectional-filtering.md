---
title: In twee richtingen kruislings filteren in Power BI Desktop (preview)
description: Kruislings filteren inschakelen met DirectQuery in Power BI Desktop
services: powerbi
documentationcenter: 
author: davidiseminger
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
ms.date: 09/06/2017
ms.author: davidi
ms.openlocfilehash: 7946a9389897c4401e581482c0630547a764616d
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/15/2017
---
# <a name="bidirectional-cross-filtering-using-directquery-in-power-bi-desktop-preview"></a>In twee richtingen kruislings filteren met DirectQuery in Power BI Desktop (preview)

Als u tabellen filtert om een geschikte gegevensweergave te maken, hebben de makers van rapporten (en makers van gegevensmodellen) moeite om te bepalen hoe filters op een rapport moeten worden toegepast. De filtercontext van een tabel staat wel aan de ene kant van de relatie maar niet aan de andere, waardoor vaak complexe DAX-formules vereist zijn om het gewenste resultaat te verkrijgen.

Met kruislings filteren in twee richtingen hebben makers van rapporten (en makers van gegevensmodellen) meer controle over de manier waarop filters worden toegepast tijdens het werken met gerelateerde tabellen. Nu kunnen deze filters dus aan *beide* kanten van een tabelrelatie worden toegepast. Dit kan door de filtercontext door te voeren naar een tweede gerelateerde tabel aan de andere kant van de tabelrelatie.

Er is een [uitgebreid technische document](http://download.microsoft.com/download/2/7/8/2782DF95-3E0D-40CD-BFC8-749A2882E109/Bidirectional%20cross-filtering%20in%20Analysis%20Services%202016%20and%20Power%20BI.docx) (Engelstalig) beschikbaar waarin het kruislings filteren in twee richtingen in Power BI Desktop wordt uitgelegd (het technische document geldt ook voor SQL Server Analysis Services 2016, beide hebben hetzelfde gedrag).

* Whitepaper [Bidirectional cross-filtering for Power BI Desktop](http://download.microsoft.com/download/2/7/8/2782DF95-3E0D-40CD-BFC8-749A2882E109/Bidirectional%20cross-filtering%20in%20Analysis%20Services%202016%20and%20Power%20BI.docx) (Kruislings filteren in twee richtingen in Power BI Desktop) downloaden

### <a name="enabling-bidirectional-cross-filtering-for-directquery"></a>Kruislings filteren in twee richtingen voor DirectQuery inschakelen
Als u kruislings filteren in twee richtingen voor DirectQuery wilt gebruiken, moet u het eerst inschakelen. Dit zijn functies in een preview-versie, dus de beschikbaarheid en het gedrag ervan zijn onderhevig aan mogelijke wijzigingen in aanstaande releases van Power BI Desktop.

Als u kruislings filteren in twee richtingen voor DirectQuery in Power BI Desktop wilt inschakelen, selecteert u **Bestand > Opties en instellingen > Opties** en schakelt u het selectievakje in naast **Kruislings filteren in twee richtingen voor DirectQuery inschakelen**, zoals weergegeven in de volgende afbeelding.

![](media/desktop-bidirectional-filtering/bidirectional-filtering_1.png)

> [!NOTE]
> Gebruik *UserPrincipalName* (vaak dezelfde naam als die van de gebruiker bij aanmelden, bijvoorbeeld *joe@contoso.com*) in plaats van *UserName* als u DAX-formules voor kruislings filteren in Power BI Desktop gaat maken. Wellicht dient u dus een gerelateerde tabel te maken die *UserName* (of bijvoorbeeld EmployeeID) toewijst aan *UserPrincipleName*.
> 
> 

Als u kruislings filteren wilt inschakelen, dient u in het dialoogvenster **Relatie bewerken** het volgende te selecteren:

* **Kruisfilterrichting** moet zijn ingesteld op **Beide**
* **Beveiligingsfilter in beide richtingen toepassen** moet ook zijn geselecteerd
  
  ![](media/desktop-bidirectional-filtering/bidirectional-filtering_2.png)

Lees het eerder genoemde [whitepaper](http://download.microsoft.com/download/2/7/8/2782DF95-3E0D-40CD-BFC8-749A2882E109/Bidirectional%20cross-filtering%20in%20Analysis%20Services%202016%20and%20Power%20BI.docx) voor meer informatie en voorbeelden over de werking van kruislings filteren in twee richtingen.

