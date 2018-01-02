---
title: Een rapport insluiten met een iFrame
description: Het installeren van Power BI Report Server zelf gaat erg snel. Inclusief downloaden, installeren en configureren, moet u binnen enkele minuten aan de slag kunnen.
services: powerbi
documentationcenter: 
author: guyinacube
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
ms.date: 11/09/2017
ms.author: asaxton
ms.openlocfilehash: df22a7ed0772979d164a9afae18f4931310ec4a1
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/15/2017
---
# <a name="quickstart-embed-a-power-bi-report-using-an-iframe-and-url-parameters"></a>Snelstartgids: een Power BI-rapport insluiten met een iFrame en URL-parameters

U kunt elk gewenst rapport insluiten door een iFrame in uw toepassing te gebruiken. 

## <a name="url-parameter"></a>URL-parameter

Voor elke URL naar een rapport, kunt u de queryreeksparameter `?rs:Embed=true` toevoegen.

Voorbeeld:

```
http://myserver/reports/powerbi/Sales?rs:embed=true
```

Dit werkt voor alle typen rapporten in Power BI Report Server.

## <a name="iframe"></a>iFrame

Zodra u de URL hebt, kunt u een iFrame binnen een webpagina maken om het rapport te hosten.

Voorbeeld:

```
<iframe width="800" height="600" src="http://myserver/reports/powerbi/Sales?rs:embed=true" frameborder="0" allowFullScreen="true"></iframe>
```

## <a name="url-filter"></a>URL-filter

U kunt een queryreeksparameter aan de URL toevoegen om de gegevens te filteren die worden geretourneerd in het Power BI-rapport.

De syntaxis is vrij eenvoudig: start met de URL van het rapport, voeg een vraagteken toe en vervolgens deze filtersyntaxis.

URL?filter=***Tabel***/***Veld*** eq '***waarde***'

Houd rekening met het volgende:

- De naam van de **tabel** en het **veld** zijn hoofdlettergevoelig, de **waarde** is dat niet.
- U kunt een rapport filteren met velden die in de rapportweergave worden verborgen.
- De **waarde** moet tussen enkele aanhalingstekens staan.
- Het veldtype moet een tekenreeks zijn.
- Tabel- en veldnamen mogen geen spaties bevatten.

###  <a name="example-filter-on-a-field"></a>Voorbeeld: filteren op een veld

Neem bijvoorbeeld het [voorbeeld van een retailanalyse](../sample-datasets.md). Stel dat dit de URL naar het rapport op de rapportserver in de map met de naam 'power bi' is:

```
https://report-server/reports/power-bi/Retail-Analysis-Sample
```

Zoals u ziet bevatten de kaartvisualisatie in het voorbeeld van een retailanalyse de winkels in North Carolina en andere staten.

![Kaartvisualisatie van het voorbeeld van een retailanalyse](media/quickstart-embed/report-server-retail-analysis-sample-map.png)

*NC* is de waarde voor North Carolina zoals opgeslagen in het veld **Gebied** van de tabel **Winkel** tabel. Als u het rapport zodanig wilt filteren dat er alleen winkels in North Carolina worden weergegeven, voegt u het volgende aan de URL toe:

?filter=Winkel/Gebied eq 'NC'

Nu is het rapport gefilterd op North Carolina. Alle visualisaties op de rapportpagina bevatten alleen gegevens voor North Carolina.

![Gefilterde visualisaties in het voorbeeld van een retailanalyse](media/quickstart-embed/report-server-retail-analysis-sample-filtered-map.png)

### <a name="create-a-dax-formula-to-filter-on-multiple-values"></a>Een DAX-formule maken om op meerdere waarden te filteren

U kunt ook op meerdere velden filteren door een berekende kolom in Power BI Desktop te maken waarmee twee velden worden samengevoegd in één waarde. Vervolgens kunt u filteren op die waarde.

Het voorbeeld met de retailanalyse bevat bijvoorbeeld twee velden: Gebied en Keten. U kunt in Power BI Desktop een [berekende kolom maken](../desktop-tutorial-create-calculated-columns.md) (veld) met de naam GebiedKeten. Houd er rekening mee dat de naam van het **veld** geen spaties mag bevatten. Hier volgt de DAX-formule voor die kolom.

GebiedKeten = [Gebied] & "-" & [Keten]

Publiceer het rapport naar Power BI Report Server en gebruik de URL-queryreeks vervolgens om te filteren om zodoende alleen gegevens voor de winkels van Lindseys in NC weer te geven.

```
https://report-server/reports/power-bi/Retail-Analysis-Sample?filter=Store/TerritoryChain eq 'NC-Lindseys'

```

## <a name="next-steps"></a>Volgende stappen

[Snelstartgids: een Power BI-rapport maken voor Power BI Report Server](quickstart-create-powerbi-report.md)  
[Snelstartgids: een gepagineerd rapport maken voor Power BI Report Server](quickstart-create-paginated-report.md)  

Nog vragen? [Misschien dat de Power Bi-community het antwoord weet](https://community.powerbi.com/).