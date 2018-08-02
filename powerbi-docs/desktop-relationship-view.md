---
title: Relatieweergave in Power BI Desktop
description: Relatieweergave in Power BI Desktop
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 07/27/2018
ms.author: davidi
LocalizationGroup: Model your data
ms.openlocfilehash: 33541b99d28bd95acb9cc923e0531cdbc2e25d63
ms.sourcegitcommit: fbb7924603f8915d07b5e6fc8f4d0c7f70c1a1e1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2018
ms.locfileid: "39327126"
---
# <a name="relationship-view-in-power-bi-desktop"></a>Relatieweergave in Power BI Desktop
In de **relatieweergave** worden alle tabellen, kolommen en relaties in uw model weergegeven. Dit kan met name handig zijn als uw model complexe relaties heeft tussen veel tabellen.

Laten we dit eens bekijken.

![](media/desktop-relationship-view/relationshipview_fullscreen.png)

**A.**  Het pictogram Relatieweergave: klik hierop om uw model in de relatieweergave weer te geven

**B.** Relatie: u kunt uw cursor over een relatie bewegen om de gebruikte kolommen weer te geven. Dubbelklik op een relatie om deze te openen in het dialoogvenster **Relatie bewerken**. 

In de bovenstaande afbeelding kunt u zien dat de tabel *Stores* een kolom *StoreKey* bevat die is gerelateerd aan de tabel *Sales* die ook een kolom *StoreKey* bevat. We zien dat het een *veel-op-één*-relatie (\*:1) is, en het pictogram in het midden van de regel laat zien dat de richting van het kruisfilter is ingesteld op *beide*. De pijl op het pictogram geeft de richting van de filtercontextstroom aan.

Zie [Relaties maken en beheren in Power BI Desktop](desktop-create-and-manage-relationships.md) voor meer informatie over relaties.

