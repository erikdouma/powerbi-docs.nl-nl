---
title: Relatieweergave in Power BI Desktop
description: Relatieweergave in Power BI Desktop
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
ms.date: 12/06/2017
ms.author: davidi
LocalizationGroup: Model your data
ms.openlocfilehash: e94977a8b9a106798f0facd962d6e766f6410da3
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/24/2018
---
# <a name="relationship-view-in-power-bi-desktop"></a>Relatieweergave in Power BI Desktop
In de **relatieweergave** worden alle tabellen, kolommen en relaties in uw model weergegeven. Dit kan met name handig zijn als uw model complexe relaties heeft tussen veel tabellen.

Laten we dit eens bekijken.

![](media/desktop-relationship-view/relationshipview_fullscreen.png)

**A.**  Het pictogram Relatieweergave: klik hierop om uw model in de relatieweergave weer te geven

**B.** Relatie: u kunt uw cursor over een relatie bewegen om de gebruikte kolommen weer te geven. Dubbelklik op een relatie om deze te openen in het dialoogvenster **Relatie bewerken**. 

In de bovenstaande afbeelding kunt u zien dat de tabel *Stores* een kolom *StoreKey* bevat die is gerelateerd aan de tabel *Sales* die ook een kolom *StoreKey* bevat. We zien dat het een *veel-op-één*-relatie (\*:1) is, en het pictogram in het midden van de regel laat zien dat de richting van het kruisfilter is ingesteld op *beide*. De pijl op het pictogram geeft de richting van de filtercontextstroom aan.

Zie [Relaties maken en beheren in Power BI Desktop](desktop-create-and-manage-relationships.md) voor meer informatie over relaties.

