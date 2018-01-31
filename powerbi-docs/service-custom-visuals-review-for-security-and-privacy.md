---
title: De beveiliging en privacy van aangepaste visuele elementen controleren
description: Voordat u een aangepast visueel element inschakelt, moet u controleren of de beveiliging en privacy van dat visuele element voldoen aan de normen van uw organisatie.
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
ms.date: 09/05/2017
ms.author: maghan
ms.openlocfilehash: 15f8d9090736a62fdaa53aa3f19e7e0fff127337
ms.sourcegitcommit: 6e693f9caf98385a2c45890cd0fbf2403f0dbb8a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2018
---
# <a name="review-custom-visuals-for-security-and-privacy"></a>De beveiliging en privacy van aangepaste visuele elementen controleren
Voordat u een aangepast visueel element inschakelt, moet u controleren of de beveiliging en privacy van dat visuele element voldoen aan de normen van uw organisatie.

## <a name="enable-a-custom-visual"></a>Een aangepast visueel element inschakelen
<a name="enable"></a>Een aangepast visueel element in het rapport is uitgeschakeld totdat u **Aangepaste visuele elementen inschakelen** kiest, zoals hieronder wordt weergegeven.  

![](media/service-custom-visuals-review-for-security-and-privacy/emptyvisual.png)

## <a name="considerations-before-you-enable-a-custom-visual"></a>Overwegingen voor het inschakelen van een aangepast visueel element
<a name="considerations"></a>

> [!WARNING]
> Aangepaste visuele elementen bevatten mogelijk code die een beveiligings- of privacyrisico kan vormen. Daarom worden aangepaste visuele elementen in het rapport uitgeschakeld totdat u ervoor kiest deze in te schakelen. Hier volgen enkele overwegingen om te bepalen of u een aangepast visueel element wilt inschakelen:
> 
> 

1. Ga na of de aangepaste visuele elementen in het rapport afkomstig zijn van een vertrouwde auteur en bron
2. Als u twijfelt wat u moet doen, neemt u contact met uw IT-team om af te wegen of u aangepaste visuele elementen voor het rapport moet inschakelen.
3. Voel u niet verplicht om het aangepaste visuele element in te schakelen als iemand een rapport met een aangepast visueel element met u deelt, ook al is diegene een collega. Denk rustig na of het essentieel is voor de betreffende taak. U kunt ook altijd vragen om een rapport zonder aangepaste visuele elementen als u het aangepaste visuele element niet vertrouwt.

## <a name="security-best-practices-for-it-professionals-to-enable-a-custom-visual"></a>Aanbevolen beveiligingsprocedures voor IT-professionals met betrekking tot het inschakelen van een aangepast visueel element
<a name="security"></a>

> [!WARNING]
> Aangepaste visuele elementen bevatten mogelijk code die een beveiligings- of privacyrisico kan vormen. Daarom worden aangepaste visuele elementen in het rapport uitgeschakeld totdat u ervoor kiest deze in te schakelen. Er zijn enkele aanbevolen procedures die u kunt volgen om de beveiliging en privacy van een aangepast visueel element te controleren.
> 
> 

1. Implementeer een controleproces voor aangepaste visuele elementen binnen de organisatie. Gecontroleerde aangepaste visuele elementen worden gedeeld met interne gebruikers via een interne website, zoals een SharePoint-documentbibliotheek of een OneNote-document.
2. Stel richtlijnen voor zakelijke gebruikers op over het juiste gebruik van aangepaste visuele elementen en maak een e-mailgroep waarin men vragen over beveiliging en privacy kan stellen.
3. Evalueer de JavaScript-code in het PBIVIZ-bestand van het visuele element.

**De JavaScript-code in een aangepast visueel element evalueren**

In een aangepast visueel element wordt JavaScript gebruikt. Dit kan een beveiligings- of privacyrisico vormen. Als u een aangepast visueel element of een PBIX-bestand met een aangepast visueel element van een onbekende bron ontvangt, kunt u de JavaScript-code evalueren om te zien of deze veilig is.

Extraheer de code van het aangepaste visuele element om de JavaScript-code ervan te evalueren. Ga als volgt te werk om de code te extraheren:  

1. Sla het PBIVIZ-bestand op in een map.
2. Wijzig de naam van het bestand in een zipbestand.
3. Pak het zipbestand uit in een lokale map.

## <a name="custom-visual-file-contents"></a>Inhoud van het bestand van het aangepaste visuele element
Een PBIVIZ-bestand bevat de volgende inhoud:

| **Bestand** | **Beschrijving** |
|:--- |:--- |
| ./package.json |Een manifestbestand waarin wordt aangegeven welke bestanden moeten worden geladen voor het aangepaste visuele element. |
| ./resources |Bevat de CSS-, TypeScript- en JavaScript-bestanden voor het aangepaste visuele element. |
| ./resources/&lt;naam&gt; |&lt;naam&gt; is de naam van het aangepaste visuele element. |
| ./resources/&lt;naam&gt;.css |Het CSS-bronbestand voor het aangepaste visuele element. |
| ./resources/&lt;naam&gt;.js |De code die wordt uitgevoerd wanneer een gebruiker op Aangepaste visuele elementen inschakelen klikt of een aangepast visueel element importeert. Waarschuwing: JavaScript-code kan een beveiligings- of privacyrisico vormen. |
| ./resources/&lt;naam&gt;.ts |De JavaScript-broncode voor het visuele element in TypeScript-indeling. Waarschuwing: JavaScript- of TypeScript-code kan een beveiligings- of privacyrisico vormen. |
| ./resources/&lt;naam&gt;.png |Het pictogram voor het visuele element dat wordt weergegeven voor de gebruiker. |

Nadat u het PBIVIZ-bestand hebt uitgepakt, kunt u de code evalueren. Hier volgen enkele aanbevolen procedures en mogelijke bedreigingen waarop u moet letten.

## <a name="best-practices-to-evaluate-the-javascript-or-typescript-code"></a>Aanbevolen procedures voor het evalueren van de JavaScript- of TypeScript-code
**JavaScript**- of **TypeScript**-code kan een beveiligings- of privacyrisico vormen. Hier volgen enkele aanbevolen procedures en mogelijke bedreigingen waarop u moet letten.

### <a name="best-practices-to-evaluate-javascript-code"></a>Aanbevolen procedures voor het evalueren van JavaScript-code
* Controleer altijd de inhoud van het JS-bestand. Dit is de code die daadwerkelijk wordt uitgevoerd. Mogelijk kan de inhoud van het TS-bestand niet worden gecompileerd naar het JS-bestand dat in het aangepaste visuele element is opgenomen.
* Controleer altijd de inhoud van het TS-bestand. U kunt het TS-bestand laden in de **ontwikkelhulpprogramma's**, het visuele element exporteren en het resulterende JS-bestand in het zojuist gemaakte PBIVIZ--bestand vergelijken met het oorspronkelijke JS-bestand in het visuele element
* Controleer of het pictogram voor het aangepaste visuele element niet te veel lijkt op dat van andere visuele elementen waarmee de gebruiker bekend is.
* Evalueer het visuele element altijd in een testaccount met minimale bevoegdheden zonder toegang tot gevoelige gegevens. Idealiter is de testaccount een lokaal account met alleen aanmeldingsgegevens voor Power BI.

### <a name="threats-to-look-for-in-javascript-code"></a>Mogelijke bedreigingen in JavaScript-code
* Controleer de netwerkactiviteit wanneer het visuele element wordt uitgevoerd in de bewerkingsmodus of de weergavemodus. Zorg ervoor dat u tevreden bent met de aanvragen die worden uitgevoerd. Als het goed is worden er geen bronnen buiten het domein van Power BI aangeroepen, tenzij de auteur van het visuele element dit van tevoren heeft gecommuniceerd.
* Alle uitgaande gegevens buiten het domein van Power BI moeten voldoen aan het door u verwachte 'normale' gebruik. Als via het visuele element bijvoorbeeld een videospeler met een IFrame wordt geïmplementeerd om een video van een andere website af te spelen, moet bepaalde informatie in de IFrame-aanvragen worden verzonden om de video correct te kunnen weergeven. Als u ziet dat de hele gegevensset wordt verzonden, wilt u wellicht nader onderzoeken of dit wel vereist en gewenst is.
* Controleer of er persoonsgegevens worden verzonden of opgeslagen door het aangepaste visuele element.
* Controleer of het aangepaste visuele element probeert toegang te krijgen tot bronnen van de lokale machine, zoals cookies, of probeert bestanden naar de schijf te schrijven.
* Controleer of het aangepaste visuele element code bevat die verborgen lijkt te zijn of geen duidelijk doel heeft.
* Sla een kopie op van elk visuele element dat u hebt bekeken.
* Als u een update van een eerder bekeken visueel element evalueert, moet u het controleren op wijzigingen. Evalueer updates van een visueel element net zo kritisch als het oorspronkelijke visuele element
* Neem contact met ons op als u iets aantreft wat u verdacht of onduidelijk vindt. We helpen u graag.

## <a name="next-steps"></a>Volgende stappen
[Visualisaties in Power BI](power-bi-report-visualizations.md)  
[Aangepaste visualisaties in Power BI](power-bi-custom-visuals.md)  
[Aangepaste visuele elementen publiceren naar de Office Store](developer/office-store.md)  
[Aan de slag met ontwikkelhulpprogramma's voor aangepaste visuele elementen](service-custom-visuals-getting-started-with-developer-tools.md)  
[Een aangepast visueel element laten certificeren](power-bi-custom-visuals-certified.md)    
[Video: Aangepaste visualisaties voor Power BI maken met Sachin Patney en Nico Cristache](https://www.youtube.com/watch?v=kULc2VbwjCc)  

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

