---
title: Een Power BI-tegel integreren in een app voor uw organisatie
description: Scenario voor het integreren van een tegel in een app, voorbeeldcode
services: powerbi
documentationcenter: 
author: markingmyname
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: get-started-article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 02/13/2018
ms.author: maghan
ms.openlocfilehash: c4c1b9223554491968a541c9d6b698a9655eded5
ms.sourcegitcommit: 2ceea44d3606c15b57142c37649c9d481ec4becc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2018
---
# <a name="integrate-a-tile-into-an-app-user-owns-data"></a>Een tegel in een app integreren (gebruiker is eigenaar van de gegevens)
Informatie over het integreren of insluiten van een tegel in een web-app met behulp van REST-API-aanroepen en de Power BI JavaScript-API voor uw organisatie.

![Ingesloten tegel in web-app](media/integrate-tile/powerbi-embedded-tile.png)

Als u wilt beginnen met dit scenario, hebt u een **Power BI**-account nodig. Als u geen account hebt, kunt u zich [aanmelden voor een gratis Power BI-account](../service-self-service-signup-for-power-bi.md). U kunt ook uw eigen [Azure Active Directory-tenant](create-an-azure-active-directory-tenant.md) maken voor testdoeleinden.

> [!NOTE]
> Wilt u in plaats daarvan een tegel insluiten voor uw klanten met een insluittoken? Zie [Een dashboard, tegel of rapport in uw toepassing integreren voor uw klanten](embed-sample-for-customers.md).
> 
> 

Als u een tegel wilt integreren in een web-app, gebruikt u de **Power BI** REST-API of de Power BI C# SDK en een **AD-toegangstoken** (Azure Active Directory) voor verificatie bij het ophalen van een tegel. Vervolgens kunt u de tegel laden met hetzelfde toegangstoken. De **Power BI** API biedt programmatische toegang tot bepaalde **Power BI**-resources. Zie voor meer informatie [Overzicht van Power BI REST-API](https://msdn.microsoft.com/library/dn877544.aspx) en de [Power BI JavaScript-API](https://github.com/Microsoft/PowerBI-JavaScript).

## <a name="download-the-sample"></a>Het voorbeeld downloaden
Dit artikel bevat de code die wordt gebruikt in de [integrate-tile-web-app](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-tile-web-app) op GitHub. Als u dit scenario wilt volgen, kunt u het voorbeeld downloaden.

## <a name="step-1---register-an-app-in-azure-ad"></a>Stap 1: een app bij Azure AD registreren
U moet uw toepassing registreren bij Azure AD om REST-API-aanroepen te kunnen uitvoeren. Zie [Een Azure AD-app voor het insluiten van Power BI-inhoud registreren](register-app.md) voor meer informatie.

Als u de [integrate-tile-web-app](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-tile-web-app) hebt gedownload, gebruikt u de **Client-ID** die en het **Clientgeheim** dat u krijgt na de registratie, zodat het voorbeeld kan verifiëren met Azure AD. Voor het configureren van het voorbeeld wijzigt u de **Client-ID** en het **Clientgeheim** in het bestand *cloud.config*.

![](media/integrate-tile/powerbi-embed-dashboard-register-app4.png)

## <a name="step-2---get-an-access-token-from-azure-ad"></a>Stap 2: een toegangstoken ophalen uit Azure AD
In uw app moet u eerst een **toegangstoken** van Azure AD ophalen voordat u de Power BI REST-API kunt aanroepen. Zie [Gebruikers verifiëren en een Azure AD-toegangstoken verkrijgen voor uw Power BI-app](get-azuread-access-token.md) voor meer informatie.

## <a name="step-3---get-a-tile"></a>Stap 3: een tegel ophalen
Als u een **Power BI**-tegel wilt ophalen, gebruikt u de bewerking [Tegels ophalen](https://msdn.microsoft.com/library/mt465741.aspx). Hiermee haalt u een lijst met **Power BI**-tegels op uit een bepaald dashboard. Vanuit de lijst met tegels kunt u een tegel-ID en insluitings-URL ophalen.

Voordat u de tegel kunt ophalen, moet eerst een dashboard-ID worden opgehaald. Zie [Een dashboard in een app integreren (gebruiker is eigenaar van gegevens)](integrate-dashboard.md) voor meer informatie over het ophalen van een dashboard.

### <a name="get-tiles-using-an-access-token"></a>Tegels ophalen met behulp van een toegangstoken
Met het **toegangstoken** dat u hebt opgehaald in [stap 2](#step-2-get-an-access-token-from-azure-ad) roept u de bewerking [Tegels ophalen](https://msdn.microsoft.com/library/mt465741.aspx) aan. Met de bewerking [Tegels ophalen](https://msdn.microsoft.com/library/mt465741.aspx) wordt een lijst met rapporten geretourneerd. U kunt een enkele tegel ophalen vanuit de lijst met rapporten. Hieronder vindt u een volledige C#-methode voor het ophalen van een tegel. 

Als u de REST-API-aanroep uitvoert, moet u de header *Autorisatie* met de indeling *Bearer {toegangstoken}* toevoegen.

#### <a name="get-tiles-with-the-rest-api"></a>Tegels ophalen met de REST-API
**Default.aspx.cs**

```
using Newtonsoft.Json;

//Get a tile from a dashboard. In this sample, you get the first tile.
protected void GetTile(string dashboardId, int index)
{
    //Configure tiles request
    System.Net.WebRequest request = System.Net.WebRequest.Create(
        String.Format("{0}Dashboards/{1}/Tiles",
        baseUri,
        dashboardId)) as System.Net.HttpWebRequest;

    request.Method = "GET";
    request.ContentLength = 0;
    request.Headers.Add("Authorization", String.Format("Bearer {0}", accessToken.Value));

    //Get tiles response from request.GetResponse()
    using (var response = request.GetResponse() as System.Net.HttpWebResponse)
    {
        //Get reader from response stream
        using (var reader = new System.IO.StreamReader(response.GetResponseStream()))
        {
            //Deserialize JSON string
            PBITiles tiles = JsonConvert.DeserializeObject<PBITiles>(reader.ReadToEnd());

            //Sample assumes at least one Dashboard with one Tile.
            //You could write an app that lists all tiles in a dashboard
            if (tiles.value.Length > 0)
                tileEmbedUrl.Text = tiles.value[index].embedUrl;
        }
    }
}

//Power BI Tiles used to deserialize the Get Tiles response.
public class PBITiles
{
    public PBITile[] value { get; set; }
}
public class PBITile
{
    public string id { get; set; }
    public string title { get; set; }
    public string embedUrl { get; set; }
}
```

#### <a name="get-tiles-using-the-net-sdk"></a>Tegels ophalen met de .NET SDK
U kunt de .NET-SDK gebruiken voor het ophalen van een lijst met dashboards. Zo hoeft u de REST-API niet rechtstreeks aan te roepen.

```
using Microsoft.IdentityModel.Clients.ActiveDirectory;
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;

var tokenCredentials = new TokenCredentials(<ACCESS TOKEN>, "Bearer");

// Create a Power BI Client object. It will be used to call Power BI APIs.
using (var client = new PowerBIClient(new Uri(ApiUrl), tokenCredentials))
{
    // Get a list of dashboards your "My Workspace"
    ODataResponseListDashboard tiles = client.Dashboards.GetDashboards();

    // Get a list of dashboards from a group (app workspace)
    ODataResponseListDashboard dashboards = client.Dashboards.GetDashboardsInGroup(groupId);

    Dashboard dashboard = dashboards.Value.FirstOrDefault();

    // Get the first tile from the above dashbaord
    ODataResponseListTile tiles = client.Dashboards.GetTiles(dashboard.Id);

    Tile tile = tiles.Value.FirstOrDefault();
}
```

## <a name="step-4---load-a-tile-using-javascript"></a>Stap 4: een tegel laden met JavaScript
U kunt JavaScript gebruiken om een tegel te laden in een div-element op uw webpagina.

**Default.aspx**

```
<!-- Embed Tile-->
<div> 
    <asp:Panel ID="PanelEmbed" runat="server" Visible="true">
        <div>
            <div><b class="step">Step 3</b>: Embed a tile</div>

            <div>Enter an embed url for a tile from Step 2 (starts with https://):</div>
            <input type="text" id="tb_EmbedURL" style="width: 1024px;" />
            <br />
            <input type="button" id="bEmbedTileAction" value="Embed Tile" />
        </div>

        <div id="tileContainer"></div>
    </asp:Panel>
</div>
```

**Site.master**

```
window.onload = function () {
    // client side click to embed a selected tile.
    var el = document.getElementById("bEmbedTileAction");
    if (el.addEventListener) {
        el.addEventListener("click", updateEmbedTile, false);
    } else {
        el.attachEvent('onclick', updateEmbedTile);
    }

    // handle server side post backs, optimize for reload scenarios
    // show embedded tile if all fields were filled in.
    var accessTokenElement = document.getElementById('MainContent_accessTokenTextbox');
    if (accessTokenElement !== null) {
        var accessToken = accessTokenElement.value;
        if (accessToken !== "")
            updateEmbedTile();
    }
};

// update embed tile
function updateEmbedTile() {

    // check if the embed url was selected
    var embedUrl = document.getElementById('tb_EmbedURL').value;
    if (embedUrl === "")
        return;

    // get the access token.
    accessToken = document.getElementById('MainContent_accessTokenTextbox').value;

    // Embed configuration used to describe the what and how to embed.
    // This object is used when calling powerbi.embed.
    // You can find more information at https://github.com/Microsoft/PowerBI-JavaScript/wiki/Embed-Configuration-Details.
    var config = {
        type: 'tile',
        accessToken: accessToken,
        embedUrl: embedUrl
    };

    // Grab the reference to the div HTML element that will host the tile.
    var tileContainer = document.getElementById('tileContainer');

    // Embed the tile and display it within the div container.
    var tile = powerbi.embed(tileContainer, config);

    // tile.on will add an event handler which prints to Log window.
    tile.on("error", function (event) {
        var logView = document.getElementById('logView');
        logView.innerHTML = logView.innerHTML + "Error<br/>";
        logView.innerHTML = logView.innerHTML + JSON.stringify(event.detail, null, "  ") + "<br/>";
        logView.innerHTML = logView.innerHTML + "---------<br/>";
    });
}
```

Als u de [integrate-tile-web-app](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-tile-web-app) hebt gedownload en uitgevoerd, ziet deze er ongeveer uit zoals hieronder.

![Ingesloten tegel in web-app](media/integrate-tile/powerbi-embedded-tile.png)

## <a name="working-with-groups-app-workspaces"></a>Met groepen werken (app-werkruimten)
Als u een tegel uit een groep (app-werkgroep) wilt insluiten, hebt u de lijst met alle beschikbare tegels in een dashboard van een groep nodig. Deze roept u aan met de volgende REST-API-aanroep. Zie [Tegels ophalen](https://msdn.microsoft.com/library/mt465741.aspx) voor meer informatie over deze REST-API-aanroep. U moet binnen de groep gemachtigd zijn, anders retourneert de aanvraag geen resultaten.

```
https://api.powerbi.com/v1.0/myorg/groups/{groupId}/dashboards/{dashboard_id}/tiles
```

De bovenstaande API retourneert de lijst met beschikbare tegels. Elke tegel heeft een EmbedUrl-eigenschap die al is gemaakt voor het ondersteunen van ingesloten groepen.

```
https://app.powerbi.com/embed?dashboardId={dashboard_id}&tileId={tile_id}&groupId={group_id}
```

## <a name="next-steps"></a>Volgende stappen
[Tegel insluiten](https://github.com/Microsoft/PowerBI-JavaScript/wiki/Tile-Embed) in Power BI-JavaScript Wiki

[Power BI JavaScript-API](https://github.com/Microsoft/PowerBI-JavaScript)

Voorbeeld van [integrate-tile-web-app](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-tile-web-app) op GitHub.

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

