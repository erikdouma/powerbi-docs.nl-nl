---
title: Abonneren op rapporten en dashboards in de Power BI-service
description: Leer hoe u uzelf en anderen kunt abonneren op een momentopname van een Power BI-rapport en -dashboard.
author: mihart
manager: kvivek
ms.reviewer: ''
featuredvideoid: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 06/04/2018
ms.author: mihart
LocalizationGroup: Common tasks
ms.openlocfilehash: bca79f79ba5bf918034231e44481ce422ebe7d97
ms.sourcegitcommit: 70192daf070ede3382ac13f6001e0c8b5fb8d934
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/22/2018
ms.locfileid: "46565999"
---
# <a name="subscribe-to-a-report-or-dashboard-in-power-bi-service-apppowerbicom"></a>Abonneren op een rapport of dashboard in de Power BI-service (app.powerbi.com)
Het is nog nooit zo eenvoudig geweest om op de hoogte blijven van uw belangrijkste dashboards en rapporten. Abonneer u en uzelf op de rapportpagina's en dashboards die voor u het belangrijkst zijn, zodat u een e-mail van Power BI in uw postvak ontvangt met een momentopname. U geeft voor Power BI op hoe vaak u de e-mails wilt ontvangen: van één keer per dag tot één keer per week. 

De e-mail en momentopname gebruiken de taal die is ingesteld in de instellingen van Power BI (zie [Ondersteunde talen en landen/regio's voor Power BI](../supported-languages-countries-regions.md)). Als er geen taal is ingesteld, gebruikt Power BI de taal van de lokale instellingen in uw huidige browser. Als u uw voorkeurstaal wilt bekijken of instellen, selecteert u het tandwielpictogram ![Tandwielpictogram](./media/end-user-subscribe/power-bi-settings-icon.png) > **Instellingen > Algemeen > Taal**. 

![Vervolgkeuzelijst Taal](./media/end-user-subscribe/power-bi-language.png)

Abonnementen kunnen alleen worden gemaakt in de Power BI-service. Wanneer u de e-mail ontvangt, bevat deze een koppeling naar het rapport of dashboard. Wanneer deze koppeling wordt geselecteerd op een mobiel apparaat waarop Power BI-apps zijn geïnstalleerd, wordt de app in plaats van het rapport of het dashboard op de website van Power BI (standaardacties) geopend.


## <a name="requirements"></a>Vereisten
- Het **maken** van een abonnement is een Power BI Pro-functie en u moet over bewerkingsmachtigingen beschikken voor de inhoud (dashboard of rapport) om dat abonnement te maken. 
- Aangezien e-mailberichten over abonnementen alleen worden verzonden wanneer een dataset wordt bijgewerkt of wordt vernieuwd, werken dergelijke abonnementen niet voor gegevenssets die niet worden bijgewerkt of vernieuwd.

## <a name="subscribe-to-a-dashboard-or-a-report-page"></a>Abonneren op een dashboard of een rapportpagina
Het proces voor het abonneren op een dashboard of rapport is grotendeels vergelijkbaar. U kunt zich (en anderen) met dezelfde knop abonneren op Power BI-service-dashboards en -rapporten.
 
![Pictogram Abonneren selecteren](./media/end-user-subscribe/power-bi-subscribe-orientation.png).

1. Open het dashboard of het rapport.
2. Selecteer in de bovenste menubalk **Abonneren** of selecteer het enveloppictogram ![Enveloppictogram](./media/end-user-subscribe/power-bi-icon-envelope.png).
   
   ![Pictogram Abonneren](./media/end-user-subscribe/power-bi-subscribe-icon.png)

3. Gebruik de gele schuifregelaar om het abonnement in of uit te schakelen.  Als u schuifregelaar instelt op Uit, wordt het abonnement niet verwijderd. Selecteer het prullenbakpictogram om het abonnement te verwijderen.

4. Vul de gegevens voor het e-mailbericht in. Uw e-mailadres is vooraf ingevuld, maar u kunt ook anderen toevoegen aan het abonnement. Alleen e-mailadressen in hetzelfde domein kunnen worden toegevoegd (Zie **Overwegingen en probleemoplossing** hieronder voor meer informatie). Als het rapport of het dashboard wordt gehost in [Premium-capaciteit](../service-premium.md), kunt u anderen abonneren met afzonderlijke e-mailadressen en groepsaliassen. Als het rapport of het dashboard niet in Premium-capaciteit wordt gehost, kunt u nog steeds anderen abonneren met hun afzonderlijke e-mailadres, maar moeten zij zelf ook een Power BI Pro-licentie hebben.

    Merk op in de onderstaande schermafbeelding dat wanneer u zich op een rapport abonneert, u zich feitelijk abonneert op een rapport*pagina*.  Als u zich op meer dan één pagina in een rapport wilt abonneren, selecteert u **Nog een abonnement toevoegen** en selecteert u een andere pagina. 
      
   ![Venster Abonneren](./media/end-user-subscribe/power-bi-subscribe2.png)

5. Selecteer **Opslaan en sluiten** om het abonnement op te slaan. Steeds wanneer een van de onderliggende gegevenssets wordt gewijzigd, ontvangen de abonnees een e-mail met een momentopname van het dashboard of de rapportpagina. Als het dashboard of rapport vaker dan één keer per dag wordt vernieuwd, ontvangt u alleen na de eerste vernieuwing een e-mail.  
   
   ![E-mail met momentopname van dashboard](./media/end-user-subscribe/power-bi-dashboard-email.jpg)
   
   > [!TIP]
   > Wilt u het e-mailbericht meteen zien? Activeer een e-mail door een van de gegevenssets te vernieuwen die zijn gekoppeld aan het dashboard of de gegevensset die aan het rapport is gekoppeld. (Als u geen bewerkingsmachtigingen hebt voor de gegevensset, moet u iemand met de juiste machtigingen vragen om dit voor u te doen.) Als u wilt weten welke gegevenssets worden gebruikt, selecteert u het pictogram **Gerelateerde items weergeven** ![Pictogram Gerelateerde items weergeven](./media/end-user-subscribe/power-bi-view-related.png) om **Gerelateerde inhoud** te openen en selecteert u vervolgens het vernieuwingspictogram ![Vernieuwingspictogram](./media/end-user-subscribe/power-bi-refresh.png). 
   > 
   > 
   
   ![Verwante gegevenssets](./media/end-user-subscribe/power-bi-view-related-screen.png)

## <a name="how-the-email-schedule-is-determined"></a>Hoe het e-mailschema wordt bepaald
In de volgende tabel wordt beschreven hoe vaak u een e-mailbericht ontvangt. Alles is afhankelijk van de verbindingsmethode van de gegevensset waarop het dashboard of rapport is gebaseerd (DirectQuery, Live Connect, geïmporteerd in Power BI of een Excel-bestand in OneDrive of SharePoint Online) en op de abonnementopties (dagelijks, wekelijks of geen).

|  | **DirectQuery** | **Live Connect** | **Geplande vernieuwing (import)** | **Excel-bestand in OneDrive/SharePoint Online** |
| --- | --- | --- | --- | --- |
| **Hoe vaak wordt het rapport/dashboard vernieuwd?** |Elke 15 minuten |Power BI controleert om de 15 minuten en als de gegevensset is gewijzigd, wordt het rapport vernieuwd. |De gebruiker selecteert geen, dagelijks of wekelijks. Dagelijks mag maximaal 8 keer per dag zijn. Wekelijks is daadwerkelijk een wekelijks schema dat de gebruiker maakt, waarbij er een vernieuwingsfrequentie van minimaal één keer per week en maximaal één keer per dag kan worden ingesteld. |Elk uur |
| **Hoeveel controle heeft de gebruiker over het e-mailschema voor het abonnement?** |Opties zijn: dagelijks of wekelijks |Geen opties: de gebruiker ontvangt een e-mailbericht als het rapport wordt vernieuwd, maar niet vaker dan één keer per dag. |Als het rapport dagelijks wordt vernieuwd, zijn de opties dagelijks en wekelijks.  Als het rapport wekelijks wordt vernieuwd, is alleen de optie wekelijks beschikbaar. |Geen opties: de gebruiker een ontvangt een e-mailbericht wanneer de gegevensset wordt bijgewerkt, maar niet vaker dan één keer per dag. |

## <a name="manage-your-subscriptions"></a>Uw abonnementen beheren
Alleen degene die het abonnement heeft gemaakt, kan dit beheren.  Er zijn 2 paden naar het scherm voor het beheren van uw abonnementen.  Voor het eerste pad selecteert u de optie **Alle abonnementen beheren** in het dialoogvenster **Abonneren op e-mails** (zie de schermafbeeldingen onder stap 4 hierboven). Voor het tweede pad selecteert u in de bovenste menubalk het tandwielpictogram ![Tandwielpictogram](./media/end-user-subscribe/power-bi-settings-icon.png) van Power BI en kiest u **Instellingen**.

![Instellingen selecteren](./media/end-user-subscribe/power-bi-subscribe-settings.png)

Welke abonnementen worden weergegeven, is afhankelijk van de werkruimte die op dat moment actief is.  Als u alle abonnementen voor alle werkruimten allemaal in één keer wilt weergeven, moet u ervoor zorgen dat **Mijn werkruimte** actief is. Zie [Werkruimten in Power BI](end-user-create-apps.md) voor meer informatie over werkruimten.

![Alle abonnementen in mijn werkruimte weergeven](./media/end-user-subscribe/power-bi-subscriptions.png)

Een abonnement wordt beëindigd als de Pro-licentie is verlopen, het dashboard of rapport door de eigenaar wordt verwijderd of het gebruikersaccount wordt verwijderd dat is gebruikt om het abonnement te maken.

## <a name="considerations-and-troubleshooting"></a>Aandachtspunten en probleemoplossing
* Als voor e-mailabonnementen in een dashboard beveiliging op rijniveau (RLS) is toegepast op een of meer tegels, worden deze tegels niet weergegeven.  Als de gegevensset RLS gebruikt voor e-mailabonnementen voor rapporten, kunt u geen abonnement maken.
* Abonnementen op rapportpagina’s zijn gekoppeld aan de naam van de rapportpagina. Als u zich abonneert op een rapportpagina en de naam ervan wijzigt, moet u uw abonnement opnieuw maken
* Momenteel worden e-mailabonnementen op rapporten/dashboards waarvoor gegevenssets van liveverbindingen worden gebruikt, niet ondersteund wanneer u andere gebruikers dan uzelf abonneert.
* Voor e-mailabonnementen op gegevenssets met een liveverbinding ontvangt u alleen e-mailberichten wanneer de gegevens worden gewijzigd. Als de gegevensset wordt vernieuwd en er geen gegevenswijzigingen zijn, ontvangt u geen mail van Power BI.
* E-mailabonnementen bieden geen ondersteuning voor de [aangepaste visuals](../power-bi-custom-visuals.md).  De enige uitzondering hierop vormen de aangepaste visuals die zijn [gecertificeerd](../power-bi-custom-visuals-certified.md).  
* E-mailabonnementen bieden op dit moment geen ondersteuning voor de aangepaste R-visuals.  
* Als beveiliging op rijniveau (RLS) is toegepast op een of meer dashboardtegels, worden deze tegels niet weergegeven.
* U kunt andere gebruikers niet abonneren op een rapport waarop RLS is toegepast.
* E-mailabonnementen worden verzonden met de standaard filter- en slicerstatus voor het rapport. De wijzigingen die u aanbrengt in de standaardwaarden nadat u zich abonneert, worden niet weergegeven in het e-mailbericht.    
* E-mailabonnementen worden nog niet ondersteund voor rapportpagina's die zijn gemaakt met de Power BI Desktop-functie voor een liveverbinding met de service.    
* Voor dashboardabonnementen geldt dat bepaalde soorten tegels nog niet worden ondersteund.  Hierbij gaat het om: streamingtegels, videotegels, tegels voor aangepaste webinhoud.     
* Als u een dashboard deelt met een collega buiten uw tenant, kunt u niet ook een abonnement maken voor deze collega. Als u aaron@xyz.com bent, kunt u delen met anyone@ABC.com, maar kunt u anyone@ABC.com nog niet abonneren en kunnen zij zich niet abonneren op gedeelde inhoud.      
* Mogelijk kunt u zich vanwege de maximale e-mailgrootte niet abonneren op dashboards of rapporten met extreem grote afbeeldingen.    
* Wanneer dashboards of rapporten langer dan twee maanden niet worden bezocht, wordt de vernieuwing van de bijbehorende gegevenssets automatisch door Power BI onderbroken.  Als u echter een abonnement aan een dashboard of rapport toevoegt, wordt het dashboard of rapport niet onderbroken, ook net als het niet wordt bezocht.    
* Als u geen e-mails voor een abonnement ontvangt, controleert u of uw User Principal Name (UPN) e-mails kan ontvangen. [Het Power BI-team werkt aan een versoepeling van deze vereiste](https://community.powerbi.com/t5/Issues/No-Mail-from-Cloud-Service/idc-p/205918#M10163). 
* Als uw dashboard of rapport zich in Premium-capaciteit bevindt, kunt u de e-mailalias van een groep gebruiken voor abonnementen, in plaats van alle collega's één voor één met het eigen e-mailadres te abonneren. De aliassen zijn gebaseerd op de huidige Active Directory. 

## <a name="next-steps"></a>Volgende stappen
* Nog vragen? [Misschien dat de Power Bi-community het antwoord weet](http://community.powerbi.com/).    
* [Lees het blogbericht](https://powerbi.microsoft.com/blog/introducing-dashboard-email-subscriptions-a-360-degree-view-of-your-business-in-your-inbox-every-day/)

