---
title: Power BI-inhoud insluiten in een toepassing voor uw klanten voor onafhankelijke clouds
description: Informatie over het integreren of insluiten van een dashboard, een tegel of een rapport in een web-app met behulp van de Power BI-API's voor uw klanten.
author: markingmyname
ms.author: maghan
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: tutorial
ms.date: 07/26/2018
ms.openlocfilehash: 2d722428ce2029ef4689e6b4bf5dfcdd208baff8
ms.sourcegitcommit: 7fb0b68203877ff01f29724f0d1761d023075445
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/26/2018
ms.locfileid: "39255866"
---
# <a name="tutorial-embed-a-power-bi-dashboard-tile-or-report-into-your-application-for-sovereign-clouds"></a>Zelfstudie: een Power BI-dashboard, -tegel of -rapport in uw toepassing insluiten voor onafhankelijke clouds
Informatie over het integreren of insluiten van een dashboard, een tegel of een rapport in een web-app met behulp van de Power BI .NET-SDK en de Power BI JavaScript API voor uw klanten. Dit is doorgaans een ISV-scenario.

Power BI ondersteunt ook onafhankelijke (privé)clouds.

Er zijn verschillende onafhankelijke clouds:

* U.S. Government Community Cloud (GCC)

* U. S. Military Contractors (DoDCON)

* U. S. Military (DoD)

* Power BI-cloud voor Duitsland

* Power BI-cloud voor China

![Ingesloten dashboard](media/embed-sample-for-customers/powerbi-embed-dashboard.png)

Als u wilt beginnen met dit scenario, hebt u een **Power BI**-account nodig. Als u geen account hebt ingesteld, kunt u zich afhankelijk van het type onafhankelijke cloud aanmelden voor een [Power BI-account voor de Amerikaanse overheid](../service-govus-signup.md), een [account voor de Power BI-cloud voor Duitsland](https://powerbi.microsoft.com/power-bi-germany/?ru=https%3A%2F%2Fapp.powerbi.de%2F%3FnoSignUpCheck%3D1) of een [account voor de Power BI-cloud voor China](http://www.21vbluecloud.com/powerbi/).

> [!NOTE]
> Wilt u liever een dashboard insluiten voor uw organisatie? Bekijk dan [Een dashboard integreren in een app voor uw organisatie](integrate-dashboard.md).
>

Als u een dashboard wilt integreren in een web-app, gebruikt u de **Power BI** API en een **AD-toegangstoken** (Azure Active Directory) voor verificatie bij het ophalen van een dashboard. Vervolgens kunt u het dashboard laden met een insluittoken. De **Power BI**-API biedt programmatische toegang tot specifieke **Power BI**-resources. Zie [Power BI REST-API](https://docs.microsoft.com/rest/api/power-bi/), [Power BI .NET-SDK](https://github.com/Microsoft/PowerBI-CSharp) en [Power BI JavaScript API](https://github.com/Microsoft/PowerBI-JavaScript) voor meer informatie.

## <a name="download-the-sample"></a>Het voorbeeld downloaden
Dit artikel bevat de code die wordt gebruikt in het [voorbeeld voor het insluiten van inhoud voor uw klanten](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/App%20Owns%20Data/PowerBIEmbedded_AppOwnsData) op GitHub. Als u dit scenario wilt volgen, kunt u het voorbeeld downloaden.

* Government Community Cloud (GCC):
    1. Overschrijf het bestand Cloud.config door GCCCloud.config.
    2. Werk clientid (client-id van systeemeigen app), groupid, de gebruiker (hoofdgebruiker) en het wachtwoord bij in het bestand Web.config.
    3. Voeg de GCC-parameters als volgt toe aan het bestand web.config.

```xml
<add key="authorityUrl" value="https://login.windows.net/common/oauth2/authorize/" />
<add key="resourceUrl" value="https://analysis.usgovcloudapi.net/powerbi/api" />
<add key="apiUrl" value="https://api.powerbigov.us/" />
<add key="embedUrlBase" value="https://app.powerbigov.us" />
```

* Military Contractors (DoDCON):
    1. Overschrijf het bestand Cloud.config door TBCloud.config.
    2. Werk clientid (client-id van systeemeigen app), groupid, de gebruiker (hoofdgebruiker) en het wachtwoord bij in het bestand Web.config.
    3. Voeg de DoDCON-parameters als volgt toe aan het bestand web.config.

```xml
<add key="authorityUrl" value="https://login.windows.net/common/oauth2/authorize/" />
<add key="resourceUrl" value="https://high.analysis.usgovcloudapi.net/powerbi/api" />
<add key="apiUrl" value="https://api.high.powerbigov.us/" />
<add key="embedUrlBase" value="https://app.high.powerbigov.us" />
```

* Military (DoD):
    1. Overschrijf het bestand Cloud.config door PFCloud.config.
    2. Werk clientid (client-id van systeemeigen app), groupid, de gebruiker (hoofdgebruiker) en het wachtwoord bij in het bestand Web.config.
    3. Voeg de DoDCON-parameters als volgt toe aan het bestand web.config.

```xml
<add key="authorityUrl" value="https://login.windows.net/common/oauth2/authorize/" />
<add key="resourceUrl" value="https://mil.analysis.usgovcloudapi.net/powerbi/api" />
<add key="apiUrl" value="https://api.mil.powerbigov.us/" />
<add key="embedUrlBase" value="https://app.mil.powerbigov.us" />
```

* Parameters voor Power BI-cloud voor Duitsland
    1. Overschrijf het bestand Cloud.config met inhoud van Power BI-cloud voor Duitsland.
    2. Werk clientid (client-id van systeemeigen app), groupid, de gebruiker (hoofdgebruiker) en het wachtwoord bij in het bestand Web.config.
    3. Voeg de parameters voor Power BI-cloud voor Duitsland als volgt toe aan het bestand web.config.

```xml
<add key="authorityUrl" value=https://login.microsoftonline.de/common/oauth2/authorize/" />
<add key="resourceUrl" value="https://analysis.cloudapi.de/powerbi/api" />
<add key="apiUrl" value="https://api.powerbi.de/" />
<add key="embedUrlBase" value="https://app.powerbi.de" />
```

* Parameters van de Power BI-cloud voor China
    1. Overschrijf het bestand Cloud.config met inhoud van de [Power BI-cloud voor China](https://github.com/Microsoft/PowerBI-Developer-Samples/blob/master/App%20Owns%20Data/PowerBIEmbedded_AppOwnsData/CloudConfigs/Power%20BI%20operated%20by%2021Vianet%20in%20China/Cloud.config).
    2. Werk clientid (client-id van systeemeigen app), groupid, de gebruiker (hoofdgebruiker) en het wachtwoord bij in het bestand Web.config.
    3. Voeg de parameters voor de Power BI-cloud voor China als volgt toe aan het bestand web.config.

```xml
<add key="authorityUrl" value=https://login.chinacloudapi.cn/common/oauth2/authorize/" />
<add key="resourceUrl" value="https://analysis.chinacloudapi.cn/powerbi/api" />
<add key="apiUrl" value="https://api.powerbi.cn/" />
<add key="embedUrlBase" value="https://app.powerbi.cn" />
```

## <a name="step-1---register-an-app-in-azure-ad"></a>Stap 1: een app bij Azure AD registreren
U moet uw toepassing registreren bij Azure AD om REST API-aanroepen te kunnen uitvoeren. Zie [Een Azure AD-app voor het insluiten van Power BI-inhoud registreren](register-app.md) voor meer informatie. Omdat er verschillende lidmaatschappen voor onafhankelijke clouds zijn, zijn er afzonderlijke URL's om uw toepassing te registreren.

* Government Community Cloud (GCC): https://app.powerbigov.us/apps 

* Military Contractors (DoDCON): https://app.high.powerbigov.us/apps 

* Military (DoD): https://app.mil.powerbigov.us/apps

* Power BI-cloud voor Duitsland: https://app.powerbi.de/apps

* Power BI-cloud voor China - https://app.powerbi.cn/apps

Als u het [voorbeeld voor het insluiten van inhoud voor uw klanten](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/App%20Owns%20Data) hebt gedownload, gebruikt u de **client-id** die u verkrijgt na de registratie, zodat het voorbeeld kan worden geverifieerd voor Azure AD. Voor het configureren van het voorbeeld wijzigt u de **clientId** in het bestand *web.config*.


## <a name="step-2---get-an-access-token-from-azure-ad"></a>Stap 2: een toegangstoken ophalen uit Azure AD
In uw toepassing moet u een **toegangstoken** van Azure AD ophalen voordat u de Power BI REST API kunt aanroepen. Zie [Gebruikers verifiëren en een Azure AD-toegangstoken verkrijgen voor uw Power BI-app](get-azuread-access-token.md) voor meer informatie. Omdat er verschillende lidmaatschappen voor onafhankelijke clouds zijn, zijn er afzonderlijke URL's om een toegangstoken voor uw toepassing op te halen.

* Government Community Cloud (GCC): https://login.microsoftonline.com

* Military Contractors (DoDCON): http://login.microsoftonline.us

* Military (DoD): https://login.microsoftonline.us

* Power BI-cloud voor Duitsland: https://login.microsoftonline.de

* Power BI-cloud voor China - https://login.microsoftonline.cn

U kunt hier voorbeelden van bekijken in elke inhoudsitemtaak in **Controllers\HomeController.cs**.

## <a name="step-3---get-a-content-item"></a>Stap 3: een inhoudsitem ophalen
Als u uw Power BI-inhoud wilt insluiten, moet u een aantal zaken doen om ervoor te zorgen dat dit op de juiste manier gebeurt. Al deze stappen kunt u rechtstreeks uitvoeren met de REST API, maar voor de voorbeeldtoepassing en deze voorbeelden wordt gebruikgemaakt van de .NET-SDK.

### <a name="create-the-power-bi-client-with-your-access-token"></a>De Power BI-client maken met uw toegangstoken
U maakt uw Power BI-clientobject met uw toegangstoken zodat het kan communiceren met de Power BI-API's. Dit wordt gedaan door AccessToken te verpakken met een *Microsoft.Rest.TokenCredentials*-object.

```csharp
using Microsoft.IdentityModel.Clients.ActiveDirectory;
using Microsoft.Rest;
using Microsoft.PowerBI.Api.V2;

var tokenCredentials = new TokenCredentials(authenticationResult.AccessToken, "Bearer");

// Create a Power BI Client object. This is used to call the Power BI APIs.
using (var client = new PowerBIClient(new Uri(ApiUrl), tokenCredentials))
{
    // Your code to embed items.
}
```

### <a name="get-the-content-item-you-want-to-embed"></a>Het inhoudsitem dat u wilt insluiten ophalen
Gebruik het Power BI-clientobject voor het ophalen van een verwijzing naar het item dat u wilt insluiten. U kunt dashboards, tegels of rapporten insluiten. Hier volgt een voorbeeld van hoe u een eerste dashboard, tegel of rapport ophaalt uit een bepaalde werkruimte.

Een voorbeeld hiervan is beschikbaar in **Controllers\HomeController.cs** van het [Voorbeeld App is eigenaar van gegevens](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/App%20Owns%20Data).

**Dashboards**

```csharp
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;

// You need to provide the GroupID where the dashboard resides.
ODataResponseListDashboard dashboards = client.Dashboards.GetDashboardsInGroup(GroupId);

// Get the first report in the group.
Dashboard dashboard = dashboards.Value.FirstOrDefault();
```

**Tegel**

```csharp
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;

// To retrieve the tile, you first need to retrieve the dashboard.

// You need to provide the GroupID where the dashboard resides.
ODataResponseListDashboard dashboards = client.Dashboards.GetDashboardsInGroup(GroupId);

// Get the first report in the group.
Dashboard dashboard = dashboards.Value.FirstOrDefault();

// Get a list of tiles from a specific dashboard
ODataResponseListTile tiles = client.Dashboards.GetTilesInGroup(GroupId, dashboard.Id);

// Get the first tile in the group.
Tile tile = tiles.Value.FirstOrDefault();
```

**Rapport**

```csharp
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;

// You need to provide the GroupID where the dashboard resides.
ODataResponseListReport reports = client.Reports.GetReportsInGroupAsync(GroupId);

// Get the first report in the group.
Report report = reports.Value.FirstOrDefault();
```

### <a name="create-the-embed-token"></a>Het insluittoken maken
U moet een insluittoken genereren dat kan worden gebruikt vanuit de JavaScript API. Het insluittoken heeft alleen betrekking op het item dat is ingesloten. Dit betekent dat u een nieuw insluittoken moet maken voor elk stukje Power BI-inhoud dat u wilt insluiten. Zie [Insluittoken](https://docs.microsoft.com/rest/api/power-bi/embedtoken) voor meer informatie, onder andere over welk **accessLevel** u moet gebruiken.

> [!IMPORTANT]
> Omdat insluittokens alleen voor ontwikkelingstesten zijn bedoeld, kan een Power BI-masteraccount een onbeperkt aantal insluittokens genereren. Er moet een [capaciteit moet worden aangeschaft](https://docs.microsoft.com/power-bi/developer/embedded-faq#technical) voor insluitingsscenario's voor de productie. Het aantal te genereren insluitingstokens is onbeperkt wanneer een capaciteit is aangeschaft.

Een voorbeeld hiervan is beschikbaar in **Controllers\HomeController.cs** van het [Voorbeeld voor insluiten voor uw organisatie](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/App%20Owns%20Data).

Hierbij wordt ervan uitgegaan dat er een klasse wordt gemaakt voor **EmbedConfig** en **TileEmbedConfig**. Er is een voorbeeld van deze items beschikbaar in **Models\EmbedConfig.cs** en **Models\TileEmbedConfig.cs**.

**Dashboard**

```csharp
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;

// Generate Embed Token.
var generateTokenRequestParameters = new GenerateTokenRequest(accessLevel: "view");
EmbedToken tokenResponse = client.Dashboards.GenerateTokenInGroup(GroupId, dashboard.Id, generateTokenRequestParameters);

// Generate Embed Configuration.
var embedConfig = new EmbedConfig()
{
    EmbedToken = tokenResponse,
    EmbedUrl = dashboard.EmbedUrl,
    Id = dashboard.Id
};
```

**Tegel**

```csharp
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;

// Generate Embed Token for a tile.
var generateTokenRequestParameters = new GenerateTokenRequest(accessLevel: "view");
EmbedToken tokenResponse = client.Tiles.GenerateTokenInGroup(GroupId, dashboard.Id, tile.Id, generateTokenRequestParameters);

// Generate Embed Configuration.
var embedConfig = new TileEmbedConfig()
{
    EmbedToken = tokenResponse,
    EmbedUrl = tile.EmbedUrl,
    Id = tile.Id,
    dashboardId = dashboard.Id
};
```

**Rapport**

```csharp
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;

// Generate Embed Token.
var generateTokenRequestParameters = new GenerateTokenRequest(accessLevel: "view");
EmbedToken tokenResponse = client.Reports.GenerateTokenInGroup(GroupId, report.Id, generateTokenRequestParameters);

// Generate Embed Configuration.
var embedConfig = new EmbedConfig()
{
    EmbedToken = tokenResponse,
    EmbedUrl = report.EmbedUrl,
    Id = report.Id
};
```
## <a name="step-4---load-an-item-using-javascript"></a>Stap 4: een item laden met JavaScript
U kunt JavaScript gebruiken om een dashboard te laden in een div-element op uw webpagina. Het voorbeeld maakt gebruik van een EmbedConfig/TileEmbedConfig-model en weergaven van een dashboard, de tegel of het rapport. Voor een volledig voorbeeld van het gebruik van de JavaScript API kunt u het [Voorbeeld van Microsoft Power BI Embedded](https://microsoft.github.io/PowerBI-JavaScript/demo) gebruiken.

Een toepassingsvoorbeeld hiervan is beschikbaar in [Voorbeeld voor insluiten voor uw organisatie](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/App%20Owns%20Data).

**Views\Home\EmbedDashboard.cshtml**

```csharp
<script src="~/scripts/powerbi.js"></script>
<div id="dashboardContainer"></div>
<script>
    // Read embed application token from Model
    var accessToken = "@Model.EmbedToken.Token";

    // Read embed URL from Model
    var embedUrl = "@Html.Raw(Model.EmbedUrl)";

    // Read dashboard Id from Model
    var embedDashboardId = "@Model.Id";

    // Get models. models contains enums that can be used.
    var models = window['powerbi-client'].models;

    // Embed configuration used to describe the what and how to embed.
    // This object is used when calling powerbi.embed.
    // This also includes settings and options such as filters.
    // You can find more information at https://github.com/Microsoft/PowerBI-JavaScript/wiki/Embed-Configuration-Details.
    var config = {
        type: 'dashboard',
        tokenType: models.TokenType.Embed,
        accessToken: accessToken,
        embedUrl: embedUrl,
        id: embedDashboardId
    };

    // Get a reference to the embedded dashboard HTML element
    var dashboardContainer = $('#dashboardContainer')[0];

    // Embed the dashboard and display it within the div container.
    var dashboard = powerbi.embed(dashboardContainer, config);
</script>
```

**Views\Home\EmbedTile.cshtml**

```csharp
<script src="~/scripts/powerbi.js"></script>
<div id="tileContainer"></div>
<script>
    // Read embed application token from Model
    var accessToken = "@Model.EmbedToken.Token";

    // Read embed URL from Model
    var embedUrl = "@Html.Raw(Model.EmbedUrl)";

    // Read tile Id from Model
    var embedTileId = "@Model.Id";

    // Read dashboard Id from Model
    var embedDashboardeId = "@Model.dashboardId";

    // Get models. models contains enums that can be used.
    var models = window['powerbi-client'].models;

    // Embed configuration used to describe the what and how to embed.
    // This object is used when calling powerbi.embed.
    // This also includes settings and options such as filters.
    // You can find more information at https://github.com/Microsoft/PowerBI-JavaScript/wiki/Embed-Configuration-Details.
    var config = {
        type: 'tile',
        tokenType: models.TokenType.Embed,
        accessToken: accessToken,
        embedUrl: embedUrl,
        id: embedTileId,
        dashboardId: embedDashboardeId
    };

    // Get a reference to the embedded tile HTML element
    var tileContainer = $('#tileContainer')[0];

    // Embed the tile and display it within the div container.
    var tile = powerbi.embed(tileContainer, config);
</script>
```

**Views\Home\EmbedReport.cshtml**

```csharp
<script src="~/scripts/powerbi.js"></script>
<div id="reportContainer"></div>
<script>
    // Read embed application token from Model
    var accessToken = "@Model.EmbedToken.Token";

    // Read embed URL from Model
    var embedUrl = "@Html.Raw(Model.EmbedUrl)";

    // Read report Id from Model
    var embedReportId = "@Model.Id";

    // Get models. models contains enums that can be used.
    var models = window['powerbi-client'].models;

    // Embed configuration used to describe the what and how to embed.
    // This object is used when calling powerbi.embed.
    // This also includes settings and options such as filters.
    // You can find more information at https://github.com/Microsoft/PowerBI-JavaScript/wiki/Embed-Configuration-Details.
    var config = {
        type: 'report',
        tokenType: models.TokenType.Embed,
        accessToken: accessToken,
        embedUrl: embedUrl,
        id: embedReportId,
        permissions: models.Permissions.All,
        settings: {
            filterPaneEnabled: true,
            navContentPaneEnabled: true
        }
    };

    // Get a reference to the embedded report HTML element
    var reportContainer = $('#reportContainer')[0];

    // Embed the report and display it within the div container.
    var report = powerbi.embed(reportContainer, config);
</script>
```

## <a name="next-steps"></a>Volgende stappen

* Er is een voorbeeldtoepassing beschikbaar op GitHub die u kunt bekijken. De bovenstaande voorbeelden zijn gebaseerd op dat voorbeeld. Voor meer informatie raadpleegt u [Voorbeeld voor insluiten voor uw organisatie](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/App%20Owns%20Data).
* Raadpleeg [Power BI JavaScript-API](https://github.com/Microsoft/PowerBI-JavaScript) voor meer informatie over de JavaScript-API.
* Raadpleeg [Veelgestelde vragen over de Power BI-cloud voor Duitsland](https://docs.microsoft.com/power-bi/service-govde-faq) voor meer informatie over de Power BI-cloud voor Duitsland
* [Inhoud van Power BI-werkruimteverzameling migreren naar Power BI](migrate-from-powerbi-embedded.md)

Beperkingen en overwegingen
* GCC-accounts bieden op dit moment alleen ondersteuning voor P- en EM-capaciteit

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)
