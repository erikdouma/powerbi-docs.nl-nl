## <a name="limitations"></a>Beperkingen
Hier volgt een lijst van de huidige beperkingen voor beveiliging op rijniveau voor cloudmodellen.

* Als u eerder rollen en regels hebt gedefinieerd binnen de Power BI-service, moet u deze rollen opnieuw maken binnen Power BI Desktop.
* U kunt RLS alleen definiëren in de gegevenssets die zijn gemaakt met behulp van de Power BI Desktop-client. Als u RLS wilt inschakelen voor gegevenssets die zijn gemaakt met Excel, moet u uw bestanden eerst naar PBIX-bestanden converteren. [Meer informatie](../desktop-import-excel-workbooks.md)
* Alleen ETL- en DirectQuery-verbindingen worden ondersteund. Live verbindingen met Analysis Services worden afgehandeld in het on-premises model.
* Q&A en Cortana wordt op dit moment niet ondersteund met RLS. Als voor alle modellen RLS is geconfigureerd, ziet u niet het Q&A-invoervak voor dashboards. Dit staat op de roadmap, maar er is geen tijdlijn beschikbaar.
* Extern delen wordt momenteel niet ondersteund met gegevenssets die RLS gebruiken.
* Voor elk gegeven model is het maximale aantal Azure AD-principals (dat is, individuele gebruikers van beveiligingsgroepen) dat kan worden toegewezen aan beveiligingsrollen 1000. Als u grote aantallen gebruikers aan rollen wilt toewijzen, kunt u beter beveiligingsgroepen toewijzen dan afzonderlijke gebruikers.

## <a name="known-issues"></a>Bekende problemen
Er is een bekend probleem waarbij er een foutmelding optreedt wanneer u probeert te publiceren vanuit Power BI Desktop als dit al eerder is gepubliceerd. Het scenario is als volgt.

1. Anna heeft een gegevensset die is gepubliceerd naar de Power BI-service en heeft RLS geconfigureerd.
2. Anna werkt het rapport bij in Power BI Desktop en publiceert opnieuw.
3. Anna krijgt een foutmelding.

**Tijdelijke oplossing:** publiceer het Power BI Desktop-bestand opnieuw vanuit de Power BI-service totdat dit probleem is opgelost. U kunt dat doen door **Gegevensbestanden** > **ophalen** te selecteren. 

