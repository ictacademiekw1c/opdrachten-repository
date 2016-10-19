# Eindopdracht
`` Uploaden en opsturen: Je pakt alle bestanden in een rar bestand en upload deze naar je JavaScript-map in je portfolio op N@tschool. Maak hiervoor een extra map aan genaamd "Eindopdracht periode 1" en upload je rar bestand hierin! `` 

## Spel: Raad het getal!

**Introductie**<br>
We gaan in deze eindopdracht een simpele uitvoering van het spelletje "Raad het getal" maken. In "Raad het getal" is het de bedoeling dat de speler binnen 3 pogingen het juiste getal raadt. De computer geeft hints door "Het getal is hoger dan jouw geraden getal" of "Het getal is lager dan jouw geraden getal" te zeggen.
De bedoeling is dat we al onze opgedane JavaScript kennis, samen met HTML en CSS gaan gebruiken om dit spelletje te maken. 

We raden je aan om de cheatsheet te gebruiken en om de presentaties (te vinden in N@tschool) na te lezen.
De opdracht bestaat uit meerdere delen, die steeds wat lastiger worden. Vraag gerust je docent om hulp! Ze helpen je graag als je vast zit.

**Spelregels en spelverloop **<br>
De speler heeft 3 pogingen om een random getal tussen de 0 en 10 te raden. De gebruiker voert een getal in, waarna de computer aangeeft of het getal hoger, lager of correct is. 
Is het getal na 3 pogingen nog niet geraden, dan heeft de gebruiker verloren. Heeft de gebruiker wel binnen 3 pogingen het getal geraden, dan heeft de gebruiker gewonnen!


**Activiteitendiagram**<br>
![Activiteitendiagram](https://raw.githubusercontent.com/ictacademiekw1c/opdrachten-repository/master/javascript/productie/afbeeldingen/eindopdracht/Activeitendiagram.png)
*Hier zie je hoe de gebruikersacties verlopen tijdens het spel. Deze opzet gaan wij naabouwen in ons spel*

<br><br><br>

>> Lees per deel goed de beoordelingscriteria door om te zien waar het spel minimaal aan moet voldoen.

## Deel 1: De opzet van "Raad het getal"

We gaan de JavaScript en HTML bestanden opzetten van het spel. Ook gaan we een H1 element maken waarin je de bezoeker welkom heet en waarin jouw naam staat.

1. Maak binnen WebMatrix een nieuwe website aan. Noem deze "getalRaden"
2. Maak een map genaamd "js" aan
3. Maak hierin een nieuw JavaScript bestand genaamd "Script.js" aan.
3. Koppel dit .js bestand in de HTML
4. Maak in het HTML bestand (in de &lt;body&gt;) een H1 element aan, waarin staat "Welkom bij Raad Het Getal. Gemaakt door *Jouw naam*". Vervang hier natuurlijk *Jouw naam*  door jouw naam!
5. Check of je JavaScript bestand uitgevoerd wordt (bv door een tijdelijke *console.log()* aan te maken)
6. Launch in browser (en check je console)
7. Check de beoordelingscriteria (om te checken of je overal aan voldoet) en ga door met deel 2

### Beoordelingscriteria deel1
- Je hebt het JavaScript bestand in een map genaamd "js" staan
- Het JavaScript is gekoppeld met de HTML
- Je hebt een H1 element gemaakt met een begroeting en je naam erin


<br><br><br>

## Deel 2: Het spel bouwen

In dit tweede deel maken we de meest simpele variant. Volg de instructies hieronder en hou je cheatsheet erbij!

1. Heet de gebruiker welkom via een *alert()*
2. Leg in een nieuwe melding kort de spelregels uit 
3. Bereken random een getal tussen de 1 en 10 en schrijf deze weg naar een variabele genaamd *getal*. Gebruik hiervoor deze code: ```parseInt( Math.random() * 10 + 1);``` 
4. Vraag in een *prompt()* aan de gebruiker om een eerste getal op te geven
5. Check via een *if statement* of het opgegeven getal gelijk, hoger of lager is dan het random *getal* van stap 3. Tip: Gebruik een *else if* om de 3 opties te checken
6. Geef de correcte melding aan de gebruiker (zie voorbeeld 1 hieronder voor de 3 opties die er zijn)
![De 3 voorbeelden van opties](https://raw.githubusercontent.com/ictacademiekw1c/opdrachten-repository/master/javascript/productie/afbeeldingen/eindopdracht/3opties.png)
7. Zorg ervoor dat de gebruiker 3 keer mag raden (tip: gebruik hiervoor meerdere <a href="http://javascript.about.com/od/decisionmaking/a/des09.htm">nested if statements</a>)
8. *alert()* op het einde van het spel het correcte antwoord naar de gebruiker
9. Schrijf je naam weg naar de *console.log()*
10. Speel je spel een aantal keer om fouten te ontdekken
11. Check de beoordelingscriteria hieronder en ga door met deel 3

### Beoordelingscriteria deel 2
- Je meldingen gaan naar de gebruiker via *alert()*
- Je input van de gebruiker krijg je via *prompt()*
- Je mag maximaal 3 pogingen doen
- Na het correct raden van het getal krijg je een felicitatie te zien en is het spel afgelopen
- Het spel werkt correct
- Je *if statements* hebben op de correcte plekken tabs


<br><br><br>

## Deel 3:  Je score wegschrijven in de HTML

In het derde en laatste gedeelte gaan we het resultaat van het spel wegschrijven in HTML. Zie de screenshot hieronder voor meer informatie over hoe het er uiteindelijk uit moet zien.
Alle onderstaande acties moeten dus pas uitgevoerd worden op het moment dat het spel klaar is.

1. Maak in de HTML de volgende structuur:
	- ![Hoe de HTML er in je browser uit moet komen te zien](https://raw.githubusercontent.com/ictacademiekw1c/opdrachten-repository/master/javascript/productie/afbeeldingen/eindopdracht/Screenshot2.png) 
2. Zet je JavaScript code binnen een *window.onload( function() {   })*. Zie cheatsheet voor meer info
3. Zodra het spel is afgelopen:
	- Zodra het spel afgelopen is, schrijf via *document.getElementById()* de uitkomst (of hij gewonnen / verloren heeft) een stukje tekst naar het H2 element met ID "result"  
	- Zodra het spel afgelopen is, schrijf via *document.getElementById()* het aantal pogingen weg. je mag hier zelf een leuke tekst omheen bedenken.
	- Zoek op <a href="http://www.giphy.com/" target="_blank">giphy.com</a> één .gif afbeelding voor verliezers en één voor de winnaars. Zorg ervoor dat winnaars de winnaars gif zien en dat verliezers de verliezers gif zien.
5. Speel het spel nu een aantal keer om alles te controleren
6. Je mag de site uitbouwen met meer leuke functies / meldingen als je dat wilt. Hiervoor krijg je extra kuddo's!
7. Je mag de site ook uitbouwen met CSS. Hiervoor krijg je extra kuddo's!
8. Check de beoordelingscriteria hieronder. Upload daarna je opdracht naar je N@tschool portfolio volgens de onderstaande instructies 


### Beoordelingscritera deel 3
- Je hebt gebruik gemaakt van document.getElementById()
- Je hebt gebruik gemaakt van het *window.onload()* event
- De winnaar krijgt een andere gif te zien dan een verliezer

![Hoe de HTML er in je browser uit moet komen te zien](https://raw.githubusercontent.com/ictacademiekw1c/opdrachten-repository/master/javascript/productie/afbeeldingen/eindopdracht/Screenshot.png)
*Voorbeeld hoe de pagina er ongeveer uit moet zien*

<br><br>


## Opsturen van je opdracht
Je hoeft de opdracht niet af te tekenen, maar alleen via de N@tschool als inleveropdracht op te sturen.

`` Uploaden en opsturen: Je pakt alle bestanden in een rar bestand en levert deze in via N@tschool inleveropdracht "Eindopdracht JS Periode 1". Zie afbeelding hieronder voor meer informatie! `` 
![Hoe de HTML er in je browser uit moet komen te zien](https://raw.githubusercontent.com/ictacademiekw1c/opdrachten-repository/master/javascript/productie/afbeeldingen/eindopdracht/Inleveren.png)