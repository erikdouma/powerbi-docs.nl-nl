---
title: PowerShell-cmdlets, REST-API's en .NET SDK voor Power BI-beheerders
description: Meer informatie over de manieren waarop u Power BI kunt beheren via scripts en programmeer-API's.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-admin
ms.topic: overview
ms.date: 06/25/2018
ms.author: mblythe
LocalizationGroup: Administration
ms.openlocfilehash: f4455fef5a2ed0e7ee23ff8ca3a0b626cd695838
ms.sourcegitcommit: a1b7ca499f4ca7e90421511e9dfa61a33333de35
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/10/2018
ms.locfileid: "51507986"
---
# <a name="powershell-cmdlets-rest-apis-and-net-sdk-for-power-bi-administration"></a>PowerShell-cmdlets, REST-API's en .NET SDK voor het beheer van Power BI
Met Power BI kunnen beheerders algemene taken uitvoeren met PowerShell-cmdlets. Verder biedt het REST-API's en een .NET SDK voor het ontwikkelen van beheerdersoplossingen. Dit onderwerp bevat een lijst met cmdlets met de bijbehorende SDK-methode en het REST API-eindpunt. Zie deze onderwerpen voor meer informatie:

  - PowerShell [downloaden](https://www.powershellgallery.com/packages/MicrosoftPowerBIMgmt/) en [documentatie](https://docs.microsoft.com/powershell/power-bi/overview?view=powerbi-ps)
  - REST API-[documentatie](https://docs.microsoft.com/rest/api/power-bi/admin)
  - .NET SDK [downloaden](https://www.nuget.org/packages/Microsoft.PowerBI.Api/) 


| **Naam van cmdlet** | **SDK-methode** | **REST API-eindpunt** | **Beschrijving** |
| --- | --- | --- | --- |
| **Get-PowerBIDatasource** | Gegevenssets\_GetDataSourcesAsAdmin | /v1.0/myorg/admin/datasets/{datasetkey}/datasources | Hiermee haalt u de gegevensbronnen voor een bepaalde gegevensset op. |
| **Get-PowerBIDataset** | Gegevenssets\_GetDatasetsAsAdmin | /v1.0/myorg/admin/datasets | Hiermee haalt u de volledige lijst met gegevenssets in een Power BI-tenant op. |
| **Get-PowerBIWorkspace** | Groepen\_GetGroupsAsAdmin | /v1.0/myorg/admin/groups | Hiermee haalt u de volledige lijst met werkruimten in een Power BI-tenant op. |
| **Add-PowerBIWorkspaceUser** | Groepen\_AddUserAsAdmin | /v1.0/myorg/admin/groups/{groupId}/users | Hiermee voegt u een gebruiker als lid aan een opgegeven werkruimte toe. |
| **Remove-PowerBIWorkspaceUser** | Groepen\_DeleteUserAsAdmin | /v1.0/myorg/admin/groups/{groupId}/users/{user} | Hiermee verwijdert u een gebruiker uit de lijst met leden van de opgegeven werkruimte. |
| **Restore-PowerBIWorkspace** | Groepen\_RestoreDeletedGroupAsAdmin | /v1.0/myorg/admin/groups/{groupId}/restore | Hiermee herstelt u een verwijderde werkruimte. |
| **Set-PowerBIWorkspace** | Groepen\_UpdateGroupAsAdmin | /v1.0/myorg/admin/groups/{groupId} | Hiermee werkt u de eigenschappen van een opgegeven werkruimte bij. |
| **Get-PowerBIDataset -WorkspaceId** | Groepen\_GetDatasetsAsAdmin | /v1.0/myorg/admin/groups/{group\_id}/datasets | Hiermee haalt u de gegevenssets binnen een opgegeven werkruimte op. |
| **Export-PowerBIReport** | Rapporten\_ExportReportAsAdmin | N.v.t. | Hiermee exporteert u een opgegeven rapport naar een lokaal bestand. |
| **Get-PowerBIReport** | Rapporten\_GetReportsAsAdmin | /v1.0/myorg/admin/reports | Hiermee haalt u de volledige lijst met rapporten in een Power BI-tenant op. |
| **Get-PowerBIDashboard** | Dashboards\_GetDashboardsAsAdmin | /v1.0/myorg/admin/dashboards | Hiermee haalt u de volledige lijst met dashboards in een Power BI-tenant op. |
| **Get-PowerBIDashboard -WorkspaceId** | Groepen\_GetDashboardsAsAdmin | /v1.0/myorg/admin/groups/{group\_id}/dashboards | Hiermee haalt u de dashboards binnen een opgegeven werkruimte op. |
| **Get-PowerBITile -DashboardId** | Dashboards\_GetTilesAsAdmin | /v1.0/myorg/admin/dashboards/{dashboard\_id}/tiles | Hiermee haalt u de tegels van een opgegeven dashboard op. |
| **Get-PowerBIReport -WorkspaceId** | Groepen\_GetReportsAsAdmin | /v1.0/myorg/admin/groups/{group\_id}/reports | Hiermee haalt u de rapporten binnen een opgegeven werkruimte op. |
| **Get-PowerBIImport** | Importbewerkingen\_GetImportsAsAdmin | /v1.0/myorg/admin/imports | Hiermee haalt u de volledige lijst met importbewerkingen in een Power BI-tenant op. |
| **Connect-PowerBIServiceAccount** | N.v.t. | N.v.t. | Meld u aan bij Power BI en start een sessie. |
| **Disconnect-PowerBIServiceAccount** | N.v.t. | N.v.t. | Meld u af bij Power BI en sluit vervolgens de bestaande sessie. |
| **Invoke-PowerBIRestMethod** | N.v.t. | N.v.t. | Verzend willekeurige REST API-aanroepen naar Power BI. |
| **Get-PowerBIAccessToken** | N.v.t. | N.v.t. | Verkrijg het Power BI-toegangstoken in een sessie. |
| **Resolve-PowerBIError** | N.v.t. | N.v.t. | Haal gedetailleerde gegevens over fouten voor mislukte cmdlet- aanroepen op. |