####[kleurcode]rgba(239,108,0,1)

#Opdracht 4 - Data Binding

Opdracht 4 is een verwerkingsopdracht voor het gebruik van Data Binding. Op een grid panel of DockPanel plaatsen we diverse controls en laten deze synchroniseren met onderliggende properties van objecten door middel van Data Binding.

------
### Opdrachten

In Opdracht 4 moeten de volgende onderwerpen worden uitgewerkt:


- Kunnen opzetten van een C# Windows Presentation Foundation applicatie met een venster.
- Kunnen toepassen van de controls:  *Textbox, Label, Button, RadioButton, Checkbox, Calendar, Listbox,  Menu, MenuItem*
- Kunnen toepassen van een *MessageBox*
- Kunnen toepassen van Data Binding 
- Kunnen toepassen van DataContext property
- Kunnen toepassen van Binding Mode



[Opdracht 4.1](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/02.%20Opdrachten/Opdracht%20WPF%204.1.pdf) - Data Binding tussen twee controls.

[Opdracht 4.2](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/02.%20Opdrachten/Opdracht%20WPF%204.2.pdf) - Data Bindings van meerdere TextBlock-en aan een geselecteerd Font en een TextBox.

[Opdracht 4.3](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/02.%20Opdrachten/Opdracht%20WPF%204.3.pdf) - Data Binding van een ListBox met een List van objecten.

## Voorbeelden

###Binding met onderliggend datamodel 

Met behulp van de *DataContext* is het gemakkelijk om een deel van je scherm of groep van UI Framework elementen met Binding te koppelen aan een datamodel object. Binnen deze groep van UI Framework elementen volstaat het dan om alleen het *Path*, de Target Property te zetten.

De *DataContext* kun je op twee manieren zetten. In de code en in XAML. In XAML is de GUI het mooiste gescheiden van de onderliggende code. De onderliggende code bevat geen verwijzingen naar een GUI.

Bij gebruik van de *DataContext* in de code kun je de *DataContext* dynamisch wijzigen tijdens de executie van de code. Dit kan in een aantal gevallen wenselijk zijn.

Hieronder twee voorbeelden uitgewerkt met de *DataContext* gezet in code en gezet in XAML. De *DataContext* is voor het gehele scherm gezet op het datamodel van object *persoon*. In het StackPanel wordt de scope verder verkleind naar het object *Adres* binnen het object *persoon*.

**Voorbeeld 1 - DataContext in Code**

![](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/04.%20Aanvullend/Hoofdstuk4_Persoon.png)

Scherm layout

```xaml
<Window x:Class="Hfst04_DataBinding03a.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
        xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
        xmlns:local="clr-namespace:Hfst04_DataBinding03a"
        mc:Ignorable="d"
        Title="Data Binding Demo 3a" Height="450" Width="600">
    <Grid>
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
        </Grid.RowDefinitions>
        
        <TextBox Grid.Row="0"
                 Margin="5,0,0,0"
                 Text="Voer een naam in:"/>

        <TextBox Grid.Row="1"
                 Width="100"
                 Margin="5,10"
                 HorizontalAlignment="Left"
                 Text="{Binding Path=Naam}"/>
        <TextBlock Grid.Row="2"
                   Margin="5,0,0,0"
                   Text="Adres"/>
        <StackPanel Grid.Row="3"
                    Orientation="Horizontal"
                    DataContext="{Binding Adres}">
            <TextBox Width="50"
                     Margin="5,0,0,0"
                     Text="{Binding Nummer}"/>
            <TextBox Width="140"
                     Margin="10,0,0,0"
                     Text="{Binding Straat}"/>
        </StackPanel>


        <Button Grid.Row="5"
                Width="100"
                Margin="5,10"
                HorizontalAlignment="Left"
                Content="Show"
                Click="Button_Click"/>

    </Grid>
</Window>
```

*XAML bestand MainWindow.xaml*

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

namespace Hfst04_DataBinding03a
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        // Aanmaken van het object persoon (Binding Source - ElementName)
        // met de property Naam (Binding Source Property - Path)
        Persoon persoon;

        public MainWindow()
        {
            persoon = new Persoon();
            InitializeComponent();
            // Koppel het Binding Target Object aan het Binding Source Object
            this.DataContext = persoon;
            // In de XAML wordt de Target Dependency Propertie Windows venster aan de Binding Source "" gekoppeld
        }

        private void Button_Click(object sender, RoutedEventArgs e)
        {
            string bericht = persoon.Naam + ", " + persoon.Adres.Nummer + ", " + persoon.Adres.Straat;
            MessageBox.Show(bericht);
        }
    }
}
```

*C# bestand MainWindow.cs*

```c#
using System;
using System.Collections.Generic;
using System.Dynamic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Hfst04_DataBinding03a
{
    public class Persoon
    {
        // De klasse Persoon heeft de property Naam
        public string Naam { get; set; }

        public Adres Adres { get; set; }

        public Persoon()
        {
            this.Adres = new Adres();
        }
    }
}
```

*C# bestand Persoon.cs*

```c#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Hfst04_DataBinding03a
{
    public class Adres
    {
        public int Nummer { get; set; }
        public string Straat { get; set; }
    }
}
```

*C# bestand Adres.cs*

**Voorbeeld 2 - DataContext in XAML**

```xaml
<Window x:Class="Hfst04_DataBinding03b.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
        xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
        xmlns:local="clr-namespace:Hfst04_DataBinding03b"
        mc:Ignorable="d"
        Title="Data Binding Demo 3b" 
        Height="450" Width="600"
        Name="gridWindow">
    
    <Grid DataContext="{Binding ElementName=gridWindow, Path=Persoon}">
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
        </Grid.RowDefinitions>
        
        <TextBox Grid.Row="0"
                 Margin="5,0,0,0"
                 Text="Voer een naam in:"/>
        <TextBox Grid.Row="1"
                 Width="100"
                 Margin="5,10"
                 HorizontalAlignment="Left"
                 Text="{Binding Path=Naam}"/>
        <TextBlock Grid.Row="2"
                   Margin="5,0,0,0"
                   Text="Adres"/>
        <StackPanel Grid.Row="3"
                    Orientation="Horizontal"
                    DataContext="{Binding Adres}">
            <TextBox Width="50"
                     Margin="5,0,0,0"
                     Text="{Binding Nummer}"/>
            <TextBox Width="140"
                     Margin="10,0,0,0"
                     Text="{Binding Straat}"/>
        </StackPanel>

        <Button Grid.Row="5"
                Width="100"
                Margin="5,10"
                HorizontalAlignment="Left"
                Content="Show"
                Click="Button_Click"/>
    </Grid>
</Window>
```

*XAML bestand MainWindow.xaml*

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

namespace Hfst04_DataBinding03b
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        // Aanmaken van het object persoon (Binding Source - ElementName)
        // Let op dat van het object persoon een property moet worden gemaakt om
        // persoon als Source Property te kunnen laten dienen.
        // Hieronder expliciet uitgeschreven
        //
        // private Persoon persoon;
        // public Persoon Persoon
        // {
        //		set{ persoon=value;}
        //		get{ return = persoon;}
        // }
        // Of in het kort:
        public Persoon Persoon { get; set;}

        public MainWindow()
        {   // Constructor Persoon
            Persoon = new Persoon();
            InitializeComponent();
        }

        private void Button_Click(object sender, RoutedEventArgs e)
        {
            string bericht = Persoon.Naam + ", " + Persoon.Adres.Nummer + ", " + Persoon.Adres.Straat;
            MessageBox.Show(bericht);
        }
    }
}
```

*C# bestand MainWindow.cs*



## Help

[WPF Data Binding Overview](https://www.wpftutorial.net/DataBindingOverview.html) - WPF-Tutorials

[WPF Data Binding](https://www.tutorialspoint.com/wpf/wpf_data_binding.htm) - Tutorials Point

[Explain Binding Mode In WPF](https://www.c-sharpcorner.com/article/explain-binding-mode-in-wpf/) - C-Sharp Corner