---
title: Een visueel Power BI-element optimaliseren voor elke grootte
description: Informatie over het optimaliseren van visuele Power BI-elementen en de Power BI-service voor de mobiele Power BI-apps.
services: powerbi
documentationcenter: 
author: maggiesMSFT
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
ms.date: 10/13/2017
ms.author: maggies
LocalizationGroup: Create reports
ms.openlocfilehash: 4c80048213b20365102bcb9c6842c342d8b9052b
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/24/2018
---
# <a name="optimize-a-power-bi-visual-for-any-size"></a>Een visueel Power BI-element optimaliseren voor elke grootte
U kunt de visuele elementen in uw dashboard of rapport zodanig instellen dat ze *responsief* zijn. Dat wil zeggen dat ze dynamisch worden gewijzigd zodat ze de maximale hoeveelheid gegevens weergeven, ongeacht de schermgrootte.

Als de grootte van een visueel element verandert, geeft Power BI de prioriteit aan de gegevensweergave, bijvoorbeeld door automatisch de opvulling te verwijderen en de legenda naar de bovenkant van het visuele element te verplaatsen, zodat het visuele element ook als het kleiner wordt informatief blijft. Reactietijd is met name nuttig in visuele elementen in de mobiele Power BI-app op telefoons.

![Reactietijd bij het wijzigen van de grootte van visuele elementen](media/desktop-create-responsive-visuals/power-bi-responsive-visual.gif)

U kunt de reactietijd voor elk visueel element inschakelen met de X- en Y-as en met slicers.

## <a name="turn-on-responsiveness-in-power-bi-desktop"></a>Reactietijd inschakelen in Power BI Desktop
1. Zorg er in Power BI Desktop op het tabblad **Weergeven** voor dat u in de modus **Bureaubladindeling** bent.
   
    ![Het pictogram Bureaubladindeling](media/desktop-create-responsive-visuals/power-bi-desktop-layout.png)
2. Selecteer een visueel element en selecteer in het deelvenster **Visualisaties** de sectie **Indeling**.
3. Vouw **Algemeen** uit > schuif **Responsief** naar **Aan**.
   
    ![Responsief aan](media/desktop-create-responsive-visuals/power-bi-turn-responsive-on.png)
   
     Wanneer u nu [een voor de telefoon geoptimaliseerd rapport maakt](desktop-create-phone-report.md) en dit visuele element toevoegt, wordt de grootte ervan correct aangepast.

## <a name="turn-on-responsiveness-in-the-power-bi-service"></a>Reactietijd inschakelen in de Power BI-service
U schakelt reactietijd voor een visueel element in een rapport in de Power BI-service in. U moet het rapport kunnen bewerken.

1. Selecteer in een rapport in de Power BI-service ([https://powerbi.com](https://powerbi.com)), de optie **Rapport bewerken**.
2. Selecteer een visueel element en selecteer in het deelvenster **Visualisaties** de sectie **Indeling**.
3. Vouw **Algemeen** uit > schuif **Responsief** naar **Aan**.
   
    ![Responsief aan](media/desktop-create-responsive-visuals/power-bi-turn-responsive-on.png)
   
     Wanneer u nu [een telefoonweergave van een dashboard maakt](service-create-dashboard-mobile-phone-view.md) en dit visuele element toevoegt, wordt de grootte ervan correct aangepast.

## <a name="next-steps"></a>Volgende stappen
* [Rapporten maken die zijn geoptimaliseerd voor de mobiele Power BI-apps](desktop-create-phone-report.md)
* [Een telefoonweergave van een dashboard maken in Power BI](service-create-dashboard-mobile-phone-view.md)
* [Voor uw telefoon geoptimaliseerde Power BI-rapporten weergeven](mobile-apps-view-phone-report.md)
* Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

