##C# Properties - get/ set##
###De basis van C# properties###
In C # gebruiken we de properties om een klasse attribuut of berekening in te kapselen. Ze bevatten meestal accessor- en mutator-methoden (getters en setters) voor de klasse attributen. Attributen zijn variabelen binnen de klasse die de status van een object weergeven. Properties stellen ons in staat om inkapseling af te dwingen voor voor alle code buiten de klasse. Deze code laten we verwijzen naar de klasse properties in plaats van rechtstreeks naar de klasse attributen.

Hier een eenvoudig voorbeeld.

```C#
public class Car
{
  private string _mark;
  public string Mark
  {
    get { return _mark; }
    set { _mark = value; }
  }

  private string _model;
  public string Model
  {
    get { return _model; }
    set { _model = value; }
  }

  public string FullName
  {
    get { return Mark + " " + Model; }
  }
}
```

In bovenstaand voorbeeld zijn de twee private attributen (_make en _model) ingekapseld in hun eigen publieke propertie. Er is een derde propertie gemaakt (*'FullName*') die de andere twee properties gebruikt. Omdat het alleen de propertie *'FullName'* een "get" -blok heeft, wordt het ook beschouwd als een *"read-only"* propertie. Het sleutelwoord *"value"* wordt gebruikt om een waarde toe te kennen aan het private attribute dat door de propertie wordt inkapseld.

Hier de voorbeeld code die gebruik maakt van de klasse en zijn properties.

```C#
class Program
{
  private static void Main()
  {
    Car firstCar = new Car();
    firstCar.Mark = "Volkswagen";
    firstCar.Model = "Golf";
    Console.WriteLine("Mijn eerste auto was een {0}.", firstCar.FullName);
  }
}
```

De voordelen van het gebruik van properties:

- Er is een fijnere toegangscontrole mogelijk met properties. Moet een attribute wel bereikbaar buiten de klasse maar niet kunnen worden gewijzigd? Zet dan de get accessor op public en laat de set mutator weg. 
- Wil je de debugger laten stoppen als er de attribute waarde veranderd? Zet een breakpoint in de set mutator van de propertie.
- Wil je de alle leesacties op een propertie loggen. Voeg een logfunctionaliteit toe in de get accessor van de propertie.
- Properties kunnen worden gebruikt voor data binding; attributen niet.

###Automatische generatie van Properties###
Om een private attribute te definieren en een bijbehorende en volledige uitgeschreven propertie te maken neemt veel tekstruimte in beslag in je code. Dit is niet erg efficient als er geen logica in de getter  en setter zijn toegevoegd. Automatisch gegenerereerde  properties geven ons de mogelijkheid om eeen private attribute en propertie te defineren in een enkele regel code.

```C#
public int CurrentSpeed { get; set; }
```

Let op dat je in deze constructie geen *“read-only”* of *“write-only”* propertie kunt definieren. De compiler genereert een hidden private attribute, maar dit attribute is niet toegankelijk vanuit de code.

Wanneer later logica aan de automatisch gegenereeerde property wordt toevoegd dan moet de propertie worden geconverteerd naar een volledig uitgeschreven propertie. Omdat echter de propertie naam niet veranderd, zal code die de klasse met automatische genereerde properties gebruikt,  blijven werken. De interface van de klasse is namelijk niet veranderd. Er zal een intern private attribute moeten worden toegevoegd aan de klasse, maar deze nieuwe attribute heeft geen consequenties voor de publieke en interne interface van de klasse.

### Visual Studio Support

Visual Studio heeft een aantal handige snippets om het definieren van properties te vergemakkelijken. 
Type *'pro'* in je code venster en selecteer de betreffende snippet. Klik twee keer op de  <Tab> toets om de betreffende propertie te genereren. 

<img src="http://www.intertech.com/Blog/wp-content/uploads/2014/05/2014-05-06_16-05-53.png">
