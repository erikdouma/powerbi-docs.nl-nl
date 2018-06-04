---
title: 'Organisatie-inhoudspakketten: toegang en kopiëren'
description: Meer informatie over het maken van kopieën van inhoudspakketten van uw organisatie in Power BI en over het oplossen van problemen hiermee
author: maggiesMSFT
manager: kfile
ms.reviewer: ajayan
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 10/12/2017
ms.author: maggies
LocalizationGroup: Share your work
ms.openlocfilehash: a4c2eaed0e8d577359ad9b5ee191ad2894ada12b
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2018
ms.locfileid: "34251110"
---
# <a name="organizational-content-packs-copy-refresh-and-get-access"></a>Organisatie-inhoudspakketten: kopiëren, vernieuwen en toegang verkrijgen
> [!NOTE]
> Hebt u al iets over de nieuwe *apps* gehoord? Apps zijn de nieuwe manier om inhoud naar grote doelgroepen te distribueren in Power BI. U maakt apps in de *app-werkruimten*, die groepen en groepswerkruimten vervangen. U kunt het beste apps in plaats van organisatie-inhoudspakketten of alleen-lezenwerkruimten gebruiken. Meer [informatie over apps](service-install-use-apps.md).
> 
> 

Wanneer een organisatie-inhoudspakket wordt gepubliceerd, zien alle ontvangers de hetzelfde dashboard en dezelfde rapporten, Excel-werkmappen, gegevenssets en gegevens (tenzij het een SSAS-gegevensbron is (SQL Server Analysis Services).  [Alleen de maker van het inhoudspakket kan het inhoudspakket bewerken en opnieuw publiceren](service-organizational-content-pack-manage-update-delete.md).  Alle ontvangers kunnen echter een kopie van het inhoudspakket opslaan die naast het origineel kan bestaan.

Het maken van inhoudspakketten verschilt van het delen van dashboards of het samenwerken aan een dashboard in een groep. Lees [Hoe kan ik samenwerken aan en dashboards en rapporten en deze delen?](service-how-to-collaborate-distribute-dashboards-reports.md) om te bepalen wat de beste optie voor uw situatie is.

## <a name="create-a-copy-of-an-organizational-content-pack"></a>Een kopie maken van een organisatie-inhoudspakket
Maak uw eigen kopie van het inhoudspakket die niet zichtbaar is voor anderen.

1. Selecteer het beletselteken (...) naast het dashboard van het inhoudspakket > Een kopie maken.
   
    ![](media/service-organizational-content-pack-copy-refresh-access/power-bi-create-copy-organizational-content-pack.png)
2. Selecteer **Opslaan**.  

U hebt nu een kopie die u kunt wijzigen. Niemand anders ziet de wijzigingen die u aanbrengt.

## <a name="help--i-can-no-longer-access-the-content-pack"></a>Help!  Ik heb geen toegang meer tot het inhoudspakket
Dit kan gebeuren om verschillende redenen:

* **Lidmaatschapswijzigingen**: inhoudspakketten worden gepubliceerd naar e-maildistributiegroepen, beveiligingsgroepen en [Power BI-groepen op basis van Office 365](https://support.office.com/article/Create-a-group-in-Office-365-7124dc4c-1de9-40d4-b096-e8add19209e9).  Als u uit de groep wordt verwijderd, hebt u geen toegang meer tot het inhoudspakket.
* **Distributiewijzigingen**: de maker van het inhoudspakket wijzigt de distributie. Als het inhoudspakket bijvoorbeeld oorspronkelijk is gepubliceerd voor de hele organisatie, maar de maker het opnieuw heeft gepubliceerd voor een kleinere doelgroep, bent u daar mogelijk niet in opgenomen.
* **Gewijzigde beveiligingsinstellingen**: als het dashboard en de rapporten verbinding hebben met on-premises SSAS-gegevensbronnen en er wijzigingen worden aangebracht in de beveiligingsinstellingen, kunnen uw toegangsrechten tot die server worden ingetrokken.

## <a name="how-are-organizational-content-packs-refreshed"></a>Hoe worden organisatie-inhoudspakketten vernieuwd?
Wanneer het inhoudspakket is gemaakt, worden de vernieuwingsinstellingen overgenomen bij de gegevensset.  Wanneer u een kopie van het inhoudspakket maakt, blijven de koppeling naar de oorspronkelijke gegevensset en het schema voor gegevensvernieuwing behouden in de nieuwe versie. 

Zie [Organisatie-inhoudspakketten beheren, bijwerken en verwijderen](service-organizational-content-pack-manage-update-delete.md).

## <a name="next-steps"></a>Volgende stappen
* [Inleiding tot organisatie-inhoudspakketten](service-organizational-content-pack-introduction.md)
* [Een groep maken in Power BI](service-create-distribute-apps.md)
* Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

