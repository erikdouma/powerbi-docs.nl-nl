---
title: Waar bevindt mijn Power BI-tenant zich?
description: Informatie over waar uw Power BI-tenant zich bevindt en hoe deze locatie wordt geselecteerd. Het is belangrijk dat u dit begrijpt, omdat dit gevolgen kan hebben voor interacties die u met de service hebt.
services: powerbi
documentationcenter: 
author: markingmyname
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
ms.date: 08/10/2017
ms.author: maghan
ms.openlocfilehash: 51d54d0ee8f21eec076389c1370f7bad415fa412
ms.sourcegitcommit: 6e693f9caf98385a2c45890cd0fbf2403f0dbb8a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2018
---
# <a name="where-is-my-power-bi-tenant-located"></a>Waar bevindt mijn Power BI-tenant zich?
<iframe width="560" height="315" src="https://www.youtube.com/embed/0fOxaHJPvdM?showinfo=0" frameborder="0" allowfullscreen></iframe>

Informatie over waar uw Power BI-tenant zich bevindt en hoe deze locatie wordt geselecteerd. Het is belangrijk dat u dit begrijpt, omdat dit gevolgen kan hebben voor interacties die u met de service hebt.

## <a name="how-to-determine-where-your-power-bi-tenant-is-located"></a>Bepalen waar uw Power BI-tenant zich bevindt
U kunt het volgende doen om de regio te zoeken waarin uw tenant zich bevindt.

1. Selecteer het **?** in de Power BI-service.
2. Selecteer **Over Power BI**.
3. Kijk naar de waarde naast **Uw gegevens worden opgeslagen in**. Dit is de regio waarin u zich bevindt.

![](media/service-admin-where-is-my-tenant-located/power-bi-data-region.png)

## <a name="how-the-data-region-is-selected"></a>Hoe de gegevensregio wordt geselecteerd
De gegevensregio is gebaseerd op het land dat werd geselecteerd toen de tenant werd gemaakt. Dit geldt voor de aanmelding voor zowel Office 365 als Power BI, aangezien deze informatie wordt gedeeld. Als dit een nieuwe tenant is, ziet u een vervolgkeuzelijst met landen wanneer u zich aanmeldt.

![](media/service-admin-where-is-my-tenant-located/sign-up-country-selection.png)

Deze selectie bepaalt op welke locatie uw gegevens worden opgeslagen. Power BI kiest een gegevensregio die het dichtst bij deze selectie ligt.

> [!WARNING]
> Deze selectie kan niet worden gewijzigd!
> 
> 

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

