## <a name="using-the-username-or-userprincipalname-dax-function"></a>De DAX-functie username() of userprincipalname() gebruiken
U kunt gebruik maken van de DAX-functies *username()* of *userprincipalname()* binnen uw gegevensset. U kunt deze gebruiken in expressies in Power BI Desktop. Wanneer u uw model publiceert, worden deze functies gebruikt in de Power BI-service.

In Power BI Desktop retourneert de functie *username()* een gebruiker met de indeling *DOMEIN\gebruiker* en retourneert de functie *userprincipalname()* een gebruiker met de indeling  <em>user@contoso.com</em>.

In de Power BI-service retourneren zowel *username()* als *userprincipalname()* de UPN (User Principal Name) van de gebruiker. Dit lijkt op een e-mailadres.

