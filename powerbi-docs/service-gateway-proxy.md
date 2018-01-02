---
title: Proxyinstellingen configureren voor de on-premises gegevensgateway
description: Informatie over de configuratie van de proxyinstellingen voor de lokale data gateway.
services: powerbi
documentationcenter: 
author: davidiseminger
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: powerbi
ms.date: 11/21/2017
ms.author: davidi
ms.openlocfilehash: 1598a2580c24623abc1bbb5fb5a3590ab0f2a6f6
ms.sourcegitcommit: b3ee37e1587f1269ee7dd9daf1685a06dea3b50c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/23/2017
---
# <a name="configuring-proxy-settings-for-the-on-premises-data-gateway"></a>Proxyinstellingen configureren voor de on-premises gegevensgateway
Het is mogelijk dat u in uw werkomgeving alleen toegang tot internet hebt via een proxy. Hierdoor is het mogelijk dat de on-premises gegevensgateway geen verbinding kan maken met de service.

## <a name="does-your-network-use-a-proxy"></a>Maakt uw netwerk gebruik van een proxy?
In het volgende bericht op superuser.com wordt beschreven hoe u kunt bepalen of er een proxy in uw netwerk wordt gebruikt.

[Hoe weet ik welke proxyserver die ik gebruik? (SuperUser.com)](https://superuser.com/questions/346372/how-do-i-know-what-proxy-server-im-using)

## <a name="configuration-file-location-and-default-configuration"></a>Locatie van het configuratiebestand en de standaardconfiguratie
De proxygegevens worden geconfigureerd in een .NET-configuratiebestand. De locatie en bestandsnamen kunnen afwijken. Dit is afhankelijk van de gateway die u gebruikt.

### <a name="on-premises-data-gateway"></a>On-premises gegevensgateway
Er zijn twee belangrijkste configuratiebestanden betrokken bij on-premises gegevensgateway.

**Configuratie**

De eerste is voor de configuratieschermen waarmee de gateway daadwerkelijk wordt geconfigureerd. Als u problemen ondervindt met het configureren van de gateway, is dit het bestand dat u moet controleren.

    C:\Program Files\On-premises data gateway\enterprisegatewayconfigurator.exe.config

**Windows-service**

Het tweede bestand is voor de Windows-service die communiceert met de Power BI-service en de aanvragen verwerkt.

    C:\Program Files\On-premises data gateway\Microsoft.PowerBI.EnterpriseGateway.exe.config

## <a name="configuring-proxy-settings"></a>Proxyinstellingen configureren
De standaardproxyconfiguratie is als volgt.

    <system.net>
        <defaultProxy useDefaultCredentials="true" />
    </system.net>

De standaardconfiguratie werkt met Windows-verificatie. Als uw proxy een andere vorm van verificatie gebruikt, moet u de instellingen wijzigen. Als u niet zeker weet welke vorm van verificatie wordt gebruikt, neemt u contact op met uw netwerkbeheerder.

Zie [Het element defaultProxy (Netwerkinstellingen)](https://msdn.microsoft.com/library/kd3cf2ex.aspx) voor meer informatie over de configuratie van de proxyelementen voor .NET-configuratiebestanden.

## <a name="changing-the-gateway-service-account-to-a-domain-user"></a>De gatewayserviceaccount wijzigen in een domeingebruiker
Wanneer de proxyinstellingen worden geconfigureerd voor het gebruik van standaardreferenties, zoals hierboven is uitgelegd, ondervindt u mogelijk verificatieproblemen met uw proxy. Dit komt omdat het standaardserviceaccount de service-SID is geen geverifieerde domeingebruiker. U kunt het serviceaccount van de gateway wijzigen om de juiste verificatie met uw proxy toe te staan.

> [!NOTE]
> U kunt het beste een beheerd serviceaccount gebruiken om te voorkomen dat wachtwoorden opnieuw moeten worden ingesteld. Meer informatie over hoe u een [beheerd serviceaccount](https://technet.microsoft.com/library/dd548356.aspx) maakt in Active Directory.
> 
> 

### <a name="change-the-on-premises-data-gateway-service-account"></a>Het serviceaccount van de on-premises gegevensgateway wijzigen
1. Wijzig het Windows-serviceaccount voor de **on-premises gegevensgatewayservice**.
   
    Het standaardaccount voor deze service is *NT SERVICE\PBIEgwService*. U kunt dit het beste wijzigen in een domeingebruikersaccount in uw Active Directory-domein. U kunt ook een beheerd serviceaccount gebruiken om te voorkomen dat het wachtwoord opnieuw moet worden ingesteld.
   
    U kunt het account wijzigen op het tabblad **Aanmelden** in de eigenschappen van de Windows-service.
2. Start de **on-premises gegevensgatewayservice** opnieuw.
   
    Open een opdrachtprompt met verhoogde bevoegdheid en voer de volgende opdrachten uit:
   
        net stop PBIEgwService
   
        net start PBIEgwService
3. Start de **configurator voor de on-premises gegevensgateway**. U kunt de startknop windows selecteren en zoeken op *lokale gegevensgateway*.
4. Meld u aan bij Power BI.
5. Gebruik de herstelsleutel om de gateway te herstellen.
   
    Zodoende stelt u het nieuwe serviceaccount in staat op de opgeslagen referenties voor gegevensbronnen te ontsleutelen.

## <a name="next-steps"></a>Volgende stappen
[On-premises gegevensgateway (personal mode)](service-gateway-personal-mode.md)
[Firewallinformatie](service-gateway-onprem-tshoot.md#firewall-or-proxy)  
Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

