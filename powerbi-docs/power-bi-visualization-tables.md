---
title: Tabelvisualisaties in Power BI-rapporten en -dashboards (zelfstudie)
description: Zelfstudie over het werken met tabelvisualisaties in Power BI-rapporten en -dashboards, met informatie over het aanpassen van de kolombreedte.
services: powerbi
documentationcenter: ''
author: mihart
manager: kfile
backup: ''
editor: ''
tags: ''
featuredvideoid: ''
qualityfocus: ''
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 04/11/2018
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: a36e2afcda7c741c871b07c526ab010f77290a3b
ms.sourcegitcommit: df94efc51f261113fa90ebdf3fe68dd149cc4936
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/18/2018
---
# <a name="working-with-tables-in-power-bi-reports-and-dashboards-tutorial"></a>Werken met tabelvisualisaties in Power BI-rapporten en -dashboards (zelfstudie)
Een tabel is een raster met gerelateerde gegevens in een logische reeks rijen en kolommen. Het kan ook koppen en een rij voor totalen bevatten. Tabellen werken goed met kwantitatieve vergelijkingen waarbij u veel waarden voor één categorie bekijkt. Deze tabel geeft bijvoorbeeld 5 verschillende eenheden  voor **Categorie** weer.

![](media/power-bi-visualization-tables/table.png)

## <a name="when-to-use-a-table"></a>Wanneer u een tabel gebruikt
Tabellen zijn een prima keuze:

* om gedetailleerde gegevens en exacte waarden (in plaats van visuele weergaven) te bekijken en vergelijken;
* om gegevens weer te gegeven in tabelvorm;
* om numerieke gegevens per categorie weer te geven.   

> [!NOTE]
> Als een tabel te veel waarden heeft, kunt u deze converteren naar een matrix en/of een detailweergave te gebruiken.
> 
> 
## <a name="prerequisites"></a>Vereisten
 - Power BI-service of Power BI Desktop
 - Voorbeeld van een retailanalyse


## <a name="create-a-table"></a>Een tabel maken
We maken de tabel hierboven om de omzet per artikelcategorie weer te geven. Meld u aan bij de Power BI-service als u de zelfstudie wilt volgen. Selecteer achtereenvolgens **Gegevens ophalen \> Voorbeelden \> Voorbeeld van een retailanalyse > Verbinding maken** en kies **Naar dashboard gaan. Voor het maken van een visualisatie hebt u bewerkmachtigingen voor de gegevensset en het rapport nodig. De voorbeelden van Power Bi zijn allemaal bewerkbaar. Als het rapport met u is gedeeld, kunt u geen visualisaties maken in rapporten.

1. Selecteer in het navigatiedeelvenster aan de linkerkant **Werkruimten >Mijn werkruimte**.    
2. Selecteer het tabblad Gegevenssets en scrol omlaag naar de gegevensset Voorbeeld van een retailanalyse die u zojuist hebt toegevoegd.  Selecteer het prictogram **Rapport maken**.
   
    ![](media/power-bi-visualization-tables/power-bi-create-report.png)
2. Selecteer in de rapporteditor **Artikel** > **Categorie**.  Power BI maakt automatisch een tabel waarin alle categorieën worden weergegeven.
   
    ![](media/power-bi-visualization-tables/power-bi-table1.png)
3. Selecteer **Verkoop > Gemiddelde eenheidsprijs** en **Verkoop > Omzet afgelopen jaar** en **Verkoop > Omzet van dit jaar** en kies alle 3 de opties (Waarde, Doel, Status).   
4. Zoek in het deelvenster Visualisaties het venster **Waarden** en sleep de waarden totdat de volgorde van de grafiekkolommen overeenkomt met de eerste afbeelding op deze pagina.  Het venster Waarden moet er als volgt uitzien.
   
    ![](media/power-bi-visualization-tables/power-bi-table2.png)
5. Maak de tabel aan het dashboard vast door het speldpictogram te selecteren  
   
     ![](media/power-bi-visualization-tables/pbi_pintile.png)

## <a name="format-the-table"></a>De tabel opmaken
Er zijn veel manieren om een tabel op te maken. Hier komen er slechts enkele aan bod. Een uitstekende manier om de andere opmaakopties te ontdekken, is het deelvenster Opmaak te openen (verfroller pictogram ![](media/power-bi-visualization-tables/power-bi-format.png)) en verschillende opties uit te proberen.

* Probeer het tabelraster op te maken. Hier hebben we een blauw verticaal raster toegevoegd, ruimte toegevoegd aan de rijen, de omlijning dikker gemaakt en de tekst groter gemaakt.
  
    ![](media/power-bi-visualization-tables/power-bi-table-gridnew.png)
  
    ![](media/power-bi-visualization-tables/power-bi-table-grid3.png)
* We hebben de achtergrondkleur van de kolomkoppen gewijzigd, omlijning toegevoegd en het lettertype groter gemaakt. 
  
    ![](media/power-bi-visualization-tables/power-bi-table-column-headers.png)

  
    ![](media/power-bi-visualization-tables/power-bi-table-column2.png)

* U kunt zelfs opmaak toepassen op afzonderlijke kolommen en kolomkoppen. Breid om te beginnen **Veldopmaak** uit en selecteer vervolgens de op te maken kolom in de vervolgkeuzelijst. Afhankelijk van de kolomwaarden kunt u met Veldopmaak dingen instellen zoals weergave-eenheden, tekstkleur, aantal decimalen, achtergrond, uitlijning en meer. Nadat u de instellingen hebt aangepast, bepaalt u of u die instellingen zowel op de veldnamenrij als op de totalenrij toepast.

    ![](media/power-bi-visualization-tables/power-bi-field-formatting.png)

* Na een paar extra opmaakstappen, is dit het resultaat. Omdat er zoveel opmaakopties zijn, kunt u het beste beginnen met de standaardopmaak, het deelvenster Opmaak ![](media/power-bi-visualization-tables/power-bi-format.png) openen en verschillende opties proberen. 
  
    ![](media/power-bi-visualization-tables/power-bi-table-format.png)

### <a name="conditional-formatting"></a>Voorwaardelijke opmaak
Een bepaald type opmaak wordt aangeduid als *Voorwaardelijke opmaak*. Deze opmaak wordt toegepast op de velden in het venster **Waarden** van het deelvenster **Visualisaties** in de Power BI-service of in Power BI Desktop. 

Met voorwaardelijke opmaak voor tabellen kunt u aangepaste celachtergrondkleuren en kleuren voor lettertypen opgeven op basis van celwaarden, inclusief het gebruik van kleurovergangen. 

1. Selecteer in het deelvenster **Visualisaties** in de Power BI-service of in Power BI Desktop de pijl omlaag naast de waarde in het venster **Waarden** die u wilt opmaken (of klik met de rechtermuisknop op het veld). U kunt voorwaardelijke opmaak alleen beheren voor velden in het gebied **Waarden** van het venster **Velden**.
   
    ![](media/power-bi-visualization-tables/power-bi-conditional-formatting-background.png)
2. Selecteer **Achtergrondkleurschalen**. In het dialoogvenster dat wordt weergegeven, kunt u de kleur configureren, evenals de *minimum*- en *maximum*waarden. Als u het vak **Afwijken** selecteert, kunt u desgewenst ook een waarde voor *Centreren* configureren.
   
    ![](media/power-bi-visualization-tables/power-bi-conditional-formatting-background2.png)
   
    Laten we wat aangepaste opmaak toepassen op de waarden voor Gemiddelde eenheidsprijs. Selecteer **Afwijken**, voeg wat kleuren toe en kies **OK**. 
   
    ![](media/power-bi-visualization-tables/power-bi-conditional-formatting-data-background.png)
3. Voeg een nieuw veld toe aan de tabel met positieve en negatieve waarden.  Selecteer **Verkoop > Afwijking van totale verkoop**. 
   
    ![](media/power-bi-visualization-tables/power-bi-conditional-formatting2.png)
4. Voeg voorwaardelijke opmaak toe aan de gegevensbalk door de pijl omlaag te selecteren naast **Afwijking van totale verkoop** en **Voorwaardelijke opmaak > Gegevensbalken** te kiezen.
   
    ![](media/power-bi-visualization-tables/power-bi-conditional-formatting-data-bars.png)
5. In het dialoogvenster dat wordt weergegeven stelt u kleuren in voor de **Positieve balk** en **Negatieve balk**, zet u een vinkje naast **Alleen balk weergeven** en brengt u eventuele andere gewenste wijzigingen aan.
   
    ![](media/power-bi-visualization-tables/power-bi-data-bars.png)
   
    Wanneer u **OK** selecteert, vervangen gegevensbalken de numerieke waarden in de tabel, waardoor deze eenvoudiger te bekijken is.
   
    ![](media/power-bi-visualization-tables/power-bi-conditional-formatting-data-bars2.png)
6. Als u voorwaardelijke opmaak uit een visualisatie wilt verwijderen, klikt u eenvoudigweg opnieuw op het veld en selecteert u **Voorwaardelijke opmaak verwijderen**.

> [!TIP]
> Voorwaardelijke opmaak is ook beschikbaar in het deelvenster Opmaak (verfrollerpictogram). Selecteer de waarde die u wilt opmaken en stel vervolgens **Kleurschalen** of **Gegevensbalken** in op Aan om de standaardinstellingen toe te passen. Als u de instellingen wilt aanpassen, selecteert u **Geavanceerde besturingselementen**.
> 
> 

## <a name="adjust-the-column-width-of-a-table"></a>De kolombreedte van een tabel aanpassen
In Power BI wordt soms een kolomkop in een rapport en in een dashboard afgekapt. Houd de muis boven de ruimte aan de rechterkant van de kolomkop om de dubbele pijlen zichtbaar te maken. Selecteer deze en versleep ze om de volledige kolomnaam weer te geven.

![](media/power-bi-visualization-tables/resizetable.gif)

Hebt u nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

