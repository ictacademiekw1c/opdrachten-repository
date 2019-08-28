####[kleurcode]rgba(239,108,0,1)

#Uitgewerkte opdracht Windows Presentation Foundation#

##Kennisgrammatica naar een 3-Tier OOP Csharp WPF  applicatie met een SQL Data Access Layer#

Met een *kennisgrammatica* analyse heb je een *dataontwerp* gemaakt van je applicatie. Alle redundante informatie is er als het goed is uit en netjes georganiseerd in diagrammen met informatie die bij elkaar hoort.

Als je een OOP ontwerp maakt is dit data ontwerp dus rechtstreeks te vertalen naar de data structuren  in je applicatie. Je *kennisgrammatica* diagram beschrijft dus je *klassen* structuur van je applicatie.

In een *3-Tier* applicatie wordt deze data structuur gebruikt om data object klassen te maken en deze object door te geven tussen de lagen in de applicatie. 

Een *3-Tier* applicatie bestaat namelijk uit verschillende lagen. Let op, een tier is niet hetzelfde als een laag.  lagen zijn meer een logische scheiding van de code terwijl een *Tiers* meer dan 1 laag kan bevatten en geïmplementeerd kan worden op verschillende fysieke machines. Client applicatie hardware, middelware server, database server.

De beschrijving van de verschillende lagen:

- De **Presentation Layer** bevat de WPF XAML code, de onderliggende code (*View* layer) en de *ModelView* layer. De *View* layer is doormiddel van *MVVM design pattern* losgekoppeld van de functionaliteit (*Model*  layer). De *ModelView* objecten zijn tussenliggende objecten die via databindings gekoppeld zijn aan de *View* layer. Door vanuit de *Model* layer de *Modelview* layer te vullen zorgen de databindings voor de automatische synchronisatie van de *View* layer. De *Model* laag is weer gesplitst in 2 lagen, de *Business Object Layer* en de *Data Acces Layer*. 
- De **Business Object Layer** is de laag waarin de data objecten zijn gedefinieerd. Deze data objecten komen overeen met de data structuur die in de kennisdiagrammen zijn vastgelegd. Deze data structuren worden gebruikt voor de transportatie van de data naar de *Data Access Layer*.
- De **Business Logic Layer** is de verbindingslaag tussen de *Presentation* en *Data Access Layer*. Om de *Presentation* en de *Data Access Layer* los te kunnen koppelen van elkaar wordt er gebruik gemaakt van een tussenlaag. Een aantal Business Logic klassen zorgen voor de koppeling tussen de presentatie en data laag
- De **Data Access Layer** is de laag die verbinding de opslag van de data verzorgd. Dit kan op diverse manieren gebeuren zoals lokale DataSets, SQL databases of XML bestanden. Alle specifieke programma code die nodig is om de administratie in deze systemen te verzorgen is in deze laag opgenomen. 

In dit voorbeeld gaan we in de *Data Access Layer* een verbinding leggen met een SQL database om daar verbinding te maken met tabelen waarin de gegevens in worden opgeslagen en uitgelezen.  

Keywords: ***DataSet, DataTable, Rows, Colums,  Listbox, Combobox, Textbox, Button, Label, View, Model, ModelView***

###Downloads###

- [Kennisgrammatica diagrammen -> OOP C# Windows Presentation Foundation applicatie](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/02.%20Opdrachten/WpfLeerlinggevens_mvvm_3tier_sq.xlsx) - Leerlinggegevens WPF SQL
- SQL script [Leerlinggegevens](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2008/Productie/03.%20Scripts/Leerlinggegevens.sql) .


