---
title: Instellingen voor gegevenssetparameters in Power BI-service weergeven en bewerken
description: Queryparameters worden gemaakt in Power BI Desktop, maar kunnen worden gecontroleerd en bijgewerkt in Power BI-service
author: mihart
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 06/26/2018
ms.author: mihart
LocalizationGroup: Create reports
ms.openlocfilehash: ac271e8013bce5824931153351a651644a716a2f
ms.sourcegitcommit: 5eb8632f653b9ea4f33a780fd360e75bbdf53b13
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/27/2018
ms.locfileid: "36965154"
---
# <a name="what-is-a-query-parameter"></a>Wat is een queryparameter?
Queryparameters worden door rapportmakers aan Power BI Desktop toegevoegd. Ze kunnen aan de hand van parameters gedeelten van rapporten maken die afhankelijk zijn van een of meerdere parameter*waarden*. Een maker van een rapport kan bijvoorbeeld een parameter maken waarmee de gegevens worden beperkt tot een land of regio of een parameter maken waarmee acceptabele indelingen worden opgegeven voor bijvoorbeeld datum-, tijd- en tekstvelden.

![Tabblad Start met de optie Parameters beheren in Desktop](media/service-parameters/power-bi-manage-parameters.png)


## <a name="review-and-edit-parameters-in-power-bi-service"></a>Parameters controleren en bewerken in Power BI-service

Nadat de parameters zijn gedefinieerd in Desktop, worden de parameterinstellingen bij het [publiceren van het rapport naar Power BI-service](desktop-upload-desktop-files.md) meegenomen in het rapport. Sommige parameterinstellingen kunnen worden gecontroleerd en bewerkt in Power BI-service, niet de parameters die de beschikbare gegevens beperken, maar de parameters waarmee acceptabele waarden worden gedefinieerd en beschreven.

1. Selecteer in Power BI-service het tandwielpictogram ![tandwielpictogram](media/service-parameters/power-bi-cog.png) om **Instellingen** te openen.

2. Selecteer het tabblad **Gegevenssets** en markeer een gegevensset in de lijst. 
    
    ![Het venster Instellingen waarin het tabblad Gegevenssets is geselecteerd](media/service-parameters/power-bi-select-dataset2.png)

3. Vouw **Parameters** uit.  Als de geselecteerde gegevensset geen parameters bevat, verschijnt een bericht met een koppeling naar Meer informatie over queryparameters. Als de gegevensset wel parameters bevat, worden deze weergegeven wanneer u **Parameters** uitvouwt. 

    ![Het venster Instellingen waarin Parameters is uitgevouwen](media/service-parameters/power-bi-settings.png)

    Controleer de parameterinstellingen en breng eventueel wijzigingen aan. Grijze velden kunnen niet worden bewerkt. 


## <a name="next-steps"></a>Volgende stappen
Een ad-hocmanier om eenvoudige parameters toe te voegen, is [de URL wijzigen](service-url-filters.md).