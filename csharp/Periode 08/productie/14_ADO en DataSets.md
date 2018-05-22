####[kleurcode]rgba(239,108,0,1)

#Uitgewerkte opdracht Windows Forms#

##Kennisgrammatica naar een 3-Tier OOP Csharp Windows Forms  applicatie met een SQL Data Access Layer#

Met een *kennisgrammatica* analyse heb je een *dataontwerp* gemaakt van je applicatie. Alle redundante informatie is er als het goed is uit en netjes georganiseerd in diagrammen met informatie die bij elkaar hoort.

Als je een OOP ontwerp maakt is dit data ontwerp dus rechtstreeks te vertalen naar de data structuren  in je applicatie. Je *kennisgrammatica* diagram beschrijft dus je *klassen* structuur van je applicatie.

In een *3-Tier* applicatie wordt deze data structuur gebruikt om data object klassen te maken en deze object door te geven tussen de lagen in de applicatie. 

De beschrijving van de verschillende lagen:

- De **Presentation Layer** bevat de Windows Forms klassen met als functionaliteit om doormiddel van een grafische user interface, de controls, de business data objecten te vullen. Deze data objecten worden gebruikt om data door te geven naar een onderste laag.
- De **Business Object Layer** is de laag waarin de data objecten zijn gedefinieerd. Deze data objecten komen overeen met de data structuur die in de kennisdiagrammen zijn vastgelegd.
- De **Business Logic Layer** is de verbindingslaag tussen de *Presentation* en *Data Access Layer*. Om de *Presentation* en de *Data Access Layer* los te kunnen koppelen van elkaar wordt er gebruik gemaakt van een tussenlaag. Een aantal Business Logic klassen zorgen voor de koppeling tussen de presentatie en data laag
- De **Data Access Layer** is de laag die verbinding de opslag van de data verzorgd. Dit kan op diverse manieren gebeuren zoals lokale DataSets, SQL databases of XML bestanden. Alle specifieke programma code die nodig is om de administratie in deze systemen te verzorgen is in deze laag opgenomen. 

In dit sectie wordt het implementeren van een Data Access Layer uitgewerkt die een connectie maakt met een SQL database.

Keywords: *** DataSet, DataTable, Rows, Colums, Lists of data objects, List<T>, ListView, Combobox, Textbox, Button, Label***

###Downloads###

- 
- SQL script [Leerlinggegevens](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2008/Productie/03.%20Scripts/Leerlinggegevens.sql) .

### Links

- [WinForms ADO.net](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2008/Productie/01.%20Reader/0012_Reader%20C-Sharp%20V7.0%20-%20ADO.NET.pdf) - Reader "Programmeren in C#"
- [WinForms werken met datasets](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2008/Productie/01.%20Reader/0013_Reader%20C-Sharp%20V7.0%20-%20Werken%20met%20datasets.pdf) - Reader "Programmeren in C#"
- [WinForms 3- Tier](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2008/Productie/01.%20Reader/0016_Reader%20C-Sharp%20V7.0%20-%20Software%20architectuur.pdf) - Reader "Programmeren in C#"