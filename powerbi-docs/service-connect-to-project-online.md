---
title: Verbinding maken met Project Online via Power BI
description: Project Online voor Power BI
author: SarinaJoan
manager: kfile
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: 52bd4b5dc27ff127eadea49cb3e761d6cda4788d
ms.sourcegitcommit: 2a7bbb1fa24a49d2278a90cb0c4be543d7267bda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/26/2018
ms.locfileid: "34249155"
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
    
Houd er rekening mee dat u machtigingen als Portfolioviewer, Portfoliomanager of beheerder moet hebben voor de Project Web App waarmee u verbinding maakt.

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

