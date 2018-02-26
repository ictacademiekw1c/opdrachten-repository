##Lesopdracht 1 (Events)

``Klaar? Toon de uitwerking aan de docent, daarna mag je verder werken aan je huiswerk.``

**Opdracht**

We gaan enkele HTML events gebruiken om op verschillende manieren meldingen (*alert()*'s) te laten zien. We gaan dit doen door in de HTML een &lt;H1&gt; element aan te maken en hierop enkele events aan te koppelen

1.  Maak in je HTML een nieuw &lt;H1&gt; element aan. Natuurlijk zorg je voor een zelf verzonnen titel in dit &lt;H1&gt; element!

2.  Zorg ervoor dat er een *alert()* naar de gebruiker gaat (bedenk zelf leuke teksten) bij de volgende events op dit element:

    -   onclick
    -   onmouseenter
    -   oncontextmenu

Tip: Bekijk de voorbeelden van de events ([*Klik hier*](https://www.w3schools.com/tags/ref_eventattributes.asp)) om allerlei voorbeelden te bekijken

**Naslagwerk**

-   <a href="https://www.w3schools.com/js/js_events.asp" target="_blank">HTML Events (Events in de HTML plaatsen)</a>
-   <a href="https://www.w3schools.com/tags/ref_eventattributes.asp" target="_blank">Heel veel voorbeelden van events</a>


---

##Lesopdracht 2 (Events)

``Klaar? Toon de uitwerking aan de docent, daarna mag je verder werken aan je huiswerk.``

**Opdracht**

We gaan enkele HTML events gebruiken om op verschillende manieren meldingen (console.logs()'s) te laten zien. We gaan dit doen door in de HTML een &lt;H1&gt`` element aan te maken en hierop enkele events aan te koppelen

1.	Maak in je HTML een nieuw ``<input type="text">`` element aan. Zorg voor een standaard tekst in dit element!

2.	Zorg ervoor dat er een console.log() melding gegenereerd wordt (bedenk zelf toepasselijke teksten) bij de volgende events op dit element:

- onselect
- onchange
- onkeydown

Tip: Bekijk de voorbeelden van de events ([*Klik hier*](https://www.w3schools.com/tags/ref_eventattributes.asp)) om allerlei voorbeelden te bekijken

**Naslagwerk**

-   <a href="https://www.w3schools.com/js/js_events.asp" target="_blank">HTML Events (Events in de HTML plaatsen)</a>
-   <a href="https://www.w3schools.com/tags/ref_eventattributes.asp" target="_blank">Heel veel voorbeelden van events</a>

---
## Lesopdracht 3 (jQuery toevoegen aan je website)

`` Klaar? Toon de uitwerking aan de docent, daarna mag je verder werken aan je huiswerk.``

**Opdracht**

1. Maak een nieuwe HTML bestand aan
2. Maak hier een &lt;H1&gt; element aan met een zelfverzonnen tekst en geef deze een ID attribuut met de waarde "zelfverzonnenTekst"
2. Koppel hier (zoals in de presentatie te zien is) de jQuery library aan
3. Koppel hier een extern JS bestand (Script.js) aan zoals je altijd doet
4. Voer onderstaande code uit:
```
	// Fade het element met ID "zelfverzonnenTekst" uit
	$("#zelfverzonnenTekst").fadeOut();
```
5. Bedenk zelf hoe dit &lt;H1&gt; element daarna weer ingefade kan worden.

---
## Lesopdracht 4 (Selectoren)

`` Klaar? Toon de uitwerking aan de docent, daarna mag je verder werken aan je huiswerk.``

**Opdracht**

1. Maak een nieuw HTML bestand aan
2. Koppel hier zoals in de vorige lessen de jQuery library aan
3. Koppel hier een extern JS bestand aan. Vergeet ``defer``` niet.
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
			<span>Dit is een span binnen de paragraag</span>
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
8. Bedenk zelf de code om ook het SPAN element binnen de H1 uit te faden
**Extra**
9. Bedenk zelf de code om daarna alle elementen binnen de BODY weer in te faden


---
## Lesopdracht 5 (CSS Selectoren)

`` Klaar? Toon de uitwerking aan de docent, daarna mag je verder werken aan je huiswerk.``

Bij deze lesopdracht heb je twee opties. Je hoeft dus niet allebei de opdrachten te maken, maar je mag kiezen welke van de twee je uitvoert. 

**Keuze 1:**
Doorloop de 32 levels van CSS Diner op https://flukeout.github.io/ 


**Keuze 2:** 
Doorloop de opdrachten die horen bij de kopjes 
-	CSS Combinators
-	CSS Pleudo-classen
-	CDD Pseudo Elements 

op deze site: <a href="https://www.w3schools.com/css/exercise.asp" target="_blank">w3schools</a> 
Naslagwerk
•	Alle selectoren zijn terug te vinden op W3Schools: <a href="http://www.w3schools.com/jquery/jquery_ref_selectors.asp">w3 schools</a>


