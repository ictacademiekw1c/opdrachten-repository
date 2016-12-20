## Lesopdracht 1 (arrays)

`` Klaar? Toon de uitwerking aan de docent, daarna mag je verder werken aan je huiswerk.``

**Opdracht**
We gaan een *array* maken met de namen van minimaal 10 klasgenoten. Daarna gaan we dit lijstje aan de gebruiker laten zien.

1. Maak een nieuwe *array* variabele aan. Bedenk een zinnige naam voor deze variabele
2. Vul deze array met de namen van minimaal 10 klasgenoten
3. Toon al deze namen stuk voor stuk aan de gebruiker. Je mag zelf bedenken hoe je namen toont
4. Voer je script uit om te kijken of je de namen van je klasgenoten ziet!

**Naslagwerk**
- <a href="http://www.w3schools.com/js/js_arrays.asp" target="_blank">Arrays maken en uitlezen</a>


---
## Lesopdracht 2 (while loop)

`` Klaar? Toon de uitwerking aan de docent, daarna mag je verder werken aan je huiswerk.``

**Opdracht**
We gaan via een *while* loop de gebruiker forceren om toe te geven dat hij het van het KW1C houdt. We gaan namelijk de *while* loop laten draaien totdat de gebruiker (via een *prompt()*) de zin "Ik hou van het KW1C" intypt.

1. Vraag de gebruiker of hij van het KW1C houdt (je mag zelf bepalen hoe je dit doet). Sla zijn antwoord op in een variabele.
2. Maak een *while* loop die blijft draaien zolang de inhoud van deze variabele niet gelijk is aan "Ik hou van het KW1C"
3. Stel binnen de *while* loop dezelfde vraag nogmaals, zodat de gebruiker lastig gevallen blijft worden met deze vraag, zolang hij niet het gewenste antwoord geeft.
4. Toon een melding "Wij houden ook van jou!" zodra de gebruiker toegegeven heeft dat hij van het KW1C houdt!
5. Voer je script uit om te kijken of hij werkt!

**Naslagwerk** 
- <a href="http://www.w3schools.com/js/js_loop_while.asp" target="_blank">While loops (skip het Do/While gedeelte)</a>


--- 
## Lesopdracht 3 (for loop) 

`` Klaar? Toon de uitwerking aan de docent, daarna mag je verder werken aan je huiswerk.``

**Opdracht**
We gaan via een *for* loop icm met een *if/else* statement een gebruiker 20 keer een *alert()* laten wegklikken. Omdat we begrijpen dat dat voor de gebruiker erg saai is, willen we hem graag aanmoedigen in dit proces.
Daarom gaan we aan de hand van zijn voortgang verschillende berichtjes laten zien (via *alert()*). 

1. Maak een *for* loop die 20 keer loopt. Tel hierin af van 20 naar 0
2. Geef aan de hand van de voortgang van de loop (tip: via een *if / else if / else*) verschillende *alert()*'s weer aan de gebruiker. Zie hieronder welke melding je wanneer moet laten zien. Je mag eventueel ook eigen bedachte aanmoedigingen voor de gebruiker tonen.
	- 1: "Hallo daar, klik mij aub door!"
	- 2 t/m 5: "Nog een keer aub!"
	- 6 t/m 10: "Dit gaat goed! Gewoon doorgaan"
	- 11 t/m 14: "Perfect! Nog heel even doorgaan"
	- 15 t/m 18: "Je bent er bijna... Zet hem op!"
	- 19: "Dit is de een na laatste.... Kom op!"
	- 20: "Jaaaaa je hebt het gehaald na deze klik! Netjes, netjes"
3. Voer je script uit om te kijken of hij werkt. 

**Naslagwerk**
- <a href="http://www.w3schools.com/js/js_loop_for.asp" target="_blank">For loops</a>


---
## Lesopdracht 4 (functions)

`` Klaar? Toon de uitwerking aan de docent, daarna mag je verder werken aan je huiswerk.``

**Opdracht**
We gaan in deze opdracht een soort rekenmachine bouwen die kan optellen, aftrekken, vermenigvuldigen en delen. De berekeningen worden door middel van *functions* uitgevoerd.
Omdat functions voor jullie nogal een nieuw iets is, gaan we de opdrachten steeds iets moeilijker maken.

1. Vraag eerst aan de gebruiker om 2 getallen op te geven. Sla deze getallen op. Je hoeft geen controles op de invoer uit te voeren.

### Deel 1 (functie zonder parameter)
1. Maak een functie genaamd *count()*. Laat de functie de volgende dingen doen: 
	- Vraag in deze functie via een *prompt()* 2 keer om een getal in te voeren aan de bezoeker
	- Doe een *parseInt()* over deze getallen, zodat we zeker weten dat we met *numbers* werken
	- Tel deze 2 getallen bij elkaar op en *alert()* de uitkomst
2. Laat je code de functie uitvoeren

### Deel 2 (functie met parameter)
1. Laat de gebruiker 2 getallen opgeven via *prompt()*. Sla deze 2 getallen op in variabelen
1. Maak een functie genaamd *multiply(getal1, getal2)*
2. Deze functie heeft 2 parameters (getal1 en getal2). Laat de functie de volgende dingen doen
	- *parseInt()* uitvoeren over deze 2 getallen (zie stap 1), zodat we zeker weten dat we met *numbers* werken.
	- Daarna de getallen vermenigvuldigen met elkaar en de uitkomst opslaan in een nieuwe variabele
	- De uitkomst laten zien aan de gebruiker (via *alert()*).
4. Maak nogmaals een functie, geef deze functie de naam *divide(getal1, getal2)* (delen) als functienaam. Laat deze functie de volgende zaken doen:
	- *parseInt()* uitvoeren over deze 2 getallen (zie stap 1), zodat we zeker weten dat we met *numbers* werken.
	- Daarna de getallen delen door elkaar en de uitkomst opslaan in een nieuwe variabele
	- De uitkomst laten zien aan de gebruiker (via *alert()*).
5. Laat je code de 2 functies uitvoeren

**Naslagwerk**
- <a href="http://www.w3schools.com/js/js_functions.asp" target="_blank">Functions</a>


---
## Lesopdracht 5 (Functions deel 2)

`` Klaar? Toon de uitwerking aan de docent, daarna mag je verder werken aan je huiswerk.``

**Opdracht**
In de vorige lesopdracht hebben we via functies een simpele rekenmachine gemaakt. Deze keer gaan we via een functie de gebruiker om een getal vragen, deze controleren en daarna via *return* een variabele vullen.
Het doel van deze opdracht is om een functie te schrijven die een getal vraagt aan een gebruiker, deze via de bekende manieren controlleert (isNan(), parseInt()). Dit doen we specifiek in een functie, zodat we deze functionaliteiten zoveel kunnen hergebruiken als dat we willen!
We gaan dus een functie schrijven die de gebruiker om een getal gaat vragen, hier allerlei acties over uitvoeren en uiteindelijk zal de functie een geldig getal *returnen*.
Ook gaan we wat commentaar toevoegen aan de code!

1. Maak een functie genaamd *getUserInput()* aan. Laat deze functie de volgende dingen doen:
	- Vraag via *prompt()* een getal op aan de gebruiker en sla deze op als een variabele
	- Voer *parseInt()* uit over het getal
	- Check of het getal geldig is via *isNan()*.
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

---
## Lesopdracht 6 (Events)

`` Klaar? Toon de uitwerking aan de docent, daarna mag je verder werken aan je huiswerk.``

**Opdracht**

We gaan enkele JavaScript events gebruiken om op verschillende manieren meldingen (*alert()*'s) te laten zien. We gaan dit doen door in de HTML een &lt;div&gt; element aan te maken en hierop enkele events aan te koppelen

1. Maak in je HTML een nieuwe &lt;H1&gt; element aan. Geef deze ook een ID attribuut (bedenk zelf een naam) en voer natuurlijk een zelf verzonnen titel hier in! 
2. Zorg ervoor dat er een *alert()* naar de gebruiker gaat (bedenk zelf leuke teksten) bij de volgende events op dit element:
	- onclick 
	- onmouseenter
	- oncontextmenu
3. Laat de volgende DOM events ook een *alert()* doen (dit doe je vanuit de JavaScript code, gebruik de *window.onload()* als voorbeeld). Probeer uit te vinden wanneer de events getriggerd worden
	- window.onload
	- document.onkeypress
	- window.onresize
	
>> Tip: Bekijk de voorbeelden van de events (<a href="http://www.w3schools.com/js/js_events_examples.asp" target="_blank">Klik hier</a>) om allerlei voorbeelden te bekijken

**Naslagwerk**
- <a href="hhttp://www.w3schools.com/js/js_events.asp" target="_blank">HTML Events (Events in de HTML plaatsen)</a>
- <a href="http://www.w3schools.com/js/js_events_examples.asp" target="_blank">Heel veel voorbeelden van events</a>	

---
## Lesopdracht 7 (objects)

`` Klaar? Toon de uitwerking aan de docent, daarna mag je verder werken aan je huiswerk.``

**Opdracht**

We gaan informatie die we hebben over het lokaal waar je je momenteel bevindt nabootsen in een *object* variabele.

1. Maak in je JavaScript code een nieuw *object* variabele aan. Bedenk zelf een passende naam
2. Zet de volgende informatie over het lokaal waar je momenteel in zit (tel dit zelf!):
	- Lokaalnummer
	- Aantal stoelen
	- Aantal ramen
	- Bord aanwezig? (Ja / Nee)
	- Beamer aanwezig? (Ja / Nee)
	- Aantal personen in dit lokaal
	- Kleur van de vloerbedekking
	- Aantal lampen
	- Bedenk zelf nog één ding dat je kan toevoegen over dit lokaal
3. *console.log()* daarna minimaal 3 dingen uit voorgaand lijstje.

**Extra opdracht**
1. Maak op het zojuist aangemaakte object een zogeheten "Object Method" (een functie binnen het object) genaamd "removeStudent()". Laat deze functie de volgende dingen doen
	- Verlaag het aantal leerlingen met één
	- Geef een alert() zodra de leerling succesvol verwijderd is. Geef ook een melding zodra er geen leerlingen meer over zijn om te verwijderen
2. Voer deze functie via de console tab in je Inspector uit (of handmatig via de JavaScript code)

**Naslagwerk**
- <a href="http://www.w3schools.com/js/js_objects.asp" target="_blank">Javascript Objects</a>
- <a href="http://www.w3schools.com/js/js_object_methods.asp" target="_blank">Object Methods (extra opdracht)</a>

--- 
## Lesopdracht 8 (Globale en lokale variabelen)

`` Klaar? Toon de uitwerking aan de docent, daarna mag je verder werken aan je huiswerk.``

**Opdracht**

1. Maak in je JavaScript een nieuwe functie genaamd "testFunctie" aan. Deze functie accepteerd één parameter genaamd *name* .Laat deze functie de volgende dingen doen:
	- Maak een nieuwe variabele genaamd *begroeting* aan. Zet hier de *name* en een verzin een welkomstekst
	- Toon *begroeting* aan de gebruiker
2. Voer de functie uit (bedenk zelf een waarde voor de *name*)
3. Probeer daaronder de variabele *begroeting* te alert'en. Krijg je een error?
4. Geef antwoord op de vraag: Bestaat de variabele *begroeting* buiten de functie?

---
## Lesopdracht 9 (jQuery toevoegen aan je website)

`` Klaar? Toon de uitwerking aan de docent, daarna mag je verder werken aan je huiswerk.``

**Opdracht**

1. Maak een nieuwe HTML bestand aan
2. Maak hier een &lt;H1&gt; element aan met een zelfverzonnen tekst en geef deze een ID attribuut met de waarde "zelfverzonnenTekst"
2. Koppel hier (zoals in de presentatie Week 4 Les 1 te zien is) de jQuery library aan
3. Koppel hier een extern JS bestand (Script.js) aan zoals je altijd doet
4. Maak binnen Script.js een *$(document).ready() {}* (Zie Week 4 Les 1, slide nummer 7) event aan
5. Voer onderstaande code binnen dit event uit:
```
	// Fade het element met ID "zelfverzonnenTekst" uit
	$("#zelfverzonnenTekst").fadeOut();
```

---
## Lesopdracht 10(Selectoren)

`` Klaar? Toon de uitwerking aan de docent, daarna mag je verder werken aan je huiswerk.``

**Opdracht**

1. Maak een nieuw HTML bestand aan
2. Koppel hier zoals in de vorige lessen de jQuery library aan
3. Koppel hier een extern JS bestand aan. Vergeet niet ```$(document)ready(  function() {  });``` toe te voegen aan je extern JS bestand
4. Voeg de volgende HTML code toe aan de &lt;body&gt;
```HTML
    <body>
        <h1>
			Dit is een H1 tag
		</h1>
        <h2>
			Dit is een H2 tag
		</h2>
        <p class="paragraaf1">
			Dit is een paragraaf met een class genaamd "paragraaf1". Dit is een paragraaf met een class genaamd "paragraaf1"
		</p>
        <h3 id="bericht1">
			Dit is een H3 met ID 'bericht1'
		</h3>        
    </body>
```
4. Laat het H1 element uitfaden via onderstaande jQuery code:
```	$("h1").fadeOut();```
5. Bedenk zelf de code om het H2 element te laden uitfaden!
6. Bedenk zelf de code om ook het element met de "paragraaf1" class uit te faden
7. Bedenk zelf de code om ook het element met het ID "bericht1" uit te faden

---
## Lesopdracht 11 (Selectors deel 2)

`` Klaar? Toon de uitwerking aan de docent, daarna mag je verder werken aan je huiswerk.``

**Opdracht**
1. Maak een nieuw HTML bestand aan
2. Koppel hier zoals in de vorige lessen de jQuery library aan
3. Koppel hier een extern JS bestand aan. Vergeet niet ```$(document).ready(  function() {  });``` toe te voegen aan je extern JS bestand
4. Voeg de volgende HTML code toe aan de &lt;body&gt;
```HTML
    <body>
		<div>
			<a href="">Eerste link</a>
		</div>
		<ul id="navbar">
			<li><a href="">Tweede sublink</a></li> 
			<li><a href="">Derde sublink</a></li>
		</ul> 
		<div id="content">
			<p>
				Paragraaf 1. Deze moet wegfaden bij de buttonklik!
			</p>
			<p>
				Paragraaf 2. Deze paragraaf mag niet wegfaden bij de buttonklik
			</p>
		</div>

		<a href="">Een andere link naar een andere pagina</a>
		<button onclick="doOpdracht5()">Opdracht 5</button>
		<button onclick="doOpdracht6()">Opdracht 6</button>
		<button onclick="doOpdracht7()">Opdracht 7</button>
    </body>
```
5. Opdracht 5: Zorg ervoor dat alle LI items van #navBar verborgen (via *fadeOut()*) worden zodra de eerste button (Opdracht 5) een klik krijgt. #navBar zelf mag niet verdwijnen!
6. Opdracht 6: Zorg ervoor dat alleen het eerste P element onder #content verborgen (via *fadeOut()*) wordt zodra de tweede button (Opdracht 6) een klik krijgt.  #content zelf mag niet verdwijnen!
7. Opdracht 7: Zorg ervoor dat alléén de eerste &lt;button&gt; onder de &lt;body&gt; verborgen wordt zodra de 3e button (Opdracht 7) een klik krijgt.

---
## Lesopdracht 12 (DOM aanpassingen)

`` Klaar? Toon de uitwerking aan de docent, daarna mag je verder werken aan je huiswerk.``

**Opdracht**
1. Maak een nieuw HTML bestand aan
2. Koppel hier zoals in de vorige lessen de jQuery library aan
3. Koppel hier een extern JS bestand aan
4. Voeg in dit extern js bestand de bekende document.ready() code toe (zie presentaties Week 4 Les1, Sheet 7)
4. Voeg de volgende HTML code toe aan de &lt;body&gt;
```HTML
<form action="index.html" method="post">
	<h1 class="mainTitle"></h1>
	<h2 id="introductie">Dit is een waardeloze introductietekst</h2>
	<table class="gegevensTable">
		<tr>
			<td>
				<label for="naam">
					Geef uw naam op
				</label>
			</td>
			<td>
				<input type="text" name="naam" id="naam">
			</td>
		</tr>
		<tr>
			<td>
				<label for="straat">
					Geef uw straatnaam op
				</label>
			</td>
			<td>
				<input type="text" name="straat" id="straat">
			</td>
		</tr>
		<tr>
			<td>
				<label for="email">
					Geef uw email op
				</label>
			</td>
			<td>
				<input type="text" name="email" id="email">
			</td>
		</tr>
		<tr>
			<td colspan="2">
				<input type="submit" value="Versturen">
			</td>
		</tr>
	</table>
</form>
```
5. "Launch in browser" om te kijken wat je precies gemaakt hebt
6. Laat via jQuery de volgende dingen gebeuren:
	- Geef de H1 met de class 'mainTitle' de text "Welkom op het inschrijf formulier". Tip: Kijk in de presentaties naar *.html()*
	- Voeg na iedere &lt;input&gt; deze html toe: ```<p>Verplicht!</p>```. Tip: Kijk in de presentaties naar *after()*
	- Voeg na de &lt;table&gt; deze html toe: ```<p>We zullen uw gegevens nooit verkopen aan derden</p>```. Tip: Kijk in de presentaties naar *before()*
	- Verwijder de h2 met de class "introductie". Tip: Kijk in de presentaties naar *remove()*
	
--- 
## Lesopdracht 13 (CSS Aanpassingen)

`` Klaar? Toon de uitwerking aan de docent, daarna mag je verder werken aan je huiswerk.``

**Opdracht**
1. Maak een nieuw HTML bestand aan
2. Koppel hier zoals in de vorige lessen de jQuery library aan
3. Koppel hier een extern JS bestand aan
4. Voeg in dit extern js bestand de bekende document.ready() code toe (zie presentaties Week 4 Les1, Sheet 7)
5. 
