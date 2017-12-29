---
title: 'Zelfstudie: Power BI-integratie met Microsoft Flow'
description: Meer informatie over het maken van stromen die worden geactiveerd door Power BI-gegevenswaarschuwingen.
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: YhmNstC39Mw
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/30/2017
ms.author: mihart
ms.openlocfilehash: efab2e6be1d376a0da70c13bb66144ba34afa58c
ms.sourcegitcommit: f2b38777ca74c28f81b25e2f739e4835a0ffa75d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2017
---
# <a name="microsoft-flow-and-power-bi"></a>Microsoft Flow en Power BI

[Microsoft Flow](https://flow.microsoft.com/en-us/documentation/getting-started) is een SaaS voor het automatiseren van werkstromen voor het groeiende aantal apps en SaaS-services waarvan zakelijke gebruikers afhankelijk zijn. Met Flow kunt u taken automatiseren door uw favoriete apps en services (inclusief Power BI) te integreren om meldingen te ontvangen, bestanden te synchroniseren, gegevens te verzamelen en meer. U kunt eenvoudig herhalende taken uitvoeren door de werkstroom te automatiseren.

[Aan de slag met Flow.](https://flow.microsoft.com/documentation/getting-started)

Kijk hoe Sirui een stroom maakt waarmee een gedetailleerde e-mail naar collega's wordt verzonden wanneer een Power BI-waarschuwing wordt geactiveerd. Volg vervolgens de stapsgewijze instructies onder de video om het zelf te proberen.

<iframe width="560" height="315" src="https://www.youtube.com/embed/YhmNstC39Mw" frameborder="0" allowfullscreen></iframe>

## <a name="create-a-flow-that-is-triggered-by-a-power-bi-data-alert"></a>Een stroom maken die wordt geactiveerd door een Power BI-gegevensmelding
In deze zelfstudie wordt uitgelegd hoe u twee verschillende stromen maakt: een stroom op basis van een sjabloon en een compleet nieuwe stroom. Als u alles op de voet wilt volgen, [maakt u een gegevensmelding Power BI](service-set-data-alerts.md) en [meldt u zich aan voor Microsoft Flow](https://flow.microsoft.com/en-us/#home-signup) (gratis).

## <a name="create-a-flow-that-uses-power-bi---from-a-template"></a>Een stroom maken die gebruikmaakt van Power BI - op basis van een sjabloon
In deze taak gebruiken we een sjabloon om een eenvoudige stroom te maken die wordt geactiveerd door een Power BI-gegevenswaarschuwing (melding).

1. Meld u aan bij Microsoft Flow (flow.microsoft.com).
2. Selecteer **Mijn stromen**.
   
   ![](media/service-flow-integration/power-bi-my-flows.png)
3. Selecteer **Maken op basis van sjabloon**.
   
    ![](media/service-flow-integration/power-bi-template.png)
4. Gebruik het zoekvak om Power BI-sjablonen te zoeken en selecteer **Een bericht op een Slack-kanaal plaatsen wanneer een waarschuwing met betrekking tot Power BI-gegevens wordt geactiveerd**.
   
    ![](media/service-flow-integration/power-bi-template2.png)
5. Selecteer **Deze sjabloon gebruiken**.
   
   ![](media/service-flow-integration/power-bi-use-template.png)
6. Maak desgevraagd verbinding met Slack en Power BI door **Aanmelden** te selecteren en vervolgens de aanwijzingen te volgen. Een groen vinkje geeft aan dat u bent aangemeld.  Nadat u de verbindingen hebt bevestigd, selecteert u **Doorgaan**.
   
   ![](media/service-flow-integration/power-bi-flow-signin.png)

### <a name="build-the-flow"></a>De stroom bouwen
Deze sjabloon bevat één trigger (Power BI-gegevenswaarschuwing voor nieuwe Olympische medaille voor Ierland) en één actie (een bericht op Slack plaatsen). Wanneer u een veld selecteert, wordt er dynamische inhoud in Flow weergegeven die u kunt opnemen.  In dit voorbeeld hebt we de waarde en de URL van de tegel opgenomen in de berichttekst.

![](media/service-flow-integration/power-bi-flow-template.png)

1. Selecteer in de vervolgkeuzelijst met triggers een Power BI-gegevenswaarschuwing. Selecteer **Nieuwe medaille voor Ierland**. Zie [Gegevenswaarschuwingen in Power BI](service-set-data-alerts.md) als u wilt weten hoe een waarschuwing maakt.
   
   ![](media/service-flow-integration/power-bi-trigger-flow.png)
2. Als u een bericht op Slack wilt plaatsen, voert u een kanaalnaam en berichttekst in (u kunt ook het standaardbericht van Flow selecteren). Zoals u kunt zien, hebben we dynamische inhoud opgenomen in het berichttekstveld.
   
   > [!NOTE]
   > Plaats een @ voor de naam van het kanaal.  Als het Slack-kanaal bijvoorbeeld channelA is genoemd, voert u in Flow @channelA in.
   > 
   > 
   
   ![](media/service-flow-integration/power-bi-flow-slacker.png)
3. Zodra u bent klaar bent, selecteert u **Stroom maken** of **Stroom opslaan**.  De stroom is gemaakt en geëvalueerd.  Als er fouten worden aangetroffen, laat Flow u dit weten.
4. Als er fouten worden aangetroffen, selecteert u **Stroom bewerken** om ze te corrigeren. Selecteer anders **Gereed** om de nieuwe stroom uit te voeren.
   
   ![](media/service-flow-integration/power-bi-flow-running.png)
5. Open uw Slack-account om het bericht weer te geven.  
   
   ![](media/service-flow-integration/power-bi-slack-message.png)

## <a name="create-a-flow-that-uses-power-bi---from-scratch-blank"></a>Een stroom maken die gebruikmaakt van Power BI - compleet nieuw (leeg)
In deze taak maken we een eenvoudige maar volledig nieuwe stroom die wordt geactiveerd door een Power BI-gegevenswaarschuwing (melding).

1. Meld u aan bij Microsoft Flow.
2. Selecteer **Mijn stromen** > **Nieuwe stroom maken**.
   
   ![](media/service-flow-integration/power-bi-my-flows.png)
3. Gebruik het zoekvak om een Power BI-trigger te zoeken en selecteer **Een stroom activeren met een waarschuwing die is gebaseerd op Power BI-gegevens**.

### <a name="build-your-flow"></a>Uw stroom maken
1. Selecteer in de vervolgkeuzelijst de naam van de waarschuwing.  Zie [Gegevenswaarschuwingen in Power BI](service-set-data-alerts.md) als u wilt weten hoe een waarschuwing maakt.
   
    ![](media/service-flow-integration/power-bi-totalstores.png)
2. Selecteer **Nieuwe stap** > **Een actie toevoegen**.
   
   ![](media/service-flow-integration/power-bi-new-step.png)
3. Zoek **Outlook** en selecteer **Gebeurtenis maken**.
   
   ![](media/service-flow-integration/power-bi-create-event.png)
4. Vul de gebeurtenisvelden in. Wanneer u een veld selecteert, wordt er dynamische inhoud in Flow weergegeven die u kunt opnemen.
   
   ![](media/service-flow-integration/power-bi-flow-event.png)
5. Als u klaar bent, selecteert u **Stroom maken**.  De stroom wordt opgeslagen in Flow en geëvalueerd. Als er geen fouten zijn, selecteert u **Gereed** om de stroom uit te voeren.  De nieuwe stroom wordt toegevoegd aan de pagina **Mijn stromen**.
   
   ![](media/service-flow-integration/power-bi-flow-running.png)
6. Wanneer de stroom wordt geactiveerd door uw Power BI-gegevenswaarschuwing, ontvangt u een Outlook-gebeurtenismelding die vergelijkbaar is met de volgende.
   
    ![](media/service-flow-integration/power-bi-flow-notice.png)

## <a name="next-steps"></a>Volgende stappen
* [Aan de slag met Microsoft-Flow](https://flow.microsoft.com/en-us/documentation/getting-started/)
* [Gegevenswaarschuwingen instellen in de Power BI-service](service-set-data-alerts.md)
* [Gegevenswaarschuwingen instellen op uw iPhone](mobile-set-data-alerts-in-the-mobile-apps.md)
* [Gegevenswaarschuwingen instellen in de mobiele Power BI-app voor Windows 10](mobile-set-data-alerts-in-the-mobile-apps.md)
* Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

