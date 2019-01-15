---
title: Waar bevindt mijn Power BI-tenant zich?
description: Informatie over waar uw Power BI-tenant zich bevindt en hoe deze locatie wordt geselecteerd. Het is belangrijk dat u dit begrijpt, omdat dit gevolgen kan hebben voor interacties die u met de service hebt.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 10/31/2018
ms.author: mblythe
LocalizationGroup: Administration
ms.openlocfilehash: e71844110eb3452cbcb3b224bbca9db57475367e
ms.sourcegitcommit: c8c126c1b2ab4527a16a4fb8f5208e0f7fa5ff5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2019
ms.locfileid: "54282167"
---
# <a name="where-is-my-power-bi-tenant-located"></a>Waar bevindt mijn Power BI-tenant zich?

<iframe width="560" height="315" src="https://www.youtube.com/embed/0fOxaHJPvdM?showinfo=0" frameborder="0" allowfullscreen></iframe>

Informatie over waar uw Power BI-tenant zich bevindt en hoe deze locatie wordt geselecteerd. Het is belangrijk om bekend te zijn met de locatie omdat deze van invloed kan zijn op interacties met de service.

## <a name="how-to-determine-where-your-power-bi-tenant-is-located"></a>Bepalen waar uw Power BI-tenant zich bevindt

Volg deze stappen om vast te stellen in welke regio uw tenant zich bevindt.

1. Selecteer in de Power BI-service in het bovenste menu Help (**?**) en vervolgens **Over Power BI**.

1. Kijk naar de waarde naast **Uw gegevens worden opgeslagen in**. Dit is de regio waar uw tenant zich bevindt.

    ![Gegevensgebied](media/service-admin-where-is-my-tenant-located/power-bi-data-region.png)

## <a name="how-the-data-region-is-selected"></a>Hoe de gegevensregio wordt geselecteerd

Het gegevensgebied is gebaseerd op het land dat u selecteert bij het maken van de tenant. Dit geldt voor de registratie voor zowel Office 365 als Power BI, aangezien deze informatie wordt gedeeld. Als dit een nieuwe tenant is, selecteert u het juiste land uit de lijst wanneer u zich registreert.

![Land/regio selecteren](media/service-admin-where-is-my-tenant-located/sign-up-country-selection.png)

Power BI kiest een gegevensgebied het dichtst in de buurt van deze selectie, waarmee wordt bepaald waar gegevens voor uw tenant worden opgeslagen.

> [!IMPORTANT]
> U kunt deze selectie niet wijzigen nadat u de tenant hebt gemaakt.

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

