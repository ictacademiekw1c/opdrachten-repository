####[kleurcode]rgba(239,108,0,1)

#Uitgewerkte opdracht WPF XML#

##Lezen van XML bestanden

C# heeft verschillende mogelijkheden om een XML bestand in te lezen en verder te gebruiken in de applicatie. Hieronder zijn twee voorbeelden uitgewerkt.

**xmlDocument klasse**

- xmlDocument is een klasse waarin een xml document in keer in het geheugen wordt geladen en waar bewerkingen en selects op kunnen worden uitgevoerd.

**DataSet klasse**

- De DataSet heeft methods om direct een DataSet te vullen vanuit een xml bestand. 


## ** Voorbeeld - gebruik xmlDocument** klasse 

In dit eenvoudig voorbeeld wordt de item nodes uitgelezen.

De nodes met de node.name "titel" en "beschrijving" worden uitgelezen en in de Console Output window geprint.

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
            XmlDocument xmlDoc = new XmlDocument();
            // Laad het xml document in het geheugen
            xmlDoc.Load("test1.xml");

            // Genereer een List met nodes

            XmlNodeList nodeList = xmlDoc.SelectNodes("nieuws/item/*");
            Console.WriteLine("#########################");
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

In dit voorbeeld worden twee methodes uitgewerkt om een XML bestand in te lezen. De data uit de xml bestand wordt gebruikt om een listView op het scherm te vullen. De ListView is doormiddel van databinding gekoppeld aan een ViewModel. De ViewModel heeft een ObservableCollection van nieuwsItems die gevuld worden  vanuit de applicatie. 



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
            // Loop door alle items en stop de gegevens in BO object
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

            }

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
                    Titel = (string) r[0],
                    Beschrijving = (string) r[1]
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



###Downloads###
In deze sectie de verschillende voorbeeld xml bestanden die gebruikt zijn in de voorbeelden.

- XML script [test1.xml](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/03.%20Scripts/test1.xml) .
- XML script [test2.xml](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/03.%20Scripts/test2.xml).


