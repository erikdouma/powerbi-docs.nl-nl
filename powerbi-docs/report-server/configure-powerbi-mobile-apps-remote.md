---
title: Toegang via Power BI mobiele iOS-apps tot rapportservers op afstand configureren
description: Leer hoe u de mobiele iOS-apps op afstand kunt configureren voor uw rapportserver.
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-report-server
ms.topic: conceptual
ms.date: 05/22/2018
ms.author: maggies
ms.openlocfilehash: bbade67c9510b8d316364d991c09444712309514
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2018
ms.locfileid: "34722173"
---
# <a name="configure-power-bi-ios-mobile-app-access-to-a-report-server-remotely"></a>Toegang via Power BI mobiele iOS-apps tot rapportservers op afstand configureren

In dit artikel leert u hoe u het MDM-hulpprogramma van uw organisatie gebruikt om toegang op afstand via de Power BI mobiele iOS-app tot een rapportserver te configureren. Om dit in te stellen maken IT-beheerders een app-configuratiebeleid waarbij de vereiste informatie naar de app wordt gepusht. 

 Vervolgens kunnen gebruikers van Power BI mobiele iOS-apps eenvoudiger op afstand verbinding maken met de rapportserver van hun organisatie omdat de verbinding met de rapportserver al is geconfigureerd. 


## <a name="create-the-app-configuration-policy-in-mdm-tool"></a>Het app-configuratiebeleid maken in het MDM-hulpprogramma 

Als beheerder volgt u deze stappen in Microsoft Intune om het app-configuratiebeleid te maken. De stappen en ervaring bij het opzetten van het app-configuratiebeleid is mogelijk anders bij andere MDM-hulpprogramma’s. 

1. Maak verbinding met uw MDM-hulpprogramma. 
2. Maak en benoem een nieuw app-configuratiebeleid. 
3. Kies naar welke gebruikers u dit app-configuratiebeleid wilt distribueren. 
4. Maak sleutel-waardeparen. 

In de volgende tabel staan de paren.

|Sleutel  |Type  |Beschrijving  |
|---------|---------|---------|
| com.microsoft.powerbi.mobile.ServerURL | Tekenreeks | Rapportserver-URL </br> Moet beginnen met http/https |
| com.microsoft.powerbi.mobile.ServerUsername | Tekenreeks | [optioneel] </br> De gebruikersnaam die u wilt gebruiken om verbinding te maken met de server. </br> Als deze niet bestaat, wordt de gebruiker gevraagd de gebruikersnaam voor de verbinding in te voeren.| 
| com.microsoft.powerbi.mobile.ServerDisplayName | Tekenreeks | [optioneel] </br> De standaardwaarde is rapportserver </br> Een beschrijvende naam die in de app wordt gebruikt als naam voor de server | 
| com.microsoft.powerbi.mobile.OverrideServerDetails | Boolean | De standaardwaarde is Waar </br> Als deze optie is ingesteld op Waar, worden hiermee alle eventuele definities van de rapportserver overschreven die al op het mobiele apparaat bestaan (bestaande servers die al zijn geconfigureerd, worden verwijderd). </br> Wanneer overschrijven is ingesteld op Waar, voorkomt u hiermee ook dat gebruikers die configuratie kunnen verwijderen. </br> Wanneer de optie is ingesteld op Onwaar, worden de gepushte waarden toegevoegd en blijven bestaande instellingen bestaan. </br> Als dezelfde server-URL al is geconfigureerd in de mobiele app, laat de app die configuratie ongewijzigd en wordt de gebruiker niet gevraagd om opnieuw een verificatie voor dezelfde server uit te voeren. |

Hier ziet u een voorbeeld van het instellen van het configuratiebeleid met behulp van Intune.

![Intune configuratie-instellingen](media/configure-powerbi-mobile-apps-remote/power-bi-ios-remote-configuration-settings.png)

## <a name="end-users-connecting-to-a-report-server"></a>Eindgebruikers maken verbinding met een rapportserver

Nadat u het app-configuratiebeleid publiceert, krijgen gebruikers en apparaten die bij de distributielijst horen die voor dat beleid is gedefinieerd, de volgende ervaring wanneer ze de Power BI mobiele iOS-app starten. 

1. Ze zien een bericht dat hun mobiele app is geconfigureerd met een rapportserver en tikken op **Aanmelden**.

    ![Aanmelden bij de rapportserver](media/configure-powerbi-mobile-apps-remote/power-bi-config-server-sign-in.png)

2.  Op de pagina **Verbinding maken met server** zijn de details over de rapportserver al ingevuld. Ze tikken op **Verbinding maken**.

    ![Ingevulde details rapportserver](media/configure-powerbi-mobile-apps-remote/power-bi-ios-remote-configure-connect-server.png)

3. Ze voeren een wachtwoord ter verificatie in en tikken op **Aanmelden**. 

    ![Ingevulde details rapportserver](media/configure-powerbi-mobile-apps-remote/power-bi-config-server-address.png)

Ze kunnen nu KPI's en Power BI-rapporten zien en gebruiken die zijn opgeslagen op de rapportserver.

## <a name="next-steps"></a>Volgende stappen
[Administratoroverzicht](admin-handbook-overview.md)  
[Power BI Report Server installeren](install-report-server.md)  

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](https://community.powerbi.com/)

