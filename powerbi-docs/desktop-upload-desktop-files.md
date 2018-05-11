---
title: Publiceren vanuit Power BI Desktop
description: Publiceren vanuit Power BI Desktop
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
ms.topic: get-started-article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 05/02/2018
ms.author: davidi
LocalizationGroup: Create reports
ms.openlocfilehash: f70088d4b6b064a72603bc59e6ba1e07cdb5e1b0
ms.sourcegitcommit: f679c05d029ad0765976d530effde744eac23af5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2018
---
# <a name="publish-from-power-bi-desktop"></a>Publiceren vanuit Power BI Desktop
Als u een **Power BI Desktop**-bestand publiceert naar de **Power BI-service**, worden de gegevens in het model en eventuele rapporten die u in de **rapportweergave** hebt gemaakt, gepubliceerd naar uw Power BI-werkruimte. U ziet een nieuwe gegevensset met dezelfde naam (en eventuele rapporten) in uw werkruimtenavigator.

Het publiceren vanuit **Power BI Desktop** heeft hetzelfde effect als **Gegevens ophalen** gebruiken in Power BI om verbinding te maken met een **Power BI Desktop**-bestand en er gegevens naar te uploaden.

> [!NOTE]
> Als u wijzigingen aanbrengt aan het Power BI-rapport (bijvoorbeeld visuele elementen toevoegen aan, verwijderen uit of wijzigen in rapporten), worden deze niet opgeslagen in het oorspronkelijke **Power BI Desktop**-bestand.
> 
> 

## <a name="to-publish-a-power-bi-desktop-dataset-and-reports"></a>Power BI Desktop-gegevenssets en -rapporten publiceren
1. In Power BI Desktop via \> **Bestand** \> **Publiceren** \> **Publiceren naar Power BI** of klik op **Publiceren** op het lint.  
   ![](media/desktop-upload-desktop-files/pbid_publish_publishbutton.png)
2. Meld u aan bij Power BI.

Als u klaar bent, ontvangt u een koppeling om uw rapport op uw Power BI-site te openen.  
    ![](media/desktop-upload-desktop-files/pbid_publish_success.png)

## <a name="re-publish-or-replace-a-dataset-published-from-power-bi-desktop"></a>Een vanuit Power BI Desktop gepubliceerde gegevensset opnieuw publiceren of vervangen
Als u een **Power BI Desktop**-bestand publiceert, worden de gegevensset en eventuele rapporten die u in **Power BI Desktop** hebt gemaakt, geüpload naar uw Power BI-site. Als u uw **Power BI Desktop**-bestand opnieuw publiceert, wordt de gegevensset op uw Power BI-site vervangen door de bijgewerkte gegevensset uit het **Power BI Desktop**-bestand.

Dit is allemaal erg eenvoudig, maar u mag een paar dingen niet vergeten:

* Als u al twee of meer gegevenssets in Power BI hebt met dezelfde naam als het **Power BI Desktop**-bestand, kan het publiceren mislukken. Zorg ervoor dat u slechts één gegevensset in Power BI hebt met dezelfde naam. U kunt het bestand ook een andere naam geven en dit publiceren, waardoor u een nieuwe gegevensset maakt met dezelfde naam als het bestand.
* Als u een kolom of meting verwijdert of een andere naam geeft, raken eventuele visuele elementen die al in Power BI met dat veld voorkomen, beschadigd. 
* Power BI negeert een aantal wijzigingen aan de indeling van bestaande kolommen. Bijvoorbeeld als u de indeling van een kolom wijzigt van 0,25 in 25%.
* Als u een vernieuwingsschema voor uw bestaande gegevensset in Power BI hebt geconfigureerd en u voegt nieuwe gegevensbronnen aan uw bestand toe om ze vervolgens opnieuw te publiceren, moet u zich bij deze gegevensbronnen aanmelden in *Gegevensbronnen beheren* voordat u een nieuwe, geplande vernieuwing uitvoert.

