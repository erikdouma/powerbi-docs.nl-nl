---
title: Power BI Gateway - Personal
description: Power BI Gateway - Personal
services: powerbi
documentationcenter: ''
author: mgblythe
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
ms.date: 12/06/2017
ms.author: mblythe
LocalizationGroup: Gateways
ms.openlocfilehash: 8d047e814eaa7c84ee7e1be20d1f4722c6cb1e56
ms.sourcegitcommit: c80fbf5b12754ce217cb47a17cb5400b1036a8f2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/06/2018
---
# <a name="power-bi-gateway---personal"></a>Power BI Gateway - Personal
> [!NOTE]
> Er is een nieuwe versie van de persoonlijke gateway voor Power BI: de **On-premises gegevensgateway (persoonlijke modus)**. Het volgende artikel beschrijft de vorige versie van de persoonlijke gateway, genaamd **Power BI Gateway - Personal**. Deze wordt op 31 juli 2017 buiten gebruik gesteld, waarna deze niet meer zal werken. Zie het artikel [**On-premises gegevensgateway (persoonlijke modus)**](service-gateway-personal-mode.md) voor meer informatie over de nieuwe versie van de persoonlijke gateway, inclusief de installatie-instructies.
> 
> 

De **Power BI Gateway - Personal** fungeert als een brug die een snelle en veilige gegevensoverdracht biedt tussen de Power BI-service en on-premises gegevensbronnen die ondersteuning bieden voor [vernieuwen](refresh-data.md). Dit artikel is bedoeld om uitgebreid in te gaan op de werking van de gateway en te helpen bepalen of een gateway voor u nodig is. We hebben ook deze [handig video](https://www.youtube.com/watch?v=de58vROLqZI) over de persoonlijke gateway samengesteld. 

De gateway wordt op uw computer geïnstalleerd en uitgevoerd als een service. Wanneer deze als een service wordt uitgevoerd, wordt hiervoor het Windows-account gebruikt dat u tijdens de configuratie opgeeft. In sommige gevallen wordt de gateway uitgevoerd als een toepassing. Daar gaan we later op in.

Wanneer gegevens uit een on-premises gegevensbron worden vernieuwd met Power BI, zorgt de gateway ervoor dat uw Power BI-account de juiste machtigingen heeft om verbinding te maken en gegevens op te vragen bij de gegevensbron.

Gegevensoverdracht tussen Power BI en de gateway wordt beveiligd via [Azure Service Bus](http://azure.microsoft.com/documentation/services/service-bus/). De Service Bus maakt een beveiligd kanaal tussen de Power BI-service en uw computer. Omdat de gateway deze beveiligde verbinding biedt, is het doorgaans niet nodig om een poort te openen in uw firewall.

Voordat we nader naar de gateway gaan kijken, is het handig eerst enkele termen te bespreken die in Power BI worden gebruikt:

Een *gegevensset* bestaat uit gegevens die van een online of on-premises gegevensbron worden geüpload naar de Power BI-service. U maakt een gegevensset wanneer u de functie Gegevens ophalen gebruikt om verbinding te maken met uw gegevens en deze te uploaden. Gegevenssets worden weergegeven in het deelvenster Mijn werkruimte in uw Power BI-werkruimte in uw browser. Wanneer u rapporten en tegels vastmaakt aan uw dashboards, ziet u gegevens uit uw gegevenssets.

Een *gegevensbron* is de plek waar de gegevens die u uploadt naar een gegevensset werkelijk vandaan komen. Dit kan van alles zijn: een database, een Excel-werkblad,  een webservice, enz. U kunt in Excel-werkmappen een eenvoudig werkblad maken met rijen gegevens en dat gebruiken als een gegevensbron. U kunt ook Power Query of Power Pivot in Excel gebruiken om verbinding te maken met gegevens in online en on-premises gegevensbronnen en deze op te vragen, allemaal in dezelfde werkmap. Ook kunt u de functie Gegevens ophalen in Power BI Desktop gebruiken om verbinding te maken met gegevens in zowel online als on-premises gegevensbronnen en deze zo op te vragen.

De persoonlijke gateway wordt geïnstalleerd via de On-premises gegevensgateway. U kunt deze downloaden via de [Power BI Gateway-pagina](https://powerbi.microsoft.com/gateway/).

## <a name="do-i-need-a-gateway"></a>Heb ik een gateway nodig?
Voordat u een gateway installeert, is het belangrijk om te bepalen of u deze echt nodig hebt. Dit hangt af van uw gegevensbronnen:

### <a name="on-premises-data-sources"></a>On-premises gegevensbronnen
Een persoonlijke gateway *is vereist* als u gegevenssets wilt vernieuwen die gegevens opvragen uit een ondersteunde on-premises gegevensbron in uw organisatie.

Met een gateway worden de functies NU VERNIEUWEN en VERNIEUWEN PLANNEN ondersteund voor gegevenssets die worden geüpload van:

* Werkmappen van Microsoft Excel 2013 (of later) waarin gebruikt wordt gemaakt van Power Query of Power Pivot om verbinding te maken met een ondersteunde on-premises gegevensbron en hiervan gegevens op te vragen. Alle on-premises gegevensbronnen die in Externe gegevens ophalen worden weergegeven in Power Query of Power Pivot, bieden ondersteuning voor vernieuwen, met uitzondering van Hadoop-bestanden (HDFS) en Microsoft Exchange.
* Microsoft Power BI Desktop-bestanden waarbij Gegevens ophalen wordt gebruikt om verbinding te maken met een ondersteunde on-premises gegevensbron en hiervan gegevens op te vragen. Alle on-premises gegevensbronnen die in Gegevens ophalen worden weergegeven, bieden ondersteuning voor vernieuwen, met uitzondering van Hadoop-bestanden (HDFS) en Microsoft Exchange.

### <a name="online-data-sources"></a>Online gegevensbronnen
Een gateway *is alleen vereist* als u de functie [**Web.Page**](https://msdn.microsoft.com/library/mt260924.aspx) gebruikt. In andere gevallen is een gateway *niet* vereist voor het vernieuwen van gegevenssets die alleen gegevens uit een online-gegevensbron bevatten.

> [!NOTE]
> Als u de functie [**Web.Page**](https://msdn.microsoft.com/library/mt260924.aspx) gebruikt, hebt u alleen een gateway nodig als u de gegevensset of uw rapport na 18 november 2016 opnieuw hebt gepubliceerd.
> 
> 

De functies NU VERNIEUWEN en VERNIEUWEN PLANNEN worden zonder gateway ondersteund voor gegevenssets die worden geüpload van:

* Inhoudspakketten uit online-gegevensbronnen (inhoudspakketten\\services). Gegevenssets uit inhoudspakketten worden standaard automatisch eens per dag bijgewerkt, maar u kunt ook handmatig vernieuwen of een schema voor gegevensvernieuwing instellen.
* Werkmappen van Microsoft Excel 2013 (of later) waarin gebruikt wordt gemaakt van Power Query of Power Pivot om verbinding te maken met een online gegevensbron en hiervan gegevens op te vragen.
* Microsoft Power BI Desktop-bestanden waarbij Gegevens ophalen wordt gebruikt om verbinding te maken met een online gegevensbron en hiervan gegevens op te vragen.

**Vraag:** wat als mijn Excel-werkmap of Power BI Desktop-bestand gegevens ontvangt uit zowel online als on-premises gegevensbronnen?

**Antwoord:** dan is een gateway *wel* vereist. U dient een gateway te installeren en configureren om gegevens van uw on-premises gegevensbronnen te vernieuwen.

**Vraag:** wat als mijn Excel-werkmap enkel bestaat uit rijen gegevens die ik met de hand heb ingevoerd?**

**Antwoord:** dan is een gateway *niet* vereist. U hoeft alleen een gateway te installeren en configureren indien uw werkmap Power Query of Power Pivot gebruikt om gegevens op te vragen en aan een gegevensmodel toe te voegen vanuit een ondersteunde on-premises gegevensbron.

## <a name="setting-up-a-gateway-for-the-first-time"></a>Een nieuwe gateway instellen
Er zijn drie stappen vereist om een nieuwe gateway in te stellen:

1. Een gateway downloaden en installeren
2. De gateway configureren
3. Aanmelden bij gegevensbronnen in Power BI

Laten we deze stappen eens nader bekijken.

### <a name="download-and-install-a-gateway"></a>Een gateway downloaden en installeren
> [!NOTE]
> Er is een nieuwe versie van de persoonlijke gateway voor Power BI, de **On-premises gegevensgateway (persoonlijke modus)**. Dit artikel beschrijft de vorige versie van de persoonlijke gateway, genaamd **Power BI Gateway - Personal**. Deze wordt op 31 juli 2017 buiten gebruik gesteld, waarna deze niet meer zal werken. Zie het artikel [**On-premises gegevensgateway (persoonlijke modus)**](service-gateway-personal-mode.md) voor meer informatie over de nieuwe versie van de persoonlijke gateway, inclusief de installatie-instructies.
> 
> 

U wordt gevraagd een gateway te installeren wanneer u bij een ondersteunde gegevensset voor het eerst klikt op NU VERNIEUWEN of VERNIEUWEN PLANNEN. Ook kunt u **Gegevensgateway** selecteren in het menu Downloads om de gateway te downloaden. Download de [On-premises gegevensgateway](http://go.microsoft.com/fwlink/?LinkID=820925).

Selecteer hier **Persoonlijke gateway** in plaats van **On-premises gegevensgateway** om een gateway voor uzelf in te richten.

Het installeren van een gateway is niet heel ingewikkeld. U selecteert een locatie om de gateway te installeren en wordt gevraagd om de gebruiksrechtovereenkomst te lezen en accepteren, net als bij elke andere toepassing. Er zijn echter enkele belangrijke zaken om rekening mee te houden. Met name het type computer waarop u de gateway installeert en het type account waarmee u op die computer bent aangemeld bij Windows zijn van belang.

> [!NOTE]
> De gateway moet toegang hebben tot de gegevensbron. Als uw computer geen verbinding met de gegevensbron kan maken, kunt u overwegen om een [On-premises gegevensgateway](service-gateway-onprem.md) te installeren op een computer die wel toegang tot de gegevensbron heeft. Dit kan bijvoorbeeld een installatie van SQL Server zijn op een virtuele machine (VM) die wordt gehost in Azure. Uw persoonlijke computer heeft mogelijk geen toegang tot de virtuele machine. U kunt dan de On-premises gegevensgateway installeren op de virtuele machine en de gegevensbron configureren in de Power BI-service.
> 
> 

### <a name="computer-type"></a>Type computer
Het type computer waarop u de gateway installeert is belangrijk.

> [!NOTE]
> De persoonlijke gateway wordt alleen ondersteund op 64-bits Windows-besturingssystemen.
> 
> 

Op een laptop: om een geplande vernieuwing te kunnen uitvoeren, moet de gateway actief en functioneel zijn. Laptopcomputers zijn doorgaans meer tijd uitgeschakeld of in de slaapstand dan ze actief zijn. Als u uw gateway op een laptop wilt installeren, dient u er dus voor te zorgen dat de vernieuwtijden zijn ingesteld op tijden dat de laptop is ingeschakeld. Als dit niet het geval is, wordt het vernieuwen uitgesteld tot de volgende geplande vernieuwing.

Op een desktopcomputer hoeft u op dit vlak weinig problemen te verwachten. U hoeft er dan alleen voor te zorgen dat de computer aanstaat en de gateway wordt uitgevoerd op de geplande tijdstippen voor vernieuwing. Veel desktopcomputers schakelen naar de slaapstand, maar geplande vernieuwing is niet mogelijk als de slaapstand actief is.

Als u eenmaal een gateway hebt geïnstalleerd, hoeft u geen andere gateway meer te installeren. Een gateway werkt voor een willekeurig aantal ondersteunde gegevenssets. Ook hoeft u geen gateway te installeren als u dezelfde computer gebruikt als waarvan u uw werkmap en Power BI Desktop-bestanden uploadt. Hier volgt een voorbeeld: stel dat u een Excel-werkmap hebt die verbinding maakt met een SQL Server-gegevensbron in uw organisatie. U hebt de functie Gegevens ophalen in Power BI gebruikt om de werkmap te uploaden vanaf uw laptop. U hebt ook een desktopcomputer die altijd aanstaat en op deze computer hebt u een gateway geïnstalleerd en geconfigureerd. U bent in Power BI aangemeld bij uw gegevensbronnen en hebt een schema voor gegevensvernieuwing ingesteld voor de gegevensset.  Wanneer het tijd is voor een geplande vernieuwing, maakt Power BI een beveiligde verbinding met de gateway die is geïnstalleerd op uw desktopcomputer. Deze maakt vervolgens een veilige verbinding met de gegevensbronnen om updates te downloaden. Voor vernieuwingen is er geen communicatie met de oorspronkelijke werkmap die u hebt geüpload vanaf uw laptop.

> [!NOTE]
> U kunt de persoonlijke en enterprise-gateways op dezelfde computer installeren.
> 
> 

### <a name="windows-account"></a>Windows-account
Wanneer u de gateway installeert, bent aangemeld bij uw computer met uw Windows-account. Het type machtigingen dat uw Windows-account heeft, is van invloed op hoe de gateway wordt geïnstalleerd en hoe deze wordt uitgevoerd in Windows.

Wanneer u bij Windows bent aangemeld:

|  | Met beheerdersmachtigingen | Zonder beheerdersmachtigingen |
| --- | --- | --- |
| **Power BI Gateway - Personal wordt uitgevoerd als een** |Service |Toepassing |
| **Vernieuwen plannen** |Als uw computer aanstaat en de gatewayservice wordt uitgevoerd, hoeft u niet aangemeld te zijn op het moment van de geplande vernieuwing. |U moet op uw computer zijn aangemeld op het moment van de geplande vernieuwing. |
| **Wachtwoord van het Windows-account wijzigen** |U moet uw wachtwoord wijzigen in de gatewayservice. Als het accountwachtwoord dat wordt gebruikt door de gateway niet meer geldig is, mislukt het vernieuwen. |De gateway wordt altijd uitgevoerd met het account en wachtwoord waarmee u momenteel bent aangemeld. Als u niet bent aangemeld bij Windows, wordt de gateway niet uitgevoerd en mislukt het vernieuwen. |

### <a name="configure-the-gateway"></a>De gateway configureren
Wanneer de installatiewizard is voltooid, wordt u gevraagd om de configuratiewizard te starten. Het configureren van een gateway is niet heel ingewikkeld. U dient zich aan te melden bij Power BI vanuit de wizard. Dit is nodig om de wizard verbinding te laten maken met uw Power BI-account in de Power BI-service.

Als u bent aangemeld bij Windows met een account met beheerdersmachtigingen, wordt u gevraagd de referenties van uw Windows-account in te voeren. U kunt een ander Windows-account opgeven, maar houd er rekening mee dat de machtigingen bepalen hoe de gateway wordt uitgevoerd. De gateway-service wordt uitgevoerd met dit account.

### <a name="sign-in-to-data-sources"></a>Aanmelden bij gegevensbronnen
Zodra de configuratiewizard is voltooid en uw gateway actief is, dient u voor iedere gegevensbron van uw gegevensset een verificatietype en uw referenties op te geven. Dit doet u in Power BI.

![](media/personal-gateway/pg_dataset_settings_signin.png)

U hoeft voor iedere gegevensbron slechts één keer een verificatietype en referenties op te geven. U dient zich aan te melden in het deelvenster **Gegevensbronnen beheren**, in het venster Instellingen voor een gegevensset. Als u meerdere gegevensbronnen hebt, dient u zich bij elke bron aan te melden. De gateway bepaalt een standaardtype voor verificatie, afhankelijk van de gegevensbron. In de meeste gevallen is dit een Windows-verificatie. In sommige gevallen is kan uw gegevensbron echter een ander verificatietype vereisen. Als u niet zeker weet welk type vereist is, neemt u contact op met uw gegevensbronbeheerder.

## <a name="up-and-running"></a>Alles werkt!
Wanneer uw gateway eenmaal werkt, kunt u op VERNIEUWEN PLANNEN klikken voor een gegevensset, om de pagina Instellingen voor uw gegevensset weer te geven.

![](media/personal-gateway/pg_awintsales_settings.png)

Deze pagina toont:

1. Vernieuwingsstatus: geeft weer of vernieuwen is geslaagd en wanneer de volgende geplande vernieuwing is.
2. **Gateway**: geeft weer of er een gateway geïnstalleerd en online is. Als een gateway geïnstalleerd is maar niet online is, worden de instellingen Gegevensbronnen beheren en Vernieuwen plannen uitgeschakeld.
3. **Gegevensbronnen beheren**: toont de gegevensbronnen waarmee de gegevensset verbinding maakt. U kunt zich aanmelden of het verificatietype wijzigen. U hoeft zich voor elke gegevensbron maar een keer aan te melden.
4. **Vernieuwen plannen**: hiermee kunt u schema-instellingen voor vernieuwen configureren. Als de gateway niet online is, worden deze instellingen uitgeschakeld.
5. Meldingen over mislukte vernieuwingen: deze optie is standaard ingeschakeld en stuurt u een e-mailmelding als een geplande vernieuwing mislukt.

## <a name="updating-your-windows-account-password"></a>Wachtwoord van uw Windows-account bijwerken
Als u tijdens het installeren van de gateway op uw computer was aangemeld met een Windows-account met beheerdersmachtigingen, wordt de gateway uitgevoerd als een service onder het Windows-account dat u hebt opgegeven in de configuratiewizard. Dit is meestal hetzelfde Windows-account als waarmee u zich bij uw computer aanmeldt. Wanneer u het wachtwoord van uw Windows-account wijzigt, dient u dit ook te wijzigen in de gateway, anders kan de service wellicht niet worden uitgevoerd en mislukt het vernieuwen. Als u het wachtwoord van uw Windows-account voor de gateway wilt wijzigen, selecteert u het pictogram van de persoonlijke gateway op de taakbalk van uw Windows-bureaublad of in Apps.

![](media/personal-gateway/pg_programicon.png)

Hier kunt u vervolgens uw wachtwoord bijwerken en de verbindingsstatus van uw gateway controleren.

![](media/personal-gateway/pg_credentials.png)

## <a name="ports"></a>Poorten
De gateway communiceert via uitgaande poorten: TCP 443 (standaard), 5671, 5672, 9350 t/m 9354.  De gateway vereist geen inkomende poorten.

| Domeinnamen | Uitgaande poorten | Beschrijving |
| --- | --- | --- |
| *.powerbi.com |443 |HTTPS |
| *.analysis.windows.net |443 |HTTPS |
| *.login.windows.net |443 |HTTPS |
| *.servicebus.windows.net |5671-5672 |Advanced Message Queuing Protocol (AMQP) |
| *.servicebus.windows.net |443, 9350-9354 |Listeners op Service Bus Relay via TCP (vereist 443 voor het ophalen van tokens voor toegangsbeheer) |
| *.frontend.clouddatahub.net |443 |HTTPS |
| *.core.windows.net |443 |HTTPS |
| login.microsoftonline.com |443 |HTTPS |
| login.windows.net |443 |HTTPS |

Als u IP-adressen in plaats van domeinen wilt goedkeuren, kunt u de lijst met IP-adresbereiken voor Microsoft Azure Datacenters downloaden en deze gebruiken. [Downloaden](https://www.microsoft.com/download/details.aspx?id=41653)

## <a name="next-steps"></a>Volgende stappen
[On-premises gegevensgateway (persoonlijke modus) - de nieuwe versie van de persoonlijke gateway](service-gateway-personal-mode.md)
[Proxy-instellingen voor de Power BI-gateways configureren](service-gateway-proxy.md)  
[Power BI Premium](service-premium.md)

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

