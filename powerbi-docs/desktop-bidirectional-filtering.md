---
title: In twee richtingen kruislings filteren in Power BI Desktop
description: Kruislings filteren inschakelen met DirectQuery in Power BI Desktop
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 12/06/2018
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: bb4ac81556541c40cfb2e96cb2139be4ea1cb820
ms.sourcegitcommit: c8c126c1b2ab4527a16a4fb8f5208e0f7fa5ff5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2019
ms.locfileid: "54285456"
---
# <a name="bidirectional-cross-filtering-using-directquery-in-power-bi-desktop"></a>In twee richtingen kruislings filteren met DirectQuery in Power BI Desktop

Als u tabellen filtert om een geschikte gegevensweergave te maken, hebben de makers van rapporten (en makers van gegevensmodellen) moeite om te bepalen hoe filters op een rapport moeten worden toegepast. De filtercontext van een tabel staat wel aan de ene kant van de relatie maar niet aan de andere, waardoor vaak complexe DAX-formules vereist zijn om het gewenste resultaat te verkrijgen.

Met kruislings filteren in twee richtingen hebben makers van rapporten (en makers van gegevensmodellen) meer controle over de manier waarop filters worden toegepast tijdens het werken met gerelateerde tabellen. Nu kunnen deze filters dus aan *beide* kanten van een tabelrelatie worden toegepast. Dit kan door de filtercontext door te voeren naar een tweede gerelateerde tabel aan de andere kant van de tabelrelatie.

## <a name="detailed-whitepaper-for-bidirectional-cross-filtering"></a>Gedetailleerd technische document over kruislings filteren in twee richtingen
Er is een [uitgebreid technische document](http://download.microsoft.com/download/2/7/8/2782DF95-3E0D-40CD-BFC8-749A2882E109/Bidirectional%20cross-filtering%20in%20Analysis%20Services%202016%20and%20Power%20BI.docx) (Engelstalig) beschikbaar waarin het kruislings filteren in twee richtingen in Power BI Desktop wordt uitgelegd (het technische document geldt ook voor SQL Server Analysis Services 2016, beide hebben hetzelfde gedrag).

* Whitepaper [Bidirectional cross-filtering for Power BI Desktop](http://download.microsoft.com/download/2/7/8/2782DF95-3E0D-40CD-BFC8-749A2882E109/Bidirectional%20cross-filtering%20in%20Analysis%20Services%202016%20and%20Power%20BI.docx) (Kruislings filteren in twee richtingen in Power BI Desktop) downloaden

## <a name="enabling-bidirectional-cross-filtering-for-directquery"></a>Kruislings filteren in twee richtingen voor DirectQuery inschakelen

Als u kruislings filteren wilt inschakelen, dient u in het dialoogvenster **Relatie bewerken** het volgende te selecteren:

* **Kruisfilterrichting** moet zijn ingesteld op **Beide**
* **Beveiligingsfilter in beide richtingen toepassen** moet ook zijn geselecteerd

  ![](media/desktop-bidirectional-filtering/bidirectional-filtering_2.png)

> [!NOTE]
> Gebruik *UserPrincipalName* (vaak dezelfde naam als die van de gebruiker bij aanmelden, bijvoorbeeld <em>joe@contoso.com</em>) in plaats van *UserName* als u DAX-formules voor kruislings filteren in Power BI Desktop gaat maken. Wellicht moet u dus een gerelateerde tabel maken die *UserName* (of bijvoorbeeld EmployeeID) toewijst aan *UserPrincipleName*.

Lees het eerder genoemde [whitepaper](http://download.microsoft.com/download/2/7/8/2782DF95-3E0D-40CD-BFC8-749A2882E109/Bidirectional%20cross-filtering%20in%20Analysis%20Services%202016%20and%20Power%20BI.docx) voor meer informatie en voorbeelden over de werking van kruislings filteren in twee richtingen.

