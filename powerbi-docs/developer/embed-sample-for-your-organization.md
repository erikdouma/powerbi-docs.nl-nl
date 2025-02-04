---
title: Ingesloten analyse om Power BI-inhoud in te sluiten in uw toepassing voor uw organisatie
description: Informatie over het integreren of insluiten van een rapport, dashboard of tegel in een toepassing voor uw organisatie met behulp van de Power BI-API's voor ingesloten analyse. Informatie over het integreren van Power BI in uw toepassing met behulp van software voor ingesloten analyse, hulpprogramma's voor ingesloten analyse of hulpprogramma's voor ingesloten business intelligence.
author: markingmyname
ms.author: maghan
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: tutorial
ms.custom: seodec18
ms.date: 03/12/2019
ms.openlocfilehash: 34d7ec423f3d4cb0f7487c78eff68c580ff0489e
ms.sourcegitcommit: f176ba9d52d50d93f264eca21bb3fd987dbf934b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2019
ms.locfileid: "57757456"
---
# <a name="tutorial-embed-power-bi-content-into-an-application-for-your-organization"></a>Zelfstudie: Power BI-inhoud insluiten in een toepassing voor uw organisatie

In **Power BI** kunt u rapporten, dashboards en tegels in een toepassing insluiten met gegevens waarvan de gebruiker eigenaar is. Uw toepassing kan met **gegevens waarvan de gebruiker eigenaar is** de Power BI-service uitbreiden voor gebruik met ingesloten analyse. In deze zelfstudie leert u hoe u een rapport in een toepassing integreert. U gebruikt de Power BI .NET-SDK met de Power BI JavaScript-API om Power BI in te sluiten in een toepassing voor uw organisatie.

![Power BI Embed-rapport](media/embed-sample-for-your-organization/embed-sample-for-your-organization-035.png)

In deze zelfstudie leert u de volgende taken:
> [!div class="checklist"]
> * Een toepassing registreren in Azure.
> * Sluit een Power BI-rapport in een toepassing in met uw Power BI-tenant.

## <a name="prerequisites"></a>Vereisten

U hebt het volgende nodig om aan de slag te gaan:

* Een [Power BI Pro-account](../service-self-service-signup-for-power-bi.md).
* Een [Microsoft Azure](https://azure.microsoft.com/)-abonnement.
* U moet beschikken over een eigen [Azure Active Directory-tenant ](create-an-azure-active-directory-tenant.md).

Als u zich niet hebt geregistreerd voor **Power BI Pro**, [kunt u zich hier aanmelden voor een gratis proefversie](https://powerbi.microsoft.com/pricing/) voordat u begint.

Als u nog geen abonnement op Azure hebt, maakt u een [gratis account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) voordat u begint.

## <a name="set-up-your-embedded-analytics-development-environment"></a>De ingesloten analytische ontwikkelomgeving instellen

Voordat u begint met het insluiten van rapporten, dashboards en tegels in uw toepassing, moet u insluiting met Power BI mogelijk maken in uw omgeving.

U kunt het [installatieprogramma voor insluiten](https://aka.ms/embedsetup/UserOwnsData) uitvoeren om snel aan de slag te gaan en een voorbeeldtoepassing te downloaden waarmee u een omgeving leert maken en een rapport leert insluiten.

Als u echter besluit de omgeving handmatig in te stellen, kunt u hieronder doorgaan.

### <a name="register-an-application-in-azure-active-directory"></a>Een toepassing registreren in Azure Active Directory

[Registreer uw toepassing](register-app.md) bij Azure Active Directory AD zodat uw toepassing toegang heeft tot de [Power BI REST API's](https://docs.microsoft.com/rest/api/power-bi/). Als u uw toepassing registreert, kunt u een identiteit instellen voor uw toepassing en machtigingen opgeven voor Power BI REST-resources.

U moet vervolgens een **webtoepassing aan de serverzijde** registreren. U registreert een webtoepassing aan de serverzijde om een toepassingsgeheim te maken.

## <a name="set-up-your-power-bi-environment"></a>Uw Power BI-omgeving instellen

### <a name="create-an-app-workspace"></a>Een app-werkruimte maken

Als u rapporten, dashboards of tegels voor uw klanten insluit, moet u uw inhoud binnen de werkruimte van een app plaatsen. Er zijn verschillende typen werkruimten die u kunt instellen: de [traditionele werkruimten](../service-create-workspaces.md) of de [nieuwe werkruimten](../service-create-the-new-workspaces.md).

### <a name="create-and-publish-your-reports"></a>Rapporten maken en publiceren

U kunt uw rapporten en gegevenssets maken met behulp van Power BI Desktop. Vervolgens kunt u die rapporten publiceren naar een app-werkruimte. De eindgebruiker die de rapporten naar een app-werkruimte publiceert, moet beschikken over een Power BI Pro-licentie.

1. Download het voorbeeld van de [demo](https://github.com/Microsoft/powerbi-desktop-samples) vanuit GitHub.

    ![De demo downloaden](media/embed-sample-for-your-organization/embed-sample-for-your-organization-026-1.png)

2. Open het .pbix-voorbeeldrapport in Power BI Desktop.

   ![Power BI Desktop-voorbeeldrapport](media/embed-sample-for-your-organization/embed-sample-for-your-organization-027.png)

3. Publiceer het rapport naar de app-werkruimte.

   ![Een Power BI Desktop-rapport publiceren](media/embed-sample-for-your-organization/embed-sample-for-your-organization-028.png)

    U kunt het rapport nu weergeven in Power BI-service online.

   ![Een Power BI Desktop-rapport weergeven](media/embed-sample-for-your-organization/embed-sample-for-your-organization-029.png)

## <a name="embed-your-content-by-using-the-sample-application"></a>Uw inhoud met behulp van de voorbeeldtoepassing insluiten

We hebben dit voorbeeld voor demonstratiedoeleinden bewust eenvoudig gehouden.

Volg de onderstaande stappen om inhoud in te sluiten met de voorbeeldtoepassing.

1. Download [Visual Studio](https://www.visualstudio.com/) (versie 2013 of later). Download het meest recente [NuGet-pakket](https://www.nuget.org/profiles/powerbi).

2. Download het [voorbeeld waarin de gebruiker eigenaar is van de gegevens](https://github.com/Microsoft/PowerBI-Developer-Samples) vanuit GitHub om aan de slag te gaan.

    ![Voorbeeldtoepassing waarin gebruiker eigenaar is van de gegevens](media/embed-sample-for-your-organization/embed-sample-for-your-organization-026.png)

3. Open het bestand **Cloud.config** in de voorbeeldtoepassing.

    Er zijn velden die u moet invullen om de toepassing uit te voeren.

    | Veld |
    |--------------------|
    | **[Toepassings-id](#application-id)** |
    | **[Toepassingsgeheim](#application-secret)** |
    | **[Werkruimte-id](#workspace-id)** |
    | **[Rapport-id](#report-id)** |
    | **[AADAuthorityUrl](#aadauthorityurl)** |

    ![Cloud.config-bestand](media/embed-sample-for-your-organization/embed-sample-for-your-organization-030.png)

### <a name="application-id"></a>Toepassings-id

Vul bij **applicationId** de **Toepassings-id** van **Azure** in. De **applicationId** wordt door de toepassing gebruikt om zich te identificeren bij de gebruikers bij wie u machtigingen aanvraagt.

Ga als volgt te werk om de **applicationId** op te halen:

1. Meld u aan bij [Azure Portal](https://portal.azure.com).

2. Selecteer in het navigatiedeelvenster links **Alle services** en selecteer **App-registraties**.

    ![App-registratie zoeken](media/embed-sample-for-customers/embed-sample-for-customers-003.png)

3. Selecteer de toepassing waarvoor de **applicationID** nodig is.

    ![App kiezen](media/embed-sample-for-customers/embed-sample-for-customers-006.png)

4. U ziet een **toepassings-id** die wordt vermeld als een GUID. Gebruik deze **Toepassings-id** als de **applicationId** voor de toepassing.

    ![applicationId](media/embed-sample-for-customers/embed-sample-for-customers-007.png)

### <a name="application-secret"></a>Toepassingsgeheim

Geef de **ApplicationSecret**-gegevens op in de sectie **Sleutels** van de sectie **App-registraties** in **Azure**.  Dit kenmerk werkt wanneer u een [service-principal](embed-service-principal.md) gebruikt.

Ga als volgt te werk om de **ApplicationSecret** op te halen:

1. Meld u aan bij [Azure Portal](https://portal.azure.com).

2. Selecteer in het navigatiedeelvenster links **Alle services** en selecteer vervolgens **App-registraties**.

    ![App-registratie zoeken](media/embed-sample-for-your-organization/embed-sample-for-your-organization-003.png)

3. Selecteer de toepassing die de **ApplicationSecret** moet gebruiken.

    ![Een app kiezen](media/embed-sample-for-your-organization/embed-sample-for-your-organization-006.png)

4. Selecteer **Instellingen**.

    ![Instellingen selecteren](media/embed-sample-for-your-organization/embed-sample-for-your-organization-038.png)

5. Selecteer **Sleutels**.

    ![Sleutels selecteren](media/embed-sample-for-your-organization/embed-sample-for-your-organization-039.png)

6. Voer in het vak **Beschrijving** een naam in en selecteer een duur. Selecteer vervolgens **Opslaan** om de **Waarde** voor uw toepassing op te halen. Wanneer u het deelvenster **Sleutels** sluit nadat u de sleutelwaarde hebt opgeslagen, wordt het waardeveld alleen nog als verborgen weergegeven. Op dat punt kunt u de sleutelwaarde niet meer ophalen. Als u de sleutelwaarde kwijtraakt, kunt u een nieuwe maken in Azure Portal.

    ![Sleutelwaarde](media/embed-sample-for-your-organization/embed-sample-for-your-organization-031.png)

### <a name="workspace-id"></a>Werkruimte-id

Vul bij **workspaceId** de app-werkruimte (groep)-GUID van Power BI in. U kunt deze informatie verkrijgen via de URL wanneer u bent aangemeld bij de Power BI-service, of via PowerShell.

URL <br>

![workspaceId](media/embed-sample-for-your-organization/embed-sample-for-your-organization-040.png)

PowerShell <br>

```powershell
Get-PowerBIworkspace -name "User Owns Embed Test"
```

   ![workspaceId van powershell](media/embed-sample-for-your-organization/embed-sample-for-your-organization-040-ps.png)

### <a name="report-id"></a>Rapport-id

Vul bij **reportId** informatie over de rapport-GUID uit Power BI in. U kunt deze informatie verkrijgen via de URL wanneer u bent aangemeld bij de Power BI-service, of via PowerShell.

URL <br>

![reportId](media/embed-sample-for-your-organization/embed-sample-for-your-organization-041.png)

PowerShell <br>

```powershell
Get-PowerBIworkspace -name "User Owns Embed Test" | Get-PowerBIReport
```

![reportId van powershell](media/embed-sample-for-your-organization/embed-sample-for-your-organization-041-ps.png)

### <a name="aadauthorityurl"></a>AADAuthorityUrl

Vul bij de **AADAuthorityUrl**-informatie de URL in waarmee u inhoud in de tenant van uw organisatie kunt insluiten of waarmee u inhoud kunt insluiten als gastgebruiker.

Voor het insluiten van inhoud met de tenant van uw organisatie, gebruikt u de URL - *https://login.microsoftonline.com/common/oauth2/authorize*.

Voor het insluiten van inhoud met een gast, gebruikt u de URL (*https://login.microsoftonline.com/report-owner-tenant-id*), waar u *report-owner-tenant-id* vervangt door de tenant-id van de rapporteigenaar.

### <a name="run-the-application"></a>De toepassing uitvoeren

1. Selecteer **Uitvoeren** in **Visual Studio**.

    ![De toepassing uitvoeren](media/embed-sample-for-your-organization/embed-sample-for-your-organization-033.png)

2. Selecteer vervolgens **Rapport insluiten**. Selecteer de optie die overeenkomt met het item dat u wilt testen (rapporten, dasboards of tegels).

    ![Inhoud selecteren](media/embed-sample-for-your-organization/embed-sample-for-your-organization-034.png)

3. U kunt het rapport nu weergeven in de voorbeeldtoepassing.

    ![Het rapport in de toepassing weergeven](media/embed-sample-for-your-organization/embed-sample-for-your-organization-035.png)

## <a name="embed-your-content-within-your-application"></a>Uw inhoud in uw toepassing insluiten

Hoewel de stappen voor het insluiten van uw inhoud kunnen worden uitgevoerd met de [Power BI REST-API's](https://docs.microsoft.com/rest/api/power-bi/), worden de voorbeeldcodes die worden beschreven in dit artikel gemaakt met de .NET SDK.

Als u een rapport in een web-app wilt integreren, gebruikt u de Power BI REST-API of de Power BI C#-SDK. U kunt ook een Azure Active Directory-verificatietoegangstoken gebruiken om een rapport op te halen. Vervolgens kunt u het rapport laden met hetzelfde toegangstoken. De Power BI Rest-API biedt programmatische toegang tot specifieke Power BI-resources. Zie [Power BI REST-API's](https://docs.microsoft.com/rest/api/power-bi/) en de [Power BI JavaScript-API](https://github.com/Microsoft/PowerBI-JavaScript) voor meer informatie.

### <a name="get-an-access-token-from-azure-ad"></a>Een toegangstoken ophalen uit Azure AD

In uw toepassing moet u een toegangstoken van Azure AD ophalen voordat u de Power BI REST API kunt aanroepen. Zie [Gebruikers verifiëren en een Azure AD-toegangstoken verkrijgen voor uw Power BI-app](get-azuread-access-token.md) voor meer informatie.

### <a name="get-a-report"></a>Een rapport ophalen

Als u een Power BI-rapport wilt ophalen, gebruikt u de bewerking [Rapporten ophalen](https://docs.microsoft.com/rest/api/power-bi/reports/getreports). Hiermee haalt u een lijst met Power BI-rapporten op. Vanuit de lijst met rapporten kunt u een rapport-id ophalen.

### <a name="get-reports-by-using-an-access-token"></a>Rapporten ophalen met behulp van een toegangstoken

Met de bewerking [Rapporten ophalen](https://docs.microsoft.com/rest/api/power-bi/reports/getreports) wordt een lijst met rapporten geretourneerd. U kunt een enkel rapport ophalen vanuit de lijst met rapporten.

Als u de REST-API-aanroep uitvoert, moet u de header *Autorisatie* met de indeling *Bearer {toegangstoken}* toevoegen.

#### <a name="get-reports-with-the-rest-api"></a>Rapporten ophalen met de REST-API

In het volgende codevoorbeeld ziet u hoe u rapporten ophaalt met de REST-API:

> [!Note]
> Een voorbeeld van het ophalen van een inhoudsitem dat u wilt insluiten, is beschikbaar in het bestand Default.aspx.cs in de [voorbeeldtoepassing](https://github.com/Microsoft/PowerBI-Developer-Samples). Voorbeelden zijn rapporten, dashboards of tegels.

```csharp
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

#### <a name="get-reports-by-using-the-net-sdk"></a>Rapporten ophalen met de .NET SDK

U kunt de .NET-SDK gebruiken voor het ophalen van een lijst met rapporten. Zo hoeft u de REST-API niet rechtstreeks aan te roepen. In het volgende codevoorbeeld ziet u hoe u rapporten vermeldt:

```csharp
using Microsoft.IdentityModel.Clients.ActiveDirectory;
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;

var tokenCredentials = new TokenCredentials(<ACCESS TOKEN>, "Bearer");

// Create a Power BI Client object. It is used to call Power BI APIs.
using (var client = new PowerBIClient(new Uri(ApiUrl), tokenCredentials))
{
    // Get the first report all reports in that workspace
    ODataResponseListReport reports = client.Reports.GetReports();

    Report report = reports.Value.FirstOrDefault();

    var embedUrl = report.EmbedUrl;
}
```

### <a name="load-a-report-by-using-javascript"></a>Een rapport laden met JavaScript

U kunt JavaScript gebruiken om een rapport te laden in een div-element op uw webpagina. Het volgende codevoorbeeld toont u hoe u een rapport uit een bepaalde werkruimte ophaalt:

> [!NOTE]  
> Een voorbeeld van het laden van een inhoudsitem dat u wilt insluiten is beschikbaar in het bestand **standaard.aspx** in de [voorbeeldtoepassing](https://github.com/Microsoft/PowerBI-Developer-Samples).

```javascript
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

#### <a name="sitemaster"></a>Site.master

```javascript
window.onload = function () {
    // client side click to embed a selected report.
    var el = document.getElementById("bEmbedReportAction");
    if (el.addEventListener) {
        el.addEventListener("click", updateEmbedReport, false);
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
    }
  );
}
```

## <a name="using-a-power-bi-premium-dedicated-capacity"></a>Een toegewezen capaciteit voor Power BI Premium gebruiken

Nu u uw toepassing hebt ontwikkeld, is het tijd om toegewezen capaciteit toe te voegen aan uw app-werkruimte.

### <a name="create-a-dedicated-capacity"></a>Een toegewezen capaciteit maken

Als u een toegewezen capaciteit maakt, profiteert u van een toegewezen resource voor de inhoud in uw app-werkruimte. U kunt een toegewezen capaciteit maken met [Power BI Premium](../service-premium.md).

In de volgende tabel ziet u de Power BI Premium-SKU's die beschikbaar zijn in [Microsoft Office 365](../service-admin-premium-purchase.md):

| Capaciteitsknooppunt | Totaal aantal vCores<br/>(back-end + front-end) | Back-end vCores | Front-end vCores | Limieten voor DirectQuery/liveverbindingen |
| --- | --- | --- | --- | --- | --- |
| EM1 |1 vCore |0,5 vCore, 10 GB RAM |0,5 vCore |3,75 per seconde |
| EM2 |2 vCores |1 vCore, 10 GB RAM |1 vCores |7,5 per seconde |
| EM3 |4 vCores |2 vCores, 10 GB RAM |2 vCores |15 per seconde |
| P1 |8 vCores |4 vCores, 25 GB RAM |4 vCores |30 per seconde |
| P2 |16 vCores |8 vCores, 50 GB RAM |8 vCores |60 per seconde |
| P3 |32 vCores |16 vCores, 100 GB RAM |16 vCores |120 per seconde |
| P4 |64 vCores |32 vCores, 200 GB RAM |32 vCores |240 per seconde |
| P5 |128 vCores |64 vCores, 400 GB RAM |64 vCores |480 per seconde |

> [!NOTE]
> - Wanneer u probeert in te voegen met Microsoft Office-apps, kunt u EM-SKU's gebruiken om met een gratis Power BI-licentie toegang te krijgen tot inhoud. U kunt echter geen toegang krijgen tot inhoud met een gratis Power BI-licentie wanneer u Powerbi.com of Power BI voor mobiel gebruikt.
> - Wanneer u probeert in te voegen in Microsoft Office-apps via Powerbi.com of Power BI voor mobiel, kunt u met een gratis Power BI-licentie toegang krijgen tot inhoud.

### <a name="assign-an-app-workspace-to-a-dedicated-capacity"></a>Een app-werkruimte toewijzen aan een toegewezen capaciteit

Nadat u toegewezen capaciteit hebt gemaakt, kunt u uw app-werkruimte toewijzen aan die toegewezen capaciteit. Ga hiervoor als volgt te werk:

1. Vouw binnen Power BI-service werkruimten uit en selecteer het beletselteken voor de werkruimte die u gebruikt voor het insluiten van uw inhoud. Selecteer vervolgens **Werkruimten bewerken**.

    ![Een werkruimte bewerken](media/embed-sample-for-your-organization/embed-sample-for-your-organization-036.png)

2. Vouw **Geavanceerd** uit en schakel **Toegewezen capaciteit** in. Selecteer de toegewezen capaciteit die u hebt gemaakt. Selecteer vervolgens **Opslaan**.

    ![Een toegewezen capaciteit toewijzen](media/embed-sample-for-your-organization/embed-sample-for-your-organization-024.png)

3. Nadat u **Opslaan** hebt geselecteerd, ziet u een ruit naast de naam van de app-werkruimte.

    ![App-werkruimte gekoppeld aan een capaciteit](media/embed-sample-for-your-organization/embed-sample-for-your-organization-037.png)

## <a name="admin-settings"></a>Beheerdersinstellingen

Globale beheerders of Power BI-servicebeheerders kunnen de mogelijkheid om REST-API's te gebruiken in- of uitschakelen voor een tenant. Power BI-beheerders kunnen deze instelling inschakelen voor de hele organisatie of voor afzonderlijke beveiligingsgroepen. Standaard is deze instelling ingeschakeld voor de hele organisatie. U kunt deze wijzigingen doorvoeren in de [Power BI-beheerportal](../service-admin-portal.md).

## <a name="next-steps"></a>Volgende stappen

In deze zelfstudie hebt u geleerd hoe u Power BI-inhoud insluit in een toepassing met uw Power BI-account voor uw organisatie. U kunt nu proberen Power BI-inhoud in een toepassing in te sluiten met behulp van apps. U kunt ook Power BI-inhoud insluiten voor uw klanten:

> [!div class="nextstepaction"]
> [Insluiten vanuit apps](embed-from-apps.md)

> [!div class="nextstepaction"]
>[Insluiten voor uw klanten](embed-sample-for-customers.md)

Als u meer vragen hebt, kunt u deze stellen [in de Power BI-community](http://community.powerbi.com/).
