---
title: Hoe beheerders het Power BI Desktop-aanmeldingsformulier kunnen beheren
description: Meer informatie over hoe u het formulier voor eerste aanmelding kunt beheren bij het openen van Power BI Desktop.
services: powerbi
documentationcenter: ''
author: davidiseminger
manager: kfile
backup: ''
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 04/24/2018
ms.author: davidi
ms.openlocfilehash: 65bf0a39351b394232211af50692072f7cec7e89
ms.sourcegitcommit: 3f2f254f6e8d18137bae879ddea0784e56b66895
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/26/2018
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

