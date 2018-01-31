---
title: Power BI-machtigingen
description: Power BI-machtigingen
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
ms.openlocfilehash: 61c910731be4ca80cc13784d623720431cd511e7
ms.sourcegitcommit: 6e693f9caf98385a2c45890cd0fbf2403f0dbb8a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2018
---
# <a name="power-bi-permissions"></a>Power BI-machtigingen
## <a name="permission-scopes"></a>Machtigingsbereiken
Power BI-machtigingen geven een toepassing de mogelijkheid om bepaalde acties namens een gebruiker uit te voeren. Machtigingen zijn pas geldig als deze door een gebruiker zijn goedgekeurd.

| Weergavenaam | Beschrijving | Bereikwaarde |
| --- | --- | --- |
| Alle gegevenssets weergeven |De app kan alle gegevenssets voor de aangemelde gebruiker en gegevenssets waartoe de gebruiker toegang heeft, weergeven. |Dataset.Read.All |
| Alle gegevenssets lezen en schrijven |De app kan alle gegevenssets voor de aangemelde gebruiker en gegevenssets waartoe de gebruiker toegang heeft, weergeven en er naar schrijven. |Dataset.ReadWrite.All |
| Gegevens toevoegen aan de gegevensset van een gebruiker (preview) |Geeft een app toegang tot het toevoegen of verwijderen van gegevenssetrijen van een gebruiker. Deze machtiging verleent de app geen toegang tot de gegevens van de gebruiker. |Data.Alter_Any |
| Inhoud maken (preview) |De app kan automatisch inhoud en gegevenssets maken voor een gebruiker. |Content.Create |
| Groepen van de gebruiker weergeven |De app kan alle groepen weergeven waartoe de aangemelde gebruiker behoort. |Group.Read |
| Alle groepen weergeven |De app kan alle groepen weergeven waartoe de aangemelde gebruiker behoort. |Group.Read.All |
| Alle dashboards weergeven (preview) |De app kan alle dashboards voor de aangemelde gebruiker en dashboards waartoe de gebruiker toegang heeft, weergeven. |Dashboard.Read.All |
| Alle rapporten weergeven (preview) |De app kan alle rapporten voor de aangemelde gebruiker en rapporten waartoe de gebruiker toegang heeft, weergeven. De app kan ook de gegevens binnen de rapporten bekijken, evenals de structuur. |Report.Read.All |
| Alle rapporten lezen en schrijven |De app kan alle rapporten voor de aangemelde gebruiker en rapporten waartoe de gebruiker toegang heeft, weergeven en er naar schrijven. Hiermee wordt niet het recht verleend om een nieuw rapport te maken. |Report.ReadWrite.All |

Een toepassing kan machtigingen aanvragen wanneer deze voor de eerste keer probeert om aan te melden bij een gebruikerspagina door de aangevraagde machtigingen door te geven in de bereikparameter van de aanroep. Als de machtigingen worden verleend, wordt een toegangstoken geretourneerd naar de app, die in toekomstige API-aanroepen kan worden gebruikt. De toegang kan alleen worden gebruikt door een specifieke toepassing.

> [!NOTE]
> In de Power BI-API's worden app-werkruimten nog steeds groepen genoemd. Als er wordt verwezen naar groepen, werkt u in feite met app-werkruimten.
> 
> 

## <a name="requesting-permissions"></a>Machtigingen aanvragen
U kunt de API aanroepen voor verificatie met een gebruikersnaam en wachtwoord, maar om acties te ondernemen namens een andere gebruiker, moeten machtigingen worden aangevraagd die de gebruiker vervolgens goedkeurt. Daarna wordt het resulterende toegangstoken verzonden in alle toekomstige aanroepen. Voor dit proces wordt het [OAuth 2.0](http://oauth.net/2/)-standaardprotocol gebruikt. De daadwerkelijke implementatie verschilt mogelijk, maar de OAuth-stroom voor Power BI bevat de volgende elementen:

* **Aanmeldings-UI**: dit is de UI die de ontwikkelaar kan aanroepen om machtigingen aan te vragen. De gebruiker moet hiervoor aangemeld zijn als dit nog niet het geval is. De gebruiker moet ook de machtigingen goedkeuren die de toepassing aanvraagt. In het aanmeldingsvenster wordt een toegangscode of een foutbericht naar een omleidings-URL die wordt opgegeven.
  * Een standaardomleidings-URL moet worden verstrekt door Power BI voor gebruik door systeemeigen toepassingen.
* **Autorisatiecode**: autorisatiecodes worden na aanmelding geretourneerd aan webtoepassingen via URL-parameters in de omleidings-URL. Omdat deze zich in parameters bevinden, is er een beveiligingsrisico. Webtoepassingen moeten de autorisatiecode uitwisselen voor een autorisatietoken
* **Autorisatietoken**: worden gebruikt om API-aanroepen te verifiëren namens een andere gebruiker. Het bereik ervan wordt beperkt tot een specifieke toepassing. Tokens hebben een ingestelde levensduur en als ze verlopen, moeten ze worden vernieuwd.
* **Vernieuwingstoken**: wanneer tokens verlopen, wordt een proces in gang gezet om deze te vernieuwen.

Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

