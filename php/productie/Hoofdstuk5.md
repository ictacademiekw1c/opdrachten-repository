# Hoofdstuk 5 - Get parameters

## 5.1 Wat ga je leren ?

Wat een Get parameter is. Hoe pas je deze aan in een URL. De eerste manier om iets door te geven aan een script.

Voorwaardelijke code: Hoe maak je in php een if else constructie.

## 5.2 Voorbeeld en uitleg 5.1 

Bekijk allereerst dit voorbeeld
[Voorbeeldvideo met $_GET parameters](https://mix.office.com/watch/16sdvrg08ufjb)

~~~php
// Maak een script aan in de map hoofdstuk 5 met de naam testget.php
// Neem de volgende code over in het script en launch het in je browser
// Wat zie je?
echo $_GET['leeftijd'];

$leeftijd = $_GET['leeftijd'];

if ($leeftijd > 17) {
    echo "Je bent volwassen";
} else {
    echo "Je bent nog een kind";
}


//Pas de URL in je browser aan door ?leeftijd=10 aan het eind toe te voegen
//Wat zie je nu als je nu de pagina opvraagt?

//Je kan een tweede get-parameter toevoegen aan het eind van de url door bijv &naam=Abu Saebu toe te voegen
//De volledige url is dan http://localhost:4567/voorbeeld.php?leeftijd=52&naam=Abu Saebu
~~~

---
## Opdracht 50

### Omschrijving
Volg alle stappen in het voorbeeld (5.2) hierboven en leg de docent uit wat er gebeurt. 

### Beoordelingscriteria
1. Je kan uitleggen wat een get-parameter is
2. Je kan uitleggen hoe je door de URL aanpast een get-parameter kan toevoegen aan je php script
3. Je hebt een script met 2 get-parameters leeftijd en naam, en een if else statement als in het voorbeeld
4. Maak een script aan met naam opdracht50.php

---
## Opdracht 51

### Omschrijving 51
Maak een script met de naam opdracht50.php en test de script met een aantal get-parameters voor: naam, leeftijd en plaats

Zet in je script 2 if-else constructies met de booleaanse expressies:
1. $plaats == "Den Bosch"
2. $leeftijd > 25 

### Visuele weergave 51

Ik ben Abu Saebu. 
Ik ben een bosschenaar.
Ik ben best oud.

of

Ik ben Jan Lucassen.
Ik ben geen bosschenaar.
Ik ben nog best jong.

De visuele weergave hierboven is afhankelijk van de waardes van je GET-parameters.

### Programmastructuur 51

~~~php
$leeftijd = $_GET['leeftijd'];
..

if ($leeftijd > 25) {
    echo ...
}
else {
    echo ...
}

if (bosschenaar?) ....

~~~

### Beoordelingscriteria 51
1. Je maakt gebruik van 3 get-parameters
2. Je script geeft foutmeldingen als je niet de get-parameters toevoegt aan je url
3. Je script geeft geen foutmeldingen als je de juiste get-parameters en waarden toevoegt aan je url
4. De visuele weergave van je script is afhankelijk van de waardes van de get-parameters.
---
