

#List <T> Klasse#
Collection klassen zijn een groep van klassen speciaal ontworpen om objecten te groeperen en specifieke taken hierop uit te voeren. De *List* klasse is een verzameling van objecten en gedefineerd in de *System.Collections.Generic* namespace en voorziet de gebruiker in methods en properties zoals *add*, *insert*, *remove*, *search* etc. *Lists* zijn een vervanging voor *arrays*, *linked lists*, *queues*, en andere 1-dimensionale data structuren. De *List* klasse heeft allerlei extra functionaliteit, waaronder het dynamisch  kunnen wijzigen van de grootte .

In C# de klasse *List < T >* representeerd een strongly typed lijst van objecten en kan worden benaderd met een index. De klasse *List <T>* ondersteund verschillende datatype zonder dat daarvoor het te verzamelen object ge-cast hoeft te worden. 

### Definitie:

**List < T >**

De parameter **T** geeft het type aan van de elementen in de lijst.

## Methods en properties

###Elementen toevoegen aan een List Collection###

In het volgende voorbeeld worden *Integer* waarden toegevoegd aan een *List Collection*

```c#
List<int> iList = new List<int>();
iList.Add(2);
iList.Add(3);
iList.Add(5);
iList.Add(7);
```

In het volgende voorbeeld worden *String* waarden toegevoegd aan een *List Collection*

```c#
List<string> colors = new List<string>();
colors.Add("Red");
colors.Add("Blue");
colors.Add("Green");
```

###Hoeveel elementen zitten er in de List Collection?###

De *List* klasse bevat een **Count** property die het aantal elementen of de lengte van de *List Collection* weergeeft.

```c#
colors.Count
```
###Elementen uit de List Collection halen###
Elementen worden typisch uit de *List* *Collection* gehaald doormiddel van loops.

**for loop**

```c#
for (int i = 0; i < colors.Count; i++)
{
    MessageBox.Show(colors[i]);
}
```

**foreach loop**

```c#
foreach (string color in colors)
{
    MessageBox.Show(color);
}
```

###Elementen aan een List Collection toevoegen###
Met de method **insert(index,element)** wordt een element toegevoegd aan de *List Collection* op een specifieke index.

```c#
colors.Insert(1, "violet");
```
In bovenstaande code wordt de kleur "violet" aan de *List Collection* toegevoegd op de index positie 1.

###Elementen in een List Collection sorteren###

Met de method **Sort()** wordt de elementen in de *List Collectie* georderend .

```c#
colors.Sort();
```

###Element verwijderen van een List Collection###

Met de method **Remove()** wordt een element te verwijderen uit een *List collection*.

```c#
colors.Remove("violet");
```

###Bevat een List Collection een specifiek element###

Met de method **Contains()** wordt gecontrolleerd of een element bestaat in de *List Collection*.

```c#
if (colors.Contains("Blue"))
{
    MessageBox.Show("Blue color exist in the list");
}
```

###Een Array kopieeren naar een List Collection###

```c#
string[] strArr = new string[3];
strArr[0] = "Red";
strArr[1] = "Blue";
strArr[2] = "Green";

//here to copy array to List
List<string> arrlist = new List<string>(strArr);
```
###Een List Collection naar een String converteren ###

Met de *String* method **Join()** wordt een *List Collection* geconverteerd naar een *string*.

```c#
string combinedString = string.Join(",", colors);
```
Na het uitvoeren van bovenstaand statement bevat de variabele *combinedString* de waarde: "Red,Blue,Green"

In plaats van "," kan elk ander karakter als scheidingsteken worden gebruikt.

###Een List Collection naar een Array converteren ###

Met de method **toArray()** wordt een *List Collection* naar een Array geconverteerd.

```c#
string[] arr = colors.ToArray();
```
###Een List Collection leeg maken###

Met de method **Clear()** worden **alle** elementen uit de *List Collection* verwijderd.

```c#
arrlist.Clear ();
```
## LINKS

[How about lists](http://csharp.net-informations.com/collection/list.htm) - Csharp_net