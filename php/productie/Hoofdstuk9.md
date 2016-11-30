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
3. Je code bevat commentaar; vooral op plekken waar het moeilijk wordt of waar jij problemen mee hebt


## 9.7 Opdracht 91 functions
### Opdrachtomschrijving 91
Herschrijf opdracht 81 (niet de alternatieve opdracht) en maak gebruik van de functie printTafel() om 1 tafel te printen. Geef de tafel die je wil printen als parameter door aan de functie printTafel(). Bijvoorbeeld om de tafel van 3 te laten printen: printTafel(3).
Zet de functie printTafel() in functies.php

### Visuele weergave 91
als opdracht 81

### Beoordelingscriteria 91
1. Comprimeer opdracht91.php en functies.php als opdracht91.rar en upload het naar je portfolio
2. Je php-script toont een volledige en geldige html pagina.
3. PrinTafel($tafel) gebruikt 1 argument
4. PrintTafel() heeft geen return waarde
5. Je code bevat commentaar; vooral op plekken waar het moeilijk wordt of waar jij problemen mee hebt


## 9.8 Functies met een return waarde

### Waarom en hoe werkt het?

### Voorbeeld 1 function zonder return
~~~php
/***********************
* functie print de $naam in hoofdletters in een h1 tag
* @param $naam een stringwaarde
* @return geen return
**************************/ 
function printWaarde ($naam) {

    echo "<h1>De waarde is:".strtoupper($naam)."</h1>";

}

printWaarde ('Luigi');
printWaarde ('Bernhard');

~~~
__Nadeel__ de naam wordt altijd in een h1 geprint.

### Voorbeeld 2 function met return
~~~php 
/***********************
* functie retourneert de $naam in hoofdletters 
* @param $naam een string-waarde
* @return de stringwaarde in hoofdletters
**************************/ 
function getHoofdletters($naam) {
    return strtoupper($naam);
}

//nu kan ik de waarde ook in andere html-tags zetten
echo "<h2>".getHoofdletters('Koen')."</h2>";
echo "<p>".getHoofdletters('Lars')."</p>";
// ipv in een echo statement kan ik de return waarde ook opvangen in een andere variabele
$naam2 = getHoofdletters('Joey');
// voordeel hiervan is dat ik de aanroep niet hoef te doen op de plek waar het getoond wordt.
echo "<ul><li>$naam2</li></ul>";
~~~

Zie ook de volgende voorbeelden op github [verschillende functie voorbeelden](https://gist.github.com/saebuabu/777fbbb8651f3a6cf26b)
## 9.9 Opdracht 92 functions met return

### Opdrachtomschrijving 92
Maak de onderstaande code af zodat de visuele weergave van een factuur wordt getoond zoals in onderstaande afbeelding.
Doe dit door de functies berekenBtw() en berekenTotaal() te maken (declareren en implementeren). 

### Programmastructuur 92

Begin met de volgende programmastructuur:
~~~php
<?php
include('functies.php');
?>
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title></title>
    </head>
    <body>        
        <table border="1">
        <tr><th></th><th>Beschrijving</th><th>Bedrag</th><th>Totaal</th><th>BTW</th></tr>
        <?php
        
        $uur = 2;
        $uurprijs = 90;
        $btw = 21;
        $subtotaal = product($uur, $uurprijs);
        $btwbedrag = berekenBtw($btw , $subtotaal);
        $totaal = berekenTotaal($subtotaal, $btwbedrag);

        echo "<tr><td>$uur uur</td><td>Advieswerkzaamheden</td><td>&euro; $uurprijs</td><td>$subtotaal</td><td>$btw %</td></tr>";
        echo "<tr><td colspan='2'></td><td>Subtotaal</td><td>$subtotaal</td><td></td></tr>";
        echo "<tr><td colspan='2'></td><td>21%BTW</td><td>$btwbedrag</td><td></td></tr>";
        echo "<tr><td colspan='2'></td><td>Totaal</td><td>$totaal</td><td></td></tr>";  
        ?>        
        </table>
    </body>
</html>
~~~

De functie product() in functies.php ziet er als volgt uit:
~~~php
/**************
* Omschrijving: berekend product van 2 getallen
* @param  $g1 en $g2: 2 getallen
* @return het product van de 2 getallen
**************/
function product($g1, $g2) {
    
    $uitkomst = $g1 * $g2;

    return $uitkomst;
}
~~~

### Visuele weergave 92
![factuur](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/images/factuur.png?raw=true)


### Beoordelingscriteria 92
1. Comprimeer opdracht92.php en functies.php als opdracht92.rar en upload het naar je portfolio
2. Je php-script toont een volledige en geldige html pagina
3. Voeg zinvolle commentaar toe aan de verschillende onderdelen van je code




