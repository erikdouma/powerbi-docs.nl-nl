---
title: Aangepaste Power BI-antwoordpagina's maken voor Cortana
description: Aangepaste antwoordpagina's voor Cortana maken in Power BI
services: powerbi
documentationcenter: 
author: yaron
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
ms.date: 12/20/2017
ms.author: mihart
ms.openlocfilehash: 79e10c7d47eb5105e0c3e79bd3451315eae6d27e
ms.sourcegitcommit: 6ea8291cbfcb7847a8d7bc4e2b6abce7eddcd0ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/21/2017
---
# <a name="use-power-bi-service-or-power-bi-desktop-to-create-a-custom-answer-page-for-cortana"></a>De Power BI-service of Power BI Desktop gebruiken om een aangepaste antwoordpagina voor Cortana te maken
Maak gebruik van de Power BI-functionaliteit om speciale rapportpagina's, de zogenaamde *Cortana-antwoordpagina's* (soms ook wel Cortana-antwoordkaarten genoemd) te maken die speciaal zijn ontworpen voor de beantwoording van Cortana-vragen.

![](media/service-cortana-answer-cards/power-bi-cortana.png)

> [!IMPORTANT]
> Als u de preview-versie van het Cortana- en Power BI-**dashboard** uitprobeert, kunt u de rest van dit artikel overslaan. Er zijn geen installatievereisten voor Cortana om uw Power BI-dashboards te doorzoeken.
> 
> 

## <a name="before-you-begin"></a>Voordat u begint
Er zijn 4 documenten die u helpen bij het instellen en gebruiken van Cortana voor Power BI. U kunt het beste eerst artikel 1 lezen, als u dit nog niet hebt gedaan. Artikel 2 is met name belangrijk omdat hierin de stappen worden beschreven die u moet uitvoeren voordat u de Cortana-antwoordpagina's kunt gebruiken.

**Artikel 1** [Lees hoe u Cortana en Power BI samen kunt gebruiken](service-cortana-intro.md)

**Artikel 2**: [Voor het zoeken in Power BI-rapporten: de integratie van Cortana, Power BI en Windows inschakelen](service-cortana-enable.md)

**Artikel 3**: dit artikel

**Artikel 4**: [Problemen oplossen](service-cortana-troubleshoot.md)

## <a name="create-a-cortana-answer-page-designed-specifically-for-cortana"></a>Een Cortana-antwoordpagina maken die speciaal is ontworpen voor Cortana
Een *Cortana-antwoordpagina* in een rapport heeft een formaat dat specifiek is afgestemd op Cortana zodat het in een Cortana-scherm kan worden weergegeven als een antwoord op een vraag.  U maakt als volgt een antwoordpagina voor Cortana:

1. U kunt het beste beginnen met een [lege rapportpagina](power-bi-report-add-page.md).
2. Selecteer in het deelvenster **Visualisaties** het pictogram met de verfroller en kies **Paginaformaat > Type > Cortana**.
   
    ![](media/service-cortana-answer-cards/pbi-cortana-page-size-new.png)
3. Maak een visueel element of een groep visuele elementen die u in Cortana wilt weergeven als antwoord op een bepaalde vraag (of een verzameling vragen).
4. Zorg ervoor dat alle visuele elementen binnen de paginaranden passen.  Wijzig eventueel de weergave-instellingen, gegevenslabels, kleuren en achtergronden.  
   
    ![](media/service-cortana-answer-cards/pbi_cortana_modify-new.png)
5. Geef de pagina een naam en voeg alternatieve namen toe.  Cortana gebruikt deze namen wanneer het naar resultaten zoekt. Selecteer in het deelvenster **Visualisaties** het pictogram met de verfroller en kies **Paginagegevens**. Schakel Q&A voor dit visuele element in door de schuifregelaar op **Aan** te zetten.
   
    ![](media/service-cortana-answer-cards/pbi_cortana_names-newer.png)
   
   > [!TIP]
   > U kunt de resultaten verbeteren door woorden die worden gebruikt als kolomnamen te vermijden.
   > 
   > 
6. Als uw rapport paginaniveaufilters heeft, kunt u eventueel **Enkelvoudige selectie vereisen** instellen. In Cortana wordt dit rapport dan alleen als een antwoord weergegeven als één, en uitsluitend één, van de filteritems in de vraag wordt vermeld. **Enkelvoudige selectie vereisen** vindt u onder aan het deelvenster **Filters**.
   
   > [!NOTE]
   > U hoeft **Enkelvoudige selectie vereisen** niet in te stellen, als u wilt dat in Cortana een rapport wordt weergegeven op basis van de paginaniveaufilters.  Voor 'omzet weergeven voor Charlotte Lindseys' bijvoorbeeld wordt de antwoordpagina weergegeven, ongeacht of u de instelling Enkelvoudige selectie vereisen hebt geselecteerd.
   > 
   > 
   
     ![](media/service-cortana-answer-cards/pbi-cortana-single-selection-new.png)
   
      Als u Cortana bijvoorbeeld vraagt:
   
   * 'omzet weergeven op winkelnaam', wordt deze antwoordpagina niet weergegeven omdat geen van de items in het vereiste paginaniveaufilter is opgenomen.
   * 'omzet weergeven voor Cary Lindseys en Charlotte Lindseys', wordt deze antwoordpagina niet weergegeven omdat u meer dan één item van het vereiste paginaniveaufilter hebt opgegeven.
   * 'omzet weergeven voor Charlotte Lindseys', wordt deze antwoordpagina weergegeven.
     
     = 'omzet weergeven', wordt deze antwoordpagina niet weergegeven omdat geen van de items in het vereiste paginaniveaufilter is opgenomen.

> [!IMPORTANT]
> U moet [de gegevensset inschakelen voor Cortana](service-cortana-enable.md) zodat Cortana toegang heeft tot uw Cortana-antwoordpagina.
> 
> 

## <a name="how-does-cortana-order-the-results"></a>Hoe worden de resultaten in Cortana geordend?
Antwoorden met een hoog scoringspercentage (wanneer bijvoorbeeld een opgegeven paginanaam precies overeenkomt) worden als *beste match* bovenaan in het resultatenoverzicht in Cortana vermeld. Er kunnen meerdere beste matches voorkomen als er meerdere Cortana-antwoordpagina's in Power BI zijn. Antwoorden met een normaal of lager scoringspercentage, zoals antwoorden die niet zijn gebaseerd op de naam van een antwoordpagina of een vraag met woorden die niet worden begrepen door Power BI, worden in Cortana als koppelingen vermeld onder de beste matches.

> [!NOTE]
> Wanneer een nieuwe gegevensset of aangepaste Cortana-antwoordpagina wordt toegevoegd aan Power BI en deze wordt ingeschakeld voor Cortana, kan het tot 30 minuten duren voordat er resultaten in Cortana worden weergegeven. Als u zich bij Windows 10 afmeldt en opnieuw aanmeldt of als u het Cortana-proces in Windows 10 op een andere manier opnieuw start, wordt nieuwe inhoud onmiddellijk weergegeven.
> 
> 

## <a name="next-steps"></a>Volgende stappen
[Cortana gebruiken met Power BI](service-cortana-intro.md)

Lukt het niet om Cortana samen met Power BI te gebruiken?  Probeer de [probleemoplosser van Cortana](service-cortana-troubleshoot.md).

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

