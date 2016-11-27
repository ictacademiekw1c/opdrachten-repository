# Hoofdstuk 9 Functies

## 9.1 Wat ga je leren ?

- Waarom functies
- Functie declaratie
- Functie implementatie
- Functie aanroep
- Functie argumenten
- return waarde
- include() functie

## 9.2 Uitleg  

Functies maak je wanneer je stukjes code op je website vaker gebruikt. Het gevolg daarvan is dat je code:
- Leesbaarder wordt
- Minder regels code omvat
- Makkelijker onderhoudbaar is
- Effectiever is

Functie declaratie 
~~~php
/***********************
* printGroet()
* @param geen parameters 
* @return geen return
**************************/ 
function functienaam() {

//code van de functie

}
~~~

## 9.3 voorbeeld functie 1 printGroet()

Het volgende voorbeeld is een functie met 1 argument.
~~~php
/***********************
* printGroet()
* @param $achternaam achternaam 
* @return geen return
**************************/ 
function printGroet ($achternaam) {

       //wat is de lokale tijdszone
    date_default_timezone_set('Europe/Amsterdam');

    //Geeft het uur van de dag terug in 24uurs notatie
    $uur = date('G');
    
    if ($uur >= 12 && $uur < 16) {
        $dagdeel = "middag";
    }
    elseif($uur > 5 && $uur < 12) {
        $dagdeel = "ochtend";
    }
    elseif( $uur> 16 && $uur<= 23) {
        $dagdeel = "avond";
    }
    else {
        $dagdeel = "nacht";
    }

    echo "Hallo meneer $achternaam, goede-$dagdeel";

}
~~~

## 9.4 Op welke plek in je code zet je een functie?
Er zijn 2 mogelijkheden:
- Bovenaan het script (Niet in het html gedeelte)
- In een apart php script, bijvoorbeeld functies.php en waar je het nodig hebt bovenin toevoegen met een include-statement.

De tweede manier heeft de voorkeur.<br> 
Noem het bijvoorbeeld __functies.php__
~~~php
//Dit is de declaratie
/***********************
* printGroet()
* @param $achternaam achternaam 
* @return geen return
**************************/ 
function printGroet ($achternaam) {

    //wat is de lokale tijdszone
    date_default_timezone_set('Europe/Amsterdam');

    //Geeft het uur van de dag terug in 24uurs notatie
    ...(dezelfde code als hierboven)

    echo "Hallo meneer $achternaam, goede-$dagdeel";
}
~~~

In het volgende script maak je er gebruik van <br>
__voorbeeld1.php__
~~~php
<?php

//Met include() wordt de code in functies.php volledig toegevoegd aan voorbeeld1.php
include('functies.php');
?>
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title><?php printGroet('Saebu'); ?></title>
    </head>
    <body>
        <article>
        <?php
             printGroet('Saebu');
        ?>
        </article>
    </body>
</html>
~~~
## 9.5 Verdere uitleg op w3schools

Bestudeer ook verder de theorie op de volgende pagina:<br>
[w3schools over functions](http://www.w3schools.com/php/php_functions.asp)

## 9.6 Opdracht 90 functions

### Opdrachtomschrijving 90
Neem functies.php over van hierboven en maak een opdracht90.php, waarin je functies.php toevoegt met een include() statement.
In opdracht90.php roep je de functie aan op 2 vrschillende plekken in je html-document.
1. Test je opdracht90.php
2. Pas de functie aan zodanig dat je een tweede argument en derde argument voor de functie moet gebruiken. Als tweede argument gebruik je de voornaam, en als derde argument de leeftijd. Als de leeftijd ouder is dan 30 print je:<br>
 __Hallo meneer Saebu, goede-middag.__<br>
 Maar als de leeftijd jonger dan 30 is print je:<br>
 __He Abu, fijne middag he?__
3. Test het vervolgens in opdracht90.php door de functie aanroepen met verschillende waardes en op verschillende plaatsen in je html-document te laten plaatsvinden.

### Visuele weergave 90

### Beoordelingscriteria 90
1. Comprimeer opdracht90.php en functies.php als opdracht90.rar en upload het naar je portfolio
2. Je php-script toont een volledige en geldige html pagina

## 9.7 Opdracht 91 functions
### Opdrachtomschrijving 91
Herschrijf opdracht 81 (niet de alternatieve opdracht) en maak gebruik van de functie printTafel() om de tafels te printen.
Zet de functie printTafel() in functies.php

### Visuele weergave 91
als opdracht 81

### Beoordelingscriteria 91
1. Comprimeer opdracht91.php en functies.php als opdracht91.rar en upload het naar je portfolio
2. Je php-script toont een volledige en geldige html pagina
3. PrinTafel() gebruikt 1 argument
4. PrintTafel() heeft geen return waarde

## 9.7 Functies met een return waarde

### Waarom en hoe werkt het?

Voorbeeld 1 function zonder return
~~~php
function printWaarde ($naam) {

    echo "<h1>De waarde is:".strtoupper($naam)."</h1>";

}

printWaarde ('Luigi');
printWaarde ('Bernhard');

~~~
__Nadeel__ de naam wordt altijd in een h1 geprint.

Voorbeeld 2 function met return
~~~php 
function getHoofdletters($naam) {
    return strtoupper($naam);
}

//nu kan ik de waarde ook in andere html-tags zetten
echo "<h2>".getHoofdletters('Koen')."</h2>";
echo "<p>".getHoofdletters('')."</p>";
// ipv in een echo statement kan ik de return waarde ook opvangen in een andere variabele
$naam2 = getHoofdletters('Joey');
// voordeel hiervan is dat ik de aanroep niet hoef te doen op de plek waar het getoond wordt.
echo "<ul><li>$naam2</li></ul>";
~~~


