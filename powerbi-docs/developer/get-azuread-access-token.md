---
title: Gebruikers verifiëren en een Azure AD-toegangstoken ophalen voor uw toepassing
description: Informatie over het registreren van een toepassing in Azure Active Directory voor gebruik met ingesloten Power BI-inhoud.
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-developer
ms.topic: conceptual
ms.date: 08/11/2017
ms.author: maghan
ms.openlocfilehash: 51ad188479c11f5a0d16768eee8c533bdc71c59c
ms.sourcegitcommit: fecea174721d0eb4e1927c1116d2604a822e4090
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/31/2018
ms.locfileid: "39359927"
---
# <a name="authenticate-users-and-get-an-azure-ad-access-token-for-your-power-bi-app"></a>Gebruikers verifiëren en een Azure AD-toegangstoken ophalen voor uw Power BI-app
Lees hoe u gebruikers kunt verifiëren in uw Power BI-toepassing en een toegangstoken kunt ophalen voor gebruik met de REST API.

Voordat u de Power BI REST API kunt aanroepen, moet u een **verificatietoegangstoken** (toegangstoken) ophalen voor Azure Active Directory (Azure AD). Een **toegangstoken** wordt gebruikt om uw app toegang tot **Power BI**-dashboards, -tegels en rapporten toe te staan. Zie voor meer informatie over het **toegangstoken** van Azure Active Directory de [toewijzingsstroom voor Azure AD-autorisatiecodes](https://msdn.microsoft.com/library/azure/dn645542.aspx).

Afhankelijk van hoe u inhoud insluit, wordt het toegangstoken op een andere manier opgehaald. In dit artikel komen twee verschillende benaderingen aan bod.

## <a name="access-token-for-power-bi-users-user-owns-data"></a>Toegangstoken voor Power BI-gebruikers (gebruikers is eigenaar van gegevens)
Dit voorbeeld is bestemd voor gevallen waarin uw gebruikers zich handmatig bij Azure AD aanmelden met hun organisatieaanmeldingsgegevens. Dit wordt gebruikt wanneer inhoud wordt ingesloten voor Power BI-gebruikers die inhoud openen waartoe zij toegang hebben in de Power BI-service.

### <a name="get-an-authorization-code-from-azure-ad"></a>Een autorisatiecode ophalen van Azure AD
De eerste stap voor het ophalen van een **toegangstoken** bestaat uit het ophalen van een autorisatiecode van **Azure AD**. Hiervoor maakt u een querytekenreeks met de volgende eigenschappen en stuurt u deze terug naar **Azure AD**.

**Querytekenreeks met autorisatiecode**

```
var @params = new NameValueCollection
{
    //Azure AD will return an authorization code. 
    //See the Redirect class to see how "code" is used to AcquireTokenByAuthorizationCode
    {"response_type", "code"},

    //Client ID is used by the application to identify themselves to the users that they are requesting permissions from. 
    //You get the client id when you register your Azure app.
    {"client_id", Properties.Settings.Default.ClientID},

    //Resource uri to the Power BI resource to be authorized
    // https://analysis.windows.net/powerbi/api
    {"resource", Properties.Settings.Default.PowerBiAPI},

    //After user authenticates, Azure AD will redirect back to the web app
    {"redirect_uri", "http://localhost:13526/Redirect"}
};
```

Nadat u de querytekenreeks hebt gemaakt, stuurt u deze naar **Azure AD** om een **autorisatiecode** te verkrijgen.  Hieronder staat een volledige C#-methode voor het maken van een querytekenreeks met een **autorisatiecode** en het sturen hiervan naar **Azure AD**. Nadat u een autorisatiecode hebt verkregen, krijgt u een **toegangstoken** met behulp van de **autorisatiecode**.

Binnen redirect.aspx.cs wordt vervolgens [AuthenticationContext.AcquireTokenByAuthorizationCode](https://msdn.microsoft.com/library/azure/dn479531.aspx) aangeroepen om het token te genereren.

**Autorisatiecode verkrijgen**

```
protected void signInButton_Click(object sender, EventArgs e)
{
    //Create a query string
    //Create a sign-in NameValueCollection for query string
    var @params = new NameValueCollection
    {
        //Azure AD will return an authorization code. 
        //See the Redirect class to see how "code" is used to AcquireTokenByAuthorizationCode
        {"response_type", "code"},

        //Client ID is used by the application to identify themselves to the users that they are requesting permissions from. 
        //You get the client id when you register your Azure app.
        {"client_id", Properties.Settings.Default.ClientID},

        //Resource uri to the Power BI resource to be authorized
        // https://analysis.windows.net/powerbi/api
        {"resource", Properties.Settings.Default.PowerBiAPI},

        //After user authenticates, Azure AD will redirect back to the web app
        {"redirect_uri", "http://localhost:13526/Redirect"}
    };

    //Create sign-in query string
    var queryString = HttpUtility.ParseQueryString(string.Empty);
    queryString.Add(@params);

    //Redirect authority
    //Authority Uri is an Azure resource that takes a client id to get an Access token
    // AADAuthorityUri = https://login.windows.net/common/oauth2/authorize/
    string authorityUri = Properties.Settings.Default.AADAuthorityUri;
    var authUri = String.Format("{0}?{1}", authorityUri, queryString);
    Response.Redirect(authUri);
}
```

### <a name="get-an-access-token-from-authorization-code"></a>Een toegangstoken verkrijgen op basis van een autorisatiecode
U moet nu een autorisatiecode hebben van Azure AD. Zodra **Azure AD** een **autorisatiecode** terugstuurt naar uw webapp, kunt u de **autorisatiecode** gebruiken om een toegangstoken te verkrijgen. Hieronder staan een C#-voorbeeld dat u kunt gebruiken op uw omleidingspagina en de Page_Load-gebeurtenis voor uw default.aspx-pagina.

De naamruimte **Microsoft.IdentityModel.Clients.ActiveDirectory** kan worden opgehaald uit het [Active Directory-verificatiebibiliotheek](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/) NuGet-pakket.

```
Install-Package Microsoft.IdentityModel.Clients.ActiveDirectory
```

**Redirect.aspx.cs**

```
using Microsoft.IdentityModel.Clients.ActiveDirectory;

protected void Page_Load(object sender, EventArgs e)
{
    //Redirect uri must match the redirect_uri used when requesting Authorization code.
    string redirectUri = String.Format("{0}Redirect", Properties.Settings.Default.RedirectUrl);
    string authorityUri = Properties.Settings.Default.AADAuthorityUri;

    // Get the auth code
    string code = Request.Params.GetValues(0)[0];

    // Get auth token from auth code
    TokenCache TC = new TokenCache();

    AuthenticationContext AC = new AuthenticationContext(authorityUri, TC);
    ClientCredential cc = new ClientCredential
        (Properties.Settings.Default.ClientID,
        Properties.Settings.Default.ClientSecret);

    AuthenticationResult AR = AC.AcquireTokenByAuthorizationCode(code, new Uri(redirectUri), cc);

    //Set Session "authResult" index string to the AuthenticationResult
    Session[_Default.authResultString] = AR;

    //Redirect back to Default.aspx
    Response.Redirect("/Default.aspx");
}
```

**Default.aspx**

```
using Microsoft.IdentityModel.Clients.ActiveDirectory;

protected void Page_Load(object sender, EventArgs e)
{

    //Test for AuthenticationResult
    if (Session[authResultString] != null)
    {
        //Get the authentication result from the session
        authResult = (AuthenticationResult)Session[authResultString];

        //Show Power BI Panel
        signInStatus.Visible = true;
        signInButton.Visible = false;

        //Set user and token from authentication result
        userLabel.Text = authResult.UserInfo.DisplayableId;
        accessTokenTextbox.Text = authResult.AccessToken;
    }
}
```

## <a name="access-token-for-non-power-bi-users-app-owns-data"></a>Toegangstoken voor niet-Power BI-gebruikers (app is eigenaar van gegevens)
Deze benadering wordt meestal gebruikt voor ISV-toepassingen waarbij de app eigenaar is van toegang tot de gegevens. Gebruikers zijn niet noodzakelijkerwijs Power BI-gebruikers en de toepassing bepaalt de verificatie en toegang voor de eindgebruikers.

Voor deze benadering gebruikt u een enkele *hoofd*account die een Power BI Pro-gebruiker is. De referenties voor deze account worden in de toepassing opgeslagen. Deze opgeslagen referenties worden door de toepassing gebruikt om te verifiëren bij Azure AD. De onderstaande voorbeeldcode is afkomstig uit het [voorbeeld waarbij de app eigenaar is van de gegevens](https://github.com/guyinacube/PowerBI-Developer-Samples/tree/master/App%20Owns%20Data)

**HomeController.cs**

```
using Microsoft.IdentityModel.Clients.ActiveDirectory;

// Create a user password cradentials.
var credential = new UserPasswordCredential(Username, Password);

// Authenticate using created credentials
var authenticationContext = new AuthenticationContext(AuthorityUrl);
var authenticationResult = await authenticationContext.AcquireTokenAsync(ResourceUrl, ClientId, credential);

if (authenticationResult == null)
{
    return View(new EmbedConfig()
    {
        ErrorMessage = "Authentication Failed."
    });
}

var tokenCredentials = new TokenCredentials(authenticationResult.AccessToken, "Bearer");
```

Zie voor meer informatie over het gebruik van **await** het onderwerp [await (C#-referentie)](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/await)

## <a name="next-steps"></a>Volgende stappen
Nu u het toegangstoken hebt, kunt u de Power BI REST API aanroepen om inhoud in te sluiten. Zie [Power BI-dashboards, -rapporten en -tegels insluiten](embed-sample-for-customers.md#embed-your-content-within-your-application) voor informatie over het insluiten van uw inhoud.

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)