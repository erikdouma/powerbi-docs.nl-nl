---
title: Relatieweergave in Power BI Desktop
description: Relatieweergave in Power BI Desktop
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 05/02/2018
ms.author: davidi
LocalizationGroup: Model your data
ms.openlocfilehash: 58886dc1ae5490113d4d0ba9af00d16aefecbe71
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2018
ms.locfileid: "34287021"
---
# <a name="relationship-view-in-power-bi-desktop"></a>Relatieweergave in Power BI Desktop
In de **relatieweergave** worden alle tabellen, kolommen en relaties in uw model weergegeven. Dit kan met name handig zijn als uw model complexe relaties heeft tussen veel tabellen.

Laten we dit eens bekijken.

![](media/desktop-relationship-view/relationshipview_fullscreen.png)

**A.**  Het pictogram Relatieweergave: klik hierop om uw model in de relatieweergave weer te geven

**B.** Relatie: u kunt uw cursor over een relatie bewegen om de gebruikte kolommen weer te geven. Dubbelklik op een relatie om deze te openen in het dialoogvenster **Relatie bewerken**. 

In de bovenstaande afbeelding kunt u zien dat de tabel *Stores* een kolom *StoreKey* bevat die is gerelateerd aan de tabel *Sales* die ook een kolom *StoreKey* bevat. We zien dat het een *veel-op-één*-relatie (\*:1) is, en het pictogram in het midden van de regel laat zien dat de richting van het kruisfilter is ingesteld op *beide*. De pijl op het pictogram geeft de richting van de filtercontextstroom aan.

Zie [Relaties maken en beheren in Power BI Desktop](desktop-create-and-manage-relationships.md) voor meer informatie over relaties.

