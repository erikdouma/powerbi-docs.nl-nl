---
title: Interactie met een ArcGIS-kaart die met u is gedeeld
description: 'ArcGIS-kaart gebruiken in de leesweergave '
author: mihart
manager: kfile
ms.reviewer: ''
tags: power bi, service, desktop, mobile
featuredvideoid: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 02/28/2018
ms.author: mihart
ms.openlocfilehash: 2a5e654062c056308431b2a94f7e2da4e3d46d17
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2018
ms.locfileid: "34240878"
---
# <a name="interacting-with-arcgis-maps-in-power-bi"></a>Interactie met ArcGIS-kaarten in Power BI
Dit onderwerp is geschreven vanuit het oogpunt van een persoon die een ArcGIS-kaart *gebruikt* in de Power BI-service, in de desktopversie of op een mobiel apparaat. Zodra een maker een ArcGIS-kaart met u deelt, kunt u deze kaart op veel manieren gebruiken.  Zie [ArcGIS maps by esri tutorial](power-bi-visualization-arcgis.md) (ArcGIS-kaarten van Esri - een zelfstudie) voor meer informatie over het maken van een ArcGIS-kaart.

De combinatie van ArcGIS-kaarten en Power BI tilt kaarten naar een volledig nieuw niveau, verder dan de presentatie van punten op een kaart. Met de beschikbare opties voor basiskaarten, locatietypen, thema's, symboolstijlen en referentielagen worden prachtige informatieve kaartvisualisaties gemaakt. De combinatie van bindende gegevenslagen (zoals censusgegevens) op een kaart met ruimtelijke analyse geeft een beter inzicht in uw visualisatiegegevens.

> [!TIP]
> GIS staat voor Geographic Information Science (geografische informatiewetenschap).
> 

Het voorbeeld dat we gebruiken is dezelfde ArcGIS-kaart die is gemaakt in [ArcGIS maps by esri tutorial](power-bi-visualization-arcgis.md) (ArcGIS-kaarten van Esri - een zelfstudie). Er wordt gekeken naar de omzet van vorig jaar per stad, en gebruikgemaakt van een basisstratenkaart, bellensymbolen om de grootte weer te geven, en een referentielaag voor het gemiddelde inkomen per huishouden. De kaart bevat 3 spelden en één radius voor de reistijd (in paars).

![](media/power-bi-visualizations-arcgis/power-bi-arcgis-esri-new.png)

> [!TIP]
> Ga naar [esri's page on Power BI](https://www.esri.com/powerbi) (Esri-pagina in Power BI) om veel voorbeelden en aanbevelingen te bekijken. Ga vervolgens naar [ArcGIS Maps for Power BI Getting Started page](https://doc.arcgis.com/en/maps-for-powerbi/get-started/about-maps-for-power-bi.htm) (Pagina Aan de slag voor ArcGIS Maps for Power BI).
> 
> 

<br/>

## <a name="user-consent"></a>Toestemming van de gebruiker
De eerste keer dat een collega een ArcGIS-kaart met u deelt, wordt in Power BI een prompt weergegeven. ArcGIS MAPS for Power BI wordt geleverd door Esri (www.esri.com) en uw gebruik van ArcGIS Maps for Power BI is onderhevig aan de voorwaarden en het privacybeleid van Esri. Power BI-gebruikers die de visuals van ArcGIS Maps for Power BI willen gebruiken, moeten hiermee akkoord gaan in het toestemmingsdialoogvenster.

## <a name="selection-tools"></a>Selectiehulpprogramma’s
ArcGIS Maps for Power BI biedt drie selectiemodi. Er kunnen maximaal 250 gegevenspunten tegelijk worden geselecteerd.

![](media/power-bi-visualizations-arcgis/power-bi-esri-selection-tools2.png)

![](media/power-bi-visualizations-arcgis/power-bi-esri-selection-single2.png): hiermee worden afzonderlijke gegevenspunten geselecteerd.

![](media/power-bi-visualizations-arcgis/power-bi-esri-selection-marquee2.png): hiermee wordt een rechthoek op de kaart getekend en worden de opgenomen gegevenspunten geselecteerd. CTRL gebruiken om meer dan één rechthoekig gebied te selecteren.

![](media/power-bi-visualizations-arcgis/power-bi-esri-selection-reference-layer2.png): hiermee wordt toegestaan dat grenzen of polygonen binnen referentielagen worden gebruikt voor het selecteren van opgenomen gegevenspunten.

<br/>

## <a name="interacting-with-an-arcgis-map"></a>Interactie met een ArcGIS-kaart
De functies die beschikbaar zijn voor u, zijn afhankelijk van het feit of u de *maker* (persoon die de kaart heeft gemaakt) of de *consument* (iemand met wie een ArcGIS-kaart is gedeeld) bent. Als u als consument gebruikmaakt van een ArcGIS-kaart (ook wel de [Leesweergave](service-reading-view-and-editing-view.md) genoemd), zijn dit de beschikbare acties.

* Net zoals bij andere visualisatietypen kunt u de kaart [vastmaken aan dashboards](service-dashboard-pin-tile-from-report.md), [weergeven](service-reports-show-data.md) en/of [de onderliggende gegevens exporteren](power-bi-visualization-export-data.md), en de kaart bekijken in [Focusmodus](service-focus-mode.md) en op [Volledig scherm](service-fullscreen-mode.md).    
* Vouw het deelvenster **Filters** uit om de kaart te verkennen met behulp van filters. Wanneer u het rapport sluit, worden de filters die u hebt toegepast, niet opgeslagen.    
    ![](media/power-bi-visualizations-arcgis/power-bi-filter-newer.png)  
* Als de kaart een referentielaag heeft, selecteert u locaties om details in een tooltip weer te geven. Hier hebben we Adams County geselecteerd en zien we gegevens uit de referentielaag voor het gemiddelde inkomen per huishouden die de maker heeft toegevoegd aan de kaart.
  
    ![](media/power-bi-visualizations-arcgis/power-bi-reference-layer.png)  
  
    In dit geval zien we ook een diagram. Selecteer een balk in het diagram om u te verdiepen in de gegevens. U ziet hier dat 79 huishoudens in Adams county een inkomen hadden van $ 200.000 of hoger.
  
    ![](media/power-bi-visualizations-arcgis/power-bi-tooltip-chart.png)
  
    Selecteer de pijl om eventuele extra diagrammen weer te geven.
* Beweeg de muisaanwijzer over de locatiesymbolen in de basiskaart om de details in een tooltip weer te geven.     
  ![](media/power-bi-visualizations-arcgis/power-bi-arcgis-hover.png)
  
  > [!TIP]
  > U moet mogelijk inzoomen om een specifieke locatie te selecteren.  Anders worden er mogelijk meerdere tooltips tegelijkertijd weergegeven in Power BI wanneer er overlappende locaties zijn. Selecteer de pijlen om te schakelen tussen de tooltips
  > 
  > ![](media/power-bi-visualizations-arcgis/power-bi-3-screens.png)
  > 
  > 
* Als de maken een Infographics-laag heeft toegevoegd aan de ArcGIS-kaart, worden in de rechterbovenhoek van de kaart extra gegevens weergegeven.  Hier heeft de maker van de kaart bijvoorbeeld 'Kinderen onder de 14' toegevoegd.
  
    ![](media/power-bi-visualizations-arcgis/power-bi-demographics.png)

## <a name="considerations-and-limitations"></a>Overwegingen en beperkingen
ArcGIS Maps for Power BI is beschikbaar in de volgende services en toepassingen:

<table>
<tr><th>Service/app</th><th>Beschikbaarheid</th></tr>
<tr>
<td>Power BI Desktop</td>
<td>Ja</td>
</tr>
<tr>
<td>Power BI-service (app.powerbi.com)</td>
<td>Ja</td>
</tr>
<tr>
<td>Mobiele Power BI-toepassingen</td>
<td>Ja</td>
</tr>
<tr>
<td>Power BI publiceren op internet</td>
<td>Nee</td>
</tr>
<tr>
<td>Power BI Embedded</td>
<td>Nee</td>
</tr>
<tr>
<td>Power BI-service insluiten (PowerBI.com)</td>
<td>Nee</td>
</tr>
</table>

**Hoe werken ArcGIS Maps en Power BI samen?**
ArcGIS Maps for Power BI wordt geleverd door Esri (www.esri.com). Uw gebruik van ArcGIS Maps for Power BI is onderhevig aan de [voorwaarden](https://go.microsoft.com/fwlink/?LinkID=8263222) en het [privacybeleid](https://go.microsoft.com/fwlink/?LinkID=826323) van Esri. Power BI-gebruikers die de visuals van ArcGIS Maps for Power BI willen gebruiken, moeten hiermee akkoord gaan in het toestemmingsdialoogvenster (raadpleeg Toestemming van gebruiker voor meer informatie).  Het gebruik van ArcGIS Maps for Power BI van Esri is onderhevig aan de voorwaarden en het privacybeleid van Esri. Een koppeling naar de voorwaarden en het privacybeleid vindt u in het toestemmingsdialoogvenster. Elke gebruiker moet toestemming geven voor het eerste gebruik van ArcGIS Maps for Power BI. Zodra de gebruiker toestemming heeft gegeven, worden de aan de visual gekoppelde gegevens naar de services van Esri verzonden voor (ten minste) geocodering, wat betekent dat de locatiegegevens worden getransformeerd in breedtegraad- en lengtegraadgegevens die in een kaart kunnen worden weergegeven. U moet ervan uitgaan dat alle gegevens die aan de gegevensvisualisatie zijn gekoppeld, naar de services van Esri kunnen worden verzonden. Esri biedt services zoals basiskaarten, analyses van ruimtelijke gegevens, geocodering, enzovoort. Voor de samenwerking tussen de visuals van ArcGIS Maps for Power BI en deze services wordt gebruikgemaakt van een SSL-verbinding. Deze verbinding wordt beveiligd met een certificaat dat door Esri wordt verstrekt en onderhouden. Meer informatie over ArcGIS Maps for Power BI vindt u op de [productpagina voor ArcGIS Maps for Power BI](https://www.esri.com/powerbi) van Esri.

Wanneer een gebruiker zich via ArcGIS Maps for Power BI voor een Plus-abonnement van Esri registreert, gaat de gebruiker een directe relatie met Esri aan. Power BI verzendt geen persoonlijke gegevens over de gebruiker naar Esri. De gebruiker meldt zich aan bij en vertrouwt een door Esri verstrekte AAD-toepassing waarbij gebruik wordt gemaakt van de eigen AAD-identiteit van de gebruiker. Op deze manier deelt de gebruiker zijn of haar persoonlijke gegevens rechtstreeks met Esri. Zodra de gebruiker Plus-inhoud aan een visual van ArcGIS Maps for Power BI toevoegt, hebben andere Power BI-gebruikers ook een Plus-abonnement van Esri nodig als zij die inhoud willen weergeven of bewerken. 

Voor gedetailleerde technische vragen over de werking van ArcGIS Maps for Power BI van Esri kunt u contact opnemen met Esri via hun ondersteuningssite.

**De ArcGIS-kaart wordt niet weergegeven**    
In services of toepassingen waarin ArcGIS Maps for Power BI niet beschikbaar is, wordt de visualisatie weergegeven als een lege visual met het logo van Power BI.

**Ik zie niet al mijn adressen op de kaart**    
Bij het geocoderen van adressen worden alleen de eerste 1500 adressen gegeocodeerd. Het geocoderen van plaatsnamen en landen is niet onderhevig aan de adreslimiet van 1500.

**Zijn er kosten verbonden aan het gebruik van ArcGIS Maps for Power BI?**

ArcGIS Maps for Power BI is beschikbaar voor alle Power BI-gebruikers zonder extra kosten. Het is een onderdeel dat wordt geleverd door **Esri**, en uw gebruik is onderhevig aan de voorwaarden en het privacybeleid van **Esri**, zoals eerder in dit artikel is aangegeven.

**Ik krijg een foutbericht dat mijn cache vol is**

Dit is een bekende bug. Er wordt aan een oplossing gewerkt.  Selecteer in de tussentijd de koppeling die wordt weergegeven in het foutbericht, voor instructies over het wissen van de Power BI-cache.

**Kan ik mijn ArcGIS-kaarten offline bekijken?**

Nee, Power BI moet zijn verbonden met het netwerk om kaarten weer te geven.

## <a name="next-steps"></a>Volgende stappen
Hulp krijgen: **Esri** biedt [uitgebreide documentatie](https://go.microsoft.com/fwlink/?LinkID=828772) over de functieset van **ArcGIS Maps for Power BI**.

U kunt vragen stellen, de meest recente informatie vinden, problemen melden en antwoorden vinden in de Power BI-[communitythread met betrekking tot **ArcGIS Maps for Power BI**](https://go.microsoft.com/fwlink/?LinkID=828771).

Als u een suggestie voor een verbetering hebt, kunt u deze indienen bij [de ideeënlijst van Power BI](https://ideas.powerbi.com).

[Productpagina van ArcGIS Maps for Power BI](https://www.esri.com/powerbi)

