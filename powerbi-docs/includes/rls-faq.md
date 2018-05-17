## <a name="faq"></a>Veelgestelde vragen
**Vraag:** Wat als ik eerder rollen en regels hebt gemaakt voor een gegevensset in de Power BI-service? Blijven ze gewoon werken als ik niets doe?  
**Antwoord:** Nee. Visuele elementen worden niet goed weergegeven. U moet de rollen en regels opnieuw maken binnen Power BI Desktop en deze publiceren naar de Power BI-service.

**Vraag:** Kan ik deze rollen voor Analysis Services gegevensbronnen maken?  
**Antwoord:** Dat kan als u de gegevens hebt geïmporteerd in Power BI Desktop. Als u een live verbinding gebruikt, kunt u RLS niet configureren binnen de Power BI-service. Dit wordt gedefinieerd in het Analysis Services-model on-premises.

**Vraag:** Kan ik RLS gebruiken om de kolommen of metingen te beperken die toegankelijk zijn voor mijn gebruikers?  
**Antwoord:** Nee. Als een gebruiker toegang heeft tot een bepaalde gegevensrij, kan deze alle gegevenskolommen voor die rij zien.

**Vraag:** Kan ik met RLS gedetailleerde gegevens verbergen maar toegang geven tot samengevatte gegevens in visuele elementen?  
**Antwoord:** Nee, u beveiligt individuele rijen met gegevens maar gebruiker kunnen altijd de details of de samengevatte gegevens zien.

