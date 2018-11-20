---
title: Comparing Power BI Report Server and the Power BI service (Power BI Report Server vergelijken met de Power BI-service)
description: In dit artikel worden de functies van Power BI Report Server en de Power BI-service vergeleken.
keywords: ''
author: maggiesMSFT
ms.author: maggies
ms.date: 11/06/2018
ms.topic: overview
ms.service: powerbi
ms.component: powerbi-report-server
manager: kfile
ms.custom: mvc
ms.openlocfilehash: a693eef85f7eafe7cfac2a02cbccc346201a6f13
ms.sourcegitcommit: a1b7ca499f4ca7e90421511e9dfa61a33333de35
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/10/2018
ms.locfileid: "51507687"
---
# <a name="comparing-power-bi-report-server-and-the-power-bi-service"></a>Comparing Power BI Report Server and the Power BI service (Power BI Report Server vergelijken met de Power BI-service)

Power BI Report Server en de Power BI-service hebben veel overeenkomsten en een paar belangrijke verschillen. In deze tabel worden de overeenkomsten en verschillen uitgelegd.

## <a name="features-of-power-bi-report-server-and-the-power-bi-service"></a>Functies van Power BI Report Server en de Power BI-service

| Functies | Power BI Report Server | Power BI-service | Opmerkingen
|---------|---------|---------|---------|
| Implementatie | On-premises of gehoste cloud | Cloud | Power BI Report Server kan worden geïmplementeerd in Azure VM’s (gehoste cloud) indien gelicentieerd via Power BI Premium
| Brongegevens | Cloud en/of on-premises | Cloud en/of on-premises |  
| Licentie | Power BI Premium of SQL Server EE met SA | Power BI Pro en/of Power BI Premium |  
| Levenscyclus | Beleid voor moderne levenscyclus | Volledig beheerde service |  
| Releasecyclus | Elke 4 maanden | Eén keer per maand | Nieuwste functies en oplossingen worden het eerst uitgebracht in de Power BI-service. De meeste kernfuncties worden in de volgende paar releases doorgevoerd in Power BI Report Server. Sommige functies zijn alleen bedoeld voor de Power BI-service.
| Power BI-rapporten maken in Power BI Desktop | Ja | Ja |  
| Power BI-rapporten maken in de browser | Nee | Ja |  
| Gateway vereist | Nee | Ja voor on-premises gegevensbronnen |  
| Realtime streaming | Nee | Ja | [Realtimestreaming in Power BI](../service-real-time-streaming.md)
| Dashboards | Nee | Ja | [Dashboards in de Power BI-service](../consumer/end-user-dashboards.md) 
| Distributiegroep met rapporten die apps gebruiken | Nee | Ja | [Apps maken en publiceren met dashboards en rapporten](../service-create-distribute-apps.md) 
| Inhoudspakketten | Nee | Ja | [Organisatie-inhoudspakketten: inleiding](../service-organizational-content-pack-introduction.md) 
| Verbinding maken met services zoals Salesforce | Nee | Ja | [Verbinding maken met de services die u gebruikt](../consumer/end-user-connect-to-services.md) met de Power BI-service
| Q&A | Nee | Ja | [Q&A in de Power BI-service en Power BI Desktop](../consumer/end-user-q-and-a.md) 
| Snelle inzichten | Nee | Ja | [Automatisch gegevensinzichten genereren met Power BI](../consumer/end-user-insights.md) 
| In Excel analyseren | Nee | Ja | [Analyseren in Excel](../service-analyze-in-excel.md) 
| Gepagineerde rapporten | Ja | Ja | [Gepagineerde rapporten zijn beschikbaar in de Power BI-service](../paginated-reports-report-builder-power-bi.md) in preview (Engelstalig)
| Power BI - Mobiel-apps | Ja | Ja | [Overzicht van mobiele Power BI-apps](../consumer/mobile/mobile-apps-for-mobile-devices.md) 
| ARC GIS-kaarten | Nee | Ja | [ArcGIS-kaarten in de Power BI-service en Power BI Desktop, door Esri](../power-bi-visualization-arcgis.md)
| E-mailabonnementen voor Power BI-rapporten | Nee | Ja | [Abonneren op een rapport of dashboard](../consumer/end-user-subscribe.md) in de Power BI-service 
| E-mailabonnementen voor gepagineerde rapporten | Ja | Nee | [E-maillevering in Reporting Services](https://docs.microsoft.com/sql/reporting-services/subscriptions/e-mail-delivery-in-reporting-services)  
| Gegevensmeldingen | Nee | Ja | [Gegevensmeldingen in de Power BI-service](../service-set-data-alerts.md)
| Beveiliging op rijniveau | Alleen via de gegevensbron in de DirectQuery-modus | Beschikbaar in de DirectQuery-modus (gegevensbron) en in de importmodus | [Beveiliging op rijniveau (RLS) met Power BI](../service-admin-rls.md) 
| Modus volledig scherm | Nee | Ja | [De modus Volledig scherm in de Power BI-service](../consumer/end-user-focus.md) 
| Geavanceerde Office 365-samenwerking | Nee | Ja | [Samenwerken in een app-werkruimte met Office 365](../service-collaborate-power-bi-workspace.md) 
| R-visuals | Nee | Ja | [R-visuals maken in de Power BI-service](../visuals/service-r-visuals.md)  
| Preview-functies | Nee | Ja | [Aanmelden voor preview-functies van de Power BI-service](../consumer/end-user-preview-features.md) 
| Aangepaste visuals | Ja | Ja | [Aangepaste visualisaties in Power BI](../power-bi-custom-visuals.md) 
| Power BI Desktop | Versie geoptimaliseerd voor Report Server, beschikbaar voor downloaden met Report Server | Versie geoptimaliseerd voor de Power BI-service, beschikbaar in de Windows Store | [Power BI Desktop voor de rapportserver](https://powerbi.microsoft.com/report-server/) <br><br> [Power BI Desktop voor de Power BI-service](http://aka.ms/pbidesktopstore)

## <a name="next-steps"></a>Volgende stappen
[Power BI Report Server installeren](install-report-server.md)  



