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

Functies maak je wanneer je stukjes code vaker gebruikt je website. Het gevolg daarvan is dat je code:
- Leesbaarder wordt
- Minder regels code omvat
- Makkelijker onderhoudbaar is
- Effectiever is

Functie declaratie 
~~~php

> function functienaam() {

//code van de functie

}
~~~

## 9.3 voorbeeld functie 1 printGroet()

Het volgende voorbeeld is een functie met 2 argumenten.
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
    elseif( $uur> 16 && $uur<= 11) {
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


