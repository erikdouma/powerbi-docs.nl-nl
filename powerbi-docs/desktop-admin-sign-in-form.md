---
title: Hoe beheerders het Power BI Desktop-aanmeldingsformulier kunnen beheren
description: Meer informatie over hoe u het formulier voor eerste aanmelding kunt beheren bij het openen van Power BI Desktop.
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 04/24/2018
ms.author: davidi
ms.openlocfilehash: 98bf9579ae7ee551634eed765138c0e78156464c
ms.sourcegitcommit: 998b79c0dd46d0e5439888b83999945ed1809c94
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/17/2018
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

