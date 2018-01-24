---
title: Power BI in uw organisatie beheren
description: Power BI in uw organisatie beheren
services: powerbi
documentationcenter: 
author: guyinacube
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 11/28/2017
ms.author: asaxton
ms.openlocfilehash: 180e80ee327342b26849aa63a3910337737ac9ad
ms.sourcegitcommit: 7742f952c20695dfb475f74965c0065b02c01521
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/29/2017
---
# <a name="administering-power-bi-in-your-organization"></a>Power BI in uw organisatie beheren
Met Microsoft Power BI kunnen gebruikers gegevens visualiseren, ontdekkingen delen en samenwerken op intuïtieve nieuwe manieren. Zie [Aan de slag met Power BI](service-get-started.md) voor meer informatie.

Het beheer van Power BI kan op verschillende locaties worden uitgevoerd. Hier volgen twee veelvoorkomende locaties.

> [!NOTE]
> Om toegang te krijgen tot het Power BI-beheerportal, moet uw account zijn ingesteld als een **Globale beheerder**, in Office 365 of Azure Active Directory, of moet de rol van beheerder van de Power BI-service aan het account zijn toegewezen. Zie [Understanding the Power BI admin role](service-admin-role.md) (Power BI-beheerdersrol) voor meer informatie over de beheerdersrol voor de Power BI-service.
> 
> 

* [Power BI-beheerportal](https://app.powerbi.com/admin-portal)
* [Office 365-beheercentrum](https://portal.office.com/adminportal/home)

Zie [Uitleg over de Power BI-beheerdersrol](service-admin-role.md) voor meer informatie over de beheerdersrol voor de Power BI-service.

## <a name="whats-in-this-article"></a>In dit artikel
**Registreren voor Power BI**

* [Hoe kunnen gebruikers zich registreren voor Power BI?](#how-do-users-sign-up-for-power-bi)
* [Hoe kunnen afzonderlijke gebruikers in mijn organisatie zich registreren?](#how-do-individual-users-in-my-organization-sign-up)
* [Hoe kan ik voorkomen dat gebruikers lid worden van mijn bestaande Office 365-tenant?](#how-can-i-prevent-users-from-joining-my-existing-office-365-tenant)
* [Hoe kan ik toestaan dat gebruikers lid worden van mijn bestaande Office 365-tenant?](#how-can-i-allow-users-to-join-my-existing-office-365-tenant)
* [Hoe kan ik controleren of blokkeren is ingeschakeld in de tenant?](#how-do-i-verify-if-i-have-the-block-on-in-the-tenant)
* [Hoe voorkom ik dat mijn bestaande gebruikers Power BI gaan gebruiken?](#how-can-i-prevent-my-existing-users-from-starting-to-use-power-bi)
* [Hoe kan ik mijn bestaande gebruikers toestaan zich te registreren voor Power BI?](#how-can-i-allow-my-existing-users-to-sign-up-for-power-bi)

**Beheer van Power BI**

* [Heeft dit invloed op hoe ik nu identiteiten voor gebruikers in mijn organisatie beheer?](#how-will-this-change-the-way-i-manage-identities-for-users-in-my-organization-today)
* [Hoe beheer ik Power BI?](#how-do-we-manage-power-bi)
* [Wat is het proces voor het beheren van een tenant die door Microsoft voor mijn gebruikers is gemaakt?](#what-is-the-process-to-manage-a-tenant-created-by-Microsoft-for-my-users)
* [Kan ik beheren aan welke Office 365-tenant gebruikers worden toegevoegd, als ik meerdere domeinen heb?](#if-i-have-multiple-domains-can-i-control-the-office-365-tenant-that-users-are-added-to)
* [Hoe verwijder ik Power BI voor gebruikers die zich al hebben geregistreerd?](#how-do-i-remove-power-bi-for-users-that-already-signed-up)
* [Hoe weet ik wanneer nieuwe gebruikers lid zijn geworden van mijn tenants?](#how-do-i-know-when-new-users-have-joined-my-tenant)
* [Zijn er nog andere zaken waarop ik me moet voorbereiden?](#are-there-any-additional-things-i-should-be-prepared-for)
* [Is dit gratis? Worden er kosten in rekening gebracht voor deze licenties?](#is-this-free-will-i-be-charged-for-these-licenses)
* [Waar bevindt mijn Power BI-tenant zich?](#where-is-my-power-bi-tenant-located)
* [Wat is de Power BI SLA (Service Level Agreement)?](#what-is-the-power-bi-sla)

**Beveiliging in Power BI**

* [Voldoet Power BI aan nationale, regionale en branchespecifieke nalevingsvereisten?](#does-power-bi-meet-national-regional-and-industry-specific-compliance-requirements)
* [Hoe werkt beveiliging in Power BI?](#how-does-security-work-in-power-bi?)

## <a name="sign-up-for-power-bi"></a>Registreren voor Power BI
### <a name="how-do-users-sign-up-for-power-bi"></a>Hoe kunnen gebruikers zich registreren voor Power BI?
U kunt zich registreren voor Power BI via de [Power BI-website](https://powerbi.microsoft.com). U kunt zich ook registreren via de pagina voor aankoopservices in het Office 365-beheercentrum. Als een beheerder zich voor Power BI registreert, kan diegene gebruikerslicenties toewijzen aan gebruikers die toegang nodig hebben.

Bovendien kunnen afzonderlijke gebruikers in uw organisatie zich mogelijk registreren voor Power BI via de [Power BI-website](https://powerbi.microsoft.com). Wanneer een gebruiker in uw organisatie zich registreert voor Power BI, krijgt die gebruiker automatisch een Power BI-licentie toegewezen. [Meer informatie](service-self-service-signup-for-power-bi.md)

### <a name="how-do-individual-users-in-my-organization-sign-up"></a>Hoe kunnen afzonderlijke gebruikers in mijn organisatie zich registreren?
Er zijn drie scenario's die mogelijk van toepassing zijn op gebruikers in uw organisatie:

Scenario 1: uw organisatie heeft een bestaande Office 365-omgeving en de gebruiker die zich registreert voor Power BI heeft al een Office 365-account.
In dit scenario wordt, als een gebruiker al een werk- of schoolaccount in de tenant heeft (bijvoorbeeld contoso.com) maar niet Power BI heeft, het abonnement voor dat account gewoon door Microsoft geactiveerd. De gebruiker wordt automatisch op de hoogte gesteld van het gebruik van de Power BI-service.

Scenario 2: uw organisatie heeft een bestaande Office 365-omgeving en de gebruiker die zich registreert voor Power BI heeft geen Office 365-account.
In dit scenario heeft de gebruiker een e-mailadres in het domein van uw organisatie (bijvoorbeeld contoso.com), maar nog geen Office 365-account. In dit geval kan de gebruiker zich voor Power BI registreren, waarna diegene automatisch een account krijgt. Hiermee krijgt de gebruiker toegang tot de Power BI-service. Als een werknemer genaamd Nancy bijvoorbeeld haar zakelijke e-mailadres (zoals Nancy@contoso.com) gebruikt om zich te registreren, voegt Microsoft Nancy automatisch toe als gebruiker in de Office 365-omgeving van Contoso en wordt Power BI voor dat account geactiveerd.

Scenario 3: uw organisatie heeft nog geen Office 365-omgeving die is gekoppeld aan uw e-maildomein.
Uw organisatie hoeft geen acties op het gebied van beheer uit te voeren om Power BI te gebruiken. Gebruikers worden toegevoegd aan een nieuwe gebruikersdirectory die alleen van toepassing is op clouddiensten en u kunt de rol van tenant-beheerder aannemen om de gebruikers te beheren.

> [!IMPORTANT]
> Als uw organisatie meerdere e-maildomeinen heeft en u alle e-mailadresextensies in dezelfde tenant wilt houden, voegt u alle e-mailadresdomeinen aan een Azure Active Directory-tenant toe voordat gebruikers zich registreren. Er is geen geautomatiseerd mechanisme om gebruikers over te plaatsen naar andere tenants als deze eenmaal zijn gemaakt. Voor meer informatie over dit proces bekijkt u [Kan ik beheren aan welke Office 365-tenant gebruikers worden toegevoegd, als ik meerdere domeinen heb?](#if-i-have-multiple-domains-can-i-control-the-office-365-tenant-that-users-are-added-to) verderop in dit artikel en [Add your domain to Office 365](https://support.office.com/article/Add-your-users-and-domain-to-Office-365-6383f56d-3d09-4dcb-9b41-b5f5a5efd611) (Uw domein toevoegen aan Office 365) online.
> 
> 

### <a name="how-can-i-prevent-users-from-joining-my-existing-office-365-tenant"></a>Hoe kan ik voorkomen dat gebruikers lid worden van mijn bestaande Office 365-tenant?
Er zijn stappen die u als beheerder kunt uitvoeren om te voorkomen dat gebruikers lid worden van uw bestaande Office 365-tenant. Als u dit blokkeert, mislukken pogingen van gebruikers om zich te registreren en krijgen ze een bericht dat ze contact kunnen opnemen met de beheerder van hun organisatie. U hoeft dit proces niet te herhalen als u automatische distributie van licenties (zoals Office 365 voor onderwijs voor studenten, onderwijsmedewerkers en personeel) al hebt uitgeschakeld.

Deze stappen vereisen het gebruik van Windows PowerShell. Zie de [instructiehandleiding voor PowerShell](http://go.microsoft.com/fwlink/p/?LinkID=286814) om mee Windows PowerShell aan de slag te gaan.

U dient de meest recente 64-bits versie van de [Azure Active Directory-module voor Windows PowerShell](http://go.microsoft.com/fwlink/p/?LinkID=236297) te installeren om de volgende stappen uit te voeren.

Selecteer de koppeling en selecteer vervolgens **Uitvoeren** om het installatiepakket uit te voeren.

**Automatisch lid worden van tenant uitschakelen**: gebruik deze Windows PowerShell-opdracht om te voorkomen dat nieuwe gebruikers lid worden van een beheerde tenant:

* Automatisch lid worden van tenant voor nieuwe gebruikers uitschakelen:
  
    $msolcred = get-credential   connect-msolservice -credential $msolcred
  
    Set-MsolCompanySettings -AllowEmailVerifiedUsers $false
* Automatisch lid worden van tenant voor nieuwe gebruikers inschakelen:
  
    $msolcred = get-credential   connect-msolservice -credential $msolcred
  
    Set-MsolCompanySettings -AllowEmailVerifiedUsers $true

> [!NOTE]
> Deze blokkering voorkomt dat nieuwe gebruikers in uw organisatie zich registreren voor Power BI. Gebruikers die zich registreren voor Power BI voordat nieuwe registraties voor uw organisatie worden uitgeschakeld, behouden hun licentie. Zie het gedeelte [How Can I Remove Licenses?] \(Hoe verwijder ik licenties?) voor instructies over hoe u toegang tot Power BI kunt verwijderen voor gebruikers die zich eerder voor de service hebben geregistreerd.
> 
> 

### <a name="how-can-i-allow-users-to-join-my-existing-office-365-tenant"></a>Hoe kan ik toestaan dat gebruikers lid worden van mijn bestaande Office 365-tenant?
Als u wilt toestaan dat gebruikers lid worden van uw tenant, voert u de tegengestelde opdracht uit dan die is beschreven in de bovenstaande vraag.

U dient de meest recente 64-bits versie van de [Azure Active Directory-module voor Windows PowerShell](http://go.microsoft.com/fwlink/p/?LinkID=236297) te installeren om de volgende stappen uit te voeren.

    $msolcred = get-credential
    connect-msolservice -credential $msolcred

    Set-MsolCompanySettings -AllowEmailVerifiedUsers $true

### <a name="how-do-i-verify-if-i-have-the-block-on-in-the-tenant"></a>Hoe kan ik controleren of blokkeren is ingeschakeld in de tenant?
Gebruik het volgende PowerShell-script.

U dient de meest recente 64-bits versie van de [Azure Active Directory-module voor Windows PowerShell](http://go.microsoft.com/fwlink/p/?LinkID=236297) te installeren om de volgende stappen uit te voeren.

    $msolcred = get-credential
    connect-msolservice -credential $msolcred

    Get-MsolCompanyInformation | fl allow*

### <a name="how-can-i-prevent-my-existing-users-from-starting-to-use-power-bi"></a>Hoe voorkom ik dat mijn bestaande gebruikers Power BI gaan gebruiken?
Er zijn stappen die u als beheerder kunt uitvoeren om te voorkomen dat gebruikers zich registreren voor Power BI. Als u dit blokkeert, mislukken pogingen van gebruikers om zich te registreren en krijgen ze een bericht dat ze contact kunnen opnemen met de beheerder van hun organisatie. U hoeft dit proces niet te herhalen als u automatische distributie van licenties (zoals Office 365 voor onderwijs voor studenten, onderwijsmedewerkers en personeel) al hebt uitgeschakeld. [Meer informatie](service-admin-service-free-in-your-organization.md#enable-or-disable-individual-user-sign-up-in-azure-active-directory)

De AAD-instelling waarmee dit wordt bepaald, is **AllowAdHocSubscriptions**. Bij de meeste tenants is deze instelling ingesteld op waar, wat betekent dat de optie is ingeschakeld. Als u Power BI hebt aangeschaft via een partner, kan deze instelling zijn ingesteld op onwaar, wat betekent dat de optie is uitgeschakeld.

U dient de meest recente 64-bits versie van de [Azure Active Directory-module voor Windows PowerShell](http://go.microsoft.com/fwlink/p/?LinkID=236297) te installeren om de volgende stappen uit te voeren.

1. U moet zich eerst aanmelden bij Azure Active Directory met uw Office 365-referenties. In de eerste regel wordt naar uw referenties gevraagd. De tweede regel maakt verbinding met Azure Active Directory.
   
     $msolcred = get-credential   connect-msolservice -credential $msolcred
2. Nadat u bent aangemeld, kunt u de volgende opdracht geven om te controleren waarvoor uw tenant momenteel is geconfigureerd.
   
     Get-MsolCompanyInformation | fl AllowAdHocSubscriptions
3. U kunt met deze opdracht AllowAdHocSubscriptions inschakelen ($true) of uitschakelen ($false).
   
     Set-MsolCompanySettings -AllowAdHocSubscriptions $true

> [!NOTE]
> De vlag AllowAdHocSubscriptions wordt gebruikt voor het beheren van verschillende gebruikersmogelijkheden in uw organisatie, inclusief de mogelijkheid voor gebruikers om zich te registreren voor de Azure Rights Management-service. Het wijzigen van deze vlag heeft invloed op al deze mogelijkheden.
> 
> 

### <a name="how-can-i-allow-my-existing-users-to-sign-up-for-power-bi"></a>Hoe kan ik mijn bestaande gebruikers toestaan zich te registreren voor Power BI?
Als u wilt toestaan dat uw bestaande gebruikers zich aanmelden voor Power BI, voert u de opdracht uit die wordt vermeld voor de bovenstaande vraag, maar geeft u false in plaats van true door.

U dient de meest recente 64-bits versie van de [Azure Active Directory-module voor Windows PowerShell](http://go.microsoft.com/fwlink/p/?LinkID=236297) te installeren om de volgende stappen uit te voeren.

1. U moet zich eerst aanmelden bij Azure Active Directory met uw Office 365-referenties. In de eerste regel wordt naar uw referenties gevraagd. De tweede regel maakt verbinding met Azure Active Directory.
   
     $msolcred = get-credential   connect-msolservice -credential $msolcred
2. Nadat u bent aangemeld, kunt u de volgende opdracht geven om te controleren waarvoor uw tenant momenteel is geconfigureerd.
   
     Get-MsolCompanyInformation | fl AllowAdHocSubscriptions
3. U kunt met deze opdracht AllowAdHocSubscriptions inschakelen ($true) of uitschakelen ($false).
   
     Set-MsolCompanySettings -AllowAdHocSubscriptions $true

> [!NOTE]
> De vlag AllowAdHocSubscriptions wordt gebruikt voor het beheren van verschillende gebruikersmogelijkheden in uw organisatie, inclusief de mogelijkheid voor gebruikers om zich te registreren voor de Azure Rights Management-service. Het wijzigen van deze vlag heeft invloed op al deze mogelijkheden.
> 
> 

## <a name="administration-of-power-bi"></a>Beheer van Power BI
### <a name="how-will-this-change-the-way-i-manage-identities-for-users-in-my-organization-today"></a>Heeft dit invloed op hoe ik nu identiteiten voor gebruikers in mijn organisatie beheer?
Als uw organisatie al een bestaande Office 365-omgeving heeft en alle gebruikers in uw organisatie Office 365-accounts hebben, verandert er niets aan het identiteitsbeheer.

Als uw organisatie al een bestaande Office 365-omgeving heeft, maar niet alle gebruikers in uw organisatie een Office 365-account hebben, maken we een gebruiker in de tenant en wijzen we licenties toe op basis van het werk- of school-e-mailadres van de gebruiker. Dit wil zeggen dat het aantal gebruikers dat u beheert, zal toenemen naarmate er meer gebruikers in uw organisatie zich registreren voor de service.

Als u uw directory on-premises beheert en Active Directory Federation Services (AD FS) gebruikt, voegt Microsoft geen gebruikers toe aan uw tenant en ontvangen gebruikers die proberen lid te worden van uw tenant een bericht waarin staat dat ze contact kunnen opnemen met de beheerder van hun organisatie.

Als uw organisatie nog geen Office 365-omgeving aan uw e-maildomein heeft gekoppeld, verandert er niets aan uw identiteitsbeheer. Gebruikers worden toegevoegd aan een nieuwe gebruikersdirectory die alleen van toepassing is op clouddiensten en u kunt de rol van tenant-beheerder aannemen om de gebruikers te beheren.

### <a name="how-do-we-manage-power-bi"></a>Hoe beheer ik Power BI?
Power BI biedt een beheerportal waarmee u gebruiksstatistieken kunt bekijken, biedt een koppeling naar het Office 365-beheercentrum om gebruikers en groepen te beheren en biedt de mogelijkheid om instellingen voor de hele tenant te beheren. 

> [!NOTE]
> Uw account moet zijn ingesteld als een **Globale beheerder** in Office 365 of Azure Active Directory om toegang te krijgen tot de Power BI-beheerportal.
> 
> 

Zie [Power BI-beheerportal](service-admin-portal.md) voor meer informatie.

### <a name="what-is-the-process-to-manage-a-tenant-created-by-microsoft-for-my-users"></a>Wat is het proces voor het beheren van een tenant die door Microsoft voor mijn gebruikers is gemaakt?
Als een tenant is gemaakt door Microsoft, kunt u deze claimen en beheren met behulp van de volgende stappen:

1. Word lid van de tenant door u te registeren voor Power BI met een e-mailadresdomein dat overeenkomt met het tenantdomein dat u wilt beheren. Als Microsoft bijvoorbeeld de tenant contoso.com heeft aangemaakt, dient u lid te worden van de tenant met een e-mailadres dat eindigt op @contoso.com.
2. Claim beheerrechten door te verifiëren dat u het domein bezit: zodra u lid bent van de tenant, kunt u uzelf de rol *Globale beheerder* geven door het eigendom van het domein te verifiëren. Hiervoor volgt u de volgende stappen:
   
   1. Ga naar [https://portal.office.com](https://portal.office.com).
   2. Selecteer het pictogram van het startprogramma voor apps linksboven en kies vervolgens **Beheerder**.
   3. Lees de instructies op de pagina **Beheerder worden** en kies vervolgens **Ja, ik wil de beheerder worden**.
      
      > [!NOTE]
      > Als deze optie niet wordt weergegeven, is er al een Office 365-beheerder.
      > 
      > 

### <a name="if-i-have-multiple-domains-can-i-control-the-office-365-tenant-that-users-are-added-to"></a>Kan ik beheren aan welke Office 365-tenant gebruikers worden toegevoegd, als ik meerdere domeinen heb?
Als u niets doet, wordt er een tenant gemaakt voor elk domein en subdomein dat hoort bij de e-mailadressen van uw gebruikers.

Als u wilt dat alle gebruikers worden toegevoegd aan dezelfde tenant, ongeacht het domein van hun e-mailadres:

* Maak van tevoren een tenant of gebruik een bestaande tenant en voeg alle bestaande domeinen en subdomeinen toe die u in deze tenant wilt samenvoegen. Alle gebruikers met een e-mailadres dat eindigt op deze domeinen en subdomeinen worden dan automatisch lid van de doeltenant wanneer ze zich registreren.

> [!IMPORTANT]
> Er is geen ondersteuning voor een geautomatiseerd mechanisme om gebruikers over te plaatsen naar andere tenants als deze eenmaal zijn gemaakt. Zie [Add your users and domain to Office 365](https://support.office.com/article/Add-your-users-and-domain-to-Office-365-6383f56d-3d09-4dcb-9b41-b5f5a5efd611) (Uw gebruikers en domein toevoegen aan Office 365) voor meer informatie over het toevoegen van domeinen aan een enkele Office 365-tenant.
> 
> 

### <a name="how-do-i-remove-power-bi-for-users-that-already-signed-up"></a>Hoe verwijder ik Power BI voor gebruikers die zich al hebben geregistreerd?
Als een gebruiker zich heeft aangemeld voor Power BI, maar u ze geen toegang tot Power BI meer wilt geven, kunt u de Power BI-licentie voor die gebruiker verwijderen.

1. Ga naar het Office 365-beheercentrum.
2. Selecteer in de navigatiebalk **Gebruikers** > **Actieve gebruikers**.
3. Zoek de gebruiker waarvoor u de licentie wilt verwijderen en selecteer vervolgens de naam > **Bewerken**.
4. Selecteer op de detailpagina van de gebruiker **Licenties** in de linkernavigatiebalk.
5. Schakel het selectievakje bij **Power BI (gratis)** of **Power BI Pro** uit, afhankelijk van welke licentie op het account is toegepast.
6. Selecteer **Opslaan**.

> [!NOTE]
> U kunt licentiebeheer voor gebruikers ook bulksgewijs uitvoeren. Als u dit wilt doen, selecteert u meerdere gebruikers en selecteert u **Bewerken**.
> 
> 

### <a name="how-do-i-know-when-new-users-have-joined-my-tenant"></a>Hoe weet ik wanneer nieuwe gebruikers lid zijn geworden van mijn tenants?
Gebruikers die lid zijn geworden van uw tenant als onderdeel van dit programma worden een unieke licentie toegewezen. U kunt hierop filteren in het beheerdashboard in het deelvenster met actieve gebruikers.

Als u deze nieuwe weergave wilt maken, gaat u in het Office 365-beheercentrum naar **Gebruikers** > **Actieve gebruikers** en selecteert u in het menu **Een weergave selecteren** de optie **Nieuwe weergave** . Geef de nieuwe weergave een naam en selecteer onder **Toegewezen licentie** **Power BI (gratis)** of **Power BI Pro**. U kunt slechts één licentie per weergave selecteren. Als u de licenties voor zowel **Power BI (gratis)** als **Power BI Pro** hebt voor uw organisatie, dient u twee weergaven te maken. Zodra de nieuwe weergave klaar is, kunt u alle gebruikers in uw tenant zien die zich voor dit programma hebben geregistreerd.

### <a name="are-there-any-additional-things-i-should-be-prepared-for"></a>Zijn er nog andere zaken waarop ik me moet voorbereiden?
U kunt een toename in aanvragen voor het opnieuw instellen van wachtwoorden ervaren. Zie [Reset a user's password](https://support.office.com/article/Reset-a-users-password-7a5d073b-7fae-4aa5-8f96-9ecd041aba9c) (Het wachtwoord van een gebruiker opnieuw instellen) voor meer informatie over dit proces.

U kunt een gebruiker uit uw tenant verwijderen via het standaardproces in het Office 365-beheercentrum. Als de gebruiker echter nog steeds een actief e-mailadres van uw organisatie heeft, kan diegene opnieuw lid worden, tenzij u lid worden voor alle gebruikers blokkeert.

### <a name="is-this-free-will-i-be-charged-for-these-licenses"></a>Is dit gratis? Worden er kosten in rekening gebracht voor deze licenties?
De licenties van **Power BI (gratis)** zijn voor de gratis versie van Power BI. Als u geïnteresseerd bent in aanvullende mogelijkheden bent, kunt u de [Power BI Pro-versie](service-premium.md) bekijken.

### <a name="where-is-my-power-bi-tenant-located"></a>Waar bevindt mijn Power BI-tenant zich?
Zie [Waar bevindt mijn Power BI-tenant zich?](service-admin-where-is-my-tenant-located.md) voor informatie over hoe u ontdekt waar uw Power BI-tenant zich bevindt, ook bekend als het gegevensgebied.

### <a name="what-is-the-power-bi-sla"></a>Wat is de SLA voor Power BI?
Raadpleeg het artikel [Licentievoorwaarden en documentatie](http://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=37) in het gedeelte **Licentieverlening** van de website Microsoft-licentieverlening voor meer informatie over de Power BI SLA (Service Level Agreement).

## <a name="security-in-power-bi"></a>Beveiliging in Power BI
### <a name="does-power-bi-meet-national-regional-and-industry-specific-compliance-requirements"></a>Voldoet Power BI aan nationale, regionale en branchespecifieke nalevingsvereisten?
Lees meer informatie over Power BI-naleving in het [Microsoft Vertrouwenscentrum](http://go.microsoft.com/fwlink/?LinkId=785324).

### <a name="how-does-security-work-in-power-bi"></a>Hoe werkt beveiliging in Power BI?
Power BI is gebouwd op basis van Office 365, dat op zijn beurt is gebaseerd op Azure-services zoals Azure Active Directory. Zie [Beveiliging van Power BI](service-admin-power-bi-security.md) voor een overzicht van Power BI-architectuur. 

## <a name="next-steps"></a>Volgende stappen
[Power BI-beheerportal](service-admin-portal.md)  
[Understanding the Power BI admin role](service-admin-role.md) (Power BI-beheerdersrol)  
[Registreren voor Power BI via selfservice](service-self-service-signup-for-power-bi.md)  
[Power BI (free) in your organization](service-admin-service-free-in-your-organization.md) (Power BI (gratis) in uw organisatie)  
[Purchasing Power BI Pro](service-admin-purchasing-power-bi-pro.md) (Power BI Pro kopen)  
[Power BI Premium - wat is het?](service-premium.md)  
[Power BI Premium aanschaffen](service-admin-premium-purchase.md)  
[Office 365 user account management](https://technet.microsoft.com/library/office-365-user-account-management.aspx) (Beheer van Office 365-gebruikersaccounts)  
[Office 365 group management](https://support.office.com/Article/Find-help-about-Groups-in-Office-365-7a9b321f-b76a-4d53-b98b-a2b0b7946de1) (Beheer van Office 365-groepen)  
[Uw groep beheren in Power BI en Office 365](service-manage-app-workspace-in-power-bi-and-office-365.md)  
[Technisch document over Power BI Premium](https://aka.ms/pbipremiumwhitepaper)  

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

