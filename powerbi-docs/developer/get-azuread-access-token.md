---
title: Gebruikers verifiëren en een Azure AD-toegangstoken ophalen voor uw toepassing
description: Informatie over het registreren van een toepassing in Azure Active Directory voor gebruik met ingesloten Power BI-inhoud.
author: markingmyname
ms.author: maghan
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 02/05/2019
ms.openlocfilehash: 7b2249964f2fff26bc68fea19fd0010d8990110b
ms.sourcegitcommit: 0abcbc7898463adfa6e50b348747256c4b94e360
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2019
ms.locfileid: "55762531"
---
# <a name="get-an-azure-ad-access-token-for-your-power-bi-application"></a>Een Azure AD toegangstoken voor uw Power BI-toepassing verkrijgen

Lees hoe u gebruikers kunt verifiëren in uw Power BI-toepassing en een toegangstoken kunt ophalen voor gebruik met de REST API.

Voordat u de Power BI REST API kunt aanroepen, moet u een **verificatietoegangstoken** (toegangstoken) ophalen voor Azure Active Directory (Azure AD). Een **toegangstoken** wordt gebruikt om uw app toegang tot **Power BI**-dashboards, -tegels en -rapporten toe te staan. Zie voor meer informatie over het **toegangstoken** van Azure Active Directory de [toewijzingsstroom voor Azure AD-autorisatiecodes](https://msdn.microsoft.com/library/azure/dn645542.aspx).

Afhankelijk van hoe u inhoud insluit, wordt het toegangstoken op een andere manier opgehaald. In dit artikel komen twee verschillende benaderingen aan bod.

## <a name="access-token-for-power-bi-users-user-owns-data"></a>Toegangstoken voor Power BI-gebruikers (gebruikers is eigenaar van gegevens)

Dit voorbeeld is bestemd voor gevallen waarin uw gebruikers zich handmatig bij Azure AD aanmelden met hun organisatieaanmeldingsgegevens. Deze taak wordt gebruikt wanneer inhoud wordt ingesloten voor Power BI-gebruikers die inhoud openen waartoe zij toegang hebben in de Power BI-service.

### <a name="get-an-authorization-code-from-azure-ad"></a>Een autorisatiecode ophalen van Azure AD

De eerste stap voor het ophalen van een **toegangstoken** bestaat uit het ophalen van een autorisatiecode van **Azure AD**. Maak een querytekenreeks met de volgende eigenschappen en stuur deze terug naar **Azure AD**.

#### <a name="authorization-code-query-string"></a>Querytekenreeks met autorisatiecode

```csharp
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

#### <a name="get-authorization-code"></a>Autorisatiecode verkrijgen

```csharp
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
    // AADAuthorityUri = https://login.microsoftonline.net/common/
    string authorityUri = Properties.Settings.Default.AADAuthorityUri;
    var authUri = String.Format("{0}?{1}", authorityUri, queryString);
    Response.Redirect(authUri);
}
```

### <a name="get-an-access-token-from-authorization-code"></a>Een toegangstoken verkrijgen op basis van een autorisatiecode

U moet nu een autorisatiecode hebben van Azure AD. Zodra **Azure AD** een **autorisatiecode** terugstuurt naar uw webapp, kunt u de **autorisatiecode** gebruiken om een toegangstoken te verkrijgen. Hieronder staan een C#-voorbeeld dat u kunt gebruiken op uw omleidingspagina en de Page_Load-gebeurtenis voor uw default.aspx-pagina.

De naamruimte **Microsoft.IdentityModel.Clients.ActiveDirectory** kan worden opgehaald uit het [Active Directory-verificatiebibiliotheek](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/) NuGet-pakket.

```powershell
Install-Package Microsoft.IdentityModel.Clients.ActiveDirectory
```

#### <a name="redirectaspxcs"></a>Redirect.aspx.cs

```csharp
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

#### <a name="defaultaspx"></a>Default.aspx

```csharp
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

### <a name="access-token-with-a-master-account"></a>Toegangstoken met een hoofdaccount

Voor deze benadering gebruikt u een enkel *hoofd*account dat een Power BI Pro-gebruiker is. De referenties voor deze account worden in de toepassing opgeslagen. Deze opgeslagen referenties worden door de toepassing gebruikt om te verifiëren bij Azure AD. De onderstaande voorbeeldcode is afkomstig uit het [voorbeeld waarbij de app eigenaar is van de gegevens](https://github.com/guyinacube/PowerBI-Developer-Samples)

### <a name="access-token-with-service-principal"></a>Toegangstoken met service-principal

Voor deze benadering gebruikt u een [service-principal](embed-service-principal.md). Dit is een token **alleen voor apps**. Deze service-principal wordt door de toepassing gebruikt om te verifiëren bij Azure AD. De onderstaande voorbeeldcode is afkomstig uit het [voorbeeld waarbij de app eigenaar is van de gegevens](https://github.com/guyinacube/PowerBI-Developer-Samples)

#### <a name="embedservicecs"></a>EmbedService.cs

```csharp
var authenticationContext = new AuthenticationContext(AuthorityUrl);
       AuthenticationResult authenticationResult = null;
       if (AuthenticationType.Equals("MasterUser"))
       {
              // Authentication using master user credentials
              var credential = new UserPasswordCredential(Username, Password);
              authenticationResult = authenticationContext.AcquireTokenAsync(ResourceUrl, ApplicationId, credential).Result;
       }
       else
       {
             // Authentication using app credentials
             var credential = new ClientCredential(ApplicationId, ApplicationSecret);
             authenticationResult = await authenticationContext.AcquireTokenAsync(ResourceUrl, credential);
       }


m_tokenCredentials = new TokenCredentials(authenticationResult.AccessToken, "Bearer");
```

## <a name="next-steps"></a>Volgende stappen

Nu u het toegangstoken hebt, kunt u de Power BI REST API aanroepen om inhoud in te sluiten. Zie [Power BI-dashboards, -rapporten en -tegels insluiten](embed-sample-for-customers.md#embed-content-within-your-application) voor informatie over het insluiten van uw inhoud.

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)