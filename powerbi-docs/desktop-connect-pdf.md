---
title: Verbinding maken met een PDF-bestand in Power BI Desktop (preview)
description: Eenvoudig verbinding maken met gegevens in PDF-bestanden in Power BI Desktop en deze gebruiken
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 11/13/2018
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: ff61c4d2cc8ec3570e7eee45b7e43ec81f8f7161
ms.sourcegitcommit: c8c126c1b2ab4527a16a4fb8f5208e0f7fa5ff5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2019
ms.locfileid: "54275106"
---
# <a name="connect-to-a-pdf-file-in-power-bi-desktop-preview"></a>Verbinding maken met een PDF-bestand in Power BI Desktop (preview)
In Power BI Desktop kunt u verbinding maken met een **PDF-bestand** en gebruikmaken van de opgenomen gegevens, net zoals elke andere gegevensbron in Power BI Desktop.

![Verbinding maken met gegevens in PDF-bestanden](media/desktop-connect-pdf/connect-pdf_04.png)

In de volgende secties wordt beschreven hoe u verbinding maakt met een **PDF-bestand**, gegevens selecteert en die gegevens overbrengt naar **Power BI Desktop**.

## <a name="enable-the-pdf-connector"></a>De PDF-connector inschakelen
De PDF-connector bevindt zich in de preview-versie voor **Power BI Desktop** en moet worden ingeschakeld. Als u de PDF-connector wilt inschakelen, selecteert u **Bestand > Opties en instellingen > Opties > Preview-functies** en schakelt u vervolgens het selectievakje naast **Gegevens ophalen uit PDF-bestanden** in. 

![De PDF-connector inschakelen vanaf Opties > Preview-functies](media/desktop-connect-pdf/connect-pdf_01.png)

**Power BI Desktop** moet opnieuw worden opgestart nadat u de selectie hebt gemaakt.

Wanneer u de **PDF (bèta)**-connector voor de eerste keer gebruikt, wordt u gewaarschuwd dat de PDF-connector nog in ontwikkeling is en in de toekomst kan veranderen. Selecteer **Doorgaan** om de connector te gebruiken.

Het wordt altijd aanbevolen te upgraden naar de meest recente versie van **Power BI Desktop**, die u via een koppeling in [Power BI Desktop downloaden](desktop-get-the-desktop.md) kunt krijgen. 

## <a name="connect-to-a-pdf-file"></a>Verbinding maken met een PDF-bestand
Als u verbinding wilt maken met een **PDF**-bestand, selecteert u **Gegevens ophalen** op het lint **Start** in Power BI Desktop. Selecteer **Bestand** in de categorieën aan de linkerkant en u ziet **PDF (bèta)**.

![PDF selecteren in Gegevens ophalen](media/desktop-connect-pdf/connect-pdf_01.png)

U wordt gevraagd naar de locatie van het PDF-bestand dat u wilt gebruiken. Als u de bestandslocatie hebt opgegeven en het PDF-bestand wordt geladen, wordt een **Navigator**-scherm weergegeven waarin de gegevens van het bestand worden getoond. Hier kunt u een of meer elementen selecteren die u in **Power BI Desktop** wilt importeren en gebruiken.

![Verbinding maken met gegevens in PDF-bestanden](media/desktop-connect-pdf/connect-pdf_04.png)

Wanneer u een selectievakje naast gedetecteerde elementen in het PDF-bestand markeert, worden deze weergegeven in het rechterdeelvenster. Wanneer u klaar bent om te importeren, selecteert u de knop **Laden** om de gegevens in **Power BI Desktop** te laden.

Sinds de **Power BI Desktop**-versie van november 2018 kunt u de **Startpagina** en **Eindpagina** opgeven als optionele parameters voor uw pdf-bestand. U kunt deze parameters ook opgeven in de M-formuletaal. Maak daarbij gebruik van de volgende indeling:

`Pdf.Tables(File.Contents("c:\sample.pdf"), [StartPage=10, EndPage=11])`


## <a name="next-steps"></a>Volgende stappen
Met Power BI Desktop kunt u verbinding maken met allerlei andere gegevens. Bekijk de volgende bronnen voor meer informatie over gegevensbronnen:

* [Wat is Power BI Desktop?](desktop-what-is-desktop.md)
* [Data Sources in Power BI Desktop](desktop-data-sources.md) (Gegevensbronnen in Power BI Desktop)
* [Shape and Combine Data with Power BI Desktop](desktop-shape-and-combine-data.md) (Gegevens vormgeven en combineren met Power BI Desktop)
* [Connect to Excel workbooks in Power BI Desktop](desktop-connect-excel.md) (Verbinding maken met Excel-werkmappen in Power BI Desktop)   
* [Enter data directly into Power BI Desktop](desktop-enter-data-directly-into-desktop.md) (Rechtstreeks gegevens in Power BI Desktop invoeren)   

