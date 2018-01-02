## <a name="firewall-or-proxy"></a>Firewall of proxy
Zie [Configuring proxy settings for the Power BI gateways](../service-gateway-proxy.md) (Proxy-instellingen voor de Power BI-gateways configureren) voor informatie over het aanleveren van proxygegevens voor uw gateway.

U kunt controleren of uw firewall of proxy verbindingen mogelijk blokkeert, door de opdracht [Test-NetConnection](https://technet.microsoft.com/library/dn372891.aspx) uit te voeren in een PowerShell-prompt. Deze opdracht test de verbinding met Azure Service Bus. De test heeft alleen betrekking op de netwerkverbinding, niet op de cloudserverservice of de gateway. Met deze opdracht kunt u controleren of uw computer verbinding kan maken met internet.

    Test-NetConnection -ComputerName watchdog.servicebus.windows.net -Port 9350

> [!NOTE]
> Test-NetConnection is alleen beschikbaar in Windows Server 2012 R2 en hoger. De opdracht is ook beschikbaar in Windows 8.1 en hoger. In eerdere versies van het besturingssysteem kunt u Telnet gebruiken om poortconnectiviteit te testen.
> 
> 

De resultaten moeten er ongeveer uitzien als in het volgende voorbeeld. Het verschil zit in TcpTestSucceeded. Als **TcpTestSucceeded** niet *true* is, wordt u mogelijk geblokkeerd door een firewall.

    ComputerName           : watchdog.servicebus.windows.net
    RemoteAddress          : 70.37.104.240
    RemotePort             : 5672
    InterfaceAlias         : vEthernet (Broadcom NetXtreme Gigabit Ethernet - Virtual Switch)
    SourceAddress          : 10.120.60.105
    PingSucceeded          : False
    PingReplyDetails (RTT) : 0 ms
    TcpTestSucceeded       : True

Als u grondig te werk wilt gaan, vervangt u de waarden **ComputerName** en **Port** door de waarden die worden vermeld onder [ports](../service-gateway-onprem.md#ports)

De firewall blokkeert mogelijk ook de verbindingen tussen Azure Service Bus en de Azure-datacenters. Als dat het geval is, kunt u de IP-adressen van de datacenters voor uw regio op de goedgekeurde lijst plaatsen (deblokkeren). U vindt [hier](https://www.microsoft.com/download/details.aspx?id=41653) een lijst met IP-adressen voor Azure.

