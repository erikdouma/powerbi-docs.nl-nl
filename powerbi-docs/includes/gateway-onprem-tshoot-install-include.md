## <a name="update-to-the-latest-version"></a>Bijwerken naar de nieuwste versie
Er kunnen zich allerlei problemen voordoen als de gatewayversie verouderd is.  Het is een goede en gangbare praktijk om ervoor te zorgen dat u de nieuwste versie gebruikt.  Als u de gateway een maand of langer niet hebt bijgewerkt, kunt u de nieuwste versie van de gateway te installeren en te kijken of het probleem zich nog steeds voordoet.

## <a name="common-issues"></a>Veel voorkomende problemen
Hier volgen enkele veelvoorkomende problemen en oplossingen die enkele klanten hebben gebruikt in omgevingen die de toegang tot internet beperken.

### <a name="authentication-to-proxy-server"></a>Verificatie bij de proxyserver
De proxy vereist mogelijk dat het domeingebruikersaccount wordt geverifieerd. De gateway gebruikt standaard een service-SID voor de Windows-service Gebruiker aanmelden. Mogelijk helpt het om de aanmeldingsgebruiker te wijzigen in een domeingebruiker. Zie [De gatewayserviceaccount wijzigen in een domeingebruiker](../service-gateway-proxy.md#changing-the-gateway-service-account-to-a-domain-user) voor meer informatie.

### <a name="your-proxy-only-allows-ports-80-and-443-traffic"></a>De proxy staat alleen verkeer van poort 80 en 443 toe
Bepaalde proxy's beperken het verkeer tot alleen de poorten 80 en 443. De communicatie met Azure Service Bus verloopt standaard via andere poorten dan poort 443.

U kunt forceren dat de gateway met Azure Service Bus communiceert via HTTPS in plaats van direct via TCP. Hiervoor moet u het bestand *Microsoft.PowerBI.DataMovement.Pipeline.GatewayCore.dll.config* wijzigen. Wijzig de waarde van `AutoDetect` in `Https`. Dit bestand bevindt zich in *C:\Program Files\On-premises data gateway*.

```
<setting name="ServiceBusSystemConnectivityModeString" serializeAs="String">
    <value>Https</value>
</setting>
```

## <a name="installation"></a>Installatie
### <a name="error-failed-to-add-user-to-group---2147463168---pbiegwservice---performance-log-users---"></a>Fout: kan de gebruiker niet toevoegen aan de groep.  (-2147463168   PBIEgwService   Prestatielogboekgebruikers)
Deze fout kan optreden als u de gateway probeert te installeren op een domeincontroller. De implementatie op een domeincontroller wordt niet ondersteund. U moet de gateway implementeren op een computer die geen domeincontroller is.

### <a name="installation-fails"></a>Kan niet installeren
U komt mogelijk installatiefouten tegen als de antivirussoftware op de installatiemachine is verouderd. U kunt ofwel de antivirusinstallatie bijwerken of de antivirussoftware alleen gedurende het voltooien van de gatewayinstallatie uitschakelen en daarna weer inschakelen.

