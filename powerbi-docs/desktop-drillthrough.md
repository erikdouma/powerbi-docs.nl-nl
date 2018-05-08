---
title: Drillthrough gebruiken in Power BI Desktop
description: Informatie over inzoomen op nieuwe gegevens op een nieuwe rapportpagina in Power BI Desktop.
services: powerbi
documentationcenter: ''
author: davidiseminger
manager: kfile
backup: ''
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 4/10/2018
ms.author: davidi
LocalizationGroup: Create reports
ms.openlocfilehash: b5da2bf43f2d38e0828571e2b9d404feb615ac69
ms.sourcegitcommit: 312390f18b99de1123bf7a7674c6dffa8088529f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2018
---
# <a name="use-drillthrough-in-power-bi-desktop"></a>Drillthrough gebruiken in Power BI Desktop
Met **drillthrough** in **Power BI Desktop** kunt u een pagina in uw rapport maken die zich op een bepaalde entiteit richt, zoals een leverancier, klant of fabrikant. Met die specifieke rapportpagina kunnen gebruikers met de rechtermuisknop op een gegevenspunt in andere rapportpagina's klikken en inzoomen op die specifieke pagina voor gefilterde details met betrekking tot die context.

![](media/desktop-drillthrough/drillthrough_01.png)

## <a name="using-drillthrough"></a>Drillthrough gebruiken
1. Als u **drillthrough** wilt gebruiken, maakt u een rapportpagina met visuals voor het type entiteit waarop u drillthrough wilt toepassen. 

    Stel dat u drillthrough voor fabrikanten beschikbaar wilt maken. Dan kunt u een drillthrough-pagina maken met visuele elementen met de totale omzet, het totale aantal verzonden eenheden, omzet per categorie of per regio, enzovoort. Als u vervolgens op die pagina inzoomt, ziet u de visuals die specifiek zijn voor de fabrikant die u hebt geselecteerd.

2. Op de drillthrough-pagina gaat u vervolgens naar de sectie **Velden** van het deelvenster **Visualisaties** en sleept u het veld waarop u drillthrough wilt toepassen eveneens naar de verdieping **Drillthrough-filters**.

    ![](media/desktop-drillthrough/drillthrough_02.png)

    Als u een veld toevoegt aan de verdieping **Drillthrough-filters**, wordt automatisch de knop **Terug** als visueel element gemaakt. Dit visuele element wordt een knop in gepubliceerde rapporten. Gebruikers die het rapport gebruiken in de **Power BI-service** kunnen er makkelijk mee teruggaan naar de rapportpagina waar ze vandaan kwamen (de pagina waar ze voor de drillthrough hebben gekozen).

    ![](media/desktop-drillthrough/drillthrough_03.png)

## <a name="use-your-own-image-for-a-back-button"></a>Uw eigen afbeelding gebruiken voor een knop Terug    
 Omdat de knop Terug een afbeelding is, kunt u deze vervangen door een andere afbeelding naar keuze. De knop werkt dan nog steeds als knop Terug om gebruikers van het rapport te laten terugkeren naar de oorspronkelijke pagina.

1. Voor het gebruik van uw eigen afbeelding voor een knop Terug plaatst u een afbeeldingsvisual op de drillthrough-pagina.
2. Selecteer de visual en stel de schuifregelaar voor **de knop Terug** in op aan. De afbeelding fungeert nu als een knop Terug.

    ![](media/desktop-drillthrough/drillthrough_05.png)

    Als uw **drillthrough**-pagina is voltooid en een gebruiker in het rapport met de rechtermuisknop klikt op een gegevenspunt waarvoor het veld wordt gebruikt dat u in de verdieping **Drillthrough-filters** hebt geplaatst, wordt een snelmenu weergegeven waarmee de gebruiker op die pagina kan inzoomen.

    ![](media/desktop-drillthrough/drillthrough_04.png)

    Als de gebruiker voor drillthrough kiest, wordt de pagina gefilterd en wordt informatie weergegeven over het gegevenspunt waarop met de rechtermuisknop is geklikt. Als de gebruiker bijvoorbeeld met de rechtermuisknop heeft geklikt op een gegevenspunt over Contoso (een fabrikant) en voor drillthrough heeft gekozen, dan is de weergegeven drillthrough-pagina op Contoso gefilterd.

    > [!NOTE]
    > Alleen het veld in de verdieping **Drillthrough-filters** wordt doorgegeven aan de drillthrough-pagina van het rapport. Er wordt geen andere contextuele informatie doorgegeven.
    > 
    > 

Meer hoeft u niet te doen om **drillthrough** in uw rapporten te gebruiken. Het is een uitstekende manier om een uitgebreid overzicht te krijgen over de entiteitsgegevens die u voor uw drillthrough-filter selecteert.

