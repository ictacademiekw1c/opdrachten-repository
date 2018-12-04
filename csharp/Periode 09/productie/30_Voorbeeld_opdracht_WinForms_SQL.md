####[kleurcode]rgba(239,108,0,1)

#Uitgewerkte opdracht Windows Forms#

##Kennisgrammatica naar een 3-Tier OOP Csharp Windows Forms  applicatie met een SQL Data Access Layer#

Met een *kennisgrammatica* analyse heb je een *dataontwerp* gemaakt van je applicatie. Alle redundante informatie is er als het goed is uit en netjes georganiseerd in diagrammen met informatie die bij elkaar hoort.

Als je een OOP ontwerp maakt is dit data ontwerp dus rechtstreeks te vertalen naar de data structuren  in je applicatie. Je *kennisgrammatica* diagram beschrijft dus je *klassen* structuur van je applicatie.

In een *3-Tier* applicatie wordt deze data structuur gebruikt om data object klassen te maken en deze object door te geven tussen de lagen in de applicatie. 

Een *3-Tier* applicatie bestaat namelijk uit verschillende lagen. Let op, een tier is niet hetzelfde als een laag.  lagen zijn meer een logische scheiding van de code terwijl een *Tiers* meer dan 1 laag kan bevatten en geïmplementeerd kan worden op verschillende fysieke machines. Client applicatie hardware, middelware server, database server.

De beschrijving van de verschillende lagen:

- De **Presentation Layer** bevat de Windows Forms klassen met als functionaliteit om doormiddel van een grafische user interface, de controls, de business data objecten te vullen. Deze data objecten worden gebruikt om data door te geven naar een onderste laag.
- De **Business Object Layer** is de laag waarin de data objecten zijn gedefinieerd. Deze data objecten komen overeen met de data structuur die in de kennisdiagrammen zijn vastgelegd.
- De **Business Logic Layer** is de verbindingslaag tussen de *Presentation* en *Data Access Layer*. Om de *Presentation* en de *Data Access Layer* los te kunnen koppelen van elkaar wordt er gebruik gemaakt van een tussenlaag. Een aantal Business Logic klassen zorgen voor de koppeling tussen de presentatie en data laag
- De **Data Access Layer** is de laag die verbinding de opslag van de data verzorgd. Dit kan op diverse manieren gebeuren zoals lokale DataSets, SQL databases of XML bestanden. Alle specifieke programma code die nodig is om de administratie in deze systemen te verzorgen is in deze laag opgenomen. 

In dit voorbeeld gaan we in de Data Access Layer een verbinding leggen met een SQL database om daar verbinding te maken met tabelen waarin de gegevens in worden opgeslagen en uitgelezen.  

Keywords: *** DataSet, DataTable, Rows, Colums,  ListView, Combobox, Textbox, Button, Label***

###Downloads###

- [Kennisgrammatica diagrammen -> OOP C# Windows Form applicatie](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2008/Productie/01.%20Reader/LeerlinggegevensSQL_kennis-Csh.xlsx) - Leerlinggegevens SQL
- SQL script [Leerlinggegevens](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2008/Productie/03.%20Scripts/Leerlinggegevens.sql) .


