---
title: Verbinding met SweetIQ maken via Power BI
description: SweetIQ voor Power BI
services: powerbi
documentationcenter: ''
author: SarinaJoan
manager: kfile
backup: maggiesMSFT
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: 61a32431e15950dd712e95779bda81bbf0ee6f43
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/24/2018
---
# <a name="connect-to-sweetiq-with-power-bi"></a>Verbinding met SweetIQ maken via Power BI
Met het Power BI-inhoudspakket worden gegevens opgehaald uit uw SweetIQ-account en wordt er een kant-en-klare gegevensset gegeneerd zodat u eenvoudig uw gegevens kunt verkennen. Gebruik het SweetIQ-inhoudspakket om gegevens te analyseren over uw locaties, vermeldingen, beoordelingen en recensies. De gegevens worden dagelijks vernieuwd, zodat u zeker weet dat uw bewakingsgegevens up-to-date zijn.

Maak verbinding met het [SweetIQ-inhoudspakket voor Power BI](https://app.powerbi.com/groups/me/getdata/services/sweetiq).

## <a name="how-to-connect"></a>Verbinding maken
1. Klik in het navigatiedeelvenster op aan de linkerkant op **Gegevens ophalen**.
   
    ![](media/service-connect-to-sweetiq/getdata.png)
2. Selecteer **SweetIQ** en klik op **Ophalen**.
   
    ![](media/service-connect-to-sweetiq/sweetiq.png)
3. Geef uw client-id voor SweetIQ op. Dit is meestal een alfanumerieke waarde. Meer informatie over het zoeken van deze waarde vindt u hieronder.
   
    ![](media/service-connect-to-sweetiq/parameter.png)
4. Selecteer het verificatietype **Sleutel** en geef uw Sweet IQ API-sleutel op. Dit is meestal een alfanumerieke waarde. Meer informatie over het zoeken van deze waarde vindt u hieronder.
   
    ![](media/service-connect-to-sweetiq/credentials.png)
5. Vervolgens worden de gegevens door Power BI geladen. Dit kan enige tijd duren, kan afhankelijk van de hoeveelheid gegevens in uw account. Zodra de gegevens zijn geladen, ziet u een nieuw dashboard, een nieuw rapport en een nieuwe gegevensset in het navigatiedeelvenster aan de linkerzijde.
   
    ![](media/service-connect-to-sweetiq/dashboard.png)

**Wat nu?**

* [Stel vragen in het vak Q&A](power-bi-q-and-a.md) boven in het dashboard.
* [Wijzig de tegels](service-dashboard-edit-tile.md) in het dashboard.
* [Selecteer een tegel](service-dashboard-tiles.md) om het onderliggende rapport te openen.
* Als uw gegevensset is ingesteld op dagelijks vernieuwen, kunt u het vernieuwingsschema wijzigen of de gegevensset handmatig vernieuwen met **Nu vernieuwen**

## <a name="finding-parameters"></a>Parameters zoeken
De client-id en API-sleutel voor dit inhoudspakket zijn niet gelijk aan uw SweetIQ-gebruikersnaam en -wachtwoord.

Selecteer een client-id voor een van de clients waartoe u toegang hebt met uw account. De lijst met clients bevindt zich in uw SweetIQ-account onder Clientbeheer.

Neem contact met de beheerder op over uw API-sleutel voor toegang tot de gegevens voor de specifieke client.

## <a name="next-steps"></a>Volgende stappen
[Aan de slag met Power BI](service-get-started.md)

[Gegevens ophalen voor Power BI](service-get-data.md)

