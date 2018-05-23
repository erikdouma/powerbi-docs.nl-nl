---
title: Apps maken en publiceren met dashboards en rapporten in Power BI
description: 'Informatie over het maken en publiceren van apps: verzamelingen van dashboards en rapporten die zijn gemaakt om belangrijke statistieken voor uw organisatie te bieden.'
author: maggiesMSFT
manager: kfile
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 02/22/2018
ms.author: maggies
LocalizationGroup: Share your work
ms.openlocfilehash: 6efd54d868a5a1f2d8d657d352c7133d4036b0b6
ms.sourcegitcommit: 998b79c0dd46d0e5439888b83999945ed1809c94
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/17/2018
---
# <a name="create-and-publish-apps-with-dashboards-and-reports-in-power-bi"></a>Apps maken en publiceren met dashboards en rapporten in Power BI

In Power BI kunt u *apps* maken om gekoppelde dashboards en rapporten op één plek te verzamelen en ze vervolgens te publiceren naar grote groepen mensen in uw organisatie. U kunt ook verbinding maken met [Power BI-apps voor externe services](service-connect-to-services.md), zoals Google Analytics en Microsoft Dynamics CRM.

![Power BI-apps](media/service-create-distribute-apps/power-bi-apps-left-nav.png)

Uw zakelijke gebruikers hebben vaak meerdere Power BI-dashboards en rapporten nodig voor hun bedrijfsvoering. Apps brengen de verschillende onderdelen samen, zodat ze niet de namen en locaties van alle dashboards hoeven te onthouden.  

Met Power BI-apps, nu beschikbaar in preview, kunt u verzamelingen van dashboards en rapporten maken en deze apps naar uw hele organisatie of naar specifieke personen of groepen publiceren. Apps maken het u als beheerder of rapportmaker gemakkelijker om machtigingen voor verzamelingen van dashboards te beheren.

Zakelijke gebruikers kunnen uw apps op een aantal verschillende manieren installeren. Als de Power BI-beheerder u toestemming geeft, kunt u ze automatisch installeren in de Power BI-accounts van uw collega's. Anders kunnen ze uw apps vanuit Microsoft AppSource installeren, of u kunt ze via een directe koppeling verzenden. Ze kunnen uw inhoud eenvoudig vinden en opnieuw bekijken, omdat alles op één plek staat. Ze ontvangen automatisch updates en u kunt bepalen hoe vaak de gegevens worden vernieuwd. Meer informatie over de [app-ervaring voor zakelijke gebruikers](service-install-use-apps.md).

### <a name="licenses-for-apps"></a>Licenties voor apps
Als maker van apps hebt u een licentie voor Power BI Pro nodig. Voor uw app-gebruikers zijn er twee opties.

* Optie 1: alle zakelijke gebruikers moeten **Power BI Pro**-licenties hebben om uw app te bekijken. 
* Optie 2: vrije gebruikers in uw organisatie kunnen app-inhoud bekijken als uw app een Power BI Premium-capaciteit heeft. Lees [Wat is Power BI Premium?](service-premium.md) voor meer informatie.

### <a name="apps-and-organizational-content-packs"></a>Apps en organisatie-inhoudspakketten
Apps zijn verbeterde organisatie-inhoudspakketten. Als u al organisatie-inhoudspakketten hebt, blijven deze gewoon naast apps werken.

Nu u een overzicht van apps hebt, gaan we het hebben over *app-werkruimten*, waarin u apps kunt maken. 

## <a name="video-apps-and-app-workspaces"></a>Video: Apps en app-werkruimten
<iframe width="640" height="360" src="https://www.youtube.com/embed/Ey5pyrr7Lk8?showinfo=0" frameborder="0" allowfullscreen></iframe>

## <a name="app-workspaces"></a>App-werkruimten
*App-werkruimten* zijn de plekken waar u apps maakt. U moet dus eerst een app-werkruimte maken voordat u de app kunt maken. Als u ooit in een groepswerkruimte in Power BI hebt gewerkt, zullen app-werkruimten u bekend voorkomen. Het zijn in feite verder ontwikkelde groepswerkruimten: ruimten met tijdelijke bestanden en containers voor de inhoud van de app. 

U kunt collega's als leden of beheerders toevoegen aan deze werkruimten. Alle leden en beheerders van de app-werkruimte hebben Power BI Pro-licenties nodig. In de werkruimte kan iedereen samenwerken aan dashboards, rapporten en andere artikelen die u wilt publiceren naar een breder publiek of zelfs uw hele organisatie. 

Wanneer de inhoud klaar is, kunt u kiezen welke dashboards en rapporten u wilt publiceren. Vervolgens publiceert u de app. U kunt een directe koppeling naar een breder publiek verzenden, of ze kunnen uw app vinden op het tabblad Apps door naar **Download and explore more apps from AppSource** (Meer apps downloaden en verkennen vanuit AppSource) te gaan. Deze mensen kunnen de inhoud van de app niet wijzigen, maar ze kunnen wel bepaalde acties uitvoeren in de Power BI-service of een van de mobiele apps: filteren, markeren en de gegevens sorteren. 

## <a name="create-an-app-workspace"></a>Een app-werkruimte maken
[!INCLUDE [powerbi-service-create-app-workspace](./includes/powerbi-service-create-app-workspace.md)]

De werkruimte is leeg, dus u moet er inhoud aan toevoegen. Houd er rekening mee dat wanneer u de werkruimte maakt, het ongeveer een uur kan duren voordat de werkruimte aan Office 365 is doorgegeven. 

Toevoegen van inhoud werkt hetzelfde als inhoud toevoegen aan uw Mijn werkruimte, behalve dat andere personen in de werkruimte de inhoud ook kunnen zien en bewerken. Een groot verschil is dat wanneer u klaar bent, u de inhoud als app kunt publiceren. In de app-werkruimte kunt u bestanden uploaden of ermee verbinding maken, of verbinding maken met services van derden, net zoals in uw Mijn werkruimte. Voorbeeld:

* [Maak verbinding met services](service-connect-to-services.md) zoals Microsoft Dynamics CRM, Salesforce of Google Analytics.
* [Haal gegevens op uit bestanden](service-get-data-from-files.md) zoals Excel, CSV of PBIX-bestanden (Power BI Desktop).

Wanneer u inhoud bekijkt in een app-werkruimte, wordt de eigenaar weergegeven als naam van de app-werkruimte.

## <a name="add-an-image-to-your-app-optional"></a>Een afbeelding aan uw app toevoegen (optioneel)
Power BI maakt standaard een kleine gekleurde cirkel voor uw app met de initialen van de app. Maar misschien wilt u deze aanpassen met een afbeelding. U hebt een licentie voor Exchange Online nodig om een afbeelding toe te voegen.

1. Selecteer **Werkruimten**, selecteer het weglatingsteken (...) naast de naam van de werkruimte, en selecteer vervolgens **Leden**. 
   
     ![Werkruimteleden selecteren](media/service-create-distribute-apps/power-bi-apps-workspace-members.png)
   
    Het Office 365 Outlook-account voor de werkruimte wordt in een nieuw browservenster geopend.
2. Wanneer u de muisaanwijzer op de gekleurde cirkel in de linkerbovenhoek plaatst, verandert deze in een potloodpictogram. Selecteer het.
   
     ![Office 365-potloodpictogram](media/service-create-distribute-apps/power-bi-apps-workspace-edit-image.png)
3. Selecteer het potloodpictogram opnieuw en zoek de afbeelding die u wilt gebruiken.
   
     ![Het potlood opnieuw selecteren](media/service-create-distribute-apps/power-bi-apps-workspace-edit-group.png)
4. Selecteer **Opslaan**.
   
     ![Opslaan selecteren](media/service-create-distribute-apps/power-bi-apps-workspace-save-image.png)
   
    De afbeelding vervangt de gekleurde cirkel in het Office 365 Outlook-venster. 
   
     ![Aangepaste afbeelding](media/service-create-distribute-apps/power-bi-apps-workspace-image-in-office-365.png)
   
    In een paar minuten verschijnt de afbeelding ook in de app in Power BI.
   
     ![Aangepaste afbeelding](media/service-create-distribute-apps/power-bi-apps-image.png)

## <a name="publish-your-app"></a>Uw app publiceren
Als de dashboards en rapporten in uw app-werkruimte klaar zijn, kunt u deze als een app publiceren. U hoeft niet alle rapporten en dashboards in de werkruimte te publiceren. U kunt ook alleen de items publiceren die gereed zijn.

1. Kies in de lijstweergave van de werkruimte welke dashboards en rapporten u in de app wilt opnemen.

     ![Het dashboard selecteren om te publiceren](media/service-create-distribute-apps/power-bi-apps-incude-dashboard.png)

     Als u ervoor kiest om een rapport niet te publiceren, wordt er een waarschuwing naast het rapport en het bijbehorende dashboard weergegeven. U kunt de app nog steeds publiceren, maar in het bijbehorende dashboard ontbreken dan de tegels uit het rapport.

     ![Waarschuwing over bijbehorend dashboard](media/service-create-distribute-apps/power-bi-apps-report-warning.png)

2. Selecteer de knop **App publiceren** in de rechterbovenhoek om het proces voor het delen van alle inhoud in de werkruimte te starten.
   
     ![App publiceren](media/service-create-distribute-apps/power-bi-apps-publish-button.png)

3. Geef bij **Details** een beschrijving op om mensen te helpen de app te vinden. U kunt een achtergrondkleur instellen om de app te personaliseren.
   
     ![App-details](media/service-create-distribute-apps/power-bi-apps-details.png)

4. Bij **Inhoud** ziet u alle inhoud die wordt gepubliceerd als onderdeel van de app: alles wat u in de werkruimte hebt geselecteerd. U kunt ook de startpagina van de app instellen: het dashboard of rapport dat mensen als eerste zien wanneer ze naar uw app gaan. U kunt **Geen** kiezen. Vervolgens komen ze op een lijst van alle inhoud in de app te staan. 
   
     ![App-inhoud](media/service-create-distribute-apps/power-bi-apps-content.png)

5. Bepaal bij **Toegang** wie toegang tot de app heeft: ofwel iedereen in uw organisatie, of specifieke personen of Active Directory-beveiligingsgroepen. Als u toestemming hiervoor hebt, kunt u de app automatisch voor de ontvangers installeren. U kunt deze instelling inschakelen in de [Power BI-beheerportal](#how-to-enable-pushing-apps). Meer overwegingen voor het [pushen van een app](#how-to-enable-pushing-apps).

    ![App-toegang](media/service-create-distribute-apps/power-bi-apps-access.png)

6. Wanneer u **Voltooien** selecteert, wordt er een bevestigingsbericht weergegeven dat de app gereed is om te publiceren. U kunt in het dialoogvenster dat na het voltooien wordt weergegeven, de URL voor de directe koppeling naar de app kopiëren en verzenden naar de personen waarmee u de app hebt gedeeld.
   
     ![App voltooien](media/service-create-distribute-apps/power-bi-apps-success.png)

De zakelijke gebruikers waarnaar u de app hebt gepubliceerd, kunnen deze op verschillende manieren vinden. Als u de app automatisch kunt installeren, wordt deze onder Apps weergegeven in hun Power BI-account. U kunt ze de directe koppeling naar de app sturen, of ze kunnen ernaar zoeken in Microsoft AppSource, waar ze alle apps kunnen zien waar ze toegang tot hebben. Het maakt niet uit hoe ze de app verkrijgen, want als ze later naar Apps gaan, zullen ze deze app in de lijst zien staan.

Meer informatie over de [app-ervaring voor zakelijke gebruikers](service-install-use-apps.md).

## <a name="change-your-published-app"></a>Uw gepubliceerde app wijzigen
Nadat u uw app hebt gepubliceerd, kunt u deze wijzigen of bijwerken. Het is gemakkelijk om de app bij te werken als u een beheerder of lid van de app-werkruimte bent. 

1. Open de app-werkruimte die bij de app hoort. 
   
     ![Werkruimte openen](media/service-create-distribute-apps/power-bi-apps-open-workspace.png)
2. Open het dashboard of het rapport. U kunt de gewenste wijzigingen aanbrengen.
   
     De app-werkruimte is uw faseringsplek. Uw wijzigingen worden pas live wanneer u de app opnieuw publiceert. Dit betekent dat u wijzigingen kunt aanbrengen zonder dat dit de gepubliceerde apps beïnvloedt.  
 
3. Ga terug naar de lijst met inhoud van de app-werkruimte en selecteer **App bijwerken**.
   
     ![Knop App bijwerken](media/service-create-distribute-apps/power-bi-app-update-button.png)

4. Werk indien nodig **Details**, **Inhoud** en **Toegang** bij en selecteer **App bijwerken**.
   
     ![Knop App bijwerken](media/service-create-distribute-apps/power-bi-app-update-complete.png)

De mensen waarnaar u de app heeft gepubliceerd, zien automatisch de bijgewerkte versie van de app. 

# <a name="automatically-install-apps-for-end-users"></a>Automatisch apps voor eindgebruikers installeren
U kunt automatisch apps installeren voor eindgebruikers, zodat u eenvoudiger de juiste apps naar de juiste personen of groepen kunt distribueren.

Apps leveren gegevens die uw eindgebruikers nodig hebben om hun werkzaamheden te kunnen uitvoeren. Nu kunt u deze apps automatisch installeren in de lijst met apps en hoeft u de apps niet meer te zoeken in Microsoft AppSource of een installatiekoppeling te volgen. Dit maakt het voor u eenvoudiger om standaardinhoud voor Power BI te implementeren voor uw gebruikers.

## <a name="how-to-install-an-app-automatically-for-end-users"></a>Procedure voor het automatisch installeren van een app voor eindgebruikers
Zodra de beheerder de functie heeft ingeschakeld, is voor app-uitgevers een nieuwe optie beschikbaar voor het **automatisch installeren van de app**. Wanneer het selectievakje is ***ingeschakeld*** en de app-uitgever **Voltooien** (of **App bijwerken** voor bestaande apps) selecteert, wordt de app gepusht naar alle gebruikers of groepen die zijn gedefinieerd de sectie **Machtigingen** van de app op het tabblad **Toegang**.

![Het pushen van apps inschakelen](media/service-create-distribute-apps/power-bi-apps-access.png)

## <a name="how-users-get-the-apps-that-were-pushed-to-them"></a>Hoe krijgen gebruikers de apps die naar ze zijn gepusht?
Nadat u een app hebt gepusht, wordt deze automatisch weergegeven in de lijst met apps. U kunt de apps cureren die gebruikers of gebruikersrollen in uw organisatie paraat moeten hebben.

![Het pushen van apps inschakelen](media/service-create-distribute-apps/power-bi-apps-left-nav.png)

### <a name="considerations-for-automatically-installing-apps"></a>Overwegingen voor het automatisch installeren van apps
Hier volgt een aantal zaken waarmee u rekening moet houden wanneer u apps naar eindgebruikers pusht:

* Het automatisch installeren van apps voor gebruikers kan enige tijd in beslag nemen. De meeste apps worden direct voor gebruikers geïnstalleerd, maar het pushen van apps kan enige tijd duren.  Hoe lang dit duurt, is afhankelijk van het aantal items in de app en het aantal personen dat toegang tot de app heeft. U wordt aangeraden apps buiten bedrijfsuren te pushen en te zorgen dat er voldoende tijd voor de installatie is voordat gebruikers de app nodig hebben. Voordat u een algemene mededeling over de beschikbaarheid van de app verzendt, kunt u bij meerdere gebruikers controleren of de app is geïnstalleerd.

* Vernieuw de browser. Voordat de gepushte app in de lijst Apps wordt weergegeven, kan het zijn dat gebruikers de browser moeten vernieuwen of moeten sluiten en vervolgens opnieuw moeten openen.

* Als gebruikers de app niet direct in de lijst met apps zien, moeten ze de browser vernieuwen of sluiten en opnieuw openen.

* Probeer gebruikers niet te overspoelen met apps. Zorg ervoor dat u niet te veel apps pusht, zodat gebruikers het gevoel hebben dat de vooraf geïnstalleerde apps ook daadwerkelijk nuttig voor ze zijn. Voor een goed afstemming van de timing is het verstandig te bepalen wie apps naar eindgebruikers mag pushen. U kunt in uw organisatie een contactpersoon toewijzen die verantwoordelijk is voor het pushen van apps naar eindgebruikers.

* Gastgebruikers die een uitnodiging niet hebben geaccepteerd krijgen geen apps die automatisch voor hen worden geïnstalleerd.  

## <a name="unpublish-an-app"></a>Een app publiceren ongedaan maken
Elk lid van een app-werkruimte kan het publiceren van de app ongedaan maken.

* Selecteer in een app-werkruimte het weglatingsteken (**...**) in de rechterbovenhoek > **Publicatie van app ongedaan maken**.
  
     ![Publicatie van app ongedaan maken](media/service-create-distribute-apps/power-bi-app-unpublish.png)

Met deze actie wordt de app verwijderd voor iedereen waarnaar u deze hebt gepubliceerd, waarna ze geen toegang meer tot de app hebben. De app-werkruimte en de inhoud ervan worden niet verwijderd.

## <a name="power-bi-apps-faq"></a>Veelgestelde vragen over Power BI-apps
### <a name="how-are-app-workspaces-different-from-group-workspaces"></a>Hoe verschillen app-werkruimten van groepswerkruimten?
in deze release hebben we alle groepswerkruimten gewijzigd in app-werkruimten. U kunt een app uit elke van deze werkruimten publiceren. De functionaliteit blijft grotendeels gelijk aan die van groepswerkruimten. We hebben in de komende maanden de volgende verbeteringen voor app-werkruimten gepland: 

* Wanneer u app-werkruimten maakt, worden er niet bijbehorende entiteiten in Office 365 gemaakt, zoals bij groepswerkruimten. Op die manier kunt u zoveel app-werkruimten maken als u maar wilt zonder dat u zich zorgen hoeft te maken over verschillende Office 365-groepen die op de achtergrond worden gemaakt (u kunt nog steeds de OneDrive voor Bedrijven van een Office 365-groep gebruiken voor het opslaan van uw bestanden). 
* U kunt op dit moment mensen alleen individueel toevoegen aan de leden- en beheerderlijsten. U kunt binnenkort meerdere AD-beveiligingsgroepen of moderne groepen aan deze lijsten toevoegen voor eenvoudiger beheer.  

### <a name="how-are-apps-different-from-organizational-content-packs"></a>Hoe verschillen apps van organisatie-inhoudspakketten?
Apps zijn een verbetering en vereenvoudiging van inhoudspakketten, met enkele belangrijke verschillen. 

* Nadat zakelijke gebruikers een inhoudspakket hebben geïnstalleerd, verliest deze de gegroepeerde identiteit; de groep is nu alleen nog een lijst met dashboards en rapporten afgewisseld met andere dashboards en rapporten. Apps behouden daarentegen ook na de installatie hun groepering en identiteit. Dit maakt het eenvoudig voor zakelijke gebruikers om ze in de toekomst opnieuw te openen.
* U kunt meerdere inhoudspakketten vanuit elke werkruimte maken, maar een app heeft een een-op-eenrelatie met de werkruimte. We denken dat apps op deze manier gemakkelijker te begrijpen en op lange termijn te onderhouden zijn. Zie het planningsgedeelte van de Power BI-blog voor meer informatie over hoe we op dit vlak verbeteringen willen aanbrengen. 
* We willen organisatie-inhoudspakketten op termijn afschaffen. Daarom raden we u aan vanaf nu apps te maken.  

### <a name="what-about-read-only-members-in-groups"></a>Hoe zit het met alleen-lezen-leden in groepen?
U kunt alleen-lezen-leden toevoegen in groepen die de inhoud alleen kunnen bekijken. Het grootste probleem met deze benadering is dat u geen beveiligingsgroepen als leden kunt toevoegen. 

Met apps kunt u een alleen-lezen-versie van uw app-werkruimte publiceren voor grote groepen, met inbegrip van beveiligingsgroepen. U kunt uw wijzigingen voor de dashboards en rapporten in de app klaarzetten zonder dat eindgebruikers hier hinder van ondervinden. We raden u aan apps voortaan op deze manier te gebruiken. Op de lange termijn willen we ook alleen-lezen-leden van werkruimten afschaffen.  

## <a name="next-steps"></a>Volgende stappen
* [Apps in Power BI installeren en gebruiken](service-install-use-apps.md)
* [Power BI-apps voor externe services](service-connect-to-services.md)
* [Power BI-beheerportal](https://docs.microsoft.com/en-us/power-bi/service-admin-portal)
* Vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)
