---
title: Verbinding maken met Project Online via Power BI
description: Project Online voor Power BI
services: powerbi
documentationcenter: 
author: SarinaJoan
manager: kfile
backup: maggiesMSFT
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: 6272b3f175d7da851e5d8086c574a91f0f00c933
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/24/2018
---
# <a name="connect-to-project-online-with-power-bi"></a>Verbinding maken met Project Online via Power BI
Microsoft Project Online is een flexibele onlineoplossing voor beheer van projectportfolio's (Project Portfolio Management; PPM) en dagelijkse werkzaamheden. Met Project Online kunnen organisaties meteen aan de slag, projectportfolio-investeringen prioriteren en de beoogde bedrijfswaarde leveren. Gebruik het Project Online-inhoudspakket voor Power BI om de projectgegevens verkennen met kant-en-klare metrische gegevens, zoals portfoliostatus- en naleving.

Maak verbinding met het [Project Online-inhoudspakket](https://app.powerbi.com/getdata/services/project-online) voor Power BI.

## <a name="how-to-connect"></a>Verbinding maken
1. Selecteer **Gegevens ophalen** onder in het linkernavigatievenster.
   
    ![](media/service-connect-to-project-online/getdata.png)
2. Selecteer in het vak **Services** de optie **Ophalen**.
   
   ![](media/service-connect-to-project-online/services.png)
3. Selecteer **Microsoft Project Online** \> **Ophalen**.
   
   ![](media/service-connect-to-project-online/mproject.png)
4. Voer in het tekstvak **Project Web App-URL** de URL in voor de Project Web Add (PWA) toe waarmee u wilt verbinden en kies **Volgende**. Houd er rekening mee dat deze instructie kan afwijken van het voorbeeld als u een aangepast domein hebt.
   
    ![](media/service-connect-to-project-online/params.png)
5. Selecteer voor de verificatiemethode **oAuth2** \> **Aanmelden**. Geef uw Project Online-referenties op als u hierom wordt gevraagd en voer het verificatieproces uit.
   
    ![](media/service-connect-to-project-online/creds.png)
6. U ziet een melding dat uw gegevens geladen worden. Dit kan enige tijd duren, afhankelijk van de grootte van uw account. Nadat de gegevens in Power BI zijn geïmporteerd, ziet u een nieuw dashboard, een nieuw rapport en een nieuwe gegevensset in het navigatiedeelvenster aan de linkerzijde. Dit is het standaarddashboard dat door Power BI is gemaakt om uw gegevens weer te geven. U kunt dit dashboard wijzigen om uw gegevens weer te geven zoals u dat wilt.
   
   ![](media/service-connect-to-project-online/dashboard2.png)

**Wat nu?**

* [Stel vragen in het vak Q&A](power-bi-q-and-a.md) boven in het dashboard.
* [Wijzig de tegels](service-dashboard-edit-tile.md) in het dashboard.
* [Selecteer een tegel](service-dashboard-tiles.md) om het onderliggende rapport te openen.
* Als uw gegevensset is ingesteld op dagelijks vernieuwen, kunt u het vernieuwingsschema wijzigen of de gegevensset handmatig vernieuwen met **Nu vernieuwen**

## <a name="next-steps"></a>Volgende stappen
[Aan de slag in Power BI](service-get-started.md)

[Gegevens ophalen in Power BI](service-get-data.md)

