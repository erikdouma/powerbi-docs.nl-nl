---
title: Aan de slag met Power BI-gateways
description: Hier vindt u basisinformatie over gegevensgateways voor Power BI.
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
ms.date: 01/24/2018
ms.author: davidi
ms.openlocfilehash: 14c96dbc88784cd76099c25508409bcc24064e35
ms.sourcegitcommit: 7249ff35c73adc2d25f2e12bc0147afa1f31c232
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/25/2018
---
# <a name="getting-started-with-power-bi-gateways"></a>Aan de slag met Power BI-gateways
Welkom bij de gids **Aan de slag met Power BI-gateways**. In deze stapsgewijze introductie maakt u kennis met wat een gateway doet, hoe deze werkt en hoe u uw eigen gateway kunt installeren, configureren en uitvoeren.  

![](media/service-gateway-getting-started/gw_gettingstarted_0a.png)

Gateways kunnen een technisch onderwerp zijn en aangezien elk netwerk en bedrijf anders is, kunnen gateways behoorlijk complex zijn. Laten we het daarom simpel houden en beginnen met de basisprincipes.

## <a name="how-power-bi-gateways-work"></a>Hoe Power BI-gateways werken
Een **gateway** is software die toegang mogelijk maakt tot gegevens die zich bevinden in een particulier, on-premises netwerk, waarna deze later kunnen worden gebruikt in een cloudservice zoals Power BI. Een gateway is een soort poortwachter die luistert of er verbindingsaanvragen worden verzonden. Een aanvraag wordt alleen geaccepteerd wanneer deze voldoet aan bepaalde criteria (bijvoorbeeld of de gebruiker toestemming heeft om de gateway te gebruiken). Zodoende kunnen organisaties hun databases en warehouses in hun on-premises netwerken laten staan en een subset van deze gegevens gebruiken om aantrekkelijke rapporten en dashboards in Power BI te maken.

Een gateway beveiligt de toegang en gegevens ook door alle gegevens, die de gateway worden verwerkt te versleutelen en te comprimeren. Daarnaast moeten er wachtwoorden worden gebruikt om verbinding met de gegevensbronnen te maken. Dit klinkt waarschijnlijk allemaal vrij logisch, maar er zijn tal van details waarmee rekening moet worden gehouden.

Soms wilt u een eigen gateway alleen voor uzelf gebruiken. Misschien hebt u een grote Excel-werkmap plus drie SQL-databases met jaren aan verkoop- en marketinggegevens en u wilt een Power BI-dashboard maken waarin de verkoopcijfers vanuit verschillende perspectieven worden belicht. U bent de enige persoon die rapporten maakt, u bent eigenaar van de Excel-werkmap en alleen u gebruikt deze databases om Power BI-rapporten te maken. Het enige wat u nodig hebt is een gateway voor persoonlijk gebruik. U hoeft de gegevensbronnen immers niet te delen met anderen.

Het is echter ook mogelijk dat u voor een organisatie werkt met allerlei soorten databases van verschillende leveranciers, zoals Analysis Services, SAP, Oracle, IBM en diverse andere soorten gegevensbronnen, die toegankelijk moeten zijn voor tal van mensen, zodat ze verschillende rapporten kunnen maken. In dit geval hebt u een gateway nodig waarmee de toegang tot al deze bronnen kunt configureren. Vervolgens u moet u de toegang delen met een groot aantal mensen binnen uw organisatie. Dat is een heel ander type gateway.

Gelukkig biedt Power BI twee gateways die geschikt zijn voor elk van deze scenario's. De volgende twee gateway zijn beschikbaar in Power BI:

* **On-premises gegevensgateway (personal mode)**: Met deze gateway kan één gebruiker verbinding maken met bronnen. Kan niet worden gedeeld met anderen. Kan alleen worden gebruikt met Power BI.
* **On-premises gegevensgateway**: Hiermee kunnen meerdere gebruikers verbinding maken met meerdere on-premises gegevensbronnen. De gateway kan worden gebruikt met Power BI-, PowerApps-, Flow- en Azure Logic-apps. Hiervoor is slechts één gatewayinstallatie nodig.

Beide gateways hebben een soortgelijke functie. Ze faciliteren de toegang tot gegevens in een particulier on-premises netwerk, zodat deze gegevens kunnen worden gebruikt in cloudservices als Power BI. De persoonlijke gateway kan slechts door één persoon worden gebruikt en alleen met Power BI. De **on-premises gegevensgateway** kan worden gebruikt door verschillende gebruikers en verschillende services.

Als u een gateway wilt gebruiken, moet u drie stappen uitvoeren:

* De gateway installeren
* Gebruikers toevoegen aan de gateway (zodat ze de gateway kunnen gebruiken)
* Verbinding maken met gegevensbronnen

Als u een gateway gebruikt, kunt u bovendien nog iets dat belangrijk kan zijn:

* On-premises gegevens vernieuwen, zodat de Power BI-rapporten kunnen worden bijgewerkt met nieuwe gegevens

Wanneer u de gegevens kunt vernieuwen, betekent dit dat uw Power BI-dashboards en -rapporten altijd up-to-date zijn en de meest recente gegevens bevatten. Wanneer iemand een rapport weergeeft dat u hebt gemaakt met on-premises gegevens, bevat dat rapport de meest recent informatie, zelfs wanneer het rapport een tijd geleden is gemaakt.

Het eerste deel, het installeren van de gateway, is eenvoudig. U kunt gebruikers ook eenvoudig toegang geven tot de gateway. U kunt ze gewoon toevoegen via een dialoogvenster in Power BI. Het wordt wat ingewikkelder om verbinding met de gegevensbronnen te maken, aangezien er tal van verschillende gegevensbronnen zijn met verschillende verbindingsvereisten en nuances. Het vernieuwen van de gegevens komt in een andere handleiding aan de orde, zodat we ons in dit artikel volledig kunnen richten op de gateway.

Laten we niet te moeilijk beginnen en de installatieprocedure voor een gateway doorlopen.

## <a name="install-the-gateway"></a>De gateway installeren
Als u een gateway wilt installeren, opent u de Power BI-service (u kunt deze koppeling gebruiken om de Power BI-service in uw browser te starten en u aan te melden) en meld u zich aan met uw Power BI-account. Selecteer in de rechterbovenhoek van de Power BI-service het **downloadpictogram**, zoals in de volgende afbeelding, en selecteer **Gegevensgateway**.

![](media/service-gateway-getting-started/gw_gettingstarted_01.png)

U wordt omgeleid naar een downloadpagina, waar u op de knop **Gateway downloaden** klikt om het downloaden te starten.

![](media/service-gateway-getting-started/gw_gettingstarted_02.png)

In dit scherm wordt in het kort uitgelegd wat een gateway doet. Het bevat ook een aantal belangrijke **waarschuwingen**: wanneer u een gateway installeert, wordt deze uitgevoerd op de computer waarop u de installatie uitvoert. En als die computer wordt uitgeschakeld, wordt de gateway ook uitgeschakeld (de gateway werkt niet als deze niet wordt uitgevoerd). Ook kunt u de gateway beter niet installeren op een computer met een draadloos netwerk. Gebruik dus een computer die verbonden is met een bedraad netwerk.

Wanneer u klaar bent, selecteert u **Volgende** om door te gaan met de installatie.

![](media/service-gateway-getting-started/gw_gettingstarted_03.png)

Hier bepaalt u welk gateway u installeert: een on-premises gateway of een persoonlijke gateway. In deze gids wordt de **on-premises gegevensgateway**geïnstalleerd.

Er is een aantal punten waarmee u rekening moet houden om tot een beslissing te komen:

* Beide gateways vereisen een 64-bits Windows-besturingssysteem.
* Gateways kunnen niet worden geïnstalleerd op een domeincontroller.
* U kunt maximaal twee on-premises gegevensgateways installeren op dezelfde computer, één in beide modi (persoonlijk en standaard). 
* U kunt niet meer dan één gateway in dezelfde modus op dezelfde computer uitvoeren.
* U kunt meerdere on-premises gegevensgateways op verschillende computers installeren en deze allemaal beheren vanuit één Power BI-gatewaybeheerinterface (dit geldt niet voor de persoonlijke modus; zie het volgende punt).
* Voor elke Power BI-gebruiker kunt u slechts één gateway in de persoonlijke modus uitvoeren. Als u voor dezelfde gebruiker een andere gateway in de persoonlijke modus installeert, zelfs op een andere computer, wordt de bestaande voorgaande installatie vervangen door de meest recente installatie.

Wanneer we **Volgende** selecteert, wordt de installatie van de gateway gestart. U moet opgeven waar deze moet worden geïnstalleerd. Doorgaans is de standaardlocatie de beste locatie.

![](media/service-gateway-getting-started/gw_gettingstarted_06.png)

Het installatieproces gaat snel, en er wordt een statusbalk weergegeven.

![](media/service-gateway-getting-started/gw_gettingstarted_06a.png)

Zodra de installatie bijna is voltooid, moet u aangeven welk account u voor de gateway wilt gebruiken. Dit moet het account (gebruikersnaam en wachtwoord) zijn dat u gebruik om u aan te melden bij Power BI. De gateway is gekoppeld aan uw Power BI-account en u configureert de gateways via de Power BI-service.

![](media/service-gateway-getting-started/gw_gettingstarted_07.png)

U wordt aangemeld, zoals weergegeven in de volgende afbeelding.

![](media/service-gateway-getting-started/gw_gettingstarted_08.png)

Nadat u bent aangemeld, moet u een **herstelsleutel** maken. Herstelsleutels worden in een ander artikel uitvoerig behandeld, maar voor nu hoeft u alleen maar te weten dat u een herstelsleutel nodig hebt om uw gateway te herstellen of te verplaatsen.

![](media/service-gateway-getting-started/gw_gettingstarted_09.png)

Als alles goed gaat, wordt er een venster weergegeven met het bericht dat uw gateway klaar is.

![](media/service-gateway-getting-started/gw_gettingstarted_10.png)

Dat is alles voor de installatie van een on-premises gateway. Zoals beloofd, was dit een vrij eenvoudig proces. Tijdens de volgende stap kunt u **gebruikers toevoegen** of **gegevensbronnen toevoegen**. Het maakt niet uit waar u mee begint. Na de initiële configuratie kunt u altijd nog gebruikers of gegevensbronnen toevoegen.

In de volgende sectie wordt beschreven hoe u gebruikers aan de gateway toevoegt. Vervolgens wordt besproken waar u gegevensbronnen kunt toevoegen aan de gateway.

## <a name="add-users-to-a-gateway"></a>Gebruikers toevoegen aan een gateway
Nu er een gateway is geïnstalleerd, kunnen we deze beheren via de **Power BI-service**. Als u het beheerscherm voor gateways wilt weergeven, selecteert u in de rechterbovenhoek van de Power BI-service het tandwielpictogram en vervolgens **Gateways beheren**.

![](media/service-gateway-getting-started/gw_gettingstarted_15.png)

Er wordt een pagina binnen het canvas van de Power BI-service weergegeven waarin u uw gateways kunt beheren. De pagina **Gatewayinstellingen** ziet er ongeveer als volgt uit.

![](media/service-gateway-getting-started/gw_gettingstarted_12.png)

Als u op **Beheerders** tikt of klikt, wordt de volgende beheerpagina voor beheerders weergegeven. Op deze pagina kunt u alleen zien welke gebruikers de gateway kunnen *beheren*. Als u gebruikers van de gateway wilt toevoegen (of verwijderen) voor afzonderlijk gegevensbronnen, moet u een andere pagina gebruiken. Deze wordt besproken in de volgende alinea's.

![](media/service-gateway-getting-started/gw_gettingstarted_13.png)

Zodra u een gegevensbron hebt geïnstalleerd en gevalideerd, wordt deze links het venster **Gateways beheren** weergegeven onder de gekoppelde gateway, zoals in de volgende afbeelding. Het rechterdeelvenster bevat overigens twee secties waartussen u kunt schakelen: **Instellingen voor gegevensbron** en **Gebruikers**. Het daaropvolgende scherm is de sectie **Instellingen voor gegevensbron**.

![](media/service-gateway-getting-started/gw_gettingstarted_16.png)

Wanneer u **Gebruikers**, wordt er een tekstvak weergegeven waarin u gebruikers in uw organisatie kunt opgeven die u toegang wilt verlenen tot de geselecteerde gegevensbron. In het volgende scherm kunt u zien dat ik Maggie en Adam heb toegevoegd.

Wanneer u een e-mailadres in het tekstvak typt, toont Power BI u een lijst met gebruikers waarvan het e-mailadres overeenkomt met wat u typt. Zodoende kunt u op de naam klikken en deze toevoegen aan de lijst.

U kunt ook e-mailgroepen (aliassen) toevoegen om zowel groepen mensen als individuen toegang te bieden.

![](media/service-gateway-getting-started/gw_gettingstarted_17.png)

Zodra u **Toevoegen** hebt geselecteerd, worden de toegevoegde leden weergegeven in het vak en kunt u desgewenst meer leden toevoegen. Het is net zo gemakkelijk om gebruikers te verwijderen. Hiervoor schakelt u het selectievakje naast hu naam in en selecteert de knop **Verwijderen** onder het vak.

![](media/service-gateway-getting-started/gw_gettingstarted_18.png)

Zo eenvoudig werkt dat. Houd er rekening mee dat u gebruikers moet toevoegen aan elke gegevensbron waartoe u toegang wilt verlenen. Elke gegevensbron heeft een afzonderlijke lijst met gebruikers. De gebruikers moeten afzonderlijk worden toegevoegd aan de elke gegevensbron.

## <a name="adding-data-sources"></a>Gegevensbronnen toevoegen
U moet natuurlijk gegevensbronnen toevoegen om uw gateway bruikbaar te maken. Hier komt de complexiteit van Power BI-gateways om de hoek kijken. Er zijn tal van verschillende gegevensbronnen beschikbaar en elke gegevensbron heeft zijn eigen vereisten (en vaak ook een eigen vereist stuurprogramma).

Maar voordat we u naar een ander artikel verwijzen, kunt u hier zien hoe u een gegevensbron toevoegt. Ga naar de pagina **Gateways beheren** in de **Power BI-service**, selecteer de gateway waaraan u een gegevensbron wilt toevoegen en selecteer in de linkerbovenhoek van de pagina net boven de lijst met uw gateways de optie **Gegevensbron toevoegen**.

Wanneer u dit doet, wordt het venster **Instellingen voor gegevensbron** weergegeven in het rechterdeelvenster, zoals in de volgende afbeelding. Hier kunt u een naam voor de gegevensbron opgeven (in het tekstvak **Naam van gegevensbron**). Vervolgens selecteert u in de vervolgkeuzelijst **Gegevensbrontype** het type gegevensbron.

![](media/service-gateway-getting-started/gw_gettingstarted_14.png)

U hebt nu dus een gateway geïnstalleerd en kunt nu dus gegevensbronnen toevoegen. Mooi! Zie de bronnen in de volgende sectie voor informatie over gegevensbronnen, meer informatie over het gebruik van gateways en andere nuttige informatie.

## <a name="next-steps"></a>Volgende stappen
[De on-premises gegevensgateway gebruiken](service-gateway-onprem.md)  
[On-premises data gateway in-depth](service-gateway-onprem-indepth.md) (On-premises gegevensgateway - uitgebreid)  
[On-premises gegevensgateway (persoonlijke modus)](service-gateway-personal-mode.md)
[Problemen met de on-premises gegevensgateway oplossen](service-gateway-onprem-tshoot.md)  

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

