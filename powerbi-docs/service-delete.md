---
title: Een dashboard, rapport, werkmap, gegevensset of werkruimte verwijderen
description: Ontdek hoe u vrijwel alles verwijdert uit Power BI
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 09/11/2018
ms.author: maggies
LocalizationGroup: Common tasks
ms.openlocfilehash: 087fe859c7b1a8ca732619866d492f143ff413c9
ms.sourcegitcommit: 5e83fa6c93a0bc6599f76cc070fb0e5c1fce0082
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/13/2019
ms.locfileid: "56216120"
---
# <a name="delete-almost-anything-in-power-bi-service"></a>Vrijwel alles verwijderen in de Power BI-service
In dit artikel leert u hoe u een dashboard, rapport, rapportpagina, werkmap, gegevensset, app en werkruimte verwijdert in de Power BI-service.

## <a name="delete-a-dashboard"></a>Een dashboard verwijderen
Dashboards kunnen worden verwijderd. Als u het dashboard verwijdert, worden de onderliggende gegevensset of rapporten die zijn gekoppeld aan dit dashboard niet verwijderd.

* Als u de eigenaar van het dashboard bent, kunt u het verwijderen. Als u het dashboard hebt gedeeld met collega's, wordt het dashboard verwijderd uit hun Power BI-werkruimte als u het uit uw eigen Power BI-werkruimten verwijdert.
* Als er een dashboard met u is gedeeld en u het niet meer wilt zien, kunt u het verwijderen.  Als u een dashboard verwijdert, wordt het niet verwijderd uit de Power BI-werkruimte van een ander.
* Als een dashboard deel van uitmaakt een [inhoudspakket van een organisatie](service-organizational-content-pack-disconnect.md), is de enige manier om het te verwijderen het verwijderen van de bijbehorende dataset.

### <a name="to-delete-a-dashboard"></a>Ga als volgt te werk om een dashboard te verwijderen
1. Selecteer in uw werkruimte het tabblad **Dashboards**.
2. Zoek het dashboard dat u wilt verwijderen en selecteer het verwijderpictogram ![Verwijderpictogram](media/service-delete/power-bi-delete-icon.png).

    ![Video](media/service-delete/power-bi-delete-dash.gif)

## <a name="delete-a-report"></a>Een rapport verwijderen
Geen zorgen, als u een rapport verwijdert, wordt de gegevensset waarop het rapport is gebaseerd niet verwijderd.  En ook eventuele visualisaties die u uit het rapport hebt vastgemaakt zijn veilig. Ze blijven op het dashboard totdat u ze afzonderlijk verwijdert.

### <a name="to-delete-a-report"></a>Ga als volgt te werk om een rapport te verwijderen
1. Selecteer in uw werkruimte het tabblad **Rapporten**.
2. Zoek het rapport dat u wilt verwijderen en selecteer het verwijderpictogram   ![Verwijderpictogram](media/service-delete/power-bi-delete-icon.png).   

    ![Tabblad Rapporten van een werkruimte](media/service-delete/power-bi-delete-reportnew.png)
3. Bevestig de verwijdering.

   ![Dialoogvenster Rapport verwijderen](media/service-delete/power-bi-delete-report.png)

   > [!NOTE]
   > Als het rapport onderdeel van is een [inhoudspakket](service-organizational-content-pack-introduction.md), kunt u het niet verwijderen met behulp van deze methode.  Zie [De verbinding met een organisatie-inhoudspakket verwijderen](service-organizational-content-pack-disconnect.md).
   >
   >

## <a name="delete-a-workbook"></a>Een werkmap verwijderen
Werkmappen kunnen worden verwijderd. Met het verwijderen van een werkmap verwijdert u echter ook alle rapporten en dashboardtegels die gegevens uit deze werkmap bevatten.

Als de werkmap is opgeslagen in OneDrive voor Bedrijven, wordt deze niet verwijderd uit OneDrive als u hem verwijdert uit Power BI.

### <a name="to-delete-a-workbook"></a>Ga als volgt te werk om een werkmap te verwijderen
1. Selecteer in uw werkruimte het tabblad **Werkmappen**.
2. Zoek de werkmap die u wilt verwijderen en selecteer het verwijderpictogram ![Verwijderpictogram](media/service-delete/power-bi-delete-report2.png) .

    ![Tabblad Werkmappen](media/service-delete/power-bi-delete-workbooknew.png)
3. Bevestig de verwijdering.

   ![Dialoogvenster Werkmap verwijderen](media/service-delete/power-bi-delete-confirm.png)

## <a name="delete-a-dataset"></a>Een gegevensset verwijderen
Gegevenssets kunnen worden verwijderd. Met het verwijderen van een gegevensset verwijdert u echter ook alle rapporten en dashboardtegels die gegevens uit die gegevensset bevatten.

Als een gegevensset deel uitmaakt van een of meer [organisatie-inhoudspakketten](service-organizational-content-pack-disconnect.md), kunt u deze alleen verwijderen als u de inhoudspakketten waarin deze wordt gebruikt verwijdert, wacht totdat de verwijdering is verwerkt, en daarna opnieuw probeert om de gegevensset te verwijderen.

### <a name="to-delete-a-dataset"></a>Ga als volgt te werk om een gegevensset te verwijderen
1. Selecteer in uw werkruimte het tabblad **Gegevenssets**.
2. Zoek de gegevensset die u wilt verwijderen en selecteer het beletselteken (...).  

    ![Tabblad Gegevenssets](media/service-delete/power-bi-delete-datasetnew.png)
3. Selecteer in de vervolgkeuzelijst **Verwijderen**.

   ![Menu met weglatingstekens](media/service-delete/power-bi-delete-datasetnew2.png)
4. Bevestig de verwijdering.

   ![Dialoogvenster Dashboard verwijderen](media/service-delete/power-bi-delete-dataset-confirm.png)

## <a name="delete-an-app-workspace"></a>Een app-werkruimte verwijderen
> [!WARNING]
> Wanneer u een app-werkruimte maakt, maakt u een Office 365-groep. Wanneer u een app-werkruimte verwijdert, verwijdert u ook de betreffende Office 365-groep. Dit betekent dat de groep ook wordt verwijderd uit andere O365-producten, zoals SharePoint en Microsoft Teams.
>
>

Als u de auteur van de app-werkruimte bent, kunt u deze verwijderen. Wanneer u deze verwijdert, wordt de bijbehorende app ook verwijderd voor alle groepsleden en verwijderd uit uw AppSource als u de app had gepubliceerd naar uw hele organisatie. Het verwijderen van een app-werkruimte is iets anders dan het verlaten van een app-werkruimte.

### <a name="to-delete-an-app-workspace---if-you-are-an-admin"></a>Als u een beheerder bent, kunt u een app-werkruimte als volgt verwijderen
1. Selecteer in de linker navigatie **Werkruimten**

    ![App-werkruimten](media/service-delete/power-bi-delete-workspace.png)
2. Selecteer het beletselteken (...) aan de rechterkant van de werkruimte die u wilt verwijderen en kies **Werkruimte bewerken**.

   ![Menu met weglatingstekens > Werkruimte bewerken](media/service-delete/power-bi-edit-workspace.png)
3. In het venster **Werkruimte bewerken** selecteert u **Werkruimte verwijderen** > **verwijderen**.

    ![Werkruimte verwijderen](media/service-delete/power-bi-delete-workspace2.png)

### <a name="to-remove-an-app-workspace-from-your-list"></a>Ga als volgt te werk om een app-werkruimte uit uw lijst te verwijderen
Als u niet langer lid wilt zijn van een app-werkruimte, kunt u deze ***verlaten***. Deze wordt vervolgens verwijderd uit de lijst. Als u een werkruimte verlaat, blijft deze bestaan voor alle andere leden van de werkruimte.  

> [!IMPORTANT]
> Als u de enige beheerder van de app-werkruimte bent, kunt u deze niet verlaten.
>
>

1. Start in de werkruimte die u wilt verwijderen.
2. Selecteer in de rechterbovenhoek het beletselteken (...) en kies **Werkruimte verlaten** > **Verlaten**.

      ![Werkruimte verlaten](media/service-delete/power-bi-leave-workspace.png)

   > [!NOTE]
   > De opties die worden weergegeven in de vervolgkeuzelijst zijn afhankelijk van uw rol in de app-werkruimte: beheerder of lid.
   >
   >

## <a name="delete-or-remove-an-app"></a>Een app verwijderen of wissen
Apps kunnen eenvoudig worden verwijderd op de pagina met uw app-lijst. Maar alleen de beheerder van een app kan een app permanent wissen.

### <a name="remove-an-app-from-your-app-list-page"></a>Een app verwijderen van de pagina met uw app-lijst
Als u een app verwijdert van de pagina met uw app-lijst, wordt de app niet verwijderd voor andere leden.

1. Selecteer in de linkernavigatie **Apps** om de pagina met de app-lijst te openen.
2. Houd de muis boven de app die u wilt verwijderen en selecteer het verwijderpictogram ![](media/service-delete/power-bi-delete-report2.png).

   ![Apps selecteren](media/service-delete/power-bi-delete-app.png)

   Als u per ongeluk een app verwijdert, hebt u verschillende opties om deze terug te zetten.  U kunt de maker van de app vragen om de app opnieuw te sturen, het oorspronkelijke e-mailbericht met de koppeling naar de app zoeken, uw [meldingencentrum](service-notification-center.md) controleren om te zien of er nog meldingen voor die app worden weergegeven, of de [AppSource](consumer/end-user-apps.md) van uw organisatie controleren.

## <a name="considerations-and-troubleshooting"></a>Aandachtspunten en probleemoplossing
In dit artikel hebben we beschreven hoe u de belangrijkste bouwstenen van de Power BI-service verwijdert. Maar er zijn meer dingen die u in Power BI kunt verwijderen.  

* [Uw aanbevolen dashboard verwijderen](service-dashboard-featured.md)
* [Een dashboard verwijderen (uit uw favorieten)](service-dashboard-favorite.md)
* [Een rapportpagina verwijderen](service-delete.md)
* [Een dashboardtegel verwijderen](service-dashboard-edit-tile.md)
* [Een visualisatie van een rapport verwijderen](service-delete.md)

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)
