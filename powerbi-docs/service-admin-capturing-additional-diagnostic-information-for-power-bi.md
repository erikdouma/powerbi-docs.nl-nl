---
title: Aanvullende diagnostische gegevens vastleggen
description: Aanvullende diagnostische gegevens vastleggen
services: powerbi
documentationcenter: ''
author: mgblythe
manager: kfile
backup: ''
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 06/28/2017
ms.author: mblythe
LocalizationGroup: Troubleshooting
ms.openlocfilehash: 9aef989b4b61ce8c9d11fd4275d68c867791f644
ms.sourcegitcommit: 8552a34df8e6141eb704314c1a019992901d6e78
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/08/2018
---
# <a name="capturing-additional-diagnostic-information"></a>Aanvullende diagnostische gegevens vastleggen
## <a name="capturing-additional-diagnostic-information-for-power-bi"></a>Aanvullende diagnostische gegevens vastleggen voor Power BI
Deze instructies bieden twee mogelijke opties voor het handmatig verzamelen van aanvullende diagnostische gegevens van de Power BI-webclient.  Slechts een van deze opties moet worden gevolgd.

## <a name="network-capture---edge--internet-explorer"></a>Vastleggen van netwerk - Microsoft Edge en Internet Explorer
1. Ga naar [Power BI](https://app.powerbi.com) met Microsoft Edge of Internet Explorer.
2. Open de ontwikkelhulpprogramma's van Microsoft Edge door op F12 te drukken.
3. Hiermee opent u het venster voor ontwikkelhulpprogramma's: 
   
   ![](media/service-admin-capturing-additional-diagnostic-information-for-power-bi/edge-developer-tools.png)
4. Ga naar het tabblad Netwerk. Hier wordt een lijst weergegeven met het verkeer dat al is vastgelegd. 
   
   ![](media/service-admin-capturing-additional-diagnostic-information-for-power-bi/edge-network-tab.png)
5. U kunt in het venster bladeren en elk probleem dat u mogelijk tegen bent gekomen reproduceren. U kunt het venster voor ontwikkelhulpprogramma's op elk gewenst moment tijdens de sessie verbergen door op F12 te drukken.
6. Als u wilt stoppen met het vastleggen, kunt u het rode vierkant selecteren op het tabblad Netwerk van het gedeelte voor ontwikkelhulpprogramma's.
   
   ![](media/service-admin-capturing-additional-diagnostic-information-for-power-bi/edge-network-tab-stop.png)
7. Selecteer het pictogram van een diskette om te **exporteren als HAR**
   
   ![](media/service-admin-capturing-additional-diagnostic-information-for-power-bi/edge-network-tab-save.png)
8. Geef een bestandsnaam op en sla het HAR-bestand op.
   
    Het HAR-bestand bevat alle informatie over netwerkaanvragen tussen het browservenster en Power BI.  Dit is informatie zoals de activiteits-id's voor elke aanvraag, de exacte tijdstempel voor elke aanvraag en alle foutinformatie die wordt geretourneerd door de client.  Deze tracering bevat ook de gegevens die worden gebruikt voor het vullen van de visuele elementen die op het scherm worden weergegeven.
9. U kunt het HAR-bestand naar ondersteuning verzenden voor controle.

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

