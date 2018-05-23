---
title: Een Power BI-rapport integreren in een app voor uw organisatie
description: Informatie over het integreren of insluiten van een rapport in een web-app met behulp van de Power BI-API's.
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-developer
ms.topic: conceptual
ms.date: 10/05/2017
ms.author: maghan
ms.openlocfilehash: d2fa65587fdbd85aabd429d531b79e9e614d2f49
ms.sourcegitcommit: 638de55f996d177063561b36d95c8c71ea7af3ed
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/17/2018
---
# <a name="integrate-a-report-into-an-app-for-your-organization"></a>Een rapport integreren in een app voor uw organisatie
Informatie over het integreren of insluiten van een rapport in een web-app met behulp van REST-API-aanroepen en de Power BI JavaScript-API voor uw organisatie.

![Voorbeeld van ingesloten rapport](media/integrate-report/powerbi-embedded-report.png)

Als u wilt beginnen met dit scenario, hebt u een **Power BI**-account nodig. Als u geen account hebt, kunt u zich [aanmelden voor een gratis Power BI-account](../service-self-service-signup-for-power-bi.md). U kunt ook uw eigen [Azure Active Directory-tenant](create-an-azure-active-directory-tenant.md) maken voor testdoeleinden.

> [!NOTE]
> Wilt u in plaats daarvan een rapport insluiten voor uw klanten met een insluittoken? Zie [Een dashboard, tegel of rapport in uw toepassing integreren voor uw klanten](embed-sample-for-customers.md).
> 
> 

Als u een rapport wilt integreren in een web-app, gebruikt u de **Power BI** REST-API of de Power BI C# SDK en een **AD-toegangstoken** (Azure Active Directory) voor verificatie bij het ophalen van een rapport. Vervolgens kunt u het rapport laden met hetzelfde toegangstoken. De **Power BI** API biedt programmatische toegang tot bepaalde **Power BI**-resources. Zie voor meer informatie [Overzicht van Power BI REST-API](https://msdn.microsoft.com/library/dn877544.aspx) en de [Power BI JavaScript-API](https://github.com/Microsoft/PowerBI-JavaScript).

## <a name="download-the-sample"></a>Het voorbeeld downloaden
Dit artikel bevat de code die wordt gebruikt in de [integrate-report-web-app](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-report-web-app) op GitHub. Als u dit scenario wilt volgen, kunt u het voorbeeld downloaden.

## <a name="step-1---register-an-app-in-azure-ad"></a>Stap 1: een app bij Azure AD registreren
U moet uw toepassing registreren bij Azure AD om REST-API-aanroepen te kunnen uitvoeren. Zie [Een Azure AD-app voor het insluiten van Power BI-inhoud registreren](register-app.md) voor meer informatie.

Als u de [integrate-report-web-app](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-report-web-app) hebt gedownload, gebruikt u de **Client-ID** die en het **Clientgeheim** dat u krijgt na de registratie, zodat het voorbeeld kan verifiëren met Azure AD. Voor het configureren van het voorbeeld wijzigt u de **Client-ID** en het **Clientgeheim** in het bestand *cloud.config*.

![](media/integrate-report/powerbi-embed-dashboard-register-app4.png)

## <a name="step-2---get-an-access-token-from-azure-ad"></a>Stap 2: een toegangstoken ophalen uit Azure AD
In uw app moet u eerst een **toegangstoken** van Azure AD ophalen voordat u de Power BI REST-API kunt aanroepen. Zie [Gebruikers verifiëren en een Azure AD-toegangstoken verkrijgen voor uw Power BI-app](get-azuread-access-token.md) voor meer informatie.

## <a name="step-3---get-a-report"></a>Stap 3: een rapport ophalen
Als u een **Power BI**-rapport wilt ophalen, gebruikt u de bewerking [Rapporten ophalen](https://msdn.microsoft.com/library/mt634543.aspx). Hiermee haalt u een lijst met **Power BI**-rapporten op. Vanuit de lijst met rapporten kunt u een rapport-ID ophalen.

### <a name="get-reports-using-an-access-token"></a>Rapporten ophalen met behulp van een toegangstoken
Met het **toegangstoken** dat u hebt opgehaald in [stap 2](#step-2-get-an-access-token-from-azure-ad) roept u de bewerking [Rapporten ophalen](https://msdn.microsoft.com/library/mt634543.aspx) aan. Met de bewerking [Rapporten ophalen](https://msdn.microsoft.com/library/mt634543.aspx) wordt een lijst met rapporten geretourneerd. U kunt een enkel rapport ophalen vanuit de lijst met rapporten. Hieronder vindt u een volledige C#-methode voor het ophalen van een rapport. 

Als u de REST-API-aanroep uitvoert, moet u de header *Autorisatie* met de indeling *Bearer {toegangstoken}* toevoegen.

#### <a name="get-reports-with-the-rest-api"></a>Rapporten ophalen met de REST-API
**Default.aspx.cs**

```
using Newtonsoft.Json;

//Get a Report. In this sample, you get the first Report.
protected void GetReport(int index)
{
    //Configure Reports request
    System.Net.WebRequest request = System.Net.WebRequest.Create(
        String.Format("{0}/Reports",
        baseUri)) as System.Net.HttpWebRequest;

    request.Method = "GET";
    request.ContentLength = 0;
    request.Headers.Add("Authorization", String.Format("Bearer {0}", accessToken.Value));

    //Get Reports response from request.GetResponse()
    using (var response = request.GetResponse() as System.Net.HttpWebResponse)
    {
        //Get reader from response stream
        using (var reader = new System.IO.StreamReader(response.GetResponseStream()))
        {
            //Deserialize JSON string
            PBIReports Reports = JsonConvert.DeserializeObject<PBIReports>(reader.ReadToEnd());

            //Sample assumes at least one Report.
            //You could write an app that lists all Reports
            if (Reports.value.Length > 0)
            {
                var report = Reports.value[index];

                txtEmbedUrl.Text = report.embedUrl;
                txtReportId.Text = report.id;
                txtReportName.Text = report.name;
            }
        }
    }
}

//Power BI Reports used to deserialize the Get Reports response.
public class PBIReports
{
    public PBIReport[] value { get; set; }
}
public class PBIReport
{
    public string id { get; set; }
    public string name { get; set; }
    public string webUrl { get; set; }
    public string embedUrl { get; set; }
}
```

#### <a name="get-reports-using-the-net-sdk"></a>Rapporten ophalen met de .NET SDK
U kunt de .NET-SDK gebruiken voor het ophalen van een lijst met rapporten. Zo hoeft u de REST-API niet rechtstreeks aan te roepen.

```
using Microsoft.IdentityModel.Clients.ActiveDirectory;
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;

var tokenCredentials = new TokenCredentials(<ACCESS TOKEN>, "Bearer");

// Create a Power BI Client object. It will be used to call Power BI APIs.
using (var client = new PowerBIClient(new Uri(ApiUrl), tokenCredentials))
{
    // Get the first report all reports in that workspace
    ODataResponseListReport reports = client.Reports.GetReports();

    Report report = reports.Value.FirstOrDefault();

    var embedUrl = report.EmbedUrl;
}
```

## <a name="step-4---load-a-report-using-javascript"></a>Stap 4: een rapport laden met JavaScript
U kunt JavaScript gebruiken om een rapport te laden in een div-element op uw webpagina.

**Default.aspx**

```
<!-- Embed Report-->
<div> 
    <asp:Panel ID="PanelEmbed" runat="server" Visible="true">
        <div>
            <div><b class="step">Step 3</b>: Embed a report</div>

            <div>Enter an embed url for a report from Step 2 (starts with https://):</div>
            <input type="text" id="tb_EmbedURL" style="width: 1024px;" />
            <br />
            <input type="button" id="bEmbedReportAction" value="Embed Report" />
        </div>

        <div id="reportContainer"></div>
    </asp:Panel>
</div>
```

**Site.master**

```
window.onload = function () {
    // client side click to embed a selected report.
    var el = document.getElementById("bEmbedReportAction");
    if (el.addEventListener) {
        el.addEventListener("click", updateEmbedReporte, false);
    } else {
        el.attachEvent('onclick', updateEmbedReport);
    }

    // handle server side post backs, optimize for reload scenarios
    // show embedded report if all fields were filled in.
    var accessTokenElement = document.getElementById('MainContent_accessTokenTextbox');
    if (accessTokenElement !== null) {
        var accessToken = accessTokenElement.value;
        if (accessToken !== "")
            updateEmbedReport();
    }
};

// update embed report
function updateEmbedReport() {

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
        type: 'report',
        accessToken: accessToken,
        embedUrl: embedUrl
    };

    // Grab the reference to the div HTML element that will host the report.
    var reportContainer = document.getElementById('reportContainer');

    // Embed the report and display it within the div container.
    var report = powerbi.embed(reportContainer, config);

    // report.on will add an event handler which prints to Log window.
    report.on("error", function (event) {
        var logView = document.getElementById('logView');
        logView.innerHTML = logView.innerHTML + "Error<br/>";
        logView.innerHTML = logView.innerHTML + JSON.stringify(event.detail, null, "  ") + "<br/>";
        logView.innerHTML = logView.innerHTML + "---------<br/>";
    });
}
```

Als u de [integrate-report-web-app](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-report-web-app) hebt gedownload en uitgevoerd, ziet deze er ongeveer uit zoals hieronder.

![Voorbeeld van ingesloten rapport](media/integrate-report/powerbi-embedded-report.png)

## <a name="working-with-groups-app-workspaces"></a>Met groepen werken (app-werkruimten)
Als u een rapport uit een groep (app-werkgroep) wilt insluiten, hebt u de lijst met alle beschikbare rapporten in een dashboard van een groep nodig. Deze roept u aan met de volgende REST-API-aanroep. Zie [Rapporten ophalen](https://msdn.microsoft.com/library/mt634543.aspx) voor meer informatie over deze REST-API-aanroep. U moet binnen de groep gemachtigd zijn, anders retourneert de aanvraag geen resultaten.

```
https://api.powerbi.com/v1.0/myorg/groups/{group_id}/reports
```

De bovenstaande API retourneert de lijst met beschikbare rapporten. Elk rapport heeft een EmbedUrl-eigenschap die al is gemaakt voor het ondersteunen van ingesloten groepen.

```
https://app.powerbi.com/reportEmbed?reportId={report_id}&groupId={group_id}
```

## <a name="next-steps"></a>Volgende stappen
Er is een voorbeeldtoepassing beschikbaar op GitHub die u kunt bekijken. Zie [integrate-report-web-app](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-report-web-app) voor meer informatie.

Er is meer informatie beschikbaar voor de JavaScript-API, zie [Power BI JavaScript-API](https://github.com/Microsoft/PowerBI-JavaScript).

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

