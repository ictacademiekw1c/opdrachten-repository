---

## Opdracht 360 Highscores opslaan en weergeven!

`` Opleveren: Plaats al je gemaakte bestanden (.js, .html ) in een een rar met naam OPDRACHT360.rar en upload deze in je portfolio. Laat daarna de opdracht zien aan de docent om deze af te tekenen. Onthoud bij het uploaden dat we inmiddels in Periode 3 zitten.``

> In deze opdracht moet je zowel een Javascript als een PHP script ontwikkelen. Je kennis van beide onderwerpen komen dus aan bod! Mocht je er met het PHP script niet uitkomen, dan kun je aan de docent JS om de uitwerking hiervoor vragen. Je krijgt dan echter maar één punt.

**Opdracht**

We willen graag een systeem maken waar we onze highscores (van een nog niet bestaand spel) naartoe kunnen sturen. Deze moeten op een server opgeslagen worden, zodat we deze later weer kunnen opvragen.
We gaan in dit geval daarom via een PHP script de highscores opslaan in de cookies. Daarna is het de bedoeling dat we de highscores uit het PHP script weer gesorteerd op onze website laten zien.

Het is dus de bedoeling dat we via jQuery en AJAX highscores gaan sturen naar een eigen gemaakt PHP script. Dit PHP script slaat de nieuwe highscores op in een cookie. De website moet ook weer via dit PHP script de highscores kunnen uitlezen, om deze te tonen aan de bezoeker!    

### 1. Stappenplan: Maken PHP script

> Kom je er niet uit met het PHP script? Blijf niet hang, maar vraag deze dan op bij de docent JS. Je krijgt dan wel maar één punt voor de huiswerkopdracht.

1. Maak een nieuwe map aan in je huiswerkmap. In deze map zet je zowel je PHP als je HTML / JS / CSS bestanden.
2. Maak een nieuwe php bestand aan (bedenk zelf een naam)
3. Laat het PHP script de volgende dingen doen:
    - In een *cookie* is in eerste instantie een lege *array* aanwezig 
    - Zodra er GET variabele genaamd "newHighscore" in de URL zit, dient de waarde hiervan weggeschreven te worden in de *array* van de *cookie* (Denk terug aan Hoofdstuk 10 van PHP, periode 2).
    - Lees de *array* uit naar een nieuwe variabele en sorteer de array, zodat de hoogte score bovenaan staan. Gebruik hiervoor de functie *sort()*
    - Zorg ervoor dat de hierboven gemaakte *array* als *JSON* geencode wordt en sla dit op in een variabele. Zie codevoorbeeld 1 hieronder
    - Echo deze variabele (json is immers niets meer dan een normale *string*)
4. Run je script en test deze door enkele highscores alvast toe te voegen!

*Codevoorbeeld 1: Omzetten van een variabele naar JSON string*

``PHP
$jsonString = json_encode($cookieArray);
``

### 2. Stappenplan: Maken JS Script
1. Maak zelf een nieuw HTML bestand aan en maak de standaard HTML opzet zoals je deze in de lessen HTML / CSS geleerd hebt
2. Koppel hier de jQuery library aan
3. Koppel hier een leeg .js bestand aan
4. Maak de website (ongeveer) zoals hieronder in visueel voorbeeld 1 te zien is
5. Zorg ervoor dat bij het klikken op de "Versturen!" knop de volgende dingen gebeuren
    - Lees de waarde van het input element uit (Zie reader 1)
    - Maak een AJAX request naar je zojuist gemaakte PHP script
    - Voeg in de URL van dit AJAX request de GET parameter "newHighscore" toe en vergeet niet de waarde van het inut veld als waarde van deze GET parameter mee te geven 
    - Laat een melding zien zodra het AJAX request gelukt is
    - Laat een error zien zodra het AJAX request mislukt is (Zie reader 4 hiervoor)
6. Zorg ervoor dat bij het klikken op de "Updaten" button de volgende dingen gebeuren
    - Maak een AJAX request naar het eerder gemaakte PHP script
    - Vang de uitkomst op in een variabele
    - Bepaal (bv via de *debugger*) of je het resultaat moet omzetten via *parseJSON()* (Zie reader)
    - Toon de highscores als listitems in een UL
7. Klaar? Bekijk de beoordelingscriteria of je niets vergeten bent

**Extra  opdracht: (Hiermee krijg je alsnog één punt voor een eerder gemiste huiswerkopdracht!)**
1. Verstuur de highscore niet als GET parameter, maar als POST parameter. Zie de reader hiervoor
2. Vergeet dit niet ook in de PHP door te voeren

### Visueel voorbeeld 1
<img src style="width: 80%" src="https://raw.githubusercontent.com/ictacademiekw1c/opdrachten-repository/master/javascript/p3/productie/Afbeeldingen/360-1.png">

**Beoordelingscriteria**

**Javascript**
1. De Update en de versturen buttons maken gebruik van 2 verschillende AJAX requests
2. De website moet een nieuwe highscore kunnen opsturen
3. Je krijgt een melding zodra het AJAX request om een highscore te posten is geslaagd (of juist niet)
3. Na het opsturen van een highscore, moet deze via het drukken op de "Update" button zichtbaar worden

**PHP**
1. Het PHP script echo't valide een JSON string
2. Het PHP script kan via de GET paramater "newHighscore" nieuwe highscores ontvangen
3. Het PHP script slaat deze highscores in een cookie op

