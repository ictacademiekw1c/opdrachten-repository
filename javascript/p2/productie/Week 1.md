## Opdracht 210 Boodschappenlijstje dmv Array's

`` Opleveren: Plaats al je gemaakte bestanden (.js, .html ) in een een rar met naam OPDRACHT210.rar en upload deze in je portfolio. Laat daarna de opdracht zien aan de docent om deze af te tekenen. Onthoud bij het uploaden dat we inmiddels in Periode 2 zitten.``

### Arrays

>> **Tip:** Je kunt de presentaties de we gegeven hebben via N@tschool terug kijken. Klik op het mapje "Presentaties" en daarna het weeknummer.

**Opdracht:**
In deze opdracht gaan we boodschappenlijst tool maken. We gaan de gebruiker 5 items laten opgeven (ons boodschappenlijstje is voor deze opdracht maar 5 items groot), die worden in ons boodschappenlijstje geplaatst (middels een *array*).
Daarna laten we het boodschappen lijstje weer zien aan de gebruiker middels een &lt;OL&gt; element.

1. Maak een nieuw HTML bestand aan en koppel daar een extern JS bestand aan
2. Maak in het HTML bestand een &lt;OL&gt; aan met 5 &lt;LI&gt; elementen. Geef ze alle 5 een uniek ID attribuut. Laat deze elementen verder voor nu nog leeg
2. Laat via JavaScript aan de gebruiker 5x een vraag zien om een item op te geven
3. Sla de input (de 5 items) van de gebruiker op in een Array (Zie presentaties week 1, les 1 voor voorbeeld code)
4. Laat de 5 items vanuit de Array zien via de HTML. Doe dit in de 5 eerder aangemaakte &lt;LI&gt; elementen. Tip: Kijk de presentaties van Week 1 Les 1 door!
5. Zorg er dus voor de ieder &lt;LI&gt; element één boodschappenitem laat zien. Tip: Open de cheatsheet van Periode 1.
5. Stuur je naam en de datum van maken naar de console
6. Onthoud bij het uploaden dat we inmiddels in Periode 2 zitten!

**Beoordelingscriteria**
1. De gebruiker krijgt 5 losse vragen over zijn toe te voegen boodschappen
1. Je voegt de items toe aan de array via de *push()* of *unshift()*
2. Je plaatst de boodschappen items in een array en leest vanuit daaruit ze uit naar de HTML
3. Je laat de 5 items zien in de HTML &lt;LI&gt; elementen
4. Je naam en datum staan in de console

---

## Opdracht 211 While loop: Raad het getal

`` Opleveren: Plaats al je gemaakte bestanden (.js, .html ) in een een rar met naam OPDRACHT211.rar en upload deze in je portfolio. Laat daarna de opdracht zien aan de docent om deze af te tekenen. Onthoud bij het uploaden dat we inmiddels in Periode 2 zitten.``

### "Raad het getal" via een while loop

>> **Tip:** Je kunt de presentaties de we gegeven hebben via N@tschool terug kijken. Klik op het mapje "Presentaties" en daarna het weeknummer.

**Opdracht**
We gaan in deze opdracht opnieuw het spel "raad het getal" maken! Nu zul je waarschijnlijk denken: Waarom? 
We doen dit namelijk deze keer door gebruik te maken van een while loop. Je zult zien dat het deze maal vele keren simpeler is om dit spel te maken
Om je wat tijd te besparen zijn de regels iets simpeler dan de eindopdracht. Lees ze dus goed door

1. Genereer een random getal tussen de 1 en 10 (zie de code uit je eindopdracht of gebruik Google)
2. Gebruik een *while* loop om de gebruiker continue te blijven vragen om een getal in te geven
3. Beëindig deze loop zodra het juiste getal geraden is
4. Zorg er ook voor dat er bij gehouden wordt hoeveel pogingen er gedaan zijn
5. Toon na het raden van het getal een felicitatiemelding met het aantal pogingen erbij. Deze mag je zelf verzinnen
6. Stuur daarna je naam en de datum van maken naar de console!

**Nieuwe spelregels "Raad het getal"**
- De speler heeft oneindig aantal pogingen om het getal te raden. Een verliesmelding hoef je dus niet te laten zien
- Je hoeft de gebruikersinvoer niet controleren via IsNan o.i.d. We gaan ervanuit dat de gebruiker netjes een getal invoert
- Toon wel nog steeds per poging of de gebruiker te hoog of te laag was
- Toon na het goed raden van het getal het aantal pogingen

**Beoordelingscriteria**
1. Je gebruikt een *while* loop om het spel te laten werken
2. Het aantal pogingen wordt bijgehouden in een variabele en aan het einde getoond
3. Het aantal pogingen is oneindig (zolang de *while* loop blijft lopen)
4. Aan het einde wordt een melding getoond van het aantal pogingen

>> Mocht de opdracht nog te lastig voor je zijn, maak lesopdracht 2 nogmaals. Lees ook het naslagwerk wat je kunt vinden in de lesopdrachten. Lees ook goed de beoordelingscriteria door!


---

## Opdracht 212 Boodschappenlijstje met een for EN while loop

`` Opleveren: Plaats al je gemaakte bestanden (.js, .html ) in een een rar met naam OPDRACHT212.rar en upload deze in je portfolio. Laat daarna de opdracht zien aan de docent om deze af te tekenen. Onthoud bij het uploaden dat we inmiddels in Periode 2 zitten.``

### Boodschappenlijstje met een for EN while loop

>> **Tip:** Je kunt de presentaties de we gegeven hebben via N@tschool terug kijken. Klik op het mapje "Presentaties" en daarna het weeknummer (Week 2). 

**Opdracht**
We gaan het boodschappenlijstje uit opdracht 210 wat oppimpen. We gaan namelijk nu ook toevoegen dat het uitlezen van de boodschappenitems via een *for* loop gaat gebeuren.
We slaan nog steeds de boodschappenitems opslaan in een *Array* (Tip: bekijk opdracht 210), maar daarna de boodschappenitems uitlezen door middel van een for loop.

1. Maak een nieuw HTML bestand aan en koppel daar een extern JS bestand aan
2. Maak in het HTML bestand een &lt;OL&gt; aan met 5 &lt;LI&gt; elementen. Geef ze alle 5 een uniek ID attribuut.
2. Laat via JavaScript aan de gebruiker 5x een vraag zien om een item op te geven
3. Sla de input (de 5 items) van de gebruiker op in een Array (Zie presentaties week 1, les 1 voor voorbeeld code)
4. Laat de 5 items vanuit de Array zien via de HTML. Doe dit op de volgende manier:
	- Zorg dat de array uitgelezen wordt vanuit een *for* loop
	- Hoe je &lt;LI&gt; items vult, mag je zelf weten. *Tip: Je mag een ID ook een getal als naam geven. Deze zou je bijvoorbeeld kunnen laten overeenkomen met je teller variabele.*
5. Zorg er dus voor de ieder &lt;LI&gt; element één boodschappenitem laat zien. Tip: Open de cheatsheet van Periode 1.
5. Stuur je naam en de datum van maken naar de console
6. Onthoud bij het uploaden dat we inmiddels in Periode 2 zitten!

**Beoordelingscriteria**
1. De gebruiker krijgt 5 losse vragen over zijn toe te voegen boodschappen
1. Je voegt de items toe aan de array via de *push()* of *unshift()*
2. Je plaatst de boodschappen items in een array en leest vanuit daaruit ze uit naar de HTML
3. Je gebruikt een *for* loop om de boodschappen array uit te lezen
4. Je laat de 5 items zien in de HTML &lt;LI&gt; elementen
4. Je naam en datum staan in de console 

>> Mocht de opdracht nog te lastig voor je zijn, maak de lesopdrachten 1 en 3 nogmaals. Lees ook het naslagwerk wat je kunt vinden in de lesopdrachten. Lees ook goed deze beoordelingscriteria door!

