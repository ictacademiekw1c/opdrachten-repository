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

## 9.3 functie declaratie 1 printGroet()


## 9.4 Waar plaats je functie declaraties?

Er zijn 2 mogelijkheden:
- Bovenaan het script (Niet in het html gedeelte)
- In een apart php script, bijvoorbeeld functies.php en waar je het nodig hebt bovenin toevoegen met een include-statement.

De tweede manier heeft de voorkeur 
__functies.php__
~~~php
//Dit is de declaratie
/***********************
* printGroet()
* @param $voornaam voornaam van persoon
* @param $achternaam achternaam 
* @return geen return
**************************/ 
function printGroet ($voornaam, $achternaam) {

    //wat is de lokale tijdszone
    date_default_timezone_set('Europe/Amsterdam');

    //Geeft het uur van de dag terug in 24uurs notatie
    ...(dezelfde code als hierboven)
}
~~~

__voorbeeld1.php__
~~~php
<?php
include('functies.php');
?>
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title><?php printGroet('Abu','Saebu'); ?></title>
    </head>
    <body>
        <?php
             printGroet('Abu','Saebu');
        ?>
    </body>
</html>
~~~


