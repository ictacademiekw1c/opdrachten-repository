

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
## Interessante bronnen

[How about lists](http://csharp.net-informations.com/collection/list.htm) - Csharp_net

# WinForms ListView Klasse #

## Verschillende Views ##

De *ListView* klasse heeft verschillende verschijningsvormen. Dit is te vergelijken met je file explorer in Windows. Je kunt de *View* propertie op verschillende weergaven zetten zoals: *Large Icons*, *SmallIcons*, *Details*, *List* en *Tile*. Het is belangrijk als je meerdere kolommen dat wil weergeven dat je de View van een ListView op ***Detail*** zet.

## Meerdere kolommen.
Om een detail lijst weer te geven moet je de kolommen definiëren van een *ListView*. Tip: om een kolom van een listview op automatisch te laten meeschalen moet de tweede parameter van *Columns.Add*. op -2 worden gezet. Voorbeeld (kijk naar de opmerkingen op het einde van het code voorbeeld)

```c#
private void initListView()
{
    // Add columns
    lvPersons.Columns.Add("Id", -2,HorizontalAlignment.Left);
    lvPersons.Columns.Add("Name", -2, HorizontalAlignment.Left);
    lvPersons.Columns.Add("Age", -2, HorizontalAlignment.Left);
}
```

Je kunt ook gebruik maken van overload functies van *Add*, *Add(string)*. Bijvoorbeeld:
```c#
lvPersons.Columns.Add("Id");
lvPersons.Columns.Add("Name");
lvPersons.Columns.Add("Age");
```
## Hoe voeg je data toe aan een ListView

Om data toe te voegen aan een *ListView*, moet je eerste een instantie van de klasse *ListViewItem* creëren. Deze *ListViewItem* vul je met data en deze voeg je daarna met de *Add* Method toe aan de *ListView*'s Items lijst.

Het *ListViewItem* bestaat uit een wat aparte structuur. Het hoofd data element is de propertie Text. De overige kolommen in een ListView zijn in de definitie van het ListView element, details van deze tekst. De details zitten opgeslagen in een lijst van SubItems.  Om data in deze subitems te plaatsen moet je de Add method van de SubItems gebruiken.

```
ListViewItem item1 = new listViewItem{Text="123"}
item1.SubItems.Add("Tom");
item1.SubItems.Add("24");
lvPersons.Items.Add(item1);
```

Het interessante is dat *SubItem*[0] de *Text* propertie is en de overige kolommen in de daarop volgende subItem indexen worden geplaatst. Dus in bovenstaand voorbeeld zijn de properties van item 1 gevuld met de volgende data: 

```
item1.Text ="123", item1.SubItems[0] = "123", item1.SubItems[1]="Tom" en item1.SubItems[2]="24"
```

In plaats van met de *Text* en  *SubItems* lijst te werken kun je ook gebruik maken van  *string[]* constructor.

```c#
ListViewItem item1 = new ListViewItem(new[] {"id123", "Tom", "24"});
ListViewItem item2 = new ListViewItem(new[] {person.Id, person.Name, person.Age});
lvPersons.Items.Add(item1);
lvPersons.Items.Add(item2);
```
## Uitgewerkt voorbeeld
![]()

```c#
/************************** Module Header *******************************\
Project:		Demo ListView
Auteur:			Bart Linsen
Aanmaakdatum:   9 mei 2019
Module naam:	ListViewExample.cs

Omschrijving:	Voorbeeld hoe je een listview moet gebruiken in Detail View

\************************************************************************/
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace Hfst03_ListViewExample
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }
        private void Form1_Load(object sender, EventArgs e)
        {
            #region ListView Example Designer
            // ****************** Code hoort in ListViewExamples.Designer.cs
            // Belangrijk om View.Details te kiezen voor meerdere kolomen View
            listView1.View = View.Details; 
            listView1.GridLines = true;
            listView1.FullRowSelect = true;
            listView1.MultiSelect = false;

            // Add column headers b!!!
            // Bij View.Details moeten de kolomen worden aangemaakt!!!!
            listView1.Columns.Add("ProductName", 100);
            listView1.Columns.Add("Price", 70);
            listView1.Columns.Add("Quantity", -2);

            // ***************************************************************
            #endregion

            // Add items to the listview

            // Add first item
            // Add strings direct in ListViewItem structure
            ListViewItem newItem0 = new ListViewItem()
            {
                Text = "product_0",
            };
            newItem0.SubItems.Add("00");
            newItem0.SubItems.Add("0");
            listView1.Items.Add(newItem0);    

            string[] arrayOfProducts = new string[3];
            ListViewItem newItem1;

            // Add second 
            // make use of an array of strings
            arrayOfProducts[0] = "product_1";
            arrayOfProducts[1] = "100";
            arrayOfProducts[2] = "10";
            // Constructor
            newItem1 = new ListViewItem(arrayOfProducts);
            listView1.Items.Add(newItem1);


            // Add third and fourth
            // Short versions of array of strings ;-)
            listView1.Items.Add(new ListViewItem(new string[] { "product_3", "300", "30" }));
            listView1.Items.Add(new ListViewItem(new [] { "product_4", "400", "40" }));

        }

        private void button1_Click(object sender, EventArgs e)
        {
            // Declaratie
            string productName = null;
            string price = null;
            string quantity = null;
            
            // UI
            if (listView1.SelectedIndices.Count==0)
            {
                MessageBox.Show("Geen product geselecteerd");
            }
            else
            {
                // Initialisatie
                productName = listView1.SelectedItems[0].SubItems[0].Text;
                price = listView1.SelectedItems[0].SubItems[1].Text;
                quantity = listView1.SelectedItems[0].SubItems[2].Text;
                // UI
                MessageBox.Show(productName + " , " + price + " , " + quantity);
            }
        }
    }
}

```

## Interessante bronnen

[ListView Control (Windows Forms)](https://docs.microsoft.com/en-us/dotnet/framework/winforms/controls/listview-control-windows-forms) - Microsoft
[How to: Display Subitems in Columns with the Windows Forms ListView Control](https://docs.microsoft.com/en-us/dotnet/framework/winforms/controls/how-to-display-subitems-in-columns-with-the-windows-forms-listview-control) - Microsoft

