---
title: 'Fout: '
corporate: 
ssl: 
certificate: 
is: 
untrusted": 
'-': 
power: 
bi": 
description: Tijdens het aanmelden bij de Android-app voor Power BI ziet u mogelijk u het bericht, 'Kan niet worden geverifieerd omdat uw zakelijke SSL-certificaat niet vertrouwd is
.": 
services: powerbi
documentationcenter: 
author: maggiesMSFT
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
ms.date: 10/13/2017
ms.author: maggies
ms.openlocfilehash: 4ef29c0cab96e21045f30805d7445aa34d37697a
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2017
---
# <a name="error-corporate-ssl-certificate-is-untrusted---power-bi"></a>Fout: ‘Zakelijk SSL-certificaat is niet vertrouwd’ - Power BI
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
* Vragen? [Misschien dat de Power Bi-community het antwoord weet](http://community.powerbi.com/)

