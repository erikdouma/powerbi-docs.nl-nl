---
title: De fout 'Zakelijk SSL-certificaat is niet vertrouwd' herstellen
description: Tijdens het aanmelden bij de Android-app voor Power BI ziet u mogelijk u het bericht, 'Kan niet worden geverifieerd omdat uw zakelijke SSL-certificaat niet vertrouwd is
.": ''
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-mobile
ms.topic: conceptual
ms.date: 05/18/2018
ms.author: maggies
ms.openlocfilehash: 494e148a62675aab1a6e799c4e4b61f022483d9f
ms.sourcegitcommit: 2a7bbb1fa24a49d2278a90cb0c4be543d7267bda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/26/2018
ms.locfileid: "34444952"
---
# <a name="fixing-corporate-ssl-certificate-is-untrusted---power-bi"></a>De fout 'Zakelijk SSL-certificaat is niet vertrouwd' herstellen - Power BI
Tijdens het aanmelden bij de mobiele Android-app voor Microsoft Power BI ziet u mogelijk u het bericht, 'Kan niet worden geverifieerd omdat uw zakelijke SSL-certificaat niet vertrouwd is door dit apparaat. Neem contact op met de IT-beheerder van uw bedrijf.’ 

Wat u moet doen is meestal afhankelijk van het besturingssysteem op uw Android-apparaat, maar er zijn een aantal andere problemen waardoor deze fout kan optreden.

## <a name="on-android-7-or-later"></a>Op Android 7 of hoger
Zoek een update voor een app met de naam **Chrome** en installeer de update.

## <a name="on-android-6-and-earlier"></a>Op Android 6 en eerdere versies
Uw apparaat moet mogelijk een bijgewerkte versie van System Webview hebben. Deze kan worden geïnstalleerd op uw apparaat en u hoeft mogelijk slechts op **Updaten** te klikken.

Ga als volgt te werk als System Webview niet is geïnstalleerd op uw apparaat:

1. Sluit Power BI op uw Android-apparaat.
2. Open de Google Play Store en zoek naar **System Webview** door Google Inc.
3. Installeren de app.
4. Start de Power BI-app en meld u aan.

## <a name="time-zone-settings"></a>Tijdzone-instellingen
De tijdzone-instellingen op het apparaat zijn mogelijk onjuist. 

Ga naar **Instellingen** > **Systeem** > **Datum en tijd** en controleer of ze.

## <a name="custom-authentication-server"></a>Aangepaste verificatieserver
Als u een aangepaste verificatieserver gebruikt, wordt het SSL-certificaat in de zakelijke verificatieserver mogelijk ongeldig. Neem contact op met de IT-beheerder van uw organisatie en vraag hem om u te helpen.

## <a name="next-steps"></a>Volgende stappen
* [De Android-app downloaden](http://go.microsoft.com/fwlink/?LinkID=544867) vanuit de Android-app-store.
* Vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

