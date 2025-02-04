---
title: Verbinding maken met Zendesk met Power BI
description: Zendesk voor Power BI
author: SarinaJoan
manager: kfile
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.subservice: powerbi-template-apps
ms.topic: conceptual
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: 72b934357ec4208fa07266143b08af861659e465
ms.sourcegitcommit: 750f0bfab02af24c8c72e6e9bbdd876e4a7399de
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/04/2019
ms.locfileid: "54008322"
---
# <a name="connect-to-zendesk-with-power-bi"></a>Verbinding maken met Zendesk met Power BI
Het Zendesk-inhoudspakket biedt een Power BI-dashboard en een set Power BI-rapporten die inzicht geven in uw ticketaantallen en agentprestaties. U kunt het dashboard en de rapporten zó gebruiken, of ze aanpassen om de informatie die u het belangrijkst vindt eruit te laten springen.  De gegevens worden eenmaal per dag automatisch vernieuwd. 

Maak verbinding met het [Zendesk-inhoudspakket](https://app.powerbi.com/getdata/services/zendesk) of lees meer over de [Zendesk-integratie](https://powerbi.microsoft.com/integrations/zendesk) met Power BI.

>[!NOTE]
>Er is een Zendesk-beheerdersaccount vereist om verbinding te maken. Meer informatie over de [vereisten](#Requirements) volgt hieronder.

## <a name="how-to-connect"></a>Verbinding maken
1. Selecteer **Gegevens ophalen** onder in het linkernavigatievenster.
   
   ![](media/service-connect-to-zendesk/pbi_getdata.png)
2. Selecteer in het vak **Services** de optie **Ophalen**.
   
   ![](media/service-connect-to-zendesk/pbi_getservices.png) 
3. Selecteer **Zendesk** \> **Ophalen.**
   
   ![](media/service-connect-to-zendesk/zendesk.png)
4. Geef de URL die is gekoppeld aan uw account. Deze staat in het formulier **https://company.zendesk.com**, zie details over het [zoeken van deze parameters](#FindingParams) hieronder.
   
   ![](media/service-connect-to-zendesk/pbi_zendeskconnect.png)
5. Geef desgevraagd uw Zendesk-referenties op.  Selecteer **oAuth 2** als verificatiemethode en klik op **Aanmelden**. Volg de Zendesk-verificatieprocedure. (Als u al bent aangemeld bij Zendesk in uw browser, ontvangt u mogelijk geen prompt om referenties in te voeren.)
   
   > [!NOTE]
   > Dit inhoudspakket vereist dat u verbinding maakt met een Zendesk-beheerdersaccount. 
   > 
   > 
   
   ![](media/service-connect-to-zendesk/pbi_zendesksignin.png)
6. Klik op **Toestaan** om Power BI toegang te geven tot uw Zendesk-gegevens.
   
   ![](media/service-connect-to-zendesk/zendesk2.jpg)
7. Klik op **Verbinding maken** om het importproces te starten. Nadat de gegevens in Power BI zijn geïmporteerd, ziet u een nieuw dashboard, een nieuw rapport en een nieuwe gegevensset in het navigatiedeelvenster aan de linkerzijde. Nieuwe items zijn gemarkeerd met een geel sterretje \*.
   
   ![](media/service-connect-to-zendesk/pbi_zendeskdash.png)

**Wat nu?**

* [Stel vragen in het vak Q&A](consumer/end-user-q-and-a.md) boven in het dashboard.
* [Wijzig de tegels](service-dashboard-edit-tile.md) in het dashboard.
* [Selecteer een tegel](consumer/end-user-tiles.md) om het onderliggende rapport te openen.
* Als uw gegevensset is ingesteld op dagelijks vernieuwen, kunt u het vernieuwingsschema wijzigen of de gegevensset handmatig vernieuwen met **Nu vernieuwen**

## <a name="whats-included"></a>Wat is inbegrepen
Het Power BI-inhoudspakket bevat gegevens over het volgende:  

* Gebruikers (eindgebruikers en agents)  
* Organisaties  
* Groepen  
* Tickets  

Er is ook een set metingen die zijn berekend, zoals gemiddelde wachttijd en opgeloste tickets in de afgelopen 7 dagen. Een volledige lijst is opgenomen in het inhoudspakket.

<a name="Requirements"></a>

## <a name="system-requirements"></a>Systeemvereisten
Een Zendesk-beheerdersaccount is vereist voor toegang tot het Zendesk-inhoudspakket. Als u een agent of een gebruiker bent en u wilt uw Zendesk-gegevens weergeven, voeg een suggestie toe en controleer de Zendesk-connector in de [Power BI Desktop](desktop-connect-to-data.md).

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Parameters zoeken
De URL van uw Zendesk is hetzelfde als de URL die u gebruikt bij het aanmelden bij uw Zendesk-account. Als u niet zeker weet wat uw Zendesk-URL is, kunt u de [hulp bij aanmelden](https://www.zendesk.com/login/) van Zendesk gebruiken.

## <a name="troubleshooting"></a>Probleemoplossing
Als u problemen ondervindt bij het maken van verbinding, controleer dan uw Zendesk-URL en bevestig dat u een Zendesk-beheerdersaccount gebruikt.

## <a name="next-steps"></a>Volgende stappen
* [Wat is Power BI?](power-bi-overview.md)
* [Gegevens ophalen](service-get-data.md)

