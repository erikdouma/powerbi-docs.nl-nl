## <a name="faq"></a>Veelgestelde vragen
**Vraag:** Wat gebeurt er als ik eerder rollen/regels heb gemaakt voor een gegevensset in de Power BI-service? Blijven ze gewoon werken als ik niets doe?  
**Antwoord:** Nee. Visuele elementen worden niet goed weergegeven. U moet de rollen/regels opnieuw maken in Power BI Desktop en vervolgens publiceren naar de Power BI-service.

**Vraag:** Kan ik deze rollen maken voor gegevensbronnen van Analysis Services?  
**Antwoord:** Dat kan als u de gegevens hebt geïmporteerd in Power BI Desktop. Als u een live verbinding gebruikt, kunt u RLS niet configureren binnen de Power BI-service. Dit wordt gedefinieerd in het Analysis Services-model on-premises.

**Vraag:** Kan ik RLS gebruiken om de kolommen of metingen te beperken die toegankelijk zijn voor mijn gebruikers?  
**Antwoord:** Nee. Als een gebruiker toegang heeft tot een bepaalde gegevensrij, kan deze alle gegevenskolommen voor die rij zien.

**Vraag:** Staat RLS mij toe om gedetailleerde gegevens te verbergen, maar toegang te krijgen tot gegevens die zijn samengevat in visuele elementen?  
**Antwoord:** Nee, u beveiligt afzonderlijke gegevensrijen, maar gebruikers kunnen altijd de details of samengevatte gegevens zien.

