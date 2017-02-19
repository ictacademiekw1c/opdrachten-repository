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
        echo "<br>".$key . " : ". $value;
    }
~~~





