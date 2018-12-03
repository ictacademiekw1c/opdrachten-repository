####[kleurcode]rgba(239,108,0,1)

#Uitgewerkte opdracht WPF XML#

##Algemeen ##

XML staat voor Extensible Markup Language en is complementair met HTML en andere webtechnologieën. XML is de W3C standaard voor het online uitwisselen van informatie.

XML is geen database, maar wordt gebruikt om grote hoeveelheden ongestructureerde data in op te slaan. XML bestanden kunnen door ieder type applicatie worden ingelezen. Hier een samenvatting van de voordelen:

- Grote hoeveelheid data.
- Ongestructureerde data.
- Toegang door verschillende type applicaties.
- Makkelijk te delen tussen applicaties.
- Makkelijk te genereren.
- Makkelijk leesbaar.

**Syntax**
```xml
<root>  
       <child>  
            <subchild>.....</subchild>  
       </child>  
</root>   
```
**XML voorbeeld**

```xml
<?xml version="1.0" encoding="UTF-8"?>
<nieuws>
	<item>
		<titel>Brand</titel>
		<beschrijving>Brand in de veenstraat.</beschrijving>
	</item>
	<item>
		<titel>Fusie</titel>
		<datum>22-03</datum>
		<beschrijving>De twee lokale amateurclubs zijn gisteren gefuseerd.</beschrijving>
	</item>
	<item>
		<titel>Diefstal</titel>
		<beschrijving>Gisterenavond is de lokale supermarkt overvallen door twee mannen.</beschrijving>
	</item>
</nieuws>
```



##Lezen van XML bestanden ##

C# heeft verschillende mogelijkheden om een XML bestand in te lezen en verder te gebruiken in de applicatie. Hieronder zijn twee voorbeelden uitgewerkt.

**xmlDocument klasse**

- *xmlDocument* is een klasse waarin een XML document in keer in het geheugen wordt geladen en waar bewerkingen en selecties op kunnen worden uitgevoerd.

**DataSet klasse**

- De DataSet heeft methods om direct een DataSet te vullen vanuit een xml bestand. 


## Voorbeeld - gebruik xmlDocument klasse ##

In dit eenvoudig voorbeeld wordt de item nodes uitgelezen. Eerst wordt het hele XML bestand in een xmlDocument object ingelezen. Dit object heeft allerlei mogelijkheden om de XML structuur en zijn inhoud te onderzoeken.

Zo kan er een lijst van alle elementen (*Nodes*) worden gemaakt (*XmlNodeList*) met de method .*SelectNodes*

Van een node kan de naam van het element (*.Name*) en de inhoud van de tag (*.InnerText*) worden uitgelezen.

In de applicatie wordt de *.InnerText* van de *XmlNodeList*  in de Console Output window geprint.

```c#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Data;
using System.Windows.Documents;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Imaging;
using System.Windows.Navigation;
using System.Windows.Shapes;

// Toevoegen XML library
using System.Xml;

namespace XML_voorbeeld1
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        public MainWindow()
        {
            InitializeComponent();
            // Creeer een xmlDocument object dat alle xml data bevat
            XmlDocument xmlDoc = new XmlDocument();
            // Laad het xml document in het geheugen
            xmlDoc.Load("test1.xml");

            // Genereer een List met nodes. Neem de top 2 lagen niet mee in de list
            XmlNodeList nodeList = xmlDoc.SelectNodes("nieuws/item/*");
            Console.WriteLine("#########################");
            // Loop door de lijst van nodes en 
            foreach (XmlNode node in nodeList)
            {
                // Console.WriteLine(node.InnerText);

                    switch (node.Name)
                    {
                        case "titel":
                            Console.Write("Titel: ");
                            Console.WriteLine(node.InnerText);
                            break;
                        case "beschrijving":
                        Console.Write("Beschrijving: ");
                        Console.WriteLine(node.InnerText);

                        Console.WriteLine("---------------");
                        break;
                    }
            }
            Console.WriteLine("#########################");
        }
    }
}

```



## Voorbeeld gebruik xmlDocument en DataSet Klasse

In dit voorbeeld worden twee methodes uitgewerkt om een XML bestand in te lezen. De data uit de xml bestand wordt gebruikt om een ListView op het scherm te vullen. De ListView is doormiddel van databinding gekoppeld aan een ViewModel. De ViewModel heeft een ObservableCollection van nieuwsItems die gevuld worden  vanuit de applicatie. 



```xaml
 <!--************************* Module Header **************************
Project:		Demo XML DataSet.ReadXML functie
Auteur:			Bart Linsen
Aanmaakdatum:   3 december 2018 
Module naam:	MainWindows.xaml

Omschrijving:	WPF demo om een DataSet te vullen

***********************************************************************-->
<Window x:Class="XML_voorbeeld3.MainWindow"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    xmlns:local="clr-namespace:XML_voorbeeld3"
    mc:Ignorable="d"
    Title="Nieuws" Height="450" Width="800">
    <Grid>
        <ListView
               ItemsSource="{Binding Nieuws}">
            <ListView.Resources>
                <Style TargetType="{x:Type GridViewColumnHeader}">
                    <Setter Property="HorizontalContentAlignment" Value="Left" />
                </Style>
            </ListView.Resources>
            <ListView.View>
                <GridView>
                    <GridViewColumn Header="Titel" DisplayMemberBinding="{Binding Titel}" Width="80" />
                    <GridViewColumn Header="Beschrijving" DisplayMemberBinding="{Binding Beschrijving}" Width="300" />
                </GridView>
            </ListView.View>
        </ListView>
    </Grid>
</Window>
```

**MainWindows** XAML opmaak

```c#
/************************** Module Header *******************************\
Project:		Demo XML DataSet.ReadXML functie
Auteur:			Bart Linsen
Aanmaakdatum:   3 december 2018 
Module naam:	MainWindows.xaml.cs

Omschrijving:	WPF demo om een DataSet te vullen

\************************************************************************/
using System;
using System.Collections.Generic;
using System.Data;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Controls.Primitives;
using System.Windows.Data;
using System.Windows.Documents;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Imaging;
using System.Windows.Navigation;
using System.Windows.Shapes;

// Toevoegen XML library
using System.Xml;

namespace XML_voorbeeld3
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        // Creeer een Nieuws ViewModel object
        NieuwsViewModel NieuwsVM = new NieuwsViewModel();

        public MainWindow()
        {
            // Voorbeeld load een xml bestand via een xmlDoc documenten

            XmlDocument xmlDoc = new XmlDocument();
            // Laad het xml document in het geheugen
            xmlDoc.Load("test2.xml");

            // Genereer een List met nodes
            XmlNodeList nodeList = xmlDoc.SelectNodes("nieuws/*");
            // Loop door alle items en stop de gegevens in BO objecten
            foreach (XmlNode node in nodeList)
            {
                // Debug schrijf waarden naar Console output
                Console.WriteLine(node["titel"].InnerText);
                Console.WriteLine(node["beschrijving"].InnerText);

                NieuwsVM.Nieuws.Add(new NieuwsItemBO
                {
                    Titel = node["titel"].InnerText,
                    Beschrijving = node["beschrijving"].InnerText
                });
                
                // TIP!!!
                // Op dezelfde manier zou je ook een database kunnen vullen.
                // (3-Tier layers niet in dit voorbeeld uitgewerkt!!)
                //
                // NieuwsItemBLL.Create(new NieuwsItemBO
                // {
                //		Titel = node["titel"].InnerText,
                //		Beschrijving = node["beschrijving"].InnertText
                // });
                //
                
            } // Einde foreach loop

            /// Dummy item in listView
            NieuwsVM.Nieuws.Add(new NieuwsItemBO
            {
                Titel = "---",
                Beschrijving = "---"
            });

            // Voorbeeld Load van een XML bestand met een DataSet

            // Constructor aanroepen dsNieuws
            DataSet dsNieuws = new DataSet();

            // Lees het XML bestand in een DataSet
            dsNieuws.ReadXml("test2.xml");
            foreach (DataRow r in dsNieuws.Tables[0].Rows)
            {
                NieuwsVM.Nieuws.Add(new NieuwsItemBO
                {
                    Titel = (string) r["titel"],
                    Beschrijving = (string) r["beschrijving"]
                });

            }

            InitializeComponent();
            this.DataContext = NieuwsVM;
        }
    }
}
```

**MainWindow Klasse**



```c#
/************************** Module Header *******************************\
Project:		Demo XML DataSet.ReadXML functie
Auteur:			Bart Linsen
Aanmaakdatum:   3 december 2018 
Module naam:	NieuwsItemBO.cs

Omschrijving:	WPF demo om een DataSet te vullen

\************************************************************************/
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace XML_voorbeeld3
{
    class NieuwsItemBO
    {
        public string Titel { get; set; }
        public string Beschrijving { get; set; }

        public NieuwsItemBO()
        {
            Titel = "leeg";
            Beschrijving = "leeg";
        }
    }
}
```

**NieuwsBO klasse**

```c#
/************************** Module Header *******************************\
Project:		Demo XML DataSet.ReadXML functie
Auteur:			Bart Linsen
Aanmaakdatum:   3 december 2018 
Module naam:	NieuwsViewModel.cs

Omschrijving:	WPF demo om een DataSet te vullen

\************************************************************************/
using System.Collections.ObjectModel;
using System.ComponentModel;

namespace XML_voorbeeld3
{
    internal class NieuwsViewModel
    {
        public ObservableCollection<NieuwsItemBO> Nieuws { get; set; }

        public NieuwsViewModel()
        {
            Nieuws = new ObservableCollection<NieuwsItemBO>();
        }
    }
}
```

**NieuwsViewModel klasse**



###Downloads ###
In deze sectie de verschillende voorbeeld xml bestanden die gebruikt zijn in de voorbeelden.

- XML script [test1.xml](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/03.%20Scripts/test1.xml) .
- XML script [test2.xml](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/03.%20Scripts/test2.xml).

###Help ###

[Programmeren Kan Iedereen: Het Inlezen van XML Files](https://www.youtube.com/watch?v=q-F20427FWE) - Youtube