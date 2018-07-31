---
title: Een streepjescodeveld in Power BI Desktop taggen voor de mobile apps
description: Wanneer u een streepjescodeveld tagt in uw model in Power BI Desktop kunt u gegevens voor streepjescodes automatisch filteren in de Power BI-app op uw iPhone.
author: maggiesMSFT
manager: kfile
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 01/16/2018
ms.author: maggies
LocalizationGroup: Model your data
ms.openlocfilehash: eb0d584e2383e1b878cfc26739e77d4e50d70a0f
ms.sourcegitcommit: df7a58dae14ef311516c9b3098f87742786f0479
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/27/2018
ms.locfileid: "39280473"
---
# <a name="tag-barcodes-in-power-bi-desktop-for-the-mobile-apps"></a>Streepjescodes in Power BI Desktop taggen voor de mobile apps
In Power BI Desktop kunt u [gegevens categoriseren](desktop-data-categorization.md) in een kolom, zodat Power BI Desktop weet hoe waarden in visuele elementen moeten worden afgehandeld in een rapport. U kunt een kolom categoriseren als **streepjescode**. Wanneer u of een van uw collega‘s [een streepjescode op een product scant met de Power BI-app](mobile-apps-scan-barcode-iphone.md) op de iPhone, ziet u een rapport met die streepjescode. Wanneer u het rapport in de mobile app opent, wordt het rapport in de mobile app automatisch door Power BI gefilterd tot gegevens die relevant zijn voor die streepjescode.

1. Schakel over naar Gegevensweergave in Power BI Desktop.
2. Selecteer een kolom met streepjescodegegevens. Zie de lijst met [ondersteunde streepjescode-indelingen](#supported-barcode-formats) hieronder.
3. Selecteer op het tabblad **Model maken** de optie **Gegevenscategorie** > **Streepjescode**.
   
    ![De lijst Gegevenscategorie](media/desktop-mobile-barcodes/power-bi-desktop-barcode.png)
4. Voeg dit veld in de rapportweergave toe aan de visuele elementen die u door de streepjescode wilt laten filteren.
5. Sla het rapport op en publiceer het naar de Power BI-service.

Wanneer u de scanner opent in de [Power BI-app voor iPhone](mobile-iphone-app-get-started.md) en een streepjescode scant, ziet u dit rapport in de lijst met rapporten. Wanneer u het rapport opent, zijn die visuele elementen gefilterd op de productstreepjescode die u hebt gescand.

## <a name="supported-barcode-formats"></a>Ondersteunde streepjescode-indelingen
Dit zijn de streepjescodes die door Power BI worden herkend als u deze kunt taggen in een Power BI-rapport: 

* UPCECode 
* Code39Code  
* A39Mod43Code 
* EAN13Code 
* EAN8Code  
* 93Code  
* 128Code 
* PDF417Code 
* Interleaved2of5Code 
* ITF14Code 

## <a name="next-steps"></a>Volgende stappen
* [Een streepjescode met de Power BI-app op uw iPhone scannen](mobile-apps-scan-barcode-iphone.md)
* [Problemen met het scannen van streepjescodes op een iPhone](mobile-apps-scan-barcode-iphone.md#issues-with-scanning-a-barcode)
* [Gegevenscategorisatie in Power BI Desktop](desktop-data-categorization.md)  
* Vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

