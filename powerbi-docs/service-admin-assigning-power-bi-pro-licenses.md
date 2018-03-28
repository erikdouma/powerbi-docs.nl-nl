---
title: Power BI Pro-licenties toewijzen
description: Power BI Pro-licenties toewijzen
services: powerbi
documentationcenter: ''
author: markingmyname
manager: kfile
backup: ''
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 03/22/2018
ms.author: maghan
LocalizationGroup: Administration
ms.openlocfilehash: 010f99922e2e9d43bbb192fe53eabb17a6af43f3
ms.sourcegitcommit: 1fe3ababba34c4e7aea08adb347ec5430e0b38e4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/22/2018
---
# <a name="assigning-power-bi-pro-licenses"></a>Power BI Pro-licenties toewijzen

Beheerders kunnen kiezen uit diverse beheerportals en PowerShell-cmdlets om Power BI Pro-licenties aan gebruikers toe te wijzen. Power BI-licentiebeheer wordt ondersteund door Azure Active Directory (Azure AD).

* De eigenaren van een Azure-abonnement kunnen de Azure Active Directory-blade in [Azure Portal](https://ms.portal.azure.com/#@microsoft.onmicrosoft.com/dashboard/private/39bc3cf7-31a4-43f6-954c-f2d69ca2f0) gebruiken. 

* Globale beheerders en gebruikersaccountbeheerders kunnen gebruikmaken van het [Office 365-beheercentrum](https://portal.office.com/AdminPortal/Home#/homepage).

## <a name="managing-power-bi-pro-licenses-in-the-azure-portal"></a>Power BI Pro-licenties beheren in Azure Portal

Power BI maakt gebruik van Microsoft Azure Active Directory, dat als service een belangrijke rol speelt. Door Microsoft Azure Active Directory worden gebruikersaccounts en groepen opgeslagen, maar ook andere instellingen zoals informatie over aangeschafte producten.

### <a name="assigning-licenses-to-individual-user-accounts"></a>Licenties toewijzen aan afzonderlijke gebruikersaccounts

Voer de volgende stappen uit om Pro-licenties toe te wijzen aan afzonderlijke gebruikersaccounts als u eigenaar bent van een Azure-abonnement:

1. Navigeer naar [Azure Portal](https://ms.portal.azure.com/#@microsoft.onmicrosoft.com/dashboard/private/39bc3cf7-31a4-43f6-954c-f2d69ca2f0). 

2. Klik in de linkernavigatiebalk op Azure Active Directory.

    ![image](media/service-assigning-power-bi-pro-licenses/service-assigning-power-bi-pro-licenses-01.png)

3. Klik in de Azure Active Directory-blade op Licenties.

    ![image](media/service-assigning-power-bi-pro-licenses/service-assigning-power-bi-pro-licenses-02.png)

4. Klik in de blade Licenties op Alle producten en vervolgens op Power BI Pro om de lijst van gebruikers met een licentie weer te geven.

    ![image](media/service-assigning-power-bi-pro-licenses/service-assigning-power-bi-pro-licenses-03.png)

5. Klik op Toewijzen om een Power BI Pro-licentie toe te voegen aan een extra gebruikersaccount.

    ![image](media/service-assigning-power-bi-pro-licenses/service-assigning-power-bi-pro-licenses-04.png)

> [!NOTE]
> Hoewel de meeste aspecten van licenties kunnen worden beheerd, is het niet mogelijk om Power BI Pro-licenties aan te schaffen in Azure Portal. Gebruik het Office 365-beheercentrum om een Power BI Pro-abonnement te kopen. Zie [Purchasing Power BI Pro](https://docs.microsoft.com/en-us/power-bi/service-admin-purchasing-power-bi-pro) (Power BI Pro kopen) voor meer informatie.
>

## <a name="managing-power-bi-pro-licenses-in-the-office-365-admin-center"></a>Power BI Pro-licenties beheren in het Office 365-beheercentrum

Als u een globale beheerder bent, kunt u in het Office 365-beheercentrum een Power BI Pro-abonnement aanschaffen en de bijbehorende licenties voor de organisatie beheren.

Voer de volgende stappen uit om Pro-licenties toe te wijzen aan afzonderlijke gebruikersaccounts als u een Office 365-beheerder bent:

1. Ga naar het Office 365-beheercentrum.

2. Vouw Gebruikers uit in het linkernavigatiedeelvenster en klik vervolgens op Actieve gebruikers.

    ![image](media/service-assigning-power-bi-pro-licenses/service-assigning-power-bi-pro-licenses-05.png)

3. Selecteer een of meerdere gebruikers en klik vervolgens op Productlicenties bewerken.

    ![image](media/service-assigning-power-bi-pro-licenses/service-assigning-power-bi-pro-licenses-06.png)

4. Zet de instelling onder Power BI Pro op Aan en klik vervolgens op Opslaan.

    ![image](media/service-assigning-power-bi-pro-licenses/service-assigning-power-bi-pro-licenses-07.png)

5. Controleer onder Status voor de geselecteerde accounts of de Power BI Pro-licentie is toegewezen.

    ![image](media/service-assigning-power-bi-pro-licenses/service-assigning-power-bi-pro-licenses-08.png)

> [!NOTE]
> Als uw abonnement geen licenties meer bevat, kunt u er meer toevoegen door Facturering uit te vouwen in het linkernavigatiedeelvenster en vervolgens op Abonnementen te klikken. Selecteer op de pagina Abonnementen het Power BI Pro-abonnement en klik vervolgens op Licenties toevoegen/verwijderen.
>

## <a name="next-steps"></a>Volgende stappen
[Power BI Pro in uw organisatie](service-admin-power-bi-pro-in-your-organization.md)
</br>
[De verlengde Pro-proefversie activeren](service-extended-pro-trial.md)
</br>
[Power BI-serviceovereenkomst voor afzonderlijke gebruikers](https://powerbi.microsoft.com/terms-of-service/)
</br>
[Aankondiging Power BI Premium](https://aka.ms/pbipremium-announcement)
</br>
[Power Bi-gebruikers zoeken die zich hebben aangemeld](service-admin-access-usage.md)

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](https://community.powerbi.com/)