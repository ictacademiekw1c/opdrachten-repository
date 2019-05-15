

#DataSets#

In C# werken we nooit rechtstreeks met een database. Een database bevindt zich net zoals andere bronnen van data (*DataSources* of gegevensbronnen), altijd buiten het programma. Binnen het programma werken we met een *DataSet*, en die ziet er net zo uit als de tabellen van een relationele database.

```C#
De DataSet onderhoudt de verbindingen met de DataSources. Een DataSource kan een database zijn maar ook een XML-bestand, een spreadsheet of een willekeurig ander bestand
```

Hiermee is meteen duidelijk waarom men een *DataSet* bedacht heeft: je kunt op deze manier gegevens van allerlei *DataSources* eenvoudig in een programma combineren.

Het programma maakt gebruik van de gegevens in de *DataSet*.

Een *DataSet* bestaat uit *DataTables*. Een *DataTable* werkt net zoals een tabel in een database. Alleen bevindt een tabel zich in een database en een *DataTable* staat in een *DataSet*.

Een *DataSet* bestaat alleen in het interne geheugen en dat betekent dat zodara je het programma beeindigd alle gegevens weg zijn. Je moet er zelf voor zorgen dat de gegevens vanuit de *DataSet* weer opgeslagen worden in de oorspronkelijke *DataSources*.



## Funtionaliteiten

###Aanmaken DataSet###

Een lege *DataSet* wordt aangemaakt met een constructor

```c#
DataSet dsLeerlingen = new DataSet();
```

###Aanmaken DataTable###

In een *DataSet* moet een *DataTables* worden aangemaakt waarin de informatie kan worden opgeslagen.  In onderstaand voorbeeld voegen we *DataTable* toe aan de *DataSet*.

```c#
DataSet dsLeerlingen = new DataSet("tblLeerling");
// of
DataSet dsLeerlingen = new DataSet();
ds.Leerlingen.Tables.Add("tblLeerling");
```

De opgegeven naam is de naam eigenschap van de tabel.

###Aanmaken DataColums###

In de table moeten kolomen worden aangemaakt om de data in te kunnen opslaan.


```c#
DataColumn Naam = new DataColumn("Naam",typeof(string));
dsLeerling.Table("tblLeerling").Columns.Add(Naam);
// of
dsLeerling.Table("tblLeerling").Columns.Add("Naam",typeof(string));
dsLeerling.Table("tblLeerling").Columns.Add("LeerlingNummer",typeof(in32));

```

###Instellen van een primary key###
```c#
dsLeerling.Table("tblLeerling").PrimaryKey = new DataColumn[] {LeerlingNummer};
```
In bovenstaande code wordt de kleur "violet" aan de *List Collection* toegevoegd op de index positie 1.

###Tabel rijen vullen met data###

Als de kolomen zijn gedefinieerd dan kunnen we de tabel gaan vullen .

```c#
dsLeerling.Tables["tblLeerling"].Rows.Add("Henk", 1234, "IO2A4"", "man";
```

###Tabel rij verwijderen###

Met de method **.Delete()** wordt een rij verwijderd uit de*DataTable*.

```c#
foreach(DataRow dr in dsLeerling.Tables["tblLeerling"].Rows)
{
    if(dr["LeerlingNummer"].ToString()=="123")
    dr.Delete();
}
```

## Interessante bronnen

[DataSets, DataTables, and DataViews](https://docs.microsoft.com/en-us/dotnet/framework/data/adonet/dataset-datatable-dataview/) - Microsoft Docs