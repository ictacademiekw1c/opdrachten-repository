
---
## Lesopdracht 1 (functions)

`` Klaar? Toon de uitwerking aan de docent, daarna mag je verder werken aan je huiswerk.``

**Opdracht**

We gaan in deze opdracht een soort rekenmachine bouwen die kan optellen, aftrekken, vermenigvuldigen en delen. De berekeningen worden door middel van *functions* uitgevoerd.
Omdat functions voor jullie nogal een nieuw iets is, gaan we de opdrachten steeds iets moeilijker maken.

1. Download de template en plaats deze in de map "Hoofdstuk 7/Lesopdrachten/Lesopdracht 1".

### Deel 1 (functie zonder parameter)
1. Maak een functie genaamd *count()*. Laat de functie de volgende dingen doen: 
	- Vraag in deze functie via een *prompt()* 2 keer om een getal in te voeren.
	- Tel deze 2 getallen bij elkaar op en *alert()* de uitkomst.
2. Laat je code de functie uitvoeren.

### Deel 2 (functie met parameter)
1. Laat de gebruiker 2 getallen opgeven via *prompt()*. Sla deze 2 getallen op in variabelen.
1. Maak een functie genaamd *multiply(getal1, getal2)*.
2. Deze functie heeft 2 parameters (getal1 en getal2). Laat de functie de volgende dingen doen
	- Daarna de getallen vermenigvuldigen met elkaar en de uitkomst opslaan in een nieuwe variabele
	- De uitkomst laten zien aan de gebruiker (via *alert()*).
4. Maak nogmaals een functie, geef deze functie de naam *divide(getal1, getal2)* (delen) als functienaam. Laat deze functie de volgende zaken doen:
	- Daarna de getallen delen door elkaar en de uitkomst opslaan in een nieuwe variabele
	- De uitkomst laten zien aan de gebruiker (via *alert()*).
5. Voeg commentaar toe aan je code.
6. Laat je code de 2 functies uitvoeren

**Naslagwerk**
- <a href="http://www.w3schools.com/js/js_functions.asp" target="_blank">Functions</a>


---
## Lesopdracht 2 (Functions deel 2)

`` Klaar? Toon de uitwerking aan de docent, daarna mag je verder werken aan je huiswerk.``

**Opdracht**

In de vorige lesopdracht hebben we via functies een simpele rekenmachine gemaakt. Deze keer gaan we via een functie de gebruiker om een getal vragen, deze controleren en daarna via *return* een variabele vullen.
Het doel van deze opdracht is om een functie te schrijven die een getal vraagt aan een gebruiker, deze via de bekende manieren controlleert (isNan(), parseInt()). Dit doen we specifiek in een functie, zodat we deze functionaliteiten zoveel kunnen hergebruiken als dat we willen!
We gaan dus een functie schrijven die de gebruiker om een getal gaat vragen, hier allerlei acties over uitvoeren en uiteindelijk zal de functie een geldig getal *returnen*.
Ook gaan we wat commentaar toevoegen aan de code!

1. Download de template en plaats deze in de map "Hoofdstuk 7/Lesopdrachten/Lesopdracht 2".

1. Maak een functie genaamd *getUserInput()* aan. Laat deze functie de volgende dingen doen:
	- Vraag via *prompt()* een getal op aan de gebruiker en sla deze op als een variabele
	- Zet deze variabele om naar een Number via *parseInt()* uit over het getal. Lees <a href="https://www.w3schools.com/jsref/jsref_parseint.asp" target="_blank">hier</a> wat *parseInt()* doet.
	- Check of het getal geldig is via *isNan()*. Lees <a href="https://www.w3schools.com/jsref/jsref_isnan.asp" target="_blank">hier</a> wat *isNan()* doet.
		- Als het getal niet geldig, geef een meldig en *return* het de waarde 0
		- Als het getal wel geldig is, *return* het getal vanuit de functie
2. Laat de functie 5 keer uitgevoerd worden. Vang dus ook 5 keer het resultaat van de functie op in een variabele. Hieronder zie je een voorbeeld voor 1 keer aanroepen van de functie.
```javascript
	// Voer 1 keer de getUserInput() uit.
	var getal1 = getUserInput();
	
	// Laat het opgegeven getal aan de gebruiker zien
	alert("Getal 1 is: " + getal1);
```
3. Zorg dat je minimaal op 3 plekken commentaar hebt geplaatst

**Naslagwerk**
- <a href="http://www.w3schools.com/js/js_functions.asp" target="_blank">Functions (Kopje "Function Return")</a>
- <a href="https://www.w3schools.com/jsref/jsref_isnan.asp" target="_blank">isNan()</a>
- <a href="https://www.w3schools.com/jsref/jsref_parseint.asp" target="_blank">parseInt()</a>

--- 