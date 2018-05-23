---
title: Uw gegevensbron beheren - SQL
description: De on-premises gegevensgateway en de gegevensbronnen hiervoor beheren.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-gateways
ms.topic: conceptual
ms.date: 01/24/2018
ms.author: mblythe
LocalizationGroup: Gateways
ms.openlocfilehash: 2eb880ee512a3f13c56bb6dbf880209f05cdf7b4
ms.sourcegitcommit: 638de55f996d177063561b36d95c8c71ea7af3ed
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/17/2018
---
# <a name="manage-your-data-source---sql-server"></a>Uw gegevensbron beheren - SQL Server
Wanneer u de on-premises gegevensgateway hebt geïnstalleerd, kunt u gegevensbronnen toevoegen die met de gateway kunnen worden gebruikt. In dit artikel wordt beschreven hoe u gateways en gegevensbronnen gebruikt. U kunt de SQL Server-gegevensbron voor een geplande vernieuwing of voor DirectQuery gebruiken.

## <a name="download-and-install-the-gateway"></a>De gateway downloaden en installeren
U kunt de gateway downloaden via de Power BI-service. Selecteer **Downloads** > **Gegevensgateway** of ga naar de [pagina voor het downloaden van gateways](https://go.microsoft.com/fwlink/?LinkId=698861).

![](media/service-gateway-enterprise-manage-sql/powerbi-download-data-gateway.png)

## <a name="add-a-gateway"></a>Een gateway toevoegen
Als u een gateway wilt toevoegen, moet u deze gewoon [downloaden](https://go.microsoft.com/fwlink/?LinkId=698861) en installeren op een server in uw omgeving. Nadat u de gateway hebt geïnstalleerd, wordt deze weergegeven in de lijsten met gateways onder **Gateways beheren**.

> [!NOTE]
> **Gateways beheren** wordt alleen weergegeven als u beheerder van ten minste één gateway bent geworden. Dit wordt u doordat u als beheerder wordt toegevoegd aan een gateway of door zelf een gateway te installeren en te configureren.
> 
> 

## <a name="remove-a-gateway"></a>Een gateway verwijderen
Als u een gateway verwijdert, worden ook alle gegevensbronnen voor die gateway verwijderd.  De dashboards en rapporten die afhankelijk zijn van deze gegevensbronnen, werken hierdoor ook niet meer.

1. Selecteer het tandwielpictogram ![](media/service-gateway-enterprise-manage-sql/pbi_gearicon.png) in de rechterbovenhoek > **Gateways beheren**.
2. Gateway > **Verwijderen**
   
   ![](media/service-gateway-enterprise-manage-sql/datasourcesettings7.png)

## <a name="add-a-data-source"></a>Een gegevensbron toevoegen
U kunt een gegevensbron toevoegen door een gateway te selecteren en op **Gegevensbron toevoegen** te klikken of door naar Gateway > **Gegevensbron toevoegen** te gaan.

![](media/service-gateway-enterprise-manage-sql/datasourcesettings1.png)

U kunt vervolgens in de lijst het **gegevensbrontype** selecteren.

![](media/service-gateway-enterprise-manage-sql/datasourcesettings2.png)

> [!NOTE]
> Wanneer u DirectQuery gebruikt, biedt de gateway alleen ondersteuning voor **SQL Server 2012 SP1** en latere versies.
> 
> 

Vul vervolgens de gegevens in voor de gegevensbron, waaronder de **server** en de **database**.  

U moet ook een **verificatiemethode** kiezen.  Dit kan **Windows** of **Standaard** zijn.  Kies **Standaard** als u SQL-verificatie in plaats van Windows-verificatie wilt gebruiken. Voer vervolgens de referenties in die u voor deze gegevensbron wilt gebruiken.

> [!NOTE]
> Alle query's voor de gegevensbron worden uitgevoerd met deze referenties, tenzij eenmalige aanmelding (SSO) met Kerberos is geconfigureerd en ingeschakeld voor de gegevensbron. Bij eenmalige aanmelding gebruiken importgegevenssets de opgeslagen referenties, maar DirectQuery-gegevenssets gebruiken de huidige Power BI-gebruiker om de query's met behulp van eenmalige aanmelding uit te voeren. Lees voor meer informatie het hoofdartikel over de on-premises gegevensgateway om te zien hoe [referenties](service-gateway-onprem.md#credentials) worden opgeslagen. U kunt ook het artikel lezen waarin wordt beschreven hoe u [Kerberos gebruikt voor eenmalige aanmelding (SSO) in Power BI bij on-premises gegevensbronnen](service-gateway-kerberos-for-sso-pbi-to-on-premises-data.md).
> 
> 

![](media/service-gateway-enterprise-manage-sql/datasourcesettings3.png)

U kunt op **Toevoegen** klikken nadat u alles hebt ingevuld.  U kunt deze gegevensbron nu gebruiken voor geplande vernieuwing, of DirectQuery, bij een on-premises SQL-server. De tekst *Verbinding gemaakt* wordt weergegeven als deze bewerking is geslaagd.

![](media/service-gateway-enterprise-manage-sql/datasourcesettings4.png)

### <a name="advanced-settings"></a>Geavanceerde instellingen
U kunt het privacyniveau voor de gegevensbron configureren. Hiermee bepaalt u hoe gegevens kunnen worden gecombineerd. Dit wordt alleen gebruikt voor geplande vernieuwing. Het geldt niet voor DirectQuery. [Meer informatie](https://support.office.com/article/Privacy-levels-Power-Query-CC3EDE4D-359E-4B28-BC72-9BEE7900B540)

![](media/service-gateway-enterprise-manage-sql/datasourcesettings9.png)

## <a name="remove-a-data-source"></a>Een gegevensbron verwijderen
Als u een gegevensbron verwijdert, zullen de dashboards of rapporten die afhankelijk zijn van de gegevensbron niet meer werken.  

Ga naar Gegevensbron > **Verwijderen** om een gegevensbron te verwijderen.

![](media/service-gateway-enterprise-manage-sql/datasourcesettings6.png)

## <a name="manage-administrators"></a>Beheerders beheren
Op het tabblad Beheerders voor de gateway kunt u gebruikers (of beveiligingsgroepen) toevoegen en verwijderen die de gateway kunnen beheren.

![](media/service-gateway-enterprise-manage-sql/datasourcesettings8.png)

## <a name="manage-users"></a>Gebruikers beheren
Op het tabblad Gebruikers voor de gegevensbron kunt u gebruikers (of beveiligingsgroepen) toevoegen en verwijderen die deze gegevensbron kunnen gebruiken.

> [!NOTE]
> De lijst met gebruikers wordt uitsluitend geraadpleegd om te bepalen wie er rapporten mag publiceren. De rapporteigenaren kunnen dashboards of inhoudspakketten maken en deze delen met andere gebruikers.
> 
> 

![](media/service-gateway-enterprise-manage-sql/datasourcesettings5.png)

## <a name="using-the-data-source"></a>De gegevensbron gebruiken
Nadat u de gegevensbron hebt gemaakt, kan deze worden gebruikt met DirectQuery-verbindingen of via geplande vernieuwing.

> [!NOTE]
> De servernaam en databasenaam die worden gebruikt voor Power BI Desktop en de gegevensbron in de on-premises gegevensgateway moeten overeenkomen!
> 
> 

De koppeling tussen uw gegevensset en de gegevensbron in de gateway is gebaseerd op uw server- en databasenaam. Deze moeten overeenkomen. Als u bijvoorbeeld een IP-adres gebruikt als servernaam in **Power BI Desktop**, moet u dit IP-adres gebruiken voor de gegevensbron in de gatewayconfiguratie. Als u in Power BI Desktop *SERVER\EXEMPLAAR* gebruikt, moet u dat ook gebruiken in de gegevensbron die u voor de gateway configureert.

Dit geldt voor zowel DirectQuery als geplande vernieuwing.

### <a name="using-the-data-source-with-directquery-connections"></a>De gegevensbron gebruiken met DirectQuery-verbindingen
Zorg ervoor dat de servernaam en databasenaam voor **Power BI Desktop** en de geconfigureerde gegevensbron voor de gateway overeenkomen. Zorg er ook voor dat de gebruiker wordt vermeld op het tabblad **Gebruikers** van de gegevensbron om DirectQuery-gegevenssets te kunnen publiceren. De selectie voor DirectQuery vindt plaats in Power BI Desktop wanneer u voor het eerst gegevens importeert. [Meer informatie](desktop-use-directquery.md)

Als het goed is, werken uw rapporten nadat u de gegevens hebt gepubliceerd vanuit Power BI Desktop of via **Gegevens ophalen**. Nadat u de gegevensbron in de gateway hebt gemaakt, kan het enkele minuten duren voordat de verbinding kan worden gebruikt.

### <a name="using-the-data-source-with-scheduled-refresh"></a>De gegevensbron gebruiken met geplande vernieuwing
Als u wordt vermeld op het tabblad **Gebruikers** voor de gegevensbron die is geconfigureerd in de gateway en de server- en databasenaam overeenkomen, wordt de gateway als optie vermeld en kan deze worden gebruikt bij een geplande vernieuwing.

![](media/service-gateway-enterprise-manage-sql/powerbi-gateway-enterprise-schedule-refresh.png)

## <a name="next-steps"></a>Volgende stappen
* [On-premises gegevensgateway](service-gateway-onprem.md)  
* [On-premises data gateway in-depth](service-gateway-onprem-indepth.md) (On-premises gegevensgateway - uitgebreid)  
* [Problemen met de on-premises gegevensgateway oplossen](service-gateway-onprem-tshoot.md)
* [Kerberos gebruiken voor eenmalige aanmelding (SSO) in Power BI bij on-premises gegevensbronnen](service-gateway-kerberos-for-sso-pbi-to-on-premises-data.md). 
* Nog vragen? [Misschien dat de Power BI-community het antwoord weet](http://community.powerbi.com/)

