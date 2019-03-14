---
ms.openlocfilehash: cd6ea6fd52f929e2cd254214cf0e8c96e858f6c2
ms.sourcegitcommit: 883a58f63e4978770db8bb1cc4630e7ff9caea9a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/07/2019
ms.locfileid: "57555957"
---
Met Power BI kunt u relaties tussen meerdere tabellen maken, zoals voor tabellen die uit verschillende gegevensbronnen afkomstig zijn. U kunt deze relaties voor elk gegevensmodel bekijken in de weergave **Relaties** van Power BI Desktop.

![](media/7-5-table-relationships-and-dax/dax-relationships_1.png)

## <a name="dax-relational-functions"></a>Relationele DAX-functies
DAX bevat **relationele functies** waarmee u tabellen met relaties kunt gebruiken.

U kunt de waarde van een kolom of alle rijen in een relatie retourneren met DAX-functies.

De functie **RELATED** bijvoorbeeld volgt relaties en retourneert de waarde van een kolom, terwijl de functie **RELATEDTABLE** relaties volgt en een hele tabel retourneert die is gefilterd, zodat alleen gerelateerde rijen worden opgenomen.

![](media/7-5-table-relationships-and-dax/dax-relationships_2.png)

De functie **RELATED** werkt aan *veel-op-een-* relaties, terwijl de functie **RELATEDTABLE** is bedoeld voor *een-op-veel*relaties.

U kunt relationele functies gebruiken om expressies te bouwen die waarden tussen meerdere tabellen bevatten. DAX retourneert een resultaat met deze functies, ongeacht de lengte van de keten van de relatie.

> Met dank aan [Alberto Ferrari, SQLBI](http://www.sqlbi.com/learning-dax) voor de video
> 
> 

