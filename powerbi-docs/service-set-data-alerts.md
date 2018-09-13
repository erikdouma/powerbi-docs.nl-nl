---
title: Gegevensmeldingen instellen in de Power BI-service
description: Informatie over het instellen van waarschuwingsmeldingen om u te waarschuwen als wijzigingen aan de gegevens in uw dashboards de limieten overschrijden die u in de Power BI-service hebt ingesteld.
author: mihart
manager: kvivek
ms.reviewer: ''
featuredvideoid: JbL2-HJ8clE
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 08/28/2018
ms.author: mihart
LocalizationGroup: Dashboards
ms.openlocfilehash: 153676c983ef81bcccf1ea6bf0adf95ef29a2765
ms.sourcegitcommit: fe03f2a80f2df82219b8e026085f93a8453201df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/08/2018
ms.locfileid: "44167923"
---
# <a name="data-alerts-in-power-bi-service"></a>Gegevenswaarschuwingen in de Power BI-service
Stel meldingen in om u te waarschuwen als wijzigingen aan de gegevens in uw dashboards de limieten overschrijden die u hebt ingesteld. 

U kunt waarschuwingen op tegels instellen als u een Power BI Pro-licentie hebt of als er een dashboard van een [Premium-capaciteit](service-premium.md) met u is gedeeld. Meldingen kunnen alleen worden ingesteld op tegels die zijn vastgemaakt vanuit visuele rapportelementen, en alleen op meters, KPI's en kaarten. Meldingen kunnen worden ingesteld op visuele elementen die zijn gemaakt van sets streaminggegevens die vanaf een rapport aan een dashboard zijn vastgemaakt. Ze kunnen niet worden ingesteld op streamingtegels die rechtstreeks op het dashboard zijn gemaakt via **Tegel toevoegen** > **Aangepaste streaminggegevens**. 

U bent zelf de enige die de door u ingestelde meldingen kunt zien, ook als u uw dashboard deelt. Gegevensmeldingen worden volledig met alle platforms gesynchroniseerd. Stel gegevensmeldingen in en bekijk ze [in de mobiele Power BI-apps](mobile-set-data-alerts-in-the-mobile-apps.md) (Engelstalig) en in de Power BI-service. Ze zijn niet beschikbaar voor Power BI Desktop. Meldingen kunnen ook worden [geautomatiseerd en geïntegreerd met Microsoft Flow](https://flow.microsoft.com) - [probeer het zelf](service-flow-integration.md).

![Tegels](media/service-set-data-alerts/powerbi-alert-types-new.png)

> [!WARNING]
> Gegevensgestuurde meldingen bieden informatie over uw gegevens. Als u uw Power BI-gegevens op een mobiel apparaat weergeeft en dat apparaat wordt gestolen, wordt u aangeraden de Power BI-service te gebruiken om alle regels voor gegevensgestuurde meldingen uit te schakelen.
> 
> 

## <a name="set-data-alerts-in-power-bi-service"></a>Gegevenswaarschuwingen instellen in de Power BI-service
Kijk hoe Amanda enkele meldingen toevoegt aan tegels op haar dashboard. Volg vervolgens de stapsgewijze instructies onder de video om het zelf te proberen.

<iframe width="560" height="315" src="https://www.youtube.com/embed/JbL2-HJ8clE" frameborder="0" allowfullscreen></iframe>

In dit voorbeeld wordt een kaarttegel gebruikt van het voorbeelddashboard voor retailanalyse.

1. Begin op een dashboard. Selecteer de beletseltekens (drie puntjes) op een dashboardmeter, KPI of kaarttegel.
   
   ![Tegel Totaal aantal winkels](media/service-set-data-alerts/powerbi-card.png)
2. Selecteer het belpictogram ![waarschuwingspictogram](media/service-set-data-alerts/power-bi-bell-icon.png) of **Waarschuwingen beheren** om één of meer waarschuwingen toe te voegen voor **Totale opslaglocaties**.
   
1. Selecteer in het venster **Waarschuwingen beheren** de optie **+ Waarschuwingsregel toevoegen**.  Zorg ervoor dat de schuifregelaar staat ingesteld op **Aan** en geef uw waarschuwing een titel. Titels helpen u de meldingen makkelijk te herkennen.
   
   ![Venster Waarschuwingen beheren](media/service-set-data-alerts/powerbi-alert-title.png)
4. Schuif omlaag en voer de details van de melding in.  In dit voorbeeld maken we een melding die ons eenmaal per dag waarschuwt als het totale aantal winkels de honderd overschrijdt. Meldingen worden weergegeven in het meldingencentrum. We zorgen er ook voor dat Power BI een e-mail stuurt.
   
   ![Venster Waarschuwingen beheren, drempel instellen](media/service-set-data-alerts/power-bi-set-alert-details.png)
5. Selecteer **Opslaan en sluiten**.

## <a name="receiving-alerts"></a>Meldingen ontvangen
Als de bijgehouden gegevens een van de ingestelde drempelwaarden bereiken, vinden er een aantal dingen plaats. Eerst controleert Power BI of het langer dan een uur of langer dan 24 uur (afhankelijk van de optie die u hebt geselecteerd) is sinds de vorige waarschuwing is verzonden. U ontvangt een melding zolang de gegevens de drempelwaarde overschrijden.

Vervolgens wordt een melding verzonden naar het meldingencentrum en ontvangt u er eventueel een per e-mail. Elke melding bevat een rechtstreekse koppeling naar uw gegevens. Selecteer de koppeling om de betreffende tegel te zien, vanaf waar u kunt gaan verkennen, delen en meer informatie kunt krijgen.  

1. Als de melding zo is ingesteld dat u een e-mail ontvangt, vindt u iets soortgelijks als hieronder in uw Postvak IN.
   
   ![Waarschuwings-e-mail](media/service-set-data-alerts/powerbi-alerts-email.png)
2. Er wordt een bericht aan het **meldingencentrum** toegevoegd en een nieuw meldingenpictogram aan de desbetreffende tegel.
   
   ![Meldingspictogram in Power BI-service](media/service-set-data-alerts/powerbi-alert-notifications.png)
3. Open het meldingencentrum om de details van de melding te bekijken.
   
    ![De waarschuwing lezen](media/service-set-data-alerts/powerbi-alert-notfication.png)
   
   > [!NOTE]
   > Meldingen werken alleen voor gegevens die zijn vernieuwd. Als gegevens worden vernieuwd, controleert Power BI of er een melding voor die gegevens is ingesteld. Als de gegevens een drempelwaarde voor de melding hebben bereikt, wordt er een melding geactiveerd.
   > 
   > 

## <a name="managing-alerts"></a>Meldingen beheren
U kunt meldingen op diverse manieren beheren: vanaf het dashboardtegel zelf, vanuit het menu Instellingen in Power BI en vanaf een individuele tegel in de [mobiele Power BI-app op de iPhone](mobile-set-data-alerts-in-the-mobile-apps.md) (Engelstalig) of in de [mobiele Power BI-app voor Windows 10](mobile-set-data-alerts-in-the-mobile-apps.md) (Engelstalig).

### <a name="from-the-tile-itself"></a>Vanaf de tegel zelf
1. Als u een waarschuwing voor een tegel wilt wijzigen of verwijderen, opent u opnieuw het venster **Waarschuwingen beheren** door het belpictogram ![Waarschuwingspictogram](media/service-set-data-alerts/power-bi-bell-icon.png) te selecteren. Alle meldingen die u voor die tegel hebt ingesteld, worden weergegeven.
   
    ![Venster Waarschuwingen beheren](media/service-set-data-alerts/powerbi-see-alerts.png).
2. Als u een tegel wilt wijzigen, selecteert u de pijl links van de naam van de melding.
   
    ![Pijl naast de naam van de waarschuwing](media/service-set-data-alerts/powerbi-see-alerts-arrow.png).
3. Als u een tegel wilt verwijderen, selecteert u de prullenbak rechts van de naam van de melding.
   
      ![Pictogram met prullenbak geselecteerd](media/service-set-data-alerts/powerbi-see-alerts-delete.png)

### <a name="from-the-power-bi-settings-menu"></a>Vanuit het menu Instellingen in Power BI
1. Selecteer het tandwielpictogram in de Power BI-menubalk.
   
    ![Tandwielpictogram](media/service-set-data-alerts/powerbi-gear-icon.png).
2. Selecteer onder **Instellingen** de optie **Meldingen**.
   
    ![Tabblad Waarschuwingen in het venster Instellingen](media/service-set-data-alerts/powerbi-alert-settings.png)
3. Hier kunt u meldingen in- en uitschakelen, het venster **Meldingen beheren** openen om wijzigingen aan te brengen of de melding verwijderen.

## <a name="tips-and-troubleshooting"></a>Tips en problemen oplossen
* Meldingen worden momenteel niet ondersteund voor Bing-tegels of kaarttegels met datum-/tijdmetingen.
* Meldingen werken alleen met numerieke gegevenstypen.
* Meldingen werken alleen voor gegevens die zijn vernieuwd. Ze werken niet met statische gegevens.
* Meldingen werken alleen voor streaming gegevenssets als u een visueel rapportelement voor KPI's, kaarten of meters maakt en dit element vervolgens aan het dashboard vastmaakt.

## <a name="next-steps"></a>Volgende stappen
[Create a Microsoft Flow that includes a data alert](service-flow-integration.md)   (Een Microsoft Flow maken die een gegevensmelding bevat)  
[Gegevenswaarschuwingen instellen op uw mobiele apparaat](mobile-set-data-alerts-in-the-mobile-apps.md)    

