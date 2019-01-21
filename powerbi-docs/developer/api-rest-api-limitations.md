---
title: Beperkingen van REST-API's van Power BI
description: 'De Power BI REST-API bevat de volgende beperkingen:'
author: markingmyname
manager: kfile
ms.author: maghan
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 06/08/2018
ms.openlocfilehash: df17563d384359fe33123ed87743754bb33bf04d
ms.sourcegitcommit: c8c126c1b2ab4527a16a4fb8f5208e0f7fa5ff5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2019
ms.locfileid: "54277965"
---
# <a name="power-bi-rest-api-limitations"></a>Beperkingen van REST-API's van Power BI  
  
**Voor POSTen van rijen**  
  
* Maximaal 75 kolommen
* Maximaal 75 tabellen
* Maximaal 10.000 rijen per POST-rijaanvraag  
* 1.000.000 rijen per uur toegevoegd per gegevensset  
* Maximaal vijf POST-rijaanvragen in behandeling per gegevensset  
* 120 POST-rijaanvragen per minuut per gegevensset
* 120 POST-rijaanvragen per uur per gegevensset, als een tabel 250.000 rijen of meer bevat    
* Maximaal 200.000 rijen opgeslagen per tabel in een FIFO-gegevensset  
* Maximaal 5.000.000 rijen opgeslagen per tabel in gegevensset zonder bewaarbeleid  
* 4000 tekens per waarde voor de kolom met tekenreeksen in POST-rijbewerkingen
  
## <a name="see-also"></a>Zie ook

[Azure AD service limits and restrictions](https://docs.microsoft.com/azure/active-directory/active-directory-service-limits-restrictions)  (Limieten en beperkingen voor de Azure AD-service)  
[Overview of Power BI REST API](https://docs.microsoft.com/rest/api/power-bi/) (Overzicht van de REST-API voor Power BI)