## Opdracht 220 Welkomsboodschap

`` Opleveren: Plaats al je gemaakte bestanden (.js, .html ) in een een rar met naam OPDRACHT220.rar en upload deze in je portfolio. Laat daarna de opdracht zien aan de docent om deze af te tekenen. Onthoud bij het uploaden dat we inmiddels in Periode 2 zitten.``

### Welkomsboodschap via een functie

>> **Tip:** Je kunt de presentaties de we gegeven hebben via N@tschool terug kijken. Klik op het mapje "Presentaties" en daarna het weeknummer.

**Opdracht**

We gaan de gebruiker zijn naam laten opgeven, waarna hij via een &lt;H1&gt; element begroet wordt! Dit alles doen we door middel van een functie.
We gaan dus een functie schrijven die aan de hand van een parameter (de naam die eerder opgegeven is) de *.innerHTML* van een H1 laten veranderen. 

1. Maak in je HTML een nieuwe H1 element. Geef deze een uniek ID attribuut mee
2. Schrijf (buiten het *window.onload()* event) een functie die 1 parameter accepteert (bv naam)
3. Laat deze functie de volgende dingen doen
	- Maak een nieuwe *string* variabele met een leuke welkomsboodschap voor de gebruiker. Laat in deze boodschap zijn opgegeven naam ergens terug komen
	- Schrijf deze boodschap weg naar het zojuist aangemaakte H1 element. Zie de cheatsheet mocht je hierop vastlopen
	- Schrijf naar de console je naam en de datum waarop je dit gemaakt hebt!
4. Vraag (binnen *window.onload()*) aan de gebruiker zijn naam. Sla deze op in een variabele
5. Voer daarna de functie uit die je hierboven gemaakt hebt. Vergeet niet de naam parameter mee te geven.
6. Stuur je naam en de datum van maken naar de console.

**Beoordelingcriteria*
1. Je hebt een functie gemaakt die minimaal één parameter accepteerd
2. De naam die de gebruiker eerder heeft opgegeven is zichtbaar ergens in de H1 
3. De naam van de gebruiker wordt buiten de functie gevraagd
4. De functie doet het werk wat betreft het tonen van de boodschap
5. Er is voldoende en logisch commentaar geplaatst in de code
6. Je hebt je naam en de datum van maken naar de console gestuurd

---
## Opdracht 221 Events, functies en nog veel meer pret!

`` Opleveren: Plaats al je gemaakte bestanden (.js, .html ) in een een rar met naam OPDRACHT221.rar en upload deze in je portfolio. Laat daarna de opdracht zien aan de docent om deze af te tekenen. Onthoud bij het uploaden dat we inmiddels in Periode 2 zitten.``

### Events, functies en nog meer pret!

**Opdracht**

In deze opdracht gaan we uitvinden wat voor dingen we allemaal met events kunnen doen! Daarom gaan we spelen met events en functies, om te kijken wat er allemaal mogelijk is.
Je bent vrij om zelf voor andere events te kiezen mocht je deze leuker vinden. Let er alleen op dat de beoordelingscriteria gehaald worden!

### HTML Sctructuur opzetten
1. Maak uiteraard weer een leeg HTML bestand aan en koppel hier een leeg JavaScript bestand aan
2. Maak in je HTML bestand een &lt;H1&gt; aan en geef deze een zelfverzonnen ID attribuut
3. Maak in je HTML bestand 3een &lt;H2&gt; element aan. Vul deze met eigen verzonnen teksten
4. Maak een &lt;P&gt; element aan en geef deze via de CSS een hoogte van 1800PX, zodat er horizontale scrollbalken ontstaan in je browser

### Mouse events
3. Zorg ervoor dat je 3 zelfverzonnen teksten (via *alert()*) te zien krijgt bij de volgende 3 events op het zojuist aangemaakte &lt;H2&gt; element:
	- onclick
	- onmouseenter
	- onmousedown
	- oncontextmenu
	
### DOM / Object Events
3. Schijf een nieuwe functie genaamd "eventCatcher" en zorg dat deze twee parameters genaamd *name* en *color* accepteerd. Laat deze functie de volgende dingen doen:
	- vervang de tekst binnen het H1 element van punt 2 naar "Bedankt! U heeft event {name} uitgevoerd". Zorg ervoor dat {name} uiteraard vervangen wordt door de eerste *name* parameter
	- Vervang de achtergrondkleur van de &lt;body&gt; van het document naar de kleur die via de *color* parameter binnenkomt (gebruik *RGB* of *HEX*). <a href="http://www.w3schools.com/jsref/prop_style_backgroundcolor.asp" target="_blank">Lees meer hierover</a>
	- Schrijf naar de *console* de volgende zin weg "Event {name} is uitgevoerd"
	- Vind er zelf nog minimaal één!
4. Zorg ervoor dat de eventCatcher functie aangeroepen wordt (bedenk zelf de waardes voor de *name* en *color* parameters) tijdens de onderstaande events. Bekijk het kopje "Frame / Object Events" van <a href="http://www.w3schools.com/jsref/dom_obj_event.asp" target="_blank">deze pagina</a> voor meer informatie.
	- Na het laden van de HTML en het downloaden van alle afbeeldingen en scripts (zie de cheatsheet)
	- Resizen van je browservenster
	- Scrollen door de pagina (vergeet niet punt 4 van het kopje "HTML Structuur opzetten" om scrollbalken te tonen)
	- Zodra een pagina getoond wordt (tip: *onpageshow*). Kijk wat het verschil is met *window.onload*
	- Vind er zelf nog minimaal één!
	

>> *Tip*: Check <a href="http://www.w3schools.com/js/js_events_examples.asp" target="_blank">deze link</a> voor een aardige lijst met bruikbare voorbeelden van events

**Beoordelingcriteria**
1. Je hebt minimaal 3 verschillende events direct in de HTML geplaatst (bv *onclick*, *onmouseover*)
2. Je hebt minimaal 3 verschillende DOM events gebruikt (bv *window.onload*, etc)

