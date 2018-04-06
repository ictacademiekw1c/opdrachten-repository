####[kleurcode]rgba(239,108,0,1)

##Coding Conventions##
•	Gebruik *PascalCasing* voor de namen van klassen en methoden.

```C#
public class ClientActivity
{
    public void ClearStatistics()
    {
        //...
    }
    public void CalculateStatistics()
    {
        //...
    }
}
```

* Gebruik *CamelCasing* voor de parameters van methoden, lokale variabelen en voor de instantie van classes.

```C#
public class UserLog
{
   public void Add(LogEvent logEvent)
    {
        int itemCount = logEvent.Items.Count;
        // ...
    }
}

UserGroup userGroup;
Assignment employeeAssignment;
CustomerId customerId;
XmlDocument xmlDocument;
FtpHelper ftpHelper;
UriPart uriPart;
HtmlHelper htmlHelper;
FtpTransfer ftpTransfer;
UIControl uiControl;
```

* Gebruik *géén underscore* (onderstreepte spatie) in namen. Uitzondering: Je mag een onderstreepte spatie streepje gebruiken als prefix van statische variabelen.

```C#
public DateTime clientAppointment;
public TimeSpan timeLeft;
private DateTime _registrationDate;
```

* Gebruik de standaard gedefinieerde typenamen (string, int, bool) in plaats van de system typenamen zoals Int16, Single, UInt64, etc.

```C#
string firstName;
int lastIndex;
bool isSaved;
```

* Gebruik zelfstandige naamwoorden of zelfstandig naamwoord-zinnen voor de naam van een klasse.

```C#
public class Employee
{
}

public class BusinessLocation
{
}

public class DocumentCollection
{
}
```

* Lijn alle accolades verticaal uit: zet ze netjes onder elkaar. Spring binnen de accolades in met tabs van 4 spaties.

```C#
class Program
{
    static void Main(string[] args)
    {
    }
}
```

* Declareer alle variabelen bovenin de klasse. 

```C#
public class Account
{
    public string Number {get; set;}
    public DateTime DateOpened {get; set;}
    public DateTime DateClosed {get; set;}
    public decimal Balance {get; set;}
 
    // Constructor
    public Account()
    {
        // ...
    }
}
```

**Begrippen**
* Pascal case
	Eén woord maken van afzonderlijke woorden die met een hoofdletter beginnen.
	Voorbeeld: **Gekookte Eieren Eten** wordt in *PascalCasing*: **GekookteEierenEten**.

* Camel case
	Is gelijk aan *Pascal case*, maar de eerste letter van het eerste woord is altijd een kleine letter.
	Voorbeeld: **Gekookte Eieren Eten** wordt in *CamelCasing*: **gekookteEierenEten**.

