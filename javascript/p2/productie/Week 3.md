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
4. Voer daarna de functie "drawStatistics" uit en vergeet niet je eerder aangemaakte *object* variabele mee te geven als parameter
5. Test de pagina
6. Schijf je naam en de datum van vandaag naar de console

### Extra opdracht (voor de eindbazen onder jullie!):
We gaan het aangemaakte *object* uitbreidden met 2 zogeheten *Object methods*. Lees meer <a href="http://www.w3schools.com/js/js_object_methods.asp" target="_blank">hierover</a>

1. Voeg een zogeheten *Object method* toe aan je aangemaakte object van punt 3 (functie binnen een object) genaamd *addLeerling()*. Deze functie verhoogt het leerlingen aantal op met 1
2. Schrijf nog een *Object method* genaamd *removeLeerling()* die het aantal leerlingen verlaagt met 1
3. Voer via de inspector een paar keer *addLeerling()* uit. Doe dit op je aangemaakte object
4. Voer via de inspector de eerder gemaakte *drawStatitics()* daarna uit, zodat je table geupdate wordt
5. De table zou nu moeten geupdate zijn met een ander leerling aantal!

>> Lees meer over Object methods: http://www.w3schools.com/js/js_object_methods.asp  


*De gegevens komen uit het jaarverslag van 2014. <a href="https://www.kw1c.nl/media/website/documenten/kw1cjaarverslag2014c.pdf" target="_blank">Klik hier</a>*

**Beoordelingcriteria*
1. Je hebt een object aangemaakt met minimaal 9 properties
2. Je hebt de gegevens uit het *object* variabele gehaald
3. De naam van de gebruiker wordt buiten de functie gevraagd
4. De functie drawStatistics doet het werk wat betreft het tonen van de gegeven
5. Er is voldoende en logisch commentaar geplaatst in de code
6. Je hebt je naam en de datum van maken naar de console gestuurd

---

## Opdracht 231

`` Opleveren: Plaats al je gemaakte bestanden (.js, .html ) in een een rar met naam OPDRACHT230.rar en upload deze in je portfolio. Laat daarna de opdracht zien aan de docent om deze af te tekenen. Onthoud bij het uploaden dat we inmiddels in Periode 2 zitten.``
