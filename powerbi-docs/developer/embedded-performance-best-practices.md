---
title: Aanbevolen procedures voor de prestaties van Power BI Embedded
description: Dit artikel bevat richtlijnen voor aanbevolen procedures voor ingesloten analyses
author: markingmyname
ms.author: maghan
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-embedded
ms.topic: conceptual
ms.date: 12/12/2018
ms.openlocfilehash: e28801a15cf50351d737af63bc48f655ca85d28f
ms.sourcegitcommit: 750f0bfab02af24c8c72e6e9bbdd876e4a7399de
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/04/2019
ms.locfileid: "54008161"
---
# <a name="power-bi-embedded-performance-best-practices"></a>Aanbevolen procedures voor de prestaties van Power BI Embedded

Dit artikel bevat aanbevelingen voor het sneller weergeven van rapporten, dashboards en tegels in uw toepassing

## <a name="embed-parameters"></a>Ingesloten parameters

Met de methode Powerbi.embed() worden enkele parameters ontvangen voor het insluiten van een rapport, dashboard of tegel. Deze parameters hebben gevolgen voor de prestaties.

### <a name="embed-url"></a>Insluitings-URL

Genereer de insluitings-URL niet zelf. Haal in plaats daarvan de insluitings-URL op door de API [Rapporten ophalen](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Frest%2Fapi%2Fpower-bi%2Freports%2Fgetreportsingroup&data=02%7C01%7CMark.Ghanayem%40microsoft.com%7C07ca68ceb37a48e3f3de08d64968707a%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636777110256168308&sdata=22lkqRM2w1MQfrM8dooedaPqqIU8PufTq9TT4VDzRo0%3D&reserved=0), [Dashboards ophalen](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Frest%2Fapi%2Fpower-bi%2Fdashboards%2Fgetdashboardsingroup&data=02%7C01%7CMark.Ghanayem%40microsoft.com%7C07ca68ceb37a48e3f3de08d64968707a%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636777110256168308&sdata=nfWRgbSoXVF42Rg%2Ba9491u19uksXp%2FAyz%2Fa%2Ba7%2FCtdA%3D&reserved=0) of [Tegels ophalen](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Frest%2Fapi%2Fpower-bi%2Fdashboards%2Fgettilesingroup&data=02%7C01%7CMark.Ghanayem%40microsoft.com%7C07ca68ceb37a48e3f3de08d64968707a%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636777110256178318&sdata=LgZ27TynNpqQJDrb3aHWGQXIS%2FzichAO9De5M2uhF1Q%3D&reserved=0) aan te roepen. Er is een nieuwe parameter toegevoegd aan de URL **_config_**; deze wordt gebruikt voor prestatieverbeteringen.

### <a name="permissions"></a>Machtigingen

Bied machtigingen voor **weergave** aan als u niet van plan bent om een rapport in te sluiten in de **bewerkingsmodus**. Op deze manier worden met invoegcode geen onderdelen geïnitialiseerd die normaal in de bewerkingsmodus worden gebruikt.

### <a name="filters-bookmarks-and-slicers"></a>Filters, bladwijzers en slicers

Meestal worden rapportvisuals opgeslagen met gegevens in cache. De gegevens in cache worden gebruikt om te rapporteren over de prestaties. In rapporten worden de gegevens in cache weergegeven na het uitvoeren van query's. Als er filters, bladwijzers of slicers zijn opgegeven, zijn de gegevens in cache niet relevant. De visuals worden dan pas weergegeven nadat de visualquery is uitgevoerd.

Als u rapporten met dezelfde filters insluit, slaat u het rapport met toegepaste filters op om te voorkomen dat er een lijst filters wordt doorgegeven in de laadconfiguratie.

## <a name="preload"></a>Vooraf laden

Gebruik de JavaScript-API voor *vooraf laden* om de prestaties voor eindgebruikers te verbeteren.
Met Powerbi.preload() worden JavaScript-bestanden, CSS_bestanden en andere artefacten gedownload. Deze worden later gebruikt voor insluiting in rapporten.

Laad de aanroep vooraf als u het rapport niet direct gaat insluiten. Als u bijvoorbeeld een rapport insluit door op één knop te klikken, kunt u de aanroep het beste vooraf laden bij het laden van de voorgaande pagina. Wanneer de toepassingsgebruiker dan op de knop klikt, wordt het rapport sneller weergegeven.

## <a name="measure-performance"></a>Prestaties meten

Als u de prestaties wilt meten, gebruikt u:

1. Geladen: tijd totdat rapport is geïnitialiseerd (de gebruiker ziet geen laadpictogram).
2. Weergegeven: tijd totdat het volledige rapport wordt weergegeven met de werkelijke gegevens. De weergavegebeurtenis wordt steeds opnieuw geactiveerd wanneer het rapport wordt vernieuwd (d.w.z. na het toepassen van filters). Als u een rapport eerst wilt meten, voert u de berekeningen uit tijdens de eerste gebeurtenis.

De gegevens in cache worden waar beschikbaar weergegeven, maar er is nog geen gebeurtenis voor deze gegevens.

## <a name="update-tools-and-sdk-packages"></a>Hulpprogramma's voor bijwerken en SDK-pakketten

Hiermee houdt u hulpprogramma's en SDK-pakketten bijgewerkt.

* Gebruik altijd de nieuwste versie van [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).

* Installeer de nieuwste versie van de [Power BI-client-SDK](https://github.com/Microsoft/PowerBI-JavaScript). Er worden doorlopend nieuwe verbeteringen geïntroduceerd. Verdiep u er van tijd tot tijd in.

* Pakketten die moeten worden geïnstalleerd:
    * NPM-pakket: Power BI-client
    * NuGet-pakket: Microsoft.PowerBI.JavaScript

> [!Note]
> De laadtijd is voornamelijk afhankelijk van zaken die relevant zijn voor het rapport en de gegevens zelf. De laadtijd wordt bijvoorbeeld beïnvloed door het aantal visuals, de grootte van de gegevens en de complexiteit van de query's en metingen die moeten worden uitgevoerd. Volg de [aanbevolen procedures](../power-bi-reports-performance.md) voor het verbeteren van de laadtijd van het rapport.

## <a name="next-steps"></a>Volgende stappen

* [Aanbevolen procedures voor de prestaties van Power BI-rapporten](../power-bi-reports-performance.md)
* [Problemen met Power BI Embedded oplossen](embedded-troubleshoot.md)
* [Veelgestelde vragen over Power BI Embedded](embedded-faq.md)
