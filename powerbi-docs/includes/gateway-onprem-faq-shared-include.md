## <a name="general"></a>Algemeen
**Vraag:** Hoe heet de Windows-service precies?  
**Antwoord**: De gateway heet 'On-premises gegevensgatewayservice' in Services

**Vraag:** Wat zijn de vereisten voor de gateway?  
**Antwoord**: Zie het gedeelte met vereisten in het [hoofdartikel over de gateway](../service-gateway-onprem.md).

**Vraag:** Welke gegevensbronnen worden met de gateway ondersteund?  
**Antwoord**: Zie de tabel met gegevensbronnen in het [hoofdartikel over de gateway](../service-gateway-onprem.md).

**Vraag:** Heb ik een gateway nodig voor cloudgegevensbronnen zoals Azure SQL Database?  
**Antwoord**: Nee. De service kan ook zonder gateway verbinding maken met een dergelijke gegevensbron.

**Vraag:** Zijn er inkomende verbindingen met de gateway vanuit de cloud?  
**Antwoord**: Nee. De gateway gebruikt uitgaande verbindingen naar Azure Service Bus.

**Vraag:** Wat gebeurt er als ik uitgaande verbindingen blokkeer? Wat moet ik openen?  
**Antwoord**: Bekijk welke [poorten](../service-gateway-onprem.md#ports) en hosts de gateway gebruikt.

**Vraag:** Moet de gateway worden geïnstalleerd op dezelfde computer als de gegevensbron?  
**Antwoord**: Nee. De gateway maakt verbinding met de gegevensbron met behulp van de opgegeven verbindingsgegevens. U kunt de gateway in dit opzicht beschouwen als een clienttoepassing. De gateway moet enkel verbinding kunnen maken met de opgegeven servernaam.

**Vraag:** Wat is de latentie voor het uitvoeren van query's in een gegevensbron vanuit de gateway? Wat is de beste architectuur?  
**Antwoord**: Het wordt aanbevolen om de gateway zo dicht mogelijk bij de gegevensbron te installeren om netwerklatentie te voorkomen. Als u de gateway op de daadwerkelijke gegevensbron kunt installeren, is de latentie minimaal. Een datacenter is ook het overwegen waard. Als uw service bijvoorbeeld het datacentrum US - west gebruikt en u SQL Server host op een virtuele Azure-machine, kunt u deze het beste ook in US - west plaatsen. Zo wordt de latentie tot een minimum beperkt en voorkomt u kosten voor uitgaand verkeer voor de virtuele Azure-machine.

**Vraag:** Zijn er vereisten voor de netwerkbandbreedte?  
**Antwoord**: Het wordt aanbevolen een netwerkverbinding met een goede doorvoer te gebruiken. Elke omgeving is anders. Veel hangt ook af van de hoeveelheid gegevens die wordt verzonden. Door ExpressRoute te gebruiken, kunt u een bepaalde doorvoer garanderen tussen on-premises en de Azure-datacenters.

U kunt een hulpprogramma van derden, de app [Azure Speed Test](http://azurespeedtest.azurewebsites.net/), gebruiken om de doorvoer te meten.

**Vraag:** Kan de Windows-gatewayservice worden uitgevoerd met een Azure Active Directory-account?  
**Antwoord**: Nee. De Windows-service moet een geldig Windows-account hebben. Standaard wordt de service uitgevoerd met de service-SID *NT SERVICE\PBIEgwService*.

**Vraag:** Hoe worden resultaten teruggezonden naar de cloud?  
**Antwoord**: Dit gebeurt via Azure Service Bus. Zie [Hoe het werkt](../service-gateway-onprem.md#how-the-gateway-works) voor meer informatie.

**Vraag:** Waar worden mijn referenties opgeslagen?  
**Antwoord**: De referenties die u voor een gegevensbron opgeeft, worden versleuteld opgeslagen in de gatewaycloudservice. De referenties worden on-premises versleuteld bij de gateway.

**Vraag:** Kan ik de gateway plaatsen in een perimeternetwerk (ook wel 'DMZ' of 'gescreend subnet' genoemd)?  
**Antwoord**: De gateway vereist een verbinding met de gegevensbron. Als de gegevensbron niet in uw perimeternetwerk toegankelijk is, kan de gateway mogelijk geen verbinding tot stand brengen. Stel dat bijvoorbeeld uw SQL Server zich niet in uw perimeternetwerk bevindt. En u kunt bijvoorbeeld uw SQL Server niet verbinden met het perimeternetwerk. Als u de gateway in uw perimeternetwerk hebt geplaatst, kan deze de SQL-server niet bereiken.

**Vraag:** Is het mogelijk de gateway te dwingen om HTTPS-verkeer met Azure Service Bus te gebruiken in plaats van TCP?  
**Antwoord**: Ja. Dit beperkt de prestaties echter aanzienlijk. Hiervoor moet u het bestand *Microsoft.PowerBI.DataMovement.Pipeline.GatewayCore.dll.config* wijzigen. Wijzig de waarde van `AutoDetect` in `Https`. Dit bestand bevindt zich in *C:\Program Files\On-premises data gateway*.

**Vraag:** Moet ik de lijst met IP-adressen van Azure-datacenters opnemen in de whitelist? Waar vind ik de lijst?  
**Antwoord**: Als u uitgaand IP-verkeer blokkeert, moet u de lijst met IP-adressen van Azure-datacenters mogelijk inderdaad opnemen in de whitelist. De gateway communiceert momenteel met Azure Service Bus via het IP-adres, in combinatie met de volledig gekwalificeerde domeinnaam. De lijst met IP-adressen van Azure-datacenters wordt wekelijks bijgewerkt. U kunt de lijst met IP-adressen van Microsoft Azure-datacenters [hier](https://www.microsoft.com/download/details.aspx?id=41653) downloaden.

```xml
<setting name="ServiceBusSystemConnectivityModeString" serializeAs="String">
    <value>Https</value>
</setting>
```

## <a name="high-availabilitydisaster-recovery"></a>Hoge beschikbaarheid/herstel na noodgevallen
**Vraag:** Zijn er plannen om scenario's voor hoge beschikbaarheid mogelijk te maken met de gateway?  
**Antwoord**: Ja, het Power BI-team is hier momenteel actief mee bezig. Houd het [Power BI-blog](https://powerbi.microsoft.com/blog/) in de gaten voor verdere updates over deze functie.

**Vraag:** Welke opties zijn er beschikbaar voor herstel na noodgevallen?  
**Antwoord**: U kunt de herstelsleutel gebruiken om een gateway te herstellen of te verplaatsen. Geef de herstelsleutel op tijdens de installatie van de gateway.

**Vraag:** Wat is het voordeel van de herstelsleutel?  
**Antwoord**: De herstelsleutel maakt het mogelijk om de gateway-instellingen te migreren of te herstellen. De sleutel wordt ook gebruikt voor herstel na noodgevallen.

## <a name="troubleshooting"></a>Problemen oplossen
**Vraag:** Waar worden de logboeken van de gateway opgeslagen?  
**Antwoord**: Zie het gedeelte over hulpprogramma's in het [artikel over het oplossen van problemen](../service-gateway-onprem-tshoot.md#tools-for-troubleshooting).

**Vraag:** Hoe kan ik zien welke query's er worden verzonden naar de on-premises gegevensbron?  
**Antwoord**: U kunt querytracering inschakelen.  Dit geeft ook inzicht in de verzonden query's. Vergeet niet om de oorspronkelijke waarde te herstellen wanneer u klaar bent met het oplossen van problemen. Als querytracering is ingeschakeld, zijn de logboeken groter.

U kunt ook kijken welke hulpmiddelen uw gegevensbron biedt om query's te traceren. Voor SQL Server en Analysis Services kunt u bijvoorbeeld Extended Events of SQL Profiler gebruiken.

