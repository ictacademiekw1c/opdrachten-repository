####[kleurcode]rgba(239,108,0,1)

#Uitgewerkte opdracht Windows Forms#

##Kennisgrammatica naar een 3-Tier OOP Csharp Windows Forms  applicatie#

Met een *kennisgrammatica* analyse heb je een *dataontwerp* gemaakt van je applicatie. Alle redundante informatie is er als het goed is uit en netjes georganiseerd in diagrammen met informatie die bij elkaar hoort.

Als je een OOP ontwerp maakt is dit data ontwerp dus rechtstreeks te vertalen naar de data structuren  in je applicatie. Je *kennisgrammatica* diagram beschrijft dus je *klassen* structuur van je applicatie.

In een *3-Tier* applicatie wordt deze data structuur gebruikt om data object klassen te maken en deze object door te geven tussen de lagen in de applicatie. 

Een *3-Tier* applicatie bestaat namelijk uit verschillende lagen. Let op, een tier is niet hetzelfde als een laag.  lagen zijn meer een logische scheiding van de code terwijl een *Tiers* meer dan 1 laag kan bevatten en geïmplementeerd kan worden op verschillende fysieke machines. Client applicatie hardware, middelware server, database server.

De beschrijving van de verschillende lagen:

- De **Presentation Layer** bevat de Windows Forms klassen met als functionaliteit om doormiddel van een grafische user interface, de controls, de business data objecten te vullen. Deze data objecten worden gebruikt om data door te geven naar een onderste laag.
- De **Business Object Layer** is de laag waarin de data objecten zijn gedefinieerd. Deze data objecten komen overeen met de data structuur die in de kennisdiagrammen zijn vastgelegd.
- De **Business Logic Layer** is de verbindingslaag tussen de *Presentation* en *Data Access Layer*. Om de *Presentation* en de *Data Access Layer* los te kunnen koppelen van elkaar wordt er gebruik gemaakt van een tussenlaag. Een aantal Business Logic klassen zorgen voor de koppeling tussen de presentatie en data laag
- De **Data Access Layer** is de laag die verbinding de opslag van de data verzorgd. Dit kan op diverse manieren gebeuren zoals lokale DataSets, SQL databases of XML bestanden. Alle specifieke programma code die nodig is om de administratie in deze systemen te verzorgen is in deze laag opgenomen. 

Hoe je vanuit een *kennisgrammatica* diagrammen je *klassen* bouwt en een 3-Tier applicatie bouwt  uit de data laag doorgeeft tussen de verschillende windows forms objecten in de presentatie laag, is als voorbeeld uitgewerkt in onderstaand Excel bestand.  

Keywords: *** DataSet, DataTable, Rows, Colums, Lists of data objects, List<T>, ListView, Combobox, Textbox, Button, Label***

###Downloads###

- [Kennisgrammatica diagrammen -> OOP C# Windows Form applicatie](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2008/Productie/01.%20Reader/Leerlinggegevens3-Tier_kennis-Csh.xlsx) - Leerlinggegevens 3-Tier

### Links

- [Understand 3- Tier Architecture in C#](https://www.codeproject.com/Tips/662107/Understand-Tier-Architecture-in-Csharp) - Codeproject
- [Three Tier Architecture In ASP.NET](https://www.c-sharpcorner.com/UploadFile/5d683d/three-tier-architecture-in-Asp-Net/) - C# Corner
- [Software Architectuur](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.07%20CSh%5D%20C%20Sharp/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2008/Productie/01.%20Reader/0016_Reader%20C-Sharp%20V7.0%20-%20Software%20architectuur.pdf) - C# Reader KW1C
- [Four Ways of passing data through Layers](https://www.codeproject.com/Articles/493389/Four-ways-of-passing-data-between-layers#Method3:-Datatransferobjects(DTO)) - Codeproject


