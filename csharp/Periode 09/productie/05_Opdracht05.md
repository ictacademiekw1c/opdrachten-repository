####[kleurcode]rgba(239,108,0,1)

#Opdracht 5 - Binding  Modes

### Opdrachten

In Opdracht 5 moeten de volgende onderwerpen worden uitgewerkt:

- Kunnen opzetten van een C# Windows Presentation Foundation applicatie met een venster.
- Kunnen toepassen van de controls:  *Textbox, Label*, 
- Kunnen toepassen van een *MessageBox*
- Kunnen toepassen van *Data Binding* 
- Kunnen toepassen van *DataContext* property
- Kunnen toepassen van *Binding Mode*
- Kunnen toepassen  van de *UpdateSourceTrigger* property



[Opdracht 5.1](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/02.%20Opdrachten/Opdracht%20WPF%205.1.pdf) - Kikkersprong spel

[Opdracht 5.2](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/02.%20Opdrachten/Opdracht%20WPF%205.2.pdf) - Data Binding met Listview en SQL database

Opdracht 5.2 script [Personen.sql](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/03.%20Scripts/Personen.sql) - Personen SQL database

[Opdracht 5.3 -Draft](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/02.%20Opdrachten/Opdracht%20WPF%205.3_draft.pdf) - DataBinding met Listview en SQL database

Opdracht 5.3 script [NYCM.sql](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/03.%20Scripts/Nycm.sql) - deelnemers, registratie SQL database

## Theorie

Opdracht 5 is een verwerkingsopdracht voor het toepassen van Binding Modes bij Data Bindings. Op een grid panel of DockPanel plaatsen we diverse controls. Hoe er wordt gesynchroniseerd kunnen we sturen met de volgende Binding Modes:

- **One Way**: Wijzigingen van de source property wordt ook overgenomen door de target property, maar niet in de andere richting.

- **Two Way**: Wijzigingen van de source of target properties worden automatisch overgenomen door de andere property.

- **One Way to Source**: Wijzigingen van de target property wordt ook overgenomen door de source property, maar niet in de andere richting.

- **One Time**: Een **OneWay** binding die alleen wordt uitgevoerd bij het initialiseren  van de target property.

-----

Bij de Binding Modes **One Way** en **Two Way** wordt de  UI  niet automatisch geïnformeerd over wijzingen in een Source property. Dit moet door in de code expliciet worden uitgevoerd door:
- Het implementeren van de **INotifyPropertyChanged** interface in het data model.
- Het activeren van het **PropertyChanged** event om de UI te informeren.

Dit heeft een aantal redenen namelijk:

- Performance. Je wilt niet altijd direct de Target Source wijzigen als de Source wijzigt.
- De notificaties kan afhankelijk zijn van meerdere properties.

Een datamodel klasse uitbreiden met de INotifyPropertyChanged interface :

```c#
 public class Persoon: INotifyPropertyChanged
    {
        private string _naam;
        // De klasse Persoon heeft de property Naam
        // Bij het zetten van de naam activeren we ook
        // het event RaisePropertyChanged.
        public string Naam
        {
            get
            {
                return _naam;
            }
            set
            {
                if (value != _naam)
                {
                    _naam = value;
                    RaisePropertyChanged("Naam");
                }
            }
        }

        public Adres Adres { get; set; }

        public Persoon()
        {
            this.Adres = new Adres();
        }

        // De implementatie van de INotifyPropertyChanged interface
        public event PropertyChangedEventHandler PropertyChanged;
	
	    public void RaisePropertyChanged(string propertyName)
            {
                if (PropertyChanged != null)
                {
                    PropertyChanged.Invoke(this, new PropertyChangedEventArgs(propertyName));
                }
            }
    }
```

Het is gebruikelijk om de INotifyPropertyChanged definitie in een aparte klasse onder te brengen zodat ook voor andere datamodelen deze code kan worden hergebruikt doormiddel van overerving.

Hier de voorbeeld code van deze klasse:

```c#

public class BindableBase : INotifyPropertyChanged
    {
        public event PropertyChangedEventHandler PropertyChanged;
	
	    public void RaisePropertyChanged(string propertyName)
            {
                if (PropertyChanged != null)
                {
                    PropertyChanged.Invoke(this, new PropertyChangedEventArgs(propertyName));
                }
            }
    }
```



-----

Bij de Binding Modes **One Way to Source** en **One Time** kunnen we het moment van sychronisatie sturen doormiddel van de eigenschap **UpdateSourceTrigger**

De UpdateSourceTrigger heeft de volgende opties:

- **Default**: De focus
- **PropertyChanged**: bij iedere verandering van de Target Source
- **Explicit**: wanneer **UpdateSource()** wordt aangeroepen vanuit de code.

------

## Help
[Kikkersprong spel uitleg](http://www.davdata.nl/kikkers.html)

[WPF Data Binding - responding to chances](https://www.wpf-tutorial.com/data-binding/responding-to-changes/) - WPF Tutorial

[WPF Data Binding Overview](https://www.wpftutorial.net/DataBindingOverview.html) - WPF-Tutorials

[WPF Data Binding - Binding Modes](https://www.tutorialspoint.com/wpf/wpf_data_binding.htm) - Tutorials Point

[Explain Binding Mode In WPF](https://www.c-sharpcorner.com/article/explain-binding-mode-in-wpf/) - C-Sharp Corner

[C# WPF and GUI - Pages and Navigation](https://www.youtube.com/watch?v=aBh0weP1bmo) - Youtube