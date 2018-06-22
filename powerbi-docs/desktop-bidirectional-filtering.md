---
title: In twee richtingen kruislings filteren in Power BI Desktop
description: Kruislings filteren inschakelen met DirectQuery in Power BI Desktop
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 04/24/2018
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: a584d61e1f2f55c244b453e6c086f3222217ee9a
ms.sourcegitcommit: 638de55f996d177063561b36d95c8c71ea7af3ed
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/17/2018
ms.locfileid: "34288999"
---
# <a name="bidirectional-cross-filtering-using-directquery-in-power-bi-desktop"></a>In twee richtingen kruislings filteren met DirectQuery in Power BI Desktop

Als u tabellen filtert om een geschikte gegevensweergave te maken, hebben de makers van rapporten (en makers van gegevensmodellen) moeite om te bepalen hoe filters op een rapport moeten worden toegepast. De filtercontext van een tabel staat wel aan de ene kant van de relatie maar niet aan de andere, waardoor vaak complexe DAX-formules vereist zijn om het gewenste resultaat te verkrijgen.

Met kruislings filteren in twee richtingen hebben makers van rapporten (en makers van gegevensmodellen) meer controle over de manier waarop filters worden toegepast tijdens het werken met gerelateerde tabellen. Nu kunnen deze filters dus aan *beide* kanten van een tabelrelatie worden toegepast. Dit kan door de filtercontext door te voeren naar een tweede gerelateerde tabel aan de andere kant van de tabelrelatie.

Er is een [uitgebreid technische document](http://download.microsoft.com/download/2/7/8/2782DF95-3E0D-40CD-BFC8-749A2882E109/Bidirectional%20cross-filtering%20in%20Analysis%20Services%202016%20and%20Power%20BI.docx) (Engelstalig) beschikbaar waarin het kruislings filteren in twee richtingen in Power BI Desktop wordt uitgelegd (het technische document geldt ook voor SQL Server Analysis Services 2016, beide hebben hetzelfde gedrag).

* Whitepaper [Bidirectional cross-filtering for Power BI Desktop](http://download.microsoft.com/download/2/7/8/2782DF95-3E0D-40CD-BFC8-749A2882E109/Bidirectional%20cross-filtering%20in%20Analysis%20Services%202016%20and%20Power%20BI.docx) (Kruislings filteren in twee richtingen in Power BI Desktop) downloaden

### <a name="enabling-bidirectional-cross-filtering-for-directquery"></a>Kruislings filteren in twee richtingen voor DirectQuery inschakelen

Als u kruislings filteren wilt inschakelen, dient u in het dialoogvenster **Relatie bewerken** het volgende te selecteren:

* **Kruisfilterrichting** moet zijn ingesteld op **Beide**
* **Beveiligingsfilter in beide richtingen toepassen** moet ook zijn geselecteerd
  
  ![](media/desktop-bidirectional-filtering/bidirectional-filtering_2.png)

> [!NOTE]
> Gebruik *UserPrincipalName* (vaak dezelfde naam als die van de gebruiker bij aanmelden, bijvoorbeeld *joe@contoso.com*) in plaats van *UserName* als u DAX-formules voor kruislings filteren in Power BI Desktop gaat maken. Wellicht dient u dus een gerelateerde tabel te maken die *UserName* (of bijvoorbeeld EmployeeID) toewijst aan *UserPrincipleName*.
> 
> 

Lees het eerder genoemde [whitepaper](http://download.microsoft.com/download/2/7/8/2782DF95-3E0D-40CD-BFC8-749A2882E109/Bidirectional%20cross-filtering%20in%20Analysis%20Services%202016%20and%20Power%20BI.docx) voor meer informatie en voorbeelden over de werking van kruislings filteren in twee richtingen.

