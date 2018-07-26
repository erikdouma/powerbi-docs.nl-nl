---
title: Een alternatief e-mailadres gebruiken voor Power BI
description: Een alternatief e-mailadres gebruiken voor Power BI
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 03/08/2018
ms.author: mblythe
LocalizationGroup: Troubleshooting
ms.openlocfilehash: 5013c70e4d3998eb39e0de2a92f890417175fd62
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2018
ms.locfileid: "34240901"
---
# <a name="using-an-alternate-email-address"></a>Een alternatief e-mailadres gebruiken voor Power BI
Standaard wordt het e-mailadres dat u gebruikt voor het aanmelden bij Power BI gebruikt om u updates over de activiteit in Power BI te sturen.  Wanneer iemand u bijvoorbeeld een uitnodiging om iets te delen stuurt, wordt deze naar dit adres verzonden.

Soms wilt u deze e-mailberichten ontvangen via een alternatief e-mailadres, in plaats van het adres dat u oorspronkelijk hebt gebruikt om u aan te melden bij Power BI.

## <a name="updating-through-office-365-personal-info-page"></a>Bijwerken via de pagina Persoonlijke gegevens van Office 365
1. Ga naar uw [pagina Persoonlijke gegevens in Office 365](https://portal.office.com/account/#personalinfo).  Als u wordt gevraagd u aan te melden, doet u dit met het e-mailadres en wachtwoord dat u voor Power BI gebruikt.
2. Klik op de bewerkingskoppeling in de sectie Contactgegevens.  
   
   > [!NOTE]
   > Als u geen bewerkingskoppeling ziet, betekent dit dat uw e-mailadres wordt beheerd door uw Office 365-beheerder en moet u contact met hem of haar opnemen om uw e-mailadres bij te werken.
   > 
   > 
   
   ![](media/service-admin-alternate-email-address-for-power-bi/contact-details.png)
3. Voer in het veld Alternatief e-mailadres het e-mailadres in waarnaar Power BI-updates voortaan moeten worden verzonden.

> [!NOTE]
> Als u deze instelling wijzigt, heeft dit geen invloed op het e-mailadres dat wordt gebruikt voor het verzenden van service-updates, nieuwsbrieven en andere aanbiedingsberichten.  Deze worden altijd verzonden naar e-mailadres dat u oorspronkelijk hebt gebruikt bij het registreren voor Power BI.
> 
> 

## <a name="updating-through-azure-active-directory"></a>Bijwerken via Azure Active Directory
Wanneer u een insluittoken van Active Azure Directory (AAD) voor Power BI wilt vastleggen, kunt u gebruikmaken van drie verschillende typen e-mailberichten. De drie verschillende typen zijn:

* het belangrijkste e-mailadres dat is gekoppeld aan een AAD-account van een gebruiker;
* het e-mailadres UserPrincipalName (UPN);
* het matrixkenmerk van een 'ander' e-mailadres

Power BI selecteert welk e-mailadres moet worden gebruikt op basis van de volgende criteria:
1.  Als het e-mailkenmerk in het gebruikersobject van de AAD-tenant aanwezig is, wordt dat mailkenmerk door Power BI als e-mailadres gebruikt
2.  Als het UPN-e-mailadres *niet* tot het domein  **\*. onmicrosoft.com** behoort (de gegevens na het '\@’-symbool), wordt dat mailkenmerk door Power BI als e-mailadres gebruikt
3.  Als het matrixkenmerk 'ander' e-mailadres in het AAD-gebruikersobject aanwezig is, wordt het eerste e-mailadres in de lijst gebruikt (omdat er een lijst kan zijn van e-mailadressen in dit kenmerk)
4. Als geen van de bovenstaande voorwaarden aanwezig zijn, wordt het UPN-adres gebruikt

## <a name="updating-with-powershell"></a>Bijwerken met PowerShell
U kunt het alternatieve e-mailadres ook bijwerken via PowerShell voor Azure Active Directory. Dit doet u met de opdracht [Set-AzureADUser](https://docs.microsoft.com/powershell/module/azuread/set-azureaduser).

```
Set-AzureADUser -ObjectId john@contoso.com -OtherMails "otheremail@somedomain.com"
```

Zie [Azure Active Directory PowerShell versie 2 downloaden](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2) voor meer informatie.

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

