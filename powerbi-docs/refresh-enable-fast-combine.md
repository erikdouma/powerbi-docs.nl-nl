---
title: Privacyinstellingen uitschakelen
description: Snel combineren in Personal Gateway inschakelen om privacyinstellingen voor het vernieuwen uit te schakelen.
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
ms.date: 02/06/2018
ms.author: davidi
ms.openlocfilehash: 5d754dbdd5d52e7a5b123755015e656d9fb2cea2
ms.sourcegitcommit: db37f5cef31808e7882bbb1e9157adb973c2cdbc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/09/2018
---
# <a name="disable-privacy-setting-in-power-bi-gateway---personal"></a>Privacyinstelling in Power BI Gateway - Personal uitschakelen
> [!NOTE]
> Er is een nieuwe versie van de persoonlijke gateway voor Power BI: de **on-premises gegevensgateway (persoonlijke modus)**. Het volgende artikel beschrijft de vorige versie van de persoonlijke gateway, genaamd **Power BI Gateway - Personal**. Deze wordt op 31 juli 2017 buiten gebruik gesteld, waarna deze niet meer zal werken. Zie het artikel [**On-premises gegevensgateway (persoonlijke modus)**](service-gateway-personal-mode.md) voor meer informatie over de nieuwe versie van de persoonlijke gateway, inclusief de installatie-instructies. Snel combineren is ook beschikbaar in de nieuwe versie van de persoonlijke gateway en wordt ook in dat artikel beschreven.
> 
> 

Mogelijk wordt er een foutbericht weergegeven op basis van de privacyinstellingen voor uw gegevensbronnen wanneer u deze gebruikt in combinatie met de persoonlijke gateway.

> *Er is een fout opgetreden tijdens het verwerken van de gegevens in de gegevensset.*
> 
> *[Kan gegevens niet combineren] &lt;queryonderdeel&gt;/&lt;...&gt;/&lt;...&gt; wil toegang tot gegevensbronnen met privacyniveaus die niet samen kunnen worden gebruikt. Bouw deze gegevenscombinatie opnieuw.*
> 
> 

U kunt deze fout omzeilen door **Snel combineren** in te schakelen. Als **Snel combineren** is ingeschakeld, worden de privacy-instellingen genegeerd zodat de verschillende gegevensbronnen kunnen worden gecombineerd.

> [!NOTE]
> Bij het combineren van de gegevens wordt dan geen rekening gehouden met privacyniveaus. Hierdoor kunnen gevoelige of vertrouwelijke gegevens beschikbaar worden gemaakt voor een andere gegevensbron bij het combineren van gegevens.
> 
> 

## <a name="what-is-fast-combine"></a>Wat is Snel combineren?
Zie [Privacyniveaus](https://support.office.com/article/Privacy-levels-Power-Query-CC3EDE4D-359E-4B28-BC72-9BEE7900B540) voor meer informatie over privacyniveaus en Snel combineren. Standaard wordt het privacyniveau ingesteld op Privé, hetgeen kan resulteren in de hierboven beschreven fout. De instelling Privé zorgt ervoor dat de gegevensbron wordt gescheiden van andere bronnen. In bepaalde gevallen kan dit een probleem zijn, bijvoorbeeld bij een query met parameters waarmee invoer wordt opgehaald uit een andere gegevensbron.

Door Snel combineren in te schakelen wordt de instelling Privé genegeerd en kan de query worden uitgevoerd.

## <a name="turn-on-fast-combine"></a>Snel combineren inschakelen
Gebruik de volgende stappen om Snel combineren in te schakelen voor uw persoonlijke gateway. Deze instelling is niet beschikbaar in de on-premises gegevensgateway.

1. Open **ConnectorConfig.xml**.  Dit bestand kan zich op twee locaties op uw computer bevinden.  Als u een beheerder bent, vindt u het op deze locatie.
   
    <pre><code>C:\Program Files\Power BI Personal Gateway\1.0\Configurator\Connector</code></pre>
   
    Als u geen beheerder bent, vindt u het op deze locatie.
   
    <pre><code>C:\Users\[username]\AppData\Local\Power BI Personal Gateway\1.0\Configurator\Connector</code></pre>
    
2. Voeg het element **&lt;EnableFastCombine&gt;** toe aan het configuratiebestand, met de waarde true. Door dit element toe te voegen, wordt **Snel combineren** ingeschakeld.
   
   <pre><code>&lt;EnableFastCombine&gt;true&lt;/EnableFastCombine&gt;</code></pre>
   
   ![](media/refresh-enable-fast-combine/configfile.png)
3. Sluit het configuratiescherm voor de gateway en start de gateway opnieuw op.
4. U ziet een status die aangeeft dat Snel combineren is ingeschakeld.
   
   ![](media/refresh-enable-fast-combine/fastcombineenabled.png)

## <a name="turn-off-fast-combine"></a>Snel combineren uitschakelen
1. Open **ConnectorConfig.xml**.  Dit bestand kan zich op twee locaties op uw computer bevinden.  Als u een beheerder bent, vindt u het op deze locatie.
   
    <pre><code>C:\Program Files\Power BI Personal Gateway\1.0\Configurator\Connector</code></pre>
   
    Als u geen beheerder bent, vindt u het op deze locatie.
   
    <pre><code>C:\Users\[username]\AppData\Local\Power BI Personal Gateway\1.0\Configurator\Connector</code></pre>

2. Verwijder het element **&lt;EnableFastCombine&gt;** uit het configuratiebestand. Door dit element te verwijderen, wordt **Snel combineren** uitgeschakeld.
3. Sluit het configuratiescherm voor de gateway en start de gateway opnieuw op.
4. U ziet niet langer een status die aangeeft dat **Snel combineren** is ingeschakeld.

## <a name="next-steps"></a>Volgende stappen
[On-premises gegevensgateway (persoonlijke modus): de nieuwe versie van de persoonlijke gateway](service-gateway-personal-mode.md)
[Privacyniveaus](https://support.office.com/article/Privacy-levels-Power-Query-CC3EDE4D-359E-4B28-BC72-9BEE7900B540)  
[Algemene querytaken in Power BI Desktop](desktop-common-query-tasks.md)  
Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

