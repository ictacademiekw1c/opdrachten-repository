####[kleurcode]rgba(239,108,0,1)

# ADO

## Koppelingen met een SQL database

In deze sectie gaan we specifiek in op de verbinding met een SQL database. Deze verbinding maken onderhouden en data over uitwisselen is een taak van de **Data Access Layer**.

- De **Data Access Layer** is de laag die verbinding de opslag van de data verzorgd. Dit kan op diverse manieren gebeuren zoals lokale DataSets, SQL databases of XML bestanden. Alle specifieke programma code die nodig is om de administratie in deze systemen te verzorgen is in deze laag opgenomen. 



Keywords: ***SqlConnection, configurationStrings, ConfigurationManager, SqlCommand, DataAdapter, DataReader***



## Verbinden met een SQL Server

De .NET Framework Data Provider voor SQL Server gebruikt een  [SqlConnection](<https://docs.microsoft.com/en-us/dotnet/api/system.data.sqlclient.sqlconnection?view=netframework-4.8>) klasse om een verbinding te maken naar een SQL database. De klasse heeft een aantal methods en properties tot beschikking Om de verbinding op te bouwen en te sluiten.

| Property               | Description                                                  |
| ---------------------- | ------------------------------------------------------------ |
| ```ConnectionString``` | Verbindings string voor de database. Bevat het pad naar de server, de database naam en de inloggevens op de database |

| Methods       | Description                                                  |
| ------------- | ------------------------------------------------------------ |
| ```Open()```  | Object opent de verbinding met de database. Hierbij wordt gebruik gemaakt van de inloggevens die beschreven zijn in de ConnectionString. |
| ```Close()``` | Object sluit de verbinding met de database. <br>**Let op: sluit altijd de verbinding als je hem niet meer nodig hebt.** |

De volgende code geeft een voorbeeld van het creeren en openen van een verbinding met een SQL Server database. Hier wordt de connectionstring al meegegeven met de constructor van het connection object.

```c#
// Er van uitgaand dat de connectionString een geldige connection string is.  
using (SqlConnection connection = new SqlConnection(connectionString))  
{  
    connection.Open();  
    // Voer de verdere code uit op de database.  
}
```

Als de [SqlConnection](https://docs.microsoft.com/en-us/dotnet/api/system.data.sqlclient.sqlconnection?view=netframework-4.7.2) niet meer gebruikt wordt, wordt het niet automatisch gesloten. De connection moet expliciet door het programma worden gesloten door de commando's `Close` of  `Dispose` aan te roepen. `Close en` `Dispose` zijn functioneel identiek . 

Om te waarborgen dat een verbinding altijd wordt gesloten wordt de verbinding binnen een `using` blok geopend, zoals te zien is in bovenstaand code fragment. Door de code in een `using` block te zetten zijn we er zeker van dat de verbinding automatisch wordt gesloten als het programma het blok verlaat..

## Connection Strings en Configuration bestand

Connection strings die zijn opgenomen in de applicatie code kunnen leiden tot veiligheids risico's en onderhouds problemen. Unencrypted connection strings in de code van de applicaties kunnen met disassembleer tools worden uitgelezen en worden misbruikt. 

Verder heb je een onderhoudsprobleem als de connection string regelmatig wijzigd. Iedere keer dat de connection string wijzigd moet de code weer opnieuw gebouwd en gedistrubeerd worden. Om deze redenen is gaan we de connection strings opslaan in een applicatie configuratie bestand. 

In Windows applicatie is de App.config het configuratie bestand waar we de connection string kunnen opslaan. In dit configuratie bestand worden meer configuratie ondewerpen komen te staan. Het configuratiebestand bestaat uit XML tags om de verschillende secties te kunnen onderscheiden.

### De connectionStrings Section

Connection strings kunnen worden opgeslagen in key/value paren in de **connectionStrings** subsectie van de **configuration** sectie van het applicatie configuratie bestand. In de connectionStrings secties dkunnen de de commando's  **add**, **clear**, en **remove** worden gebruikt.

In het volgende configuratie file fragment is een voorbeeld weergegeven van een connection string. De **name** attribute is de unieke naam die je geeft aan de connection string om de connection string tijdens de uitvoering van het programma op te vragen. De **providerName** is naam van de .NET Framework data provider, die is geregistreerd in het machine.config bestand. In 

```xml
<?xml version='1.0' encoding='utf-8'?>  
  <configuration>  
    <connectionStrings>  
      <clear />  
    <add name="MyConnectionString"
         connectionString="Data Source=PROBOOK\SQLEXPRESS;Initial Catalog=Leerlinggegevens;Integrated Security=True"
         providerName="System.Data.SqlClient" />
    </connectionStrings>  
  </configuration>
```

Om de connection string in te kunnen lezen in de code gebruiken we de **ConfigurationManager**.
Deze **ConfigurationManager** is niet standaard beschikbaar in je code en zul je moeten toevoegen aan je bestand via de volgende code 

`using System.Configuration`

**LET OP!** kent je project **System.Configuration** niet voeg deze dan toe via je project **References** in je Solution Explorer. (Rechter muis klik op *References*, *Add Reference*' en zoek op '*Configuration*'. Zet vinkje voor de bibliotheek en druk op OK)

ConfigurationManager heeft 2 properties:

AppSettings
ConnectionStrings

Hiermee lees je de secties uit.
Je kunt meerdere connectionStrings hebben dus je moet deze ConnectionString is dus een list van ConnectionStrings.

Om je connectionstring te gebruiken in de code gebruik je de Configuration Settings Class.:

```
string connectionString = ConfigurationManager.ConnectionStrings["myConnectionString"].ConnectionString;
```

##   Versturen van een Sql commando

De .NET Framework Data Provider voor SQL Server gebruikt een  [SqlCommand](https://docs.microsoft.com/en-us/dotnet/api/system.data.sqlclient.sqlcommand) klasse om data naar een SQL database te sturen. De klasse heeft een aantal methods en properties tot beschikking heeft om SQL commando's uit te voeren. De keuze welk commando geschikt is afhankelijk van het type commando en de gewenste return waarde van de SQL database. 

| Property          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| ```Connection```  | Het *SqlConnection* object wat gebruikt wordt om het Sql commando te versturen. |
| ```CommandType``` | Geeft het type command aan zie voor onderstaande lijst welke CommandTypes er zijn. |
| ```CommandText```  | De commando tekst die naar de Sql server wordt verstuurd. De keuze welk commando geschikt is afhankelijk van het type commando en de gewenste return waarde van de SQL database. |

Ieder strongly typed command object ondersteund ook de [CommandType](https://docs.microsoft.com/en-us/dotnet/api/system.data.commandtype) enumeration die specificeerd hoe de command string moet worden geinterpreteerd, zoals beschreven in de volgende tabel.

| CommandType       | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| `Text`            | An SQL command defining the statements to be executed at the data source. |
| `StoredProcedure` | De naam van een stored procedure. Je kunt de  `Parameters` propertie van het command gebruiken om toegang te krijgen tot de input en output parameters en return waarden, ongeacht welk `Execute` method wordt aangeroepen. Wanneer `ExecuteReader` wordt gebruikt zijn de return waarde en de output parameters niet toegankelijk totdat de `DataReader` is gesloten. |
| `TableDirect`     | De naam van een tabel.                                       |



| Methos    | Return Value                                                 |
| ------------------ | ------------------------------------------------------------ |
| `ExecuteReader()`  | Geeft een `DataReader` object terug.                         |
| `ExecuteScalar()`    | Geeft een enkele scalar waarde terug.                        |
| `ExecuteNonQuery()`  | Voert het commando uit en geeft geen rij inhoud terug.       |
| `ExecuteXMLReader()` | Geeft een  [XmlReader](https://docs.microsoft.com/en-us/dotnet/api/system.xml.xmlreader) object terug. Dit is alleen beschikbaar voor het `SqlCommand` object. |

## Voorbeeld

 ```c#
static void GetSalesByCategory(string connectionString, 
    string categoryName)
{
    using (SqlConnection connection = new SqlConnection(connectionString))
    {
        // Create the command and set its properties.
        SqlCommand command = new SqlCommand();
        command.Connection = connection;
        command.CommandText = "SalesByCategory";
        command.CommandType = CommandType.StoredProcedure;

        // Add the input parameter and set its properties.
        SqlParameter parameter = new SqlParameter();
        parameter.ParameterName = "@CategoryName";
        parameter.SqlDbType = SqlDbType.NVarChar;
        parameter.Direction = ParameterDirection.Input;
        parameter.Value = categoryName;

        // Add the parameter to the Parameters collection. 
        command.Parameters.Add(parameter);

        // Open the connection and execute the reader.
        connection.Open();
        SqlDataReader reader = command.ExecuteReader();

        if (reader.HasRows)
        {
            while (reader.Read())
            {
                Console.WriteLine("{0}: {1:C}", reader[0], reader[1]);
            }
        }
        else
        {
            Console.WriteLine("No rows found.");
        }
        reader.Close();
    }
}
 ```



### Interessante bronnen

- [Connection strings and configuration files](https://docs.microsoft.com/en-us/dotnet/framework/data/adonet/connection-strings-and-configuration-files)
- [Execute a Command](https://docs.microsoft.com/en-us/dotnet/framework/data/adonet/executing-a-command) - Microsoft ADO.NET
- [DataAdapters and DataReaders](https://docs.microsoft.com/en-us/dotnet/framework/data/adonet/dataadapters-and-datareaders) - Microsoft ADO.NET
- [ADO.NET data provider examples](https://docs.microsoft.com/en-us/dotnet/framework/data/adonet/ado-net-code-examples#adonet-data-provider-examples) - Microsoft ADO.NET
- [Populating a DataSet from a DataAdapter](https://docs.microsoft.com/en-us/dotnet/framework/data/adonet/populating-a-dataset-from-a-dataadapter) - Microsoft ADO.NET
- [WinForms ADO.net](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2008/Productie/01.%20Reader/0012_Reader%20C-Sharp%20V7.0%20-%20ADO.NET.pdf) - Reader "Programmeren in C#"
- [WinForms werken met datasets](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2008/Productie/01.%20Reader/0013_Reader%20C-Sharp%20V7.0%20-%20Werken%20met%20datasets.pdf) - Reader "Programmeren in C#"
- [WinForms 3- Tier](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2008/Productie/01.%20Reader/0016_Reader%20C-Sharp%20V7.0%20-%20Software%20architectuur.pdf) - Reader "Programmeren in C#"