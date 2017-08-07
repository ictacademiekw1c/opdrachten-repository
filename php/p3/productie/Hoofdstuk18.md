#### [kleurcode]rgba(194,67, 74,1)

#  Hoofdstuk 18 Oefentoets opdrachten periode 3

## 18.1 Oefentoets opdracht 1

Ga uit van de volgende array:
~~~php
$aMenu = array( 'Nieuws' => 'http://nu.nl',
            'Contact' => 'contact.php',
            'Locatie' => 'locatie.php',
            'Zoeken' => 'zoeken.php' );
~~~

>Programmeer een functie die als je deze op de volgende manier aanroept:

~~~php
//Nieuws krijgt in het menu een andere achtergrondkleur
printMenu('Nieuws');
~~~

>een menu print met de volgende visuele weergave:

### Visuele weergave oefenen 1 

![Visuele weergave](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/p3/images/oefenen1.png?raw=true)

### beoordelingscriteria oefenen 1
- Elke menuoptie linkt naar de corresponderende webpagina.
- De menuoptie die wordt meegestuurd krijgt een andere achtergrondkleur.

## 18.2 Oefentoets opdracht 2

Ga uit van de volgende 2 arrays:
~~~php
 $aGente = array( 'jan'=> 'm',
                 'alice'=> 'v', 
                 'veronica'=> 'v', 
                 'herman'=> 'm',                
                 'maria'=> 'v', 
                 'angelica' => 'v' , 
                 'pieter' => 'm' ,
                 'abdel' => 'm');  

    $aLeeftijd = array(
            'jan'=> 66, 
            'alice'=> 21, 
            'veronica'=> 45, 
            'herman'=> 22,               
            'maria'=> 62, 
            'angelica' => 23, 
            'pieter' => 46,
            'abdel' => 22);
~~~

Programmeer een php script waarin je bepaalt:
- De gemiddelde leeftijd van de mannen
- De gemiddelde leeftijd van de vrouwen

Programmeer vervolgens een foreach lus, waarin je van elke man de vrouw zoekt waarvan het leeftijdsverschil niet meer is dan 5 jaar (ouder of jonger).

## 18.3 Oefentoets opdracht 3

We starten met de variabele $zin
~~~php
$zin = "Rond de wedstrijd Ajax-Feyenoord zijn zondag in Rotterdam achttien relschoppers opgepakt. Volgens de politie zijn ze aangehouden voor zaken als belediging, bedreiging, vernieling en het gooien van vuurwerk. Ajax won in de Arena met 2-1.";
~~~

Om te kunnen tellen hoeveel keer de woorden __de__, __het__ of __een__ voorkomen in de zin gaan we deze zin omzetten naar een array.
We kunnen dit doen met de array functies str_split() of explode(); Onderzoek dit door de documentatie op php.net
goed te lezen van beide functies en daarna de juiste functie te kiezen en vervolgens de code te programmeren, die nodig is om te bepalen hoe vaak de woorden __de__,__het__ of __een__ voorkomen in de bovenstaande zin.

## 18.4 Oefentoets opdracht 4

Start met formulier als in opdracht 130. Noem dit script oefenopdracht4.php
~~~html
 <form method='get' action='oefenopdracht4.php'>
         <label>Naam: </label><input name='naam' type='text' value=''>
         <label>Klas: </label><input name='klas' type='text' value=''>
         <label>Nummer: </label><input name='leerlingnummer' type='text' value=''>
         <label>Vak: </label><select name='vak'>
             <option value='PHP'>PHP</option>
             <option value='javascript'>Javascript</option>
             <option value='ASP'>ASP</option>
             <option value='SQL'>SQL</option>
         </select>
         <label>Cijfer: </label><input name='cijfer' type='number' value='5'>
         <input type='submit' value='verzend' name='verzend'>
         </form>
~~~

__Visuele weergave__<br>
De uiteindelijke weergave moet weer zijn zoals in opdracht 140, maar dan met het resultaat in de laatste regel toegevoegd.

<table border="1">
<caption><b>Rapport van leerling Abu Saebu met nummer 99900398 klas IO1B4</b></caption>
<tr><th>Vak</th><th>Cijfer</th></tr>
<tr><td>PHP</td><td>7</td></tr>
<tr><td>ASP</td><td>9</td></tr>
<tr><td>Javascript</td><td>5</td></tr>
<tr><td>Database</td><td>7</td></tr>
<tr><td>Gemiddelde</td><td>7</td></tr>
<tr><th>Resultaat</th><th>Je bent over</th></tr>
</table>

__Beoordelingscriteria__<br>
Maar de uitwerking zal aan de volgende eisen moeten voldoen:
- Maak gebruik van de sessievariabele $_SESSION['vakcijfer'] die nu een associatieve array is met key-waarde het vak en value-waarde het cijfer ervoor.
- Zorg ervoor dat je slechts 1x een vak kan invullen, door dat met een array functie uit hoofdstuk 17 te controleren.
- Bereken het gemidddelde ook met een array functie.
- Je print het resultaat 'Je blijft zitten' als je gemiddelde lager is dan 5,5 anders print je het resultaat 'Je bent over'

## 18.5 Toetsopdracht 1

Je kreeg de volgende code:
~~~php
$aGente = array( 'jan'=> 'm',
                 'alice'=> 'v', 
                 'veronica'=> 'v', 
                 'herman'=> 'm',                
                 'maria'=> 'v', 
                 'angelica' => 'v' , 
                 'pieter' => 'm' ,
                 'abdel' => 'm');  

    $aLeeftijd = array(
            'jan'=> 66, 
            'alice'=> 17, 
            'veronica'=> 45, 
            'herman'=> 17,               
            'maria'=> 62, 
            'angelica' => 22 , 
            'pieter' => 45,
            'abdel' => 22);

/* zoek de perfecte match zoekMatch() op basis van leeftijd en geslacht
@param1 de leeftijd van de perfecte match
@param2 het gezochte geslacht
@return de naam van de perfecte match
*/
function zoekMatch ($zoekLeeftijd, $zoekGeslacht ) {
    global $aLeeftijd, $aGente;

    foreach ($aLeeftijd as $naam => $leeftijd) {  
        if ($leeftijd == $zoekLeeftijd && $zoekGeslacht == $aGente[$naam]) {   
            return $naam;
        }
    }
    return 'geen match';
}

$man = 'jan';
echo "De perfecte match voor $man met leeftijd ".$aLeeftijd[$man]." is ".zoekMatch($aLeeftijd[$man],'v');
~~~
De perfecte match wordt voor jan nu niet gevonden, omdat de functie een vrouw zoekt met precies dezelfde leeftijd als jan. Wat moet je veranderen aan de functie zodanig dat het leeftijdsverschil maximaal 5 jaar mag zijn om toch een perfecte match te vinden ? jan zal dan maria als perfecte match gaan vinden. 

### 18.5.1 De uitwerking

Het enige wat moet worden aangepast is de if statement in de functie zoekMatch(). Nu kijkt de functie of er iemand is die precies dezelfde leeftijd heeft.
In plaats daarvan moet er een ondergrens: $zoekleeftijd - 5 en een bovengrens worden ingesteld: $zoekleeftijd + 5

~~~php
    //de grenzen waarbinnen een partner voldoet
    $minL = $zoekLeeftijd - 5;
    $maxL = $zoekLeeftijd + 5;

    //en de aangepaste if-statement
    if ($leeftijd >= $minL && $leeftijd <= $maxL && $zoekGeslacht == $aGente[$naam])
    
~~~

## 18.5 Toetsopdracht 2

Kopieer de volgende code naar een php script met naam lijst.php.

__lijst.php__
~~~php
session_start();
$aLijst = array(1,22,55,66,99, 234,9);
$_SESSION['getallen'] = $aLijst;
~~~

__gemiddelde.php__
Voer dit script uit. In de browser zul je slechts een pagina zien zonder inhoud ( witte pagina), maar de array is nu wel in een sessie gezet.
Programmeer een tweede script (gemiddelde.php) die deze getallen uit de sessie haalt, deze combineert met de array 
 
~~~php 
$aLijst2 = array(1,2,3,4,5,6,7,8,9,10);
~~~

En het gemiddelde bepaalt van de getallen uit deze 2 arrays.

Dus de uitvoer van je script zou moeten zijn:

Het gemiddelde van de sessiegetallen(aLijst) en aLijst2 is: 31.823529411765

### 18.5.1 Uitwerking Toetsopdracht 2

In __gemiddelde.php__
~~~php
//Haal je de eerste lijst uit de sessie
//sessie starten!!!
//Het is fout als je een include gebruikt ipv een sessie

session_start();
//if isset om te voorkomen dat je een foutmelding krijgt
if (isset($_SESSION['getallen'])) {
    $lijst1 = $_SESSION['getallen'];
}
$totaal = 0;
$tel = 0;
while ($tel < count($lijst1)) {
    $totaal = $totaal + $lijst1[$tel];
    $tel++;
}

//Nu het totaal van de tweede lijst
$aLijst2 = array(1,2,3,4,5,6,7,8,9,10);
$tel = 0;
while ($tel < count($aLijst2)) {
    $totaal = $totaal + $aLijst2[$tel];
    $tel++;
}
// Nu bevat $totaal het totaal van beide arrays
//Het gemiddelde is dan

$gem = $totaal / (count($lijst1) + count($aLijst2));

//printen
echo $gem;
~~~


