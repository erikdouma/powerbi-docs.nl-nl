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
ms.date: 01/22/2018
ms.author: mihart
ms.openlocfilehash: edae145e8eef6dfe7a2c4cea3a7f467f6f7961a9
ms.sourcegitcommit: c3be4de522874fd73fe6854333b379b85619b907
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/24/2018
---
# <a name="microsoft-flow-and-power-bi"></a>Microsoft Flow en Power BI

[Microsoft Flow](https://flow.microsoft.com/en-us/documentation/getting-started) is een SaaS voor het automatiseren van werkstromen voor het groeiende aantal apps en SaaS-services waarvan zakelijke gebruikers afhankelijk zijn. Met Flow kunt u taken automatiseren door uw favoriete apps en services (inclusief Power BI) te integreren om meldingen te ontvangen, bestanden te synchroniseren, gegevens te verzamelen en meer. U kunt eenvoudig herhalende taken uitvoeren door de werkstroom te automatiseren.

[Aan de slag met Flow.](https://flow.microsoft.com/documentation/getting-started)

Kijk hoe Sirui een stroom maakt waarmee een gedetailleerde e-mail naar collega's wordt verzonden wanneer een Power BI-waarschuwing wordt geactiveerd. Volg vervolgens de stapsgewijze instructies onder de video om het zelf te proberen.

<iframe width="560" height="315" src="https://www.youtube.com/embed/YhmNstC39Mw" frameborder="0" allowfullscreen></iframe>

## <a name="create-a-flow-that-is-triggered-by-a-power-bi-data-alert"></a>Een stroom maken die wordt geactiveerd door een Power BI-gegevensmelding

### <a name="prerequisites"></a>Vereisten
In deze zelfstudie wordt uitgelegd hoe u twee verschillende stromen maakt: een stroom op basis van een sjabloon en een compleet nieuwe stroom. Als u alles op de voet wilt volgen, [maakt u een gegevensmelding in Power BI](service-set-data-alerts.md), maakt u een gratis Slack-account en [meldt u zich aan voor Microsoft Flow](https://flow.microsoft.com/en-us/#home-signup) (gratis).

## <a name="create-a-flow-that-uses-power-bi---from-a-template"></a>Een stroom maken die gebruikmaakt van Power BI - op basis van een sjabloon
In deze taak gebruiken we een sjabloon om een eenvoudige stroom te maken die wordt geactiveerd door een Power BI-gegevenswaarschuwing (melding).

1. Meld u aan bij Microsoft Flow (flow.microsoft.com).
2. Selecteer **Mijn stromen**.
   
   ![](media/service-flow-integration/power-bi-my-flows.png)
3. Selecteer **Maken op basis van sjabloon**.
   
    ![](media/service-flow-integration/power-bi-template.png)
4. Gebruik het zoekvak om Power BI-sjablonen te zoeken en selecteer **Een e-mail versturen naar een doelgroep wanneer een waarschuwing met betrekking tot Power BI-gegevens wordt geactiveerd**.
   
    ![](media/service-flow-integration/power-bi-flow-alert.png)


### <a name="build-the-flow"></a>De stroom bouwen
Deze sjabloon bevat één trigger (Power BI-gegevenswaarschuwing voor nieuwe Olympische medaille voor Ierland) en één actie (een e-mail versturen). Wanneer u een veld selecteert, wordt er dynamische inhoud in Flow weergegeven die u kunt opnemen.  In dit voorbeeld hebt we de waarde en de URL van de tegel opgenomen in de berichttekst.

![](media/service-flow-integration/power-bi-template1.png)

1. Selecteer in de vervolgkeuzelijst met triggers een Power BI-gegevenswaarschuwing. Selecteer **Nieuwe medaille voor Ierland**. Zie [Gegevenswaarschuwingen in Power BI](service-set-data-alerts.md) als u wilt weten hoe een waarschuwing maakt.
   
   ![](media/service-flow-integration/power-bi-trigger-flow.png)
2. Voer één of meer geldige e-mailadressen in en selecteer vervolgens **Bewerken** (hieronder weergegeven) of **Dynamische inhoud toevoegen**. 
   
   ![](media/service-flow-integration/power-bi-flow-email.png)

3. Flow maakt een titel en een bericht dat u kunt behouden of bewerken. Alle waarden die u hebt ingesteld toen u de waarschuwing in Power BI maakte, zijn beschikbaar voor uw gebruik. Plaats uw cursor en selecteer de waarden in het grijs gemarkeerde gebied. 

   ![](media/service-flow-integration/power-bi-flow-email-default.png)

1.  Als u bijvoorbeeld een waarschuwingstitel in Power BI hebt gemaakt voor **We hebben nog een medaille gewonnen**, kunt u **Waarschuwingstitel** selecteren om die tekst toe te voegen aan het onderwerpsveld van uw e-mailbericht.

    ![](media/service-flow-integration/power-bi-flow-message.png)

    En u kunt het standaard e-mailbericht behouden of uw eigen bericht maken. Het bovenstaande voorbeeld bevat enkele wijzigingen in het bericht.

1. Zodra u bent klaar bent, selecteert u **Stroom maken** of **Stroom opslaan**.  De stroom is gemaakt en geëvalueerd.  Als er fouten worden aangetroffen, laat Flow u dit weten.
2. Als er fouten worden aangetroffen, selecteert u **Stroom bewerken** om ze te corrigeren. Selecteer anders **Gereed** om de nieuwe stroom uit te voeren.
   
   ![](media/service-flow-integration/power-bi-flow-running.png)
5. Wanneer de gegevenswaarschuwing wordt geactiveerd, wordt er een e-mail verzonden naar de door u opgegeven adressen.  
   
   ![](media/service-flow-integration/power-bi-flow-email2.png)

## <a name="create-a-flow-that-uses-power-bi---from-scratch-blank"></a>Een stroom maken die gebruikmaakt van Power BI - compleet nieuw (leeg)
In deze taak maken we een eenvoudige maar volledig nieuwe stroom die wordt geactiveerd door een Power BI-gegevenswaarschuwing (melding).

1. Meld u aan bij Microsoft Flow.
2. Selecteer **Mijn stromen** > **Nieuwe stroom maken**.
   
   ![](media/service-flow-integration/power-bi-my-flows.png)
3. Gebruik het zoekvak om een Power BI-trigger te zoeken en selecteer **Power BI - wanneer gegevensgebaseerde waarschuwing wordt geactiveerd**.

### <a name="build-your-flow"></a>Uw stroom maken
1. Selecteer in de vervolgkeuzelijst de naam van de waarschuwing.  Zie [Gegevenswaarschuwingen in Power BI](service-set-data-alerts.md) als u wilt weten hoe een waarschuwing maakt.
   
    ![](media/service-flow-integration/power-bi-totalstores2.png)
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

