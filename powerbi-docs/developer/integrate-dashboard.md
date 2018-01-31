---
title: Een dashboard integreren in een app voor uw organisatie
description: Informatie over het integreren of insluiten van een dashboard in een web-app met behulp van de Power BI-API's.
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
ms.date: 10/05/2017
ms.author: maghan
ms.openlocfilehash: 36b19588d76c99cb712dc481752ebdee0c867f0d
ms.sourcegitcommit: 6e693f9caf98385a2c45890cd0fbf2403f0dbb8a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2018
---
# <a name="integrate-a-dashboard-into-an-app-for-your-organization"></a>Een dashboard integreren in een app voor uw organisatie
Informatie over het integreren of insluiten van een dashboard in een web-app met behulp van REST-API-aanroepen en de Power BI JavaScript API voor uw organisatie.

![Ingesloten dashboard](media/integrate-dashboard/powerbi-embed-dashboard.png)

Als u wilt beginnen met dit scenario, hebt u een **Power BI**-account nodig. Als u geen account hebt, kunt u zich [aanmelden voor een gratis Power BI-account](../service-self-service-signup-for-power-bi.md). U kunt ook uw eigen [Azure Active Directory-tenant](create-an-azure-active-directory-tenant.md) maken voor testdoeleinden.

> [!NOTE]
> Wilt u in plaats daarvan een dashboard insluiten voor uw klanten met een insluittoken? Zie [Een dashboard, tegel of rapport in uw toepassing integreren voor uw klanten](embed-sample-for-customers.md).
> 
> 

Als u een dashboard wilt integreren in een web-app, gebruikt u de **Power BI** REST-API of de Power BI C# SDK en een **AD-toegangstoken** (Azure Active Directory) voor verificatie bij het ophalen van een dashboard. Vervolgens kunt u het dashboard laden met hetzelfde toegangstoken. De **Power BI** API biedt programmatische toegang tot bepaalde **Power BI**-resources. Zie voor meer informatie [Overzicht van Power BI REST-API](https://msdn.microsoft.com/library/dn877544.aspx) en de [Power BI JavaScript-API](https://github.com/Microsoft/PowerBI-JavaScript).

## <a name="download-the-sample"></a>Het voorbeeld downloaden
Dit artikel bevat de code die wordt gebruikt in de [integrate-dashboard-web-app](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-dashboard-web-app) op GitHub. Als u dit scenario wilt volgen, kunt u het voorbeeld downloaden.

## <a name="step-1---register-an-app-in-azure-ad"></a>Stap 1: een app bij Azure AD registreren
U moet uw toepassing registreren bij Azure AD om REST-API-aanroepen te kunnen uitvoeren. Zie [Een Azure AD-app voor het insluiten van Power BI-inhoud registreren](register-app.md) voor meer informatie.

Als u het [Voorbeeld voor het insluiten van een dashboard](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-dashboard-web-app) hebt gedownload, gebruikt u de **Client-ID** en het **Clientgeheim** die u krijgt na de registratie, zodat het voorbeeld kan verifiëren met Azure AD. Voor het configureren van het voorbeeld wijzigt u de **Client-ID** en het **Clientgeheim** in het bestand *cloud.config*.

![](media/integrate-dashboard/powerbi-embed-dashboard-register-app4.png)

## <a name="step-2---get-an-access-token-from-azure-ad"></a>Stap 2: een toegangstoken ophalen uit Azure AD
In uw app moet u eerst een **toegangstoken** van Azure AD ophalen voordat u de Power BI REST-API kunt aanroepen. Zie [Gebruikers verifiëren en een Azure AD-toegangstoken verkrijgen voor uw Power BI-app](get-azuread-access-token.md) voor meer informatie.

## <a name="step-3---get-a-dashboard"></a>Stap 3: een dashboard ophalen
Als u een **Power BI**-dashboard wilt ophalen, gebruikt u de bewerking [Dashboards ophalen](https://msdn.microsoft.com/library/mt465739.aspx). Hiermee haalt u een lijst met **Power BI**-dashboards op. U kunt een dashboard-ID ophalen uit de lijst met dashboards.

![](media/integrate-dashboard/powerbi-embed-dashboard-get-dashboards.png)

### <a name="get-dashboards-using-an-access-token"></a>Dashboards ophalen met behulp van een toegangstoken
Met het **toegangstoken** dat u hebt opgehaald in [stap 2](#step-2-get-an-access-token-from-azure-ad) roept u de bewerking [Dashboards ophalen](https://msdn.microsoft.com/library/mt465739.aspx) aan. De bewerking [Dashboards ophalen](https://msdn.microsoft.com/library/mt465739.aspx) retourneert een lijst met dashboards. U kunt één dashboard ophalen uit de lijst met dashboards. Hieronder vindt u een volledige C#-methode voor het ophalen van een dashboard. 

Als u de REST-API-aanroep uitvoert, moet u de header *Autorisatie* met de indeling *Bearer {toegangstoken}* toevoegen.

#### <a name="get-dashboards-with-the-rest-api"></a>Dashboards ophalen met de REST-API
**Default.aspx.cs**

```
protected void getDashboardsButton_Click(object sender, EventArgs e)
{
    string responseContent = string.Empty;

    //Configure dashboards request
    System.Net.WebRequest request = System.Net.WebRequest.Create(String.Format("{0}dashboards", baseUri)) as System.Net.HttpWebRequest;
    request.Method = "GET";
    request.ContentLength = 0;
    request.Headers.Add("Authorization", String.Format("Bearer {0}", authResult.AccessToken));

    //Get dashboards response from request.GetResponse()
    using (var response = request.GetResponse() as System.Net.HttpWebResponse)
    {
        //Get reader from response stream
        using (var reader = new System.IO.StreamReader(response.GetResponseStream()))
        {
            responseContent = reader.ReadToEnd();

            //Deserialize JSON string
            PBIDashboards PBIDashboards = JsonConvert.DeserializeObject<PBIDashboards>(responseContent);

            if (PBIDashboards != null)
            {
                var gridViewDashboards = PBIDashboards.value.Select(dashboard => new {
                    Id = dashboard.id,
                    DisplayName = dashboard.displayName,
                    EmbedUrl = dashboard.embedUrl
                });

                this.GridView1.DataSource = gridViewDashboards;
                this.GridView1.DataBind();
            }
        }
    }
}

//Power BI Dashboards used to deserialize the Get Dashboards response.
public class PBIDashboards
{
    public PBIDashboard[] value { get; set; }
}
public class PBIDashboard
{
    public string id { get; set; }
    public string displayName { get; set; }
    public string embedUrl { get; set; }
    public bool isReadOnly { get; set; }
}
```

#### <a name="get-dashboards-using-the-net-sdk"></a>Dashboards ophalen met de .NET-SDK
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
    ODataResponseListDashboard dashboards = client.Dashboards.GetDashboards();

    // Get a list of dashboards from a group (app workspace)
    ODataResponseListDashboard dashboards = client.Dashboards.GetDashboardsInGroup(groupId);

    Dashboard dashboard = dashboards.Value.FirstOrDefault();

    var embedUrl = dashboard.EmbedUrl
}
```

## <a name="step-4---load-a-dashboard-using-javascript"></a>Stap 4: een dashboard laden met JavaScript
U kunt JavaScript gebruiken om een dashboard te laden in een div-element op uw webpagina.

**Default.aspx**

```
<!-- Embed Dashboard-->
<div> 
    <asp:Panel ID="PanelEmbed" runat="server" Visible="true">
        <div>
            <div><b class="step">Step 3</b>: Embed a dashboard</div>

            <div>Enter an embed url for a dashboard from Step 2 (starts with https://):</div>
            <input type="text" id="tb_EmbedURL" style="width: 1024px;" />
            <br />
            <input type="button" id="bEmbedDashboardAction" value="Embed Dashboard" />
        </div>

        <div id="dashboardContainer"></div>
    </asp:Panel>
</div>
```

**Site.master**

```
window.onload = function () {
    // client side click to embed a selected dashboard.
    var el = document.getElementById("bEmbedDashboardAction");
    if (el.addEventListener) {
        el.addEventListener("click", updateEmbedDashboard, false);
    } else {
        el.attachEvent('onclick', updateEmbedDashboard);
    }

    // handle server side post backs, optimize for reload scenarios
    // show embedded dashboard if all fields were filled in.
    var accessTokenElement = document.getElementById('MainContent_accessTokenTextbox');
    if (accessTokenElement !== null) {
        var accessToken = accessTokenElement.value;
        if (accessToken !== "")
            updateEmbedDashboard();
    }
};

// update embed dashboard
function updateEmbedDashboard() {

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
        type: 'dashboard',
        accessToken: accessToken,
        embedUrl: embedUrl
    };

    // Grab the reference to the div HTML element that will host the dashboard.
    var dashboardContainer = document.getElementById('dashboardContainer');

    // Embed the dashboard and display it within the div container.
    var dashboard = powerbi.embed(dashboardContainer, config);

    // dashboard.on will add an event handler which prints to Log window.
    dashboard.on("tileClicked", function (event) {
        var logView = document.getElementById('logView');
        logView.innerHTML = logView.innerHTML + "Tile Clicked<br/>";
        logView.innerHTML = logView.innerHTML + JSON.stringify(event.detail, null, "  ") + "<br/>";
        logView.innerHTML = logView.innerHTML + "---------<br/>";
    });

    // dashboard.on will add an event handler which prints to Log window.
    dashboard.on("error", function (event) {
        var logView = document.getElementById('logView');
        logView.innerHTML = logView.innerHTML + "Error<br/>";
        logView.innerHTML = logView.innerHTML + JSON.stringify(event.detail, null, "  ") + "<br/>";
        logView.innerHTML = logView.innerHTML + "---------<br/>";
    });
}
```

Als u het [Voorbeeld voor het insluiten van een dashboard](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-dashboard-web-app) hebt gedownload en uitgevoerd, ziet het er ongeveer uit zoals hieronder.

![](media/integrate-dashboard/powerbi-embed-dashboard.png)

## <a name="tile-clicked-events"></a>Gebeurtenissen na het klikken op een tegel
U hebt wellicht in het bovenstaande voorbeeld gezien dat u gebeurtenissen kunt verwerken wanneer op de tegel wordt geklikt in het dashboard. Voor meer informatie over gebeurtenissen bekijkt u [Gebeurtenissen verwerken binnen de JavaScript API](https://github.com/Microsoft/PowerBI-JavaScript/wiki/Handling-Events).

```
// dashboard.on will add an event handler which prints to Log window.
dashboard.on("tileClicked", function (event) {
    var logView = document.getElementById('logView');
    logView.innerHTML = logView.innerHTML + "Tile Clicked<br/>";
    logView.innerHTML = logView.innerHTML + JSON.stringify(event.detail, null, "  ") + "<br/>";
    logView.innerHTML = logView.innerHTML + "---------<br/>";
});

// dashboard.on will add an event handler which prints to Log window.
dashboard.on("error", function (event) {
    var logView = document.getElementById('logView');
    logView.innerHTML = logView.innerHTML + "Error<br/>";
    logView.innerHTML = logView.innerHTML + JSON.stringify(event.detail, null, "  ") + "<br/>";
    logView.innerHTML = logView.innerHTML + "---------<br/>";
});
```

Als u het [Voorbeeld voor het insluiten van een dashboard](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/PowerBI.com%20Integrate/integrate-dashboard-web-app) hebt gedownload en uitgevoerd, verschijnt er tekstuitvoer onder het dashboard als er op een tegel wordt geklikt. De tekst moet er nu als volgt uitzien. Hiermee kunt u registreren dat er op een tegel is geklikt. Vervolgens wordt de gebruiker naar de gewenste locatie geleid.

```
Tile Clicked
{ "event": "TileClick", "reportEmbedUrl": "", "navigationUrl": "https://app.powerbi.com/dashboards/fcff76f9-15ff-4a8e-8242-275ac9c25b90/qna?q=count%20of%20new%20hires%20from%20July%202014%20to%20December%202014", "tileId": "0e99b45c-9b53-4920-b239-cee7d37d2369" }
---------
Tile Clicked
{ "event": "TileClick", "reportEmbedUrl": "https://app.powerbi.com/reportEmbed?reportId=ab199308-80b1-4626-9823-43a84623bd9c", "navigationUrl": "https://app.powerbi.com/reports/ab199308-80b1-4626-9823-43a84623bd9c/ReportSection1", "tileId": "ffc30447-674a-4511-944f-79e182d719de", "pageName": "ReportSection1" }
---------
```

## <a name="working-with-groups-app-workspaces"></a>Met groepen werken (app-werkruimten)
Als u een dashboard uit een groep (app-werkgroep) wilt insluiten, hebt u de lijst met alle beschikbare dashboards in een groep nodig. Deze roept u aan met de volgende REST-API-aanroep. Zie [Dashboards ophalen](https://msdn.microsoft.com/library/mt465739.aspx) voor meer informatie over deze REST-API-aanroep. U moet binnen de groep gemachtigd zijn, anders retourneert de aanvraag geen resultaten.

```
https://api.powerbi.com/v1.0/myorg/groups/{groupId}/dashboards
```

De bovenstaande API retourneert de lijst met beschikbare dashboards. Elke dashboard heeft een EmbedUrl-eigenschap die al is gemaakt voor het ondersteunen van ingesloten groepen.

```
https://app.powerbi.com/dashboardEmbed?dashboardId={dashboardId}&groupId={groupId}
```

## <a name="limitations"></a>Beperkingen
* De eindgebruikers die toegang hebben tot de ingesloten dashboards moeten een Power BI-account hebben en toegang hebben tot het dashboard. Ze moeten eigenaar zijn van het dashboard, of het dashboard moet zijn gedeeld met de gebruiker.
* Q&A wordt momenteel niet ondersteund in ingesloten dashboards.
* Wanneer een gebruiker een dashboard wil delen met beveiligingsgroepen, moet hij eerst toegang krijgen tot de dashboards in PowerBI.com voordat hij de ingesloten variant kan zien. Dit is een tijdelijke beperking.

## <a name="next-steps"></a>Volgende stappen
Er is een voorbeeldtoepassing beschikbaar op GitHub die u kunt bekijken. De bovenstaande voorbeelden zijn gebaseerd op dat voorbeeld. Zie [integrate-dashboard-web-app](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-dashboard-web-app) voor meer informatie.

Er is meer informatie beschikbaar voor de JavaScript API, zie [Power BI JavaScript API](https://github.com/Microsoft/PowerBI-JavaScript).

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

