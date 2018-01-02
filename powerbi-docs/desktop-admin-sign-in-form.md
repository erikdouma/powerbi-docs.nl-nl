---
title: Hoe beheerders het Power BI Desktop-aanmeldingsformulier kunnen beheren
description: Meer informatie over hoe u het formulier voor eerste aanmelding kunt beheren bij het openen van Power BI Desktop.
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
ms.date: 10/17/2017
ms.author: davidi
ms.openlocfilehash: eabb59b32234fce1ba5669b95abb41c4f7e04aa2
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2017
---
# <a name="how-administrators-can-manage-the-power-bi-desktop-sign-in-form"></a>Hoe beheerders het Power BI Desktop-aanmeldingsformulier kunnen beheren
De eerste keer dat Power BI Desktop wordt gestart, wordt een aanmeldingsformulier weergegeven. Er kunnen gegevens in worden ingevuld, of u kunt zich aanmelden bij Power BI om door te gaan. Beheerders kunnen dit formulier beheren met behulp van een registersleutel. 

![Formulier voor eerste aanmelding voor Power BI Desktop](media/desktop-admin-sign-in-form/sign-in-form.png)

Beheerders kunnen de volgende registersleutel gebruiken om het aanmeldingsformulier uit te schakelen. Dit kan ook worden geactiveerd met behulp van globaal beleid voor de gehele organisatie.

```
Key: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Power BI Desktop
valueName: ShowLeadGenDialog
```

Met een waarde van 0 wordt het dialoogvenster uitgeschakeld.

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

