---
title: Een verificatietoegangstoken ophalen
description: Stapsgewijze uitleg van het pushen van gegevens - Een verificatietoegangstoken ophalen
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-developer
ms.topic: conceptual
ms.date: 08/10/2017
ms.author: maghan
ms.openlocfilehash: 640c6dac9a896cff55bddad46ceef8bce7ccae14
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2018
ms.locfileid: "34289367"
---
# <a name="step-2-get-an-authentication-access-token"></a>Stap 2: Een toegangstoken voor verificatie ophalen
Dit artikel maakt deel uit van een stapsgewijze uitleg van hoe u [gegevens naar een gegevensset pusht](walkthrough-push-data.md).

Bij **stap 1** voor het pushen van gegevens naar een gegevensset, [De app registreren bij Azure AD](walkthrough-push-data-register-app-with-azure-ad.md), hebt u een client-app geregistreerd in Azure AD. In deze stap krijgt u een verificatietoegangstoken. Power BI-apps worden geïntegreerd met **Azure AD** om beveiligde aanmelding en autorisatie voor uw app te verzorgen. U gebruikt een token om u te verifiëren bij **Azure AD** en toegang te krijgen tot Power BI-resources.

Hieronder ziet u hoe u een verificatietoegangstoken kunt ophalen.

## <a name="get-an-authentication-access-token"></a>Een verificatietoegangstoken ophalen
> **OPMERKING**: Voordat u begint, zorgt u dat u de vorige stappen in [Gegevens naar een gegevensset pushen](walkthrough-push-data.md) hebt gevolgd.
> 
> 

1. Maak in Visual Studio 2015 een **consoletoepassing**project.
2. Installeer het [Azure AD Authentication Library-pakket voor .NET-NuGet](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/). Gebruik dit pakket om een verificatietoegangstoken op te halen in een .NET-pakket. U installeert het pakket als volgt:
   
     a. Kies in Visual Studio 2015 **Extra** > **NuGet Package Manager** > **Package Manager Console**.
   
     b. Voer in **Package Manager Console** het volgende in: Install-Package Microsoft.IdentityModel.Clients.ActiveDirectory-versie 2.21.301221612.
3. Voeg onderstaande code toe aan de klasse Program {...}.
4. Vervang "{ClientID}" door de **Client-id** die u hebt gekregen bij het registreren van de app. Zie [De app bij Azure AD registreren](walkthrough-push-data-register-app-with-azure-ad.md).
5. Voeg na installatie van het pakket Microsoft.IdentityModel.Clients.ActiveDirectory **using Microsoft.IdentityModel.Clients.ActiveDirectory;** toe aan Program.cs.
6. Voer de console-app uit en meld u aan bij uw Power BI-account. U zou nu een tokentekenreeks moeten zien in het consolevenster.

**Voorbeeldcode voor het ophalen van een verificatietoegangstoken**

Voeg deze code toe aan Program {...}.

* Een tokenvariabele voor het aanroepen van bewerkingen:
  
  ```
  private static string token = string.Empty;
  
  static void Main(string[] args)
  {
  }
  ```
* In static void Main(string[] args):
  
  ```
  static void Main(string[] args)
  {
    //Get an authentication access token
    token = GetToken();
  }
  ```
* Een methode GetToken() toevoegen:

```
       #region Get an authentication access token
       private static string GetToken()
       {
           // TODO: Install-Package Microsoft.IdentityModel.Clients.ActiveDirectory -Version 2.21.301221612
           // and add using Microsoft.IdentityModel.Clients.ActiveDirectory

           //The client id that Azure AD created when you registered your client app.
           string clientID = "{Client_ID}";

           //RedirectUri you used when you register your app.
           //For a client app, a redirect uri gives Azure AD more details on the application that it will authenticate.
           // You can use this redirect uri for your client app
           string redirectUri = "https://login.live.com/oauth20_desktop.srf";

           //Resource Uri for Power BI API
           string resourceUri = "https://analysis.windows.net/powerbi/api";

           //OAuth2 authority Uri
           string authorityUri = "https://login.windows.net/common/oauth2/authorize";

           //Get access token:
           // To call a Power BI REST operation, create an instance of AuthenticationContext and call AcquireToken
           // AuthenticationContext is part of the Active Directory Authentication Library NuGet package
           // To install the Active Directory Authentication Library NuGet package in Visual Studio,
           //  run "Install-Package Microsoft.IdentityModel.Clients.ActiveDirectory" from the nuget Package Manager Console.

           // AcquireToken will acquire an Azure access token
           // Call AcquireToken to get an Azure token from Azure Active Directory token issuance endpoint
           AuthenticationContext authContext = new AuthenticationContext(authorityUri);
           string token = authContext.AcquireToken(resourceUri, clientID, new Uri(redirectUri)).AccessToken;

           Console.WriteLine(token);
           Console.ReadLine();

           return token;
       }

       #endregion
```

Nadat u een verificatietoken hebt opgehaald, kunt u elke Power BI-bewerking aanroepen. In de volgende stap ziet u hoe u de bewerking [Gegevensset maken](https://msdn.microsoft.com/library/mt203562.aspx) kunt aanroepen voor het maken van een gegevensset om gegevens naar een dashboard te pushen.

In de volgende stap ziet u hoe u [een gegevensset maakt in Power BI](walkthrough-push-data-create-dataset.md).

Hieronder ziet u de [volledige code](#code).

<a name="code"/>

## <a name="complete-code-listing"></a>Volledige code
    using System;
    using Microsoft.IdentityModel.Clients.ActiveDirectory;

    namespace walkthrough_push_data
    {
        class Program
        {
            private static string token = string.Empty;

            static void Main(string[] args)
            {

                //Get an authentication access token
                token = GetToken();

            }

            #region Get an authentication access token
            private static string GetToken()
            {
                // TODO: Install-Package Microsoft.IdentityModel.Clients.ActiveDirectory -Version 2.21.301221612
                // and add using Microsoft.IdentityModel.Clients.ActiveDirectory

                //The client id that Azure AD created when you registered your client app.
                string clientID = "{Client_ID}";

                //RedirectUri you used when you register your app.
                //For a client app, a redirect uri gives Azure AD more details on the application that it will authenticate.
                // You can use this redirect uri for your client app
                string redirectUri = "https://login.live.com/oauth20_desktop.srf";

                //Resource Uri for Power BI API
                string resourceUri = "https://analysis.windows.net/powerbi/api";

                //OAuth2 authority Uri
                string authorityUri = "https://login.windows.net/common/oauth2/authorize";

                //Get access token:
                // To call a Power BI REST operation, create an instance of AuthenticationContext and call AcquireToken
                // AuthenticationContext is part of the Active Directory Authentication Library NuGet package
                // To install the Active Directory Authentication Library NuGet package in Visual Studio,
                //  run "Install-Package Microsoft.IdentityModel.Clients.ActiveDirectory" from the nuget Package Manager Console.

                // AcquireToken will acquire an Azure access token
                // Call AcquireToken to get an Azure token from Azure Active Directory token issuance endpoint
                AuthenticationContext authContext = new AuthenticationContext(authorityUri);
                string token = authContext.AcquireToken(resourceUri, clientID, new Uri(redirectUri)).AccessToken;

                Console.WriteLine(token);
                Console.ReadLine();

                return token;
            }

            #endregion

        }
    }


[Volgende stap >](walkthrough-push-data-create-dataset.md)

## <a name="next-steps"></a>Volgende stappen
[Een gegevensset maken in Power BI](walkthrough-push-data-create-dataset.md)  
[Een app bij Azure AD registreren](walkthrough-push-data-register-app-with-azure-ad.md)  
[Azure AD Authentication Library-pakket voor .NET-NuGet](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/)  
[Gegevens naar een Power BI-gegevensset pushen](walkthrough-push-data.md)  
[Overzicht van de REST-API voor Power BI](overview-of-power-bi-rest-api.md)  
[Naslag voor REST-API voor Power BI](https://msdn.microsoft.com/library/mt147898.aspx)  
Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

