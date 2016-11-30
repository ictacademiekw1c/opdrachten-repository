## Opdracht 240 HTML / CSS Opdracht 6.3 met jQuery opleuken!

`` Opleveren: Plaats al je gemaakte bestanden (.js, .html ) in een een rar met naam OPDRACHT240.rar en upload deze in je portfolio. Laat daarna de opdracht zien aan de docent om deze af te tekenen. Onthoud bij het uploaden dat we inmiddels in Periode 2 zitten.``

### Objecten: HTML / CSS Opdracht 6.3 met jQuery opleuken!

>> Heb je opdracht 6.3 niet gemaakt? Geen probleem, download <a href="" target="_blank">hier</a> de uitwerking.

**Opdracht**
We gaan jullie uitwerking van de HTML/CSS opdracht 6.3 een beetje opleuken (het recept voor Albert Heijn). Dit gaan we doen door gebruik te maken van de kracht van jQuery!
Zo gaan we de grote afbeelding laten infaden, de H1 komt met een effect binnen en ook doen we iets grappigs met de H2 en de P elementen. Wellicht kun je zelf nog een ander leuk effect vinden!


1. Kopieer / plak je uitwerking van opdracht 6.3. Mocht je dit niet hebben, dan kun <a href="" target="_blank">hier</a> de uitwerking downloaden.
2. Koppel hier de jQuery (zoals )
2. Maak onderstaande &lt;table&gt; aan in de HTML. Geef alle 2'e &lt;td&gt; kolommen een uniek ID attribuut (hier gaan we later data in plaatsen):
![Webpagina om na te maken](https://raw.githubusercontent.com/ictacademiekw1c/opdrachten-repository/master/javascript/p2/productie/Afbeeldingen/Opdracht230.png)
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
![Webpagina om na te maken](https://raw.githubusercontent.com/ictacademiekw1c/opdrachten-repository/master/javascript/p2/productie/Afbeeldingen/Opdracht230_2.png)
*Je mag de pagina zelf helemaal aanpassen zoals je zelf wilt. Zolang de 9 object properties er maar door de JavaScript in geplaatst zijn*
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
1. 
5. Er is voldoende en logisch commentaar geplaatst in de code
6. Je hebt je naam en de datum van maken naar de console gestuurd

---
