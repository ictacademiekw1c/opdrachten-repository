#### [kleurcode]rgba(214,67,54,1)

#  Hoofdstuk 15 Associatieve arrays en foreach() lussen

## 15.1 Associatieve arrays

### 15.1.1 Numerieke arrays
Tot nu toe hebben we de volgende arrays gehad:
~~~php
    $aLijst = array(1,5,9,10,23,5);
    // of
    $aNamen = array("Gijs","Duncan","Aron","Ayoub");
    // of 
    $aMixed = array("Gijs", 12, "PHP", true);
~~~
En gebruikten we een while loop om alle elementen los te kunnen zien.
~~~php

    $tel = 0;
    $aantal = count($aLijst);
    while ($tel < $aantal) {
        echo $aLijst[$tel];
        $tel++;
    }
~~~
Dit noemen we numerieke arrays omdat elke element uit de array een numerieke(=getals) waarde heeft als index.
Bijvoorbeeld het tweede element uit de lijst $aLijst heeft als index waarde 1 (tellen vanaf 0). 

~~~php
 // de tweede waarde uit de lijst heeft index-waarde 1
 echo $aLijst[1];
~~~

### 15.1.2 Associatieve arrays

Associatieve arrays zien er anders uit:
~~~php
    $aLeerling = array( "naam" => "Aron", "leeftijd" => 18, "woonplaats" => "Vught"); 
~~~

De index waardes van de elementen zijn hier niet numeriek maar zijn strings.

De index waarde van de waarde Aron is de string "naam".

## 15.2 Foreach loop

Associatieve arrays doorloop je met een foreach lus:
~~~php
    //foreach heeft geen teller nodig om de loop te stoppen
    // de lus stopt zodra alle elementen zijn gepasseerd
    foreach ($aLeerling as $key => $value) {    
        echo "<br>".$key . ": ". $value;
    }
~~~
## 15.3 Lesopdracht

~~~php
$aClubs = array("Jörgensen"=>"Feyenoord"
,"Ghoochannejhad"=>"sc Heerenveen"
,"Armenteros"=>"Heracles"
,"Weghorst"=>"AZ"
,"Dolberg"=>"Ajax"
,"ünal"=>"FC Twente"
,"v.Wolfswinkel"=>"Vitesse"
,"Klaassen"=>"Ajax"
,"Mahi"=>"FC Groningen"
,"Sol"=>"Willem"
,"Baker"=>"Vitesse"
,"Haller"=>"FC Utrecht"
,"Pereiro"=>"PSV");

$aDoelpunten = array("Jörgensen" => 15
,"Ghoochannejhad" => 13
,"Armenteros" => 10
,"Weghorst" => 10
,"Dolberg" => 10
,"ünal" => 10
,"v.Wolfswinkel" => 10
,"Klaassen" => 10
,"Mahi" => 9
,"Sol" => 9
,"Baker" => 9
,"Haller" => 9
,"Pereiro" => 8);
~~~

>Maak het script foreach.php in de map hoofdstuk15, die de volgende uitvoer heeft.

>Speler Jörgensen speelt bij Feyenoord en heeft 15 doelpunten gescoord.
<br>Speler Ghoochannejhad speelt bij sc Heerenveen en heeft 13 doelpunten gescoord.
<br>Speler Armenteros speelt bij Heracles en heeft 10 doelpunten gescoord.
 <br>Speler Weghorst speelt bij AZ en heeft 10 doelpunten gescoord.
<br>etc.
Maak gebruik van de volgende foreach lus:
~~~php
foreach ($aClubs as $key=>$value) {
...
}
~~~
##15.4 Opdracht 150 doelpuntgemiddelde 
~~~php
$aWedstrijden = array(
,"Jörgensen" => 22
,"Ghoochannejhad" => 23
,"Armenteros" => 17
,"Weghorst" => 19
,"Dolberg" => 21
,"ünal" => 21
,"v.Wolfswinkel" => 21
,"Klaassen" => 21
,"Mahi" => 20
,"Sol" => 20
,"Baker" => 21
,"Haller" => 23
,"Pereiro" => 21);
~~~

### Opdrachten 150
- Bepaal welke speler het hoogste doelpuntgemiddelde heeft.
- Bepaal welke club de meeste doelpunten heeft gescoord
- Bepaal het totaal aan doelpunten van spelers van clubs die beginnen met FC

### Beoordelingscriteria 150

- Je maakt gebruik van een of meerdere foreach lussen
- Je mag geen gebruik maken van een array functie die totalen voor jou berekent, of hoogste waardes of laagste waardes bepaalt.
- Je maakt gebruikt van de bovenstaande associatieve arrays $aClubs, $aDoelpunten en $aWedstrijden, waarin per speler de club, het aantal gescoorde doelpunten en het aantal gespeelde wedstrijden staan.