---
title: Aanvullende diagnostische gegevens vastleggen
description: Aanvullende diagnostische gegevens vastleggen
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 06/28/2017
ms.author: mblythe
LocalizationGroup: Troubleshooting
ms.openlocfilehash: 76860e740d43a1907692a7cd4fed1a6df68c93d4
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2018
ms.locfileid: "34239217"
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

