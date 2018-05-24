Met Power BI kunt u relaties tussen meerdere tabellen maken, zoals voor tabellen die uit verschillende gegevensbronnen afkomstig zijn. U kunt deze relaties voor elk gegevensmodel bekijken in de weergave **Relaties** van Power BI Desktop.

![](media/7-5-table-relationships-and-dax/dax-relationships_1.png)

## <a name="dax-relational-functions"></a>Relationele DAX-functies
DAX bevat **relationele functies** waarmee u tabellen met relaties kunt gebruiken.

U kunt de waarde van een kolom of alle rijen in een relatie retourneren met DAX-functies.

De functie **TABEL** bijvoorbeeld volgt relaties en retourneert de waarde van een kolom, terwijl de functie **RELATEDTABLE** relaties volgt en een hele tabel retourneert die is gefilterd, zodat alleen gerelateerde rijen worden opgenomen.

![](media/7-5-table-relationships-and-dax/dax-relationships_2.png)

De functie **RELATED** werkt aan *veel-op-een-* relaties, terwijl de functie **RELATEDTABLE** is bedoeld voor *een-op-veel*relaties.

U kunt relationele functies gebruiken om expressies te bouwen die waarden tussen meerdere tabellen bevatten. DAX retourneert een resultaat met deze functies, ongeacht de lengte van de keten van de relatie.

> Met dank aan [Alberto Ferrari, SQLBI](http://www.sqlbi.com/learning-dax/?utm_source=powerbi&utm_medium=marketing&utm_campaign=after-summit) voor de video
> 
> 

