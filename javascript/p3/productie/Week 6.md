---

## Opdracht 360 Highscores opslaan en weergeven!

`` Opleveren: Plaats al je gemaakte bestanden (.js, .html ) in een een rar met naam OPDRACHT360.rar en upload deze in je portfolio. Laat daarna de opdracht zien aan de docent om deze af te tekenen. Onthoud bij het uploaden dat we inmiddels in Periode 3 zitten.``

> In deze opdracht moet je zowel een Javascript als een PHP script ontwikkelen. Je kennis van beide onderwerpen komen dus aan bod! Mocht je er met het PHP script niet uitkomen, dan kun je aan de docent JS om de uitwerking hiervoor vragen. Je krijgt dan echter maar één punt.

**Opdracht**

We willen graag een systeem maken waar we onze highscores (van een nog niet bestaand spel) naartoe kunnen sturen. Deze moeten op een server opgeslagen worden, zodat we deze later weer kunnen opvragen.
We gaan in dit geval daarom via een PHP script de highscores opslaan in de $_SESSION. Daarna is het de bedoeling dat we de highscores uit het PHP script weer gesorteerd op onze website laten zien.

Het is dus de bedoeling dat we via jQuery en AJAX highscores gaan sturen naar een eigen gemaakt PHP script. Dit PHP script slaat de nieuwe highscores op in de $_SESSION. De website moet ook weer via dit PHP script de highscores kunnen uitlezen, om deze te tonen aan de bezoeker!    

1. Download de <a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.16%20JAV%5D%20Javascript/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2003/Productie/03.%20Scripts/Huiswerkopdrachten/Opdracht%20360.zip" target="_new">template</a>
2. Pak deze uit in je huiswerkmap
3. Open de gehele directory in je editor
4. Run index.html in je browser
5. We starten nu met het maken van het PHP script. Zie "1. Stappenplan: Maken PHP script"


### 1. Stappenplan: Maken PHP script

> Kom je er niet uit met het PHP script? Blijf niet hang, maar vraag deze dan op bij de docent JS. Je krijgt dan wel maar één punt voor de huiswerkopdracht.


**Omschrijving**

We gaan in de $_SESSION['highscores'] een *array* opslaan die de highscores bevat.
Een nieuwe highscore komt binnen via $_GET['newHighscore'] en wordt via *array_push()* weggeschreven in deze $_SESSION['highscores'].

Als laatste echo'd ons PHP script een JSON String. Hieronder zie je een voorbeeld hoe dit de uitvoer van dit PHP bestand in de browser er ongeveer uit moet zien:
<img style="width: 80%" src="https://raw.githubusercontent.com/ictacademiekw1c/opdrachten-repository/master/javascript/p3/productie/Afbeeldingen/360-2.png">


**Stappenplan**
1. Laat het PHP script de volgende dingen doen:
    - Start de sessie
    - Check of $_SESSION['highscores'] *isset()*. Als dat niet is, maak deze aan en vul deze met een lege *array*
    - Zodra er GET variabele genaamd "newHighscore" in de URL zit, dient de waarde hiervan weggeschreven te worden in de *array* van de *$_SESSION* (Denk terug aan Hoofdstuk 10 van PHP, periode 2).
    - Lees de *array* uit naar een nieuwe variabele en sorteer de array, zodat de hoogte score bovenaan staan. Gebruik voor het sorteren de functie *rsort()*
    - Zorg ervoor dat de hierboven gemaakte *array* als *JSON* omgezet wordt en sla dit op in een variabele. Zie codevoorbeeld 1 hieronder
    - Echo deze variabele (*JSON* is immers niets meer dan een normale *string*)
4. Run je script en test deze door enkele highscores alvast toe te voegen!
5. Check of je perongeluk geen HTML mee echo'd!
6. Check of de uitvoer van je PHP script er ongeveer uitziet zoals de afbeelding hier vlak boven

*Codevoorbeeld 1: Uitlezen sessie en omzetten naar een JSON string*

```
// Lees de Array met de highscores uit de $_SESSION in
$sessionArray = $_SESSION["highScores"];

// Verander de Array naar een JSON string
$jsonString = json_encode($sessionArray);

// Echo de JSON String
echo $jsonString;
```


### 2.1 JS: Versturen van een nieuwe highscore
1. Het PHP script is nu klaar als het goed is, we gaan verder met de Javascript.
2. Check of de jquery library en Script.js gekoppeld zijn aan het HTML bestand
3. Zorg ervoor dat bij het klikken op de "Versturen!" knop de volgende dingen gebeuren
    - Lees de waarde van het input element uit (Zie reader 1)
    - Maak een AJAX request naar je zojuist gemaakte PHP script
    - Voeg in de URL van dit AJAX request de GET parameter "newHighscore" toe en vergeet niet de waarde van het inut veld als waarde van deze GET parameter mee te geven 
    - Laat een melding zien zodra het AJAX request gelukt is
    - Laat een error zien zodra het AJAX request mislukt is (Zie reader 4 hiervoor)
4. Verstuur een highscore via AJAX en check via de Network tab in je Inspector of deze ook daadwerkelijk opgeslagen wordt in je PHP script	
	
### 2.2 JS: Ophalen van de huidige highscores 
6. Zorg ervoor dat bij het klikken op de "Updaten" button de volgende dingen gebeuren
    - Maak een AJAX request naar het eerder gemaakte PHP script
    - Vang de uitkomst op in een variabele
    - Bepaal (bv via de *debugger*) of je het resultaat moet omzetten via *parseJSON()* (Zie reader)
    - Toon de highscores als listitems in de UL  (Tip: Gebruik *for*, *while* of $.each() loops )
7. Run je script in de browser en check of de highscores in de list tevoorschijn komen
7. Klaar? Bekijk de beoordelingscriteria of je niets vergeten bent

**Extra  opdracht: (Hiermee krijg je alsnog één punt voor een eerder gemiste huiswerkopdracht!)**
1. Verstuur de highscore niet als GET parameter, maar als POST parameter. Zie de reader hiervoor
2. Vergeet dit niet ook in de PHP door te voeren

### Visueel voorbeeld 1
<img style="width: 80%" src="https://raw.githubusercontent.com/ictacademiekw1c/opdrachten-repository/master/javascript/p3/productie/Afbeeldingen/360-1.png">

**Beoordelingscriteria**

**Javascript**
1. De Update en de versturen buttons maken gebruik van 2 verschillende AJAX requests
2. De website moet een nieuwe highscore kunnen opsturen
3. Je krijgt een melding zodra het AJAX request om een highscore te posten is geslaagd (of juist niet)
4. Na het opsturen van een highscore, moet deze via het drukken op de "Update" button zichtbaar worden
5. De highscores worden getoond als LI items

**PHP**
1. Het PHP script echo't valide een JSON string
2. Het PHP script kan via de GET paramater "newHighscore" nieuwe highscores ontvangen
3. Het PHP script slaat deze highscores in een sessie op

