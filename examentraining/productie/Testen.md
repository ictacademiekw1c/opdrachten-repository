# Testen

(Zie ook het materiaal van leerjaar 2 de Studieroute Onderhoud & Beheer, het onderdeel testen)

## 1. Black en Whitebox testing

### 1.1 Black Box testing

![Black Box Testing](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/examentraining/images/blackboxtesting.png?raw=true)

### 1.2 White Box testing

![White Box Testing](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/examentraining/images/whiteboxtesting.png?raw=true)

## 2. Geautomatiseerd testen

Geautomatiseerde testen worden aangemaakt en uitgevoerd in de ontwikkel- en uitbreidingsfase van het systeem. 
Deze testen worden uitgevoerd door het ontwikkelteam zelf op het moment van integratietesten.

    ## 2.1 Unittesten in C#

Deze manier van testen testen van iedere klasse alle methodes op gewenste en ongewenste invoer de gewenste uitvoer.

-   __Walkthrough__ 

[Unit test in C#](https://docs.microsoft.com/nl-nl/visualstudio/test/walkthrough-creating-and-running-unit-tests-for-managed-code#BKMK_Prepare_the_walkthrough)

### OefenOpdrachten

### Assert Tests
- Assert.AreEqual
- Assert.IsTrue
- Assert.AreNotEqual
- Assert.IsNotNull
- Assert.IsNull
- Assert.Isfalse
- Assert.AreSame
- inconclusive()
- fails()

## 3.1 Acceptatietest

    - Wat is een acceptatietest?

Een acceptatietest wordt meestal uitgevoerd door een speciale testgroep die de uiteindelijke gebruikers representeren.
De testers zijn aldus echte eindgebruikers en de test wordt ook uitgevoerd met echte productiegegevens, weliswaar in een
kopie van de echte omgeving. De test kan gezien worden als een black box test, waarbij op de volgende onderdelen wordt getest:

__Taakgeschiktheid__. 
<br>
De gebruikersinterface moet aansluiten op de werkzaamheden van de gebruiker. Een gebruikersinterface is er voor de gebruiker en niet andersom. 

Wanneer een timmerman een spijker in de muur slaat met een hamer, denkt hij niet na over de bediening van de hamer; hij concentreert zich op de spijker. Een goede gebruikersinterface laat zich vergelijken met de hamer. 

De gebruiker kan de interface intuitief bedienen waardoor hij zich volledig kan concentreren op zijn werk.

__Consistentie__ 
<br>In onze samenleving is praktisch iedereen in staat om een doosje lucifers op de juiste wijze te bedienen. Een Indiaan uit het Amazonegebied die nog nooit met onze cultuur in aanraking is geweest, zal echter grote moeite hebben om met het doosje vuur te maken. Zo is het ook met gebruikersinterfaces. Een gebruiker die nog nooit met een grafische gebruikersinterface heeft gewerkt, zal meer moeite hebben om zich een nieuwe applicatie eigen te maken dan een gebruiker die vertrouwd is met de concepten van grafische gebruikersinterfaces. 

Consistentie is niet alleen tussen verschillende interfaces belangrijk maar ook binnen een interface.

__Bestuurbaarheid__ 
<br>De gebruiker moet het idee hebben dat hij de gebruikersinterface bestuurt en niet dat de gebruikersinterface hem bestuurt. De gebruiker hoort een actieve rol te spelen in de bediening, niet een reactieve.

__Herkenbaarheid__ 
<br>De gebruikersinterface moet herkenbaar zijn voor de gebruiker. De gebruiker moet de structuur en werking als het ware zelf kunnen afleiden. Dit is mogelijk door een goed conceptueel model te hanteren. Een conceptueel model biedt de gebruikers een zodanige abstractie van de onderliggende techniek dat de gebruikers begrijpen hoe ze de gebruikersinterface moeten bedienen. 

Neem de bestuurder van een auto. Deze hoeft niet te weten wat een bobine is, wat bougies zijn en waar de koppakking toe dient. Al deze technische zaken zijn in de moderne auto verstopt achter een gaspedaal, koppeling, versnelling, rem en stuur.

__Terugkoppeling__ 
<br>Vergelijk een elektrisch fornuis met een gasfornuis. Bij het koken op een elektrisch fornuis is er altijd sprake van een zekere vertraging tussen het moment waarop de gebruiker de temperatuur van een kookplaat instelt en het moment waarop de kookplaat de ingestelde temperatuur bereikt. Bij een gasfornuis daarentegen krijgt de gebruiker vrijwel direct terugkoppeling wanneer hij het gas hoger of lager draait. Over het algemeen wordt dit als prettiger ervaren. 

Een ander goed voorbeeld is een printfunctie. Vaak duurt het enige tijd voordat er iets uit de printer komt. Ongeduldige gebruikers hebben dan al meerdere malen op de printknop gedrukt. Zorg je voor een melding dat het document wordt afgedrukt, dan zal er minder ergernis ontstaan over de ‘extra’ afdrukken.

__Eenvoud__ 
<br>Beschouw de ontwikkeling van de afstandsbediening van televisies. De eerste afstandsbedieningen waren apparaten met veel knoppen die bovendien allemaal dezelfde grootte hadden. De huidige generatie afstandsbedieningen kenmerkt zich door weinig knoppen. De belangrijkste knoppen (kanaal vooruit/achteruit, volume harder/zachter) zijn groter uitgevoerd dan de andere. Daarnaast zijn specialistische knoppen (om bijvoorbeeld de kanalen te programmeren en de helderheid en het contrast in te stellen) vaak verborgen achter een klepje.
Aantrekkelijkheid. 
Vergelijk de vormgeving van de website van de ene krant eens met die van een andere. De presentaties komen overeen met die van de echte kranten en appelleren aan de beoogde doelgroepen. Of vergelijk het uiterlijk van de ene auto met dat van een andere. Beide auto's hebben een specifieke doelgroep voor ogen. Een goede interface roept positieve gevoelens op bij de doelgroep.

  - Hoe stel je een acceptatietestplan op?

        - Een acceptatietestplan test op bovenstaande onderdelen
        - Een acceptatieplan test op de gewenste functionaliteiten.
  
De gewenste functionaliteiten worden beschreven in het functioneel ontwerp (Use Case en activity diagrammen).
Het acceptatietestplan bevat aldus alle activiteiten die ook in de Use Case en/of activity diagrammen zijn beschreven.

  - Uitvoeren en rapporteren van een acceptatietestplan
        - verbeterpunten (Change Request) n.a.v. een acceptatietest
        - Alle tests die op bovenstaande onderdelen een 'onvoldoende' scoren moet als change request worden aangemerkt (en moeten dus worden aangepast door de leverancier).
 
