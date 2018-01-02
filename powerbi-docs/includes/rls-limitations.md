## <a name="limitations"></a>Beperkingen
Hier volgt een lijst met de huidige beperkingen voor de beveiliging op rijniveau in cloudmodellen.

* Als u eerder rollen/regels hebt gedefinieerd binnen de Power BI-service, moet u deze opnieuw maken in Power BI Desktop.
* U kunt RLS alleen definiëren in de gegevenssets die zijn gemaakt met behulp van de Power BI Desktop-client. Als u RLS wilt inschakelen voor gegevenssets die zijn gemaakt met Excel, moet u uw bestanden eerst naar PBIX-bestanden converteren. [Meer informatie](../desktop-import-excel-workbooks.md)
* Alleen ETL en DirectQuery-verbindingen worden ondersteund. Live verbindingen met Analysis Services worden afgehandeld in het on-premises model.
* Q&A en Cortana wordt op dit moment niet ondersteund met RLS. Als voor alle modellen RLS is geconfigureerd, ziet u niet het Q&A-invoervak voor dashboards. Dit staat op de roadmap, maar er is geen tijdlijn beschikbaar.
* Extern delen wordt momenteel niet ondersteund met gegevenssets die RLS gebruiken.
* Voor een gegeven model is het maximum aantal Azure AD-principals (bijv. afzonderlijke gebruikers of beveiligingsgroepen) dat kan worden toegewezen aan beveiligingsrollen 1.000. Als u grote aantallen gebruikers aan rollen wilt toewijzen, kunt u beter beveiligingsgroepen toewijzen dan afzonderlijke gebruikers.

## <a name="known-issues"></a>Bekende problemen
Er is een bekend probleem waarbij u een foutbericht ontvangt wanneer u inhoud probeert te publiceren vanuit Power BI Desktop die eerder is gepubliceerd. Het scenario is als volgt.

1. Anna heeft een gegevensset die is gepubliceerd naar de Power BI-service en heeft RLS geconfigureerd.
2. Anna werkt het rapport bij in Power BI Desktop en publiceert opnieuw.
3. Anna ontvangt een foutbericht.

**Tijdelijke oplossing:** publiceer het Power BI Desktop-bestand opnieuw vanuit de Power BI-service totdat dit probleem is opgelost. Selecteer hiertoe **Gegevens ophalen** > **Bestanden**. 

