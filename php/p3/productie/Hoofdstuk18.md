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
