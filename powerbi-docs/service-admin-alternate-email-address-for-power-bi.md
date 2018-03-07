---
title: Een alternatief e-mailadres gebruiken voor Power BI
description: Een alternatief e-mailadres gebruiken voor Power BI
services: powerbi
documentationcenter: 
author: markingmyname
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
ms.date: 08/09/2017
ms.author: maghan
LocalizationGroup: Troubleshooting
ms.openlocfilehash: c97f60e39d68060c8eb3396bac4eb7725dab9c86
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/24/2018
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

## <a name="updating-with-powershell"></a>Bijwerken met PowerShell
U kunt het alternatieve e-mailadres ook bijwerken via PowerShell voor Azure Active Directory. Dit doet u met de opdracht [Set-AzureADUser](https://docs.microsoft.com/powershell/module/azuread/set-azureaduser).

```
Set-AzureADUser -ObjectId john@contoso.com -OtherMails "otheremail@somedomain.com"
```

Zie [Azure Active Directory PowerShell versie 2 downloaden](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2) voor meer informatie.

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

