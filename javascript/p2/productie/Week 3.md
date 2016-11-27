## Opdracht 230 Objecten: Het KW1C nabootsen

`` Opleveren: Plaats al je gemaakte bestanden (.js, .html ) in een een rar met naam OPDRACHT230.rar en upload deze in je portfolio. Laat daarna de opdracht zien aan de docent om deze af te tekenen. Onthoud bij het uploaden dat we inmiddels in Periode 2 zitten.``

### Objecten: Het KW1C College nabootsen

>> **Tip:** Je kunt de presentaties de we gegeven hebben via N@tschool terug kijken. Klik op het mapje "Presentaties" en daarna het weeknummer.

**Opdracht**
We gaan wat gegevens die we hebben over het KW1C in een *object* zetten. 
Hierdoor bootsen we binnen onze webpagina het KW1C na, zodat we in staat zijn om daarna de gegevens over het KW1C te laten zien in onze webpagina. Ook kunnen we later gemakkelijk deze gegevens aanpassen.

1. Maak een nieuw HTML document aan en koppel hier een extern JavaScript bestand aan
2. Maak onderstaande &lt;table&gt; aan in de HTML. Geef alle 2é &lt;td&gt; kolommen een uniek ID attribuut (hier gaan we later data in plaatsen):
![Webpagina om na te maken](https://raw.githubusercontent.com/ictacademiekw1c/opdrachten-repository/master/javascript/p2/productie/afbeeldingen/Opdracht230_2.png)
3. Maak een nieuw *object* variabele aan (bedenk zelf een naam) en koppel de volgende gegevens aan dit *object*:
	- Naam: "Koning Willem 1 College"
	- Student van het jaar: "Asef Mahmoudi"
	- Beste afdeling: "ICT Academy"
	- Vestigingen: 7
	- Werknemers: 1171
	- Leerlingen: 11930
	- VSV'ers (Vroegtijdig School Verlater): 311
	- Jaarlijkse omzet (euro): 88.457.940
	- Jaarlijkse uitgaven (euro): 88.098.573
	- Weet je zelf nog leuke gegevens? Voeg ze toe!
3. Maak een nieuwe *function* aan genaamd "drawStatistics" die één *parameter* (schoolStatistics) accepteerd. Laat deze functie de volgende dingen doen:
	- De schoolStatistics *parameter* die je hier binnenkrijgt is de eerder aangemaakte *object* variabele 
	- Zorg ervoor dat de gemaakte table (uit punt 3) gevuld wordt met data uit de schoolStatistics *parameter*. Zie onderstaande screenshot
![Webpagina om na te maken](https://raw.githubusercontent.com/ictacademiekw1c/opdrachten-repository/master/javascript/p2/productie/afbeeldingen/Opdracht230.png)
*Je mag de pagina zelf helemaal aanpassen zoals je zelf wilt. Zolang de 9 object properties er maar door de JavaScript erin geplaatst zijn*
4. Maak een nieuwe button aan in de HTML
5. Test de pagina
6. Schijf je naam en de datum van vandaag naar de console

### Extra opdracht (voor de eindbazen onder jullie!):
We gaan het aangemaakte *object* uitbreidden met 2 zogeheten *Object methods*. Lees meer <a href="http://www.w3schools.com/js/js_object_methods.asp" target="_blank">hierover</a>

1. Voeg een zogeheten *Object method* toe aan je aangemaakte object van punt 3 (functie binnen een object) genaamd *addLeerling()*. Deze functie verhoogt het leerlingen aantal op met 1
2. Schrijf nog een *Object method* genaamd *removeLeerling()* die het aantal leerlingen verlaagt met 1
3. Voer via de inspector een paar keer *addLeerling()* uit. Doe dit op je aangemaakte object
4. Voer via de inspector de eerder gemaakte *drawStatistics()* daarna uit, zodat je table geupdate wordt
5. Je kan eventueel ook een button maken die *drawStatistics()* uitvoert (via een onClick event)
5. De table zou nu moeten geupdate zijn met een ander leerling aantal!

>> Lees meer over Object methods: http://www.w3schools.com/js/js_object_methods.asp  


**Beoordelingcriteria**
1. Je hebt een object aangemaakt met minimaal 9 properties
2. Je hebt de gegevens uit het *object* variabele gehaald
3. Je hebt een table gebruikt in de HTML
4. De functie drawStatistics doet het werk wat betreft het tonen van de gegevens
5. Er is voldoende en logisch commentaar geplaatst in de code
6. Je hebt je naam en de datum van maken naar de console gestuurd

---

## Opdracht 231 Klikcounter

`` Opleveren: Plaats al je gemaakte bestanden (.js, .html ) in een een rar met naam OPDRACHT231.rar en upload deze in je portfolio. Laat daarna de opdracht zien aan de docent om deze af te tekenen. Onthoud bij het uploaden dat we inmiddels in Periode 2 zitten.``

>> In deze opdracht vragen we wat uitzoekwerk van jullie zelf. Lees daarom de opdracht goed door en gebruik de hulpbronnen!

**Opdracht**

We gaan in deze opdracht een spelletje maken. Het doel van het spel is om zovaak mogelijk te klikken op een button binnen 5 seconden. Hiervoor gebruiken we kennis van week 1 en week 2.
Ook gaan we stof behandelen die nieuw is voor jullie. Zo gaan we onder andere gebruik maken van een timer.

Begin dus met het nabouwen van onderstaande afbeelding in de HTML. Maak daarna het spel, zoals het uitgelegd is in de speluitleg.

![Webpagina om na te maken](https://raw.githubusercontent.com/ictacademiekw1c/opdrachten-repository/master/javascript/p2/productie/afbeeldingen/Opdracht231.png)

**Speluitleg**

Als de gebruiker op de knop 'Start het spel' klikt, verschijnt er onder de button een nieuwe
button met de tekst 'Klik hier'. Het is de bedoeling dat de speler zo vaak mogelijk op die knop
drukt. Na 5 seconden verdwijnt de button weer. De score van de speler is gelijk aan het aantal
keer dat er op de knop is gedrukt.

Afhankelijk van zijn of haar score wordt bepaald of de speler een highscore heeft behaald. Geef feedback of de gebruiker een highscore heeft behaald en op 
welke plaats de speler heeft behaald, of dat de gebruiker geen highscore heeft behaald. 
Dit doe je door het bewerken van een paragraaftekst (dus geen alert).

**Hulpbronnen**
<a href="http://www.w3schools.com/jsref/prop_style_display.asp" target="_blank">Elementen verbergen / tonen met Javascript (display: none)</a>
<a href="http://www.w3schools.com/jsref/prop_style_display.asp" target="_blank">Elementen verbergen / tonen met Javascript (visibility: hidden)</a>
<a href="http://www.w3schools.com/jsref/prop_html_innerhtml.asp" target="_blank">Text wegschrijven in een P element</a>
<a href="http://www.w3schools.com/js/js_timing.asp" target="_blank">Werken met een timer</a>
<a href="http://www.w3schools.com/js/js_arrays.asp" target="_blank">Aanmaken van Arrays</a>
<a href="http://www.w3schools.com/js/js_array_methods.asp" target="_blank">Standaard array functies</a>
<a href="http://www.w3schools.com/jsref/jsref_obj_array.asp" target="_blank">Algemene array info</a>
<a href="http://www.w3schools.com/jsref/jsref_sort.asp" target="_blank"></a>


**Beoordelingcriteria**
1. Javascript code is geschreven in een eigen JavaScript-bestand.
2. CSS code is geschreven in een eigen CSS-bestand.
3. De code is voorzien van waardevol commentaar.
4. De webpagina bevat alle HTML-elementen die nodig zijn voor het spel.
5. Als je op de aanwezige button klikt verschijnt er een nieuwe button met de tekst 'Klik hier'.
6. De nieuwe button blijft slechts 5 seconden in beeld.
7. De score van de speler is gelijk aan het aantal keer klikken
8. binnen de 5 seconden. Dit geldt ook voor een eventuele volgende ronde.
9. De feedback of de gebruiker een highscore gehaald heeft wordt weergegeven in een paragraaf.
10. In de feedback wordt aangegeven op welke plaats de speler terecht is gekomen of dat de speler geen highscore gehaald heeft.
11. De score wordt op de juiste positie toegevoegd in de highscore tabel.
12. Er is gebruik gemaakt van een functie op het moment dat de code meer dan 1x gebruikt wordt.