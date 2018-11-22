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
ms.openlocfilehash: 1ed4298e4ed4cddcdf965bd427c654cab6adf1e6
ms.sourcegitcommit: 46f1ba3f972f6e64bce05ad0fd527b27c49aedd6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/20/2018
ms.locfileid: "52157006"
---
# <a name="powershell-cmdlets-rest-apis-and-net-sdk-for-power-bi-administration"></a>PowerShell-cmdlets, REST-API's en .NET SDK voor het beheer van Power BI
Met Power BI kunnen beheerders algemene taken uitvoeren met PowerShell-cmdlets. Verder biedt het REST-API's en een .NET SDK voor het ontwikkelen van beheerdersoplossingen. Dit onderwerp bevat een lijst met cmdlets met de bijbehorende SDK-methode en het REST API-eindpunt. Zie deze onderwerpen voor meer informatie:

- PowerShell [downloaden](https://www.powershellgallery.com/packages/MicrosoftPowerBIMgmt/) en [documentatie](https://docs.microsoft.com/powershell/power-bi/overview?view=powerbi-ps)
- REST API-[documentatie](https://docs.microsoft.com/rest/api/power-bi/admin)
- .NET SDK [downloaden](https://www.nuget.org/packages/Microsoft.PowerBI.Api/)

| **Naam van cmdlet** | **Aliassen** | **SDK-methode** | **REST API-eindpunt** | **Beschrijving** |
| --- | --- | --- | --- | --- |
| **Get-PowerBIDatasource** | N.v.t. | Gegevenssets\_GetDataSourcesAsAdmin | /v1.0/myorg/admin/datasets/{datasetkey}/datasources | Hiermee haalt u de gegevensbronnen voor een bepaalde gegevensset op. |
| **Get-PowerBIDataset** | N.v.t. | Gegevenssets\_GetDatasetsAsAdmin | /v1.0/myorg/admin/datasets | Hiermee haalt u de volledige lijst met gegevenssets in een Power BI-tenant op. |
| **Get-PowerBIWorkspace** | **Get-PowerBIGroup** | Groepen\_GetGroupsAsAdmin | /v1.0/myorg/admin/groups | Hiermee haalt u de volledige lijst met werkruimten in een Power BI-tenant op. |
| **Add-PowerBIWorkspaceUser** | **Add-PowerBIGroupUser** |Groepen\_AddUserAsAdmin | /v1.0/myorg/admin/groups/{groupId}/users | Hiermee voegt u een gebruiker als lid aan een opgegeven werkruimte toe. |
| **Remove-PowerBIWorkspaceUser** | **Remove-PowerBIGroupUser** | Groepen\_DeleteUserAsAdmin | /v1.0/myorg/admin/groups/{groupId}/users/{user} | Hiermee verwijdert u een gebruiker uit de lijst met leden van de opgegeven werkruimte. |
| **Restore-PowerBIWorkspace** |**Restore-PowerBIGroup** | Groepen\_RestoreDeletedGroupAsAdmin | /v1.0/myorg/admin/groups/{groupId}/restore | Hiermee herstelt u een verwijderde werkruimte. |
| **Set-PowerBIWorkspace** |**Set-PowerBIGroup** | Groepen\_UpdateGroupAsAdmin | /v1.0/myorg/admin/groups/{groupId} | Hiermee werkt u de eigenschappen van een opgegeven werkruimte bij. |
| **Get-PowerBIDataset -WorkspaceId** | N.v.t. | Groepen\_GetDatasetsAsAdmin | /v1.0/myorg/admin/groups/{group\_id}/datasets | Hiermee haalt u de gegevenssets binnen een opgegeven werkruimte op. |
| **Export-PowerBIReport** | N.v.t. | Rapporten\_ExportReportAsAdmin | N.v.t. | Hiermee exporteert u een opgegeven rapport naar een lokaal bestand. |
| **Get-PowerBIReport** | N.v.t. | Rapporten\_GetReportsAsAdmin | /v1.0/myorg/admin/reports | Hiermee haalt u de volledige lijst met rapporten in een Power BI-tenant op. |
| **Get-PowerBIDashboard** | N.v.t. | Dashboards\_GetDashboardsAsAdmin | /v1.0/myorg/admin/dashboards | Hiermee haalt u de volledige lijst met dashboards in een Power BI-tenant op. |
| **Get-PowerBIDashboard** | N.v.t. | Groepen\_GetDashboardsAsAdmin | /v1.0/myorg/admin/groups/{group\_id}/dashboards | Hiermee haalt u de dashboards binnen een opgegeven werkruimte op. |
| **Get-PowerBITile** | **Get-PowerBIDashboardTile** | Dashboards\_GetTilesAsAdmin | /v1.0/myorg/admin/dashboards/{dashboard\_id}/tiles | Hiermee haalt u de tegels van een opgegeven dashboard op. |
| **Get-PowerBIReport** | N.v.t. | Groepen\_GetReportsAsAdmin | /v1.0/myorg/admin/groups/{group\_id}/reports | Hiermee haalt u de rapporten binnen een opgegeven werkruimte op. |
| **Get-PowerBIImport** | N.v.t. | Importbewerkingen\_GetImportsAsAdmin | /v1.0/myorg/admin/imports | Hiermee haalt u de volledige lijst met importbewerkingen in een Power BI-tenant op. |
| **Connect-PowerBIServiceAccount** | **Login-PowerBI** &  **Login-PowerBIServiceAccount** | N.v.t. | N.v.t. | Meld u aan bij Power BI en start een sessie. |
| **Disconnect-PowerBIServiceAccount** | **Logout-PowerBI** & **Logout-PowerBIServiceAccount** | N.v.t. | N.v.t. | Meld u af bij Power BI en sluit vervolgens de bestaande sessie. |
| **Invoke-PowerBIRestMethod**| N.v.t. | N.v.t. | N.v.t. | Verzend willekeurige REST API-aanroepen naar Power BI. |
| **Get-PowerBIAccessToken**| N.v.t. | N.v.t. | N.v.t. | Verkrijg het Power BI-toegangstoken in een sessie. |
| **Resolve-PowerBIError**| N.v.t. | N.v.t. | N.v.t. | Haal gedetailleerde gegevens over fouten voor mislukte cmdlet- aanroepen op. |