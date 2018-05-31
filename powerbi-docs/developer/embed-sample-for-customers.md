---
title: Power BI-inhoud insluiten in een toepassing voor uw klanten
description: Informatie over het integreren of insluiten van een rapport, dashboard of tegel in een web-app met behulp van de Power BI-API's voor uw klanten.
services: powerbi
author: markingmyname
ms.author: maghan
ms.date: 05/07/2018
ms.topic: tutorial
ms.service: powerbi
ms.custom: mvc
manager: kfile
ms.openlocfilehash: 2d4fdee8d3e4cca60294acd0a9167da1f048afa5
ms.sourcegitcommit: 9fa954608e78dcdb8d8a503c3c9b01c43ca728ab
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2018
ms.locfileid: "34051928"
---
# <a name="tutorial-embed-a-power-bi-report-dashboard-or-tile-into-an-application-for-your-customers"></a>Zelfstudie: een Power BI-rapport, dashboard of tegel insluiten in een toepassing voor uw klanten
Met **Power BI Embedded in Azure** kunt u rapporten, dashboards en tegels in een toepassing insluiten, zodat uw klanten gegevens kunnen delen. Dit is doorgaans een scenario voor **ISV-ontwikkelaars** waarin de **app eigenaar is van de gegevens**. Wanneer de **app eigenaar is van de gegevens**, betekent dit dat u Power BI-inhoud insluit voor uw eigen klanten. De gebruiker van de Power BI-inhoud kan bijvoorbeeld rapporten, dashboards of tegels bekijken zonder dat deze zich hoeft aan te melden bij **Power BI**. Deze zelfstudie laat zien hoe u een rapport in een toepassing kunt integreren of insluiten met behulp van de .NET SDK voor **Power BI** en de JavaScript-API voor **Power BI** bij gebruik van **Power BI Embedded in Azure** voor uw klanten wanneer de **app eigenaar is van de gegevens**.

In deze zelfstudie leert u het volgende:
>[!div class="checklist"]
>* Een toepassing registreren in Azure.
>* Een rapport, dashboard of tegel insluiten in een toepassing met Power BI Embedded in Azure.

## <a name="prerequisites"></a>Vereisten
Als u wilt beginnen, hebt u een **Power BI Pro**-account en een **Microsoft Azure**-account nodig.

* Als u zich niet hebt geregistreerd voor **Power BI Pro**, [kunt u zich hier aanmelden voor een gratis proefversie](https://powerbi.microsoft.com/en-us/pricing/) voordat u begint.
* Als u nog geen abonnement op Azure hebt, maakt u een [gratis account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) voordat u begint.
* U moet beschikken over een eigen [Azure Active Directory-tenant ](create-an-azure-active-directory-tenant.md).
* [Visual Studio](https://www.visualstudio.com/) moet zijn geïnstalleerd (versie 2013 of hoger).

## <a name="setup-your-embedded-analytics-development-environment"></a>De ingesloten analytische ontwikkelomgeving instellen

Voordat u begint met het insluiten van dashboards, rapporten en tegels in uw toepassing, moet u ervoor zorgen dat uw omgeving is ingesteld voor het insluiten van inhoud. Als onderdeel van het instellingsproces moet u het volgende doen.

### <a name="register-an-application-in-azure-active-directory-azure-ad"></a>Een toepassing registreren in Azure Active Directory (Azure AD)

U kunt uw toepassing registreren bij Azure Active Directory AD zodat uw toepassing toegang heeft tot de Power BI REST-API's. Hiermee kunt u een identiteit instellen voor uw toepassing en machtigingen opgeven voor Power BI REST-resources.

1. Accepteer de [algemene voorwaarden van de Microsoft Power BI-API](https://powerbi.microsoft.com/api-terms).

2. Meld u aan bij [Azure Portal](https://portal.azure.com).
 
    ![Hoofdweergave van Azure Portal](media/embed-sample-for-customers/embed-sample-for-customers-002.png)

3. Kies in het navigatiedeelvenster links **Alle services**, selecteer **App-registraties** en selecteer **Registratie van nieuwe toepassing**.
   
    ![App-registratie zoeken](media/embed-sample-for-customers/embed-sample-for-customers-003.png)</br>
    ![Nieuwe app-registratie](media/embed-sample-for-customers/embed-sample-for-customers-004.png)

4. Volg de aanwijzingen en maak een nieuwe toepassing. Als de app eigenaar is van de gegevens, gebruikt **Systeemeigen** als het toepassingstype. Daarnaast moet u een **omleidings-URI** opgeven, die **Azure AD** gebruikt om tokenantwoorden te retourneren. Voer een specifieke waarde in voor uw toepassing (bijvoorbeeld http://localhost:13526/redirect).

    ![App maken](media/embed-sample-for-customers/embed-sample-for-customers-005.png)

### <a name="apply-permissions-to-your-application-within-azure-active-directory"></a>Machtigingen toepassen op uw toepassing in Azure Active Directory

U moet extra machtigingen inschakelen voor uw toepassing naast de informatie die u hebt opgegeven op de pagina voor de app-registratie. U moet zijn aangemeld met het *hoofd*account, dat wordt gebruikt voor insluiting, of een globaal beheerdersaccount.

### <a name="use-the-azure-active-directory-portal"></a>Azure Active Directory-portal gebruiken

1. Blader naar [App-registraties](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ApplicationsListBlade) in Azure Portal en selecteer de app die u gebruikt voor insluiting.
   
    ![App kiezen](media/embed-sample-for-customers/embed-sample-for-customers-006.png)

2. Selecteer **Instellingen** en selecteer **Vereiste machtigingen**, onder **API-toegang**.
   
    ![Vereiste machtigingen](media/embed-sample-for-customers/embed-sample-for-customers-008.png)

3. Selecteer **Windows Azure Active Directory** en controleer vervolgens of **De map openen als de aangemelde gebruiker** is geselecteerd. Selecteer **Opslaan**.
   
    ![Windows Azure AD-machtigingen](media/embed-sample-for-customers/embed-sample-for-customers-011.png)

4. Selecteer **Toevoegen**.

    ![Machtigingen toevoegen](media/embed-sample-for-customers/embed-sample-for-customers-012.png)

5. Selecteer **Een API selecteren**.

    ![API-toegang toevoegen](media/embed-sample-for-customers/embed-sample-for-customers-013.png)

6. Selecteer **Power BI-service** en selecteer vervolgens **Selecteren**.

    ![PBI-services selecteren](media/embed-sample-for-customers/embed-sample-for-customers-014.png)

7. Selecteer alle machtigingen onder **Gedelegeerde machtigingen**. U moet deze één voor één selecteren om ze te kunnen opslaan. Selecteer **Opslaan** wanneer u klaar bent.
   
    ![Gedelegeerde machtigingen selecteren](media/embed-sample-for-customers/embed-sample-for-customers-015.png)

8. Selecteer binnen **Vereiste machtigingen** de optie **Machtigingen verlenen**.
   
    De actie **Machtigingen verlenen** is vereist voor de *hoofdaccount* om te voorkomen dat om toestemming wordt gevraagd door Azure AD. Als de account die deze actie uitvoert een globale beheerder is, verleent u machtigingen voor alle gebruikers binnen uw organisatie voor deze toepassing. Als de account die deze actie uitvoert de *hoofdaccount* is en niet een globale beheerder, verleent u alleen machtigingen aan de *hoofdaccount* voor deze toepassing.
   
    ![Machtigingen verlenen binnen het dialoogvenster Vereiste machtigingen](media/embed-sample-for-customers/embed-sample-for-customers-016.png)

### <a name="create-your-power-bi-embedded-dedicated-capacity-in-azure"></a>Toegewezen capaciteit van Power BI Embedded maken in Azure

1. Meld u aan bij [Azure Portal](https://portal.azure.com).

    ![Hoofdweergave van Azure Portal](media/embed-sample-for-customers/embed-sample-for-customers-002.png)

2. Kies in het navigatiedeelvenster links **Alle services** en selecteer **Power BI Embedded**.

    ![PBIE zoeken](media/embed-sample-for-customers/embed-sample-for-customers-017.png)

3. Volg de aanwijzingen en vul de juiste informatie in die nodig is voor het maken van nieuwe toegewezen capaciteit van **Power BI Embedded**. Selecteer vervolgens **Maken**. Raadpleeg tijdens het kiezen van de **prijscategorie** de onderstaande tabel om te bepalen welke categorie het beste aansluit op uw behoeften. Selecteer vervolgens **Maken** en wacht totdat de resource is voltooid.

    ![PBIE instellen](media/embed-sample-for-customers/embed-sample-for-customers-018.png)

| Capaciteitsknooppunt | Totaal aantal cores<br/>*(back-end + front-end)* | Back-endcores | Front-endcores | Limieten voor DirectQuery/liveverbindingen | Maximum aantal pagina's (rendering) tijdens piekuren |
| --- | --- | --- | --- | --- | --- |
| A1 |1 v-core |0,5 core, 3 GB RAM |0,5 core | 5 per seconde |1-300 |
| A2 |2 v-cores |1 core, 5 GB RAM |1 core | 10 per seconde |301-600 |
| A3 |4 v-cores |2 cores, 10 GB RAM |2 cores | 15 per seconde |601-1200 |
| A4 |8 v-cores |4 cores, 25 GB RAM |4 cores |30 per seconde |1201-2400 |
| A5 |16 v-cores |8 cores, 50 GB RAM |8 cores |60 per seconde |2401-4800 |
| A6 |32 v-cores |16 cores, 100 GB RAM |16 cores |120 per seconde |4.801-9.600 |

Nu kunt u de nieuwe **toegewezen capaciteit van Power BI Embedded** bekijken.

   ![Toegewezen capaciteit van PBIE](media/embed-sample-for-customers/embed-sample-for-customers-019.png)

## <a name="setup-your-power-bi-environment"></a>Uw Power BI-omgeving instellen

### <a name="create-an-app-workspace"></a>Een app-werkruimte maken

Als u rapporten, dashboards of tegels voor uw klanten insluit, moet u uw inhoud binnen de werkruimte van een app plaatsen. Het *hoofd*account moet een beheerder van de app-werkruimte zijn.

1. Maak eerst de werkruimte. Selecteer **Werkruimten** > **App-werkruimte maken**. Hier wordt de inhoud geplaatst waartoe de toepassing toegang moet hebben.

    ![Werkruimte maken](media/embed-sample-for-customers/embed-sample-for-customers-020.png)

2. Geef een naam op voor de werkruimte. Als de corresponderende **werkruimte-id** niet beschikbaar is, kunt u deze bewerken tot een unieke aanduiding. Dit wordt ook de naam van de app.

    ![Werkruimte een naam geven](media/embed-sample-for-customers/embed-sample-for-customers-021.png)

3. U moet een aantal opties instellen. Als u **Openbaar** kiest, is de inhoud van de werkruimte zichtbaar voor iedereen in de organisatie. Als u **Privé** kiest, is de inhoud alleen zichtbaar voor leden van de werkruimte.

    ![Openbaar/privé](media/embed-sample-for-customers/embed-sample-for-customers-022.png)

    U kunt de instelling Openbaar/Privé niet meer wijzigen nadat u de groep hebt gemaakt.

4. U kunt ook kiezen of leden van de werkruimte rechten voor **bewerken** of **alleen-lezen** krijgen.

    ![Leden toevoegen](media/embed-sample-for-customers/embed-sample-for-customers-023.png)

5. Voeg de e-mailadressen toe van de personen die u toegang tot de werkruimte wilt geven, en selecteer **Toevoegen**. U kunt geen groepsaliassen toevoegen, alleen personen.

6. Bepaal per persoon of deze een lid of een beheerder is. Beheerders kunnen de werkruimte zelf bewerken, en bijvoorbeeld ook andere leden toevoegen. Leden kunnen de inhoud in de werkruimte bewerken, tenzij ze alleen leesrechten hebben. Zowel beheerders als leden kunnen de app publiceren.

7. Vouw **Geavanceerd** uit, schakel **Toegewezen capaciteit** in en selecteer de **toegewezen capaciteit van Power BI Embedded** die u hebt gemaakt. Selecteer vervolgens **Opslaan**.

    ![Leden toevoegen](media/embed-sample-for-customers/embed-sample-for-customers-024.png)

Nu kunt u de nieuwe werkruimte weergeven. De werkruimte wordt gemaakt en in Power BI geopend. De werkruimte wordt weergegeven in de lijst met werkruimten waarvan u lid bent. Omdat u een beheerder bent, kunt u het weglatingsteken (...) selecteren om terug te gaan en wijzigingen aanbrengen, bijvoorbeeld nieuwe leden toevoegen of machtigingen van leden wijzigen.

   ![Nieuwe werkruimte](media/embed-sample-for-customers/embed-sample-for-customers-025.png)

### <a name="create-and-publish-your-reports"></a>Rapporten maken en publiceren

U kunt de rapporten en gegevenssets maken met Power BI Desktop en de rapporten vervolgens publiceren naar een app-werkruimte. De eindgebruiker die de rapporten naar een app-werkruimte publiceert, moet beschikken over een Power BI Pro-licentie.

1. Download het voorbeeld van de [blogdemo](https://github.com/Microsoft/powerbi-desktop-samples) vanuit GitHub.

    ![Rapportvoorbeeld](media/embed-sample-for-customers/embed-sample-for-customers-026-1.png)

2. Open het voorbeeld-PBIX-rapport in **Power BI Desktop**.

   ![Rapport in PBI Desktop](media/embed-sample-for-customers/embed-sample-for-customers-027.png)

3. Publiceer het rapport naar de **app-werkruimte**.

   ![Rapport in PBI Desktop](media/embed-sample-for-customers/embed-sample-for-customers-028.png)

    U kunt het rapport nu weergeven in de Power BI-service online.

   ![Rapport in PBI Desktop](media/embed-sample-for-customers/embed-sample-for-customers-029.png)

## <a name="embed-your-content"></a>Uw inhoud insluiten

1. Download het [voorbeeld waarin de app eigenaar is van de gegevens](https://github.com/Microsoft/PowerBI-Developer-Samples) vanuit GitHub om aan de slag te gaan.

    ![Voorbeeldtoepassing waarin app eigenaar is van de gegevens](media/embed-sample-for-customers/embed-sample-for-customers-026.png)

2. Open het bestand Web.config in de voorbeeldtoepassing. Er zijn vijf velden die u moet invullen voor een correcte uitvoering van de toepassing: **clientID**, **groupId**, **reportId**, **pbiUsername** en **pbiPassword**.

      ![Bestand Web.config](media/embed-sample-for-customers/embed-sample-for-customers-030.png)

    * Vul bij **clientId** de **toepassings-ID** van **Azure** in. **clientId** wordt door de toepassing gebruikt om zich te identificeren bij de gebruikers bij wie ze machtigingen aanvragen. Ga als volgt te werk om de **client-id** op te halen:

        1. Meld u aan bij [Azure Portal](https://portal.azure.com).

        ![Hoofdweergave van Azure Portal](media/embed-sample-for-customers/embed-sample-for-customers-002.png)

        2. Kies in het navigatiedeelvenster links **Alle services** en selecteer **App-registraties**.

        ![App-registratie zoeken](media/embed-sample-for-customers/embed-sample-for-customers-003.png)
        3. Selecteer de toepassing waarvoor u de **client-id** wilt ophalen.

        ![App kiezen](media/embed-sample-for-customers/embed-sample-for-customers-006.png)

      4. U ziet een **toepassings-ID** die wordt vermeld als een GUID. Gebruik deze **toepassings-ID** als de **client-id** voor de toepassing.

        ![clientId](media/embed-sample-for-customers/embed-sample-for-customers-007.png)     

    * Vul bij **groupId** informatie over de **app-werkruimte-GUID** uit Power BI in.

        ![groupId](media/embed-sample-for-customers/embed-sample-for-customers-031.png)

    * Vul bij **reportId** informatie over de **rapport-GUID** uit Power BI in.

        ![reportId](media/embed-sample-for-customers/embed-sample-for-customers-032.png)    

    * Vul bij **pbiUsername** het Power BI-account van de hoofdgebruiker in.
    * Vul bij **pbiPassword** het wachtwoord van het Power BI-account van de hoofdgebruiker in.

3. Nu kunt u de toepassing uitvoeren.

    Selecteer eerst **Uitvoeren** in **Visual Studio**.

    ![De toepassing uitvoeren](media/embed-sample-for-customers/embed-sample-for-customers-033.png)

    Selecteer vervolgens **Rapport insluiten**. Selecteer de optie die overeenkomt met het item dat u wilt testen (rapporten, dasboards of tegels).

    ![Inhoud selecteren](media/embed-sample-for-customers/embed-sample-for-customers-034.png)
 
    U kunt het rapport nu weergeven in de voorbeeldtoepassing.

    ![Toepassing weergeven](media/embed-sample-for-customers/embed-sample-for-customers-035.png)

Voor een volledig voorbeeld van het gebruik van de JavaScript-API kunt u het [hulpprogramma Playground](https://microsoft.github.io/PowerBI-JavaScript/demo) gebruiken. Hiermee kunt u op een snelle manier verschillende typen Power BI Embedded-voorbeelden uitproberen. Op de [wikipagina voor PowerBI JavaScript](https://github.com/Microsoft/powerbi-javascript/wiki) vindt u ook meer informatie over de JavaScript-API.

Als u meer vragen hebt over Power BI Embedded, gaat u naar de pagina met [veelgestelde vragen](embedded-faq.md).  Als u in uw toepassing problemen ondervindt met Power BI Embedded, gaat u naar de pagina voor [probleemoplossing](embedded-troubleshoot.md).

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/) 