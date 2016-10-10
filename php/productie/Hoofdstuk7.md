# Hoofdstuk 7 Beslissingen

## 7.1 Wat ga je leren ?

In dit hoofdstuk worden: 
- if else constructies verder verdiept
- booleaanse expressies (php code die een true of een false opleveren)

    - ==  precies gelijk aan
    - <   kleiner dan
    - <=  kleiner dan of gelijk
    - &gt;   groter dan
    - &gt;=  groter dan of gelijk aan
    - <>  ongelijk aan

- and en or in booleaanse expressies

    - && and
    - || or

- nesten van if else constructies

- shorthand notatie if else

## 7.2 Voorbeelden

### Wanneer en waar wordt het gebruikt?
~~~php
    //Tussen de ronde haakjes
    if () {

        //deze code wordt uitgevoerd als dat wat tussen () true oplevert

    }
    else {

        //deze code wordt uitgevoerd als dat niet zo is (=false)
    }
~~~
- Hoe?

### Voorbeeld 1 met strings
~~~php

      $naam = "Sander";

    //true or false?

    echo "<hr>";    
    if ($naam == "sander") {
        echo "$naam == 'sander' is waar(true)";
    } 
    else {
        echo "$naam == 'sander' is niet waar(false)";        
    } 

    echo "<hr>";    
    if (strtolower($naam) == "sander") {
        echo strtolower($naam)." == 'sander' is waar(true)";
    } 
    else {
        echo "$naam == 'sander' is niet waar(false)";        
    } 

    echo "<hr>";    
    if ($naam <> "sander") {
        echo "$naam <> 'sander' is waar(true)";
    } 
    else {
        echo "$naam <> 'sander' is niet waar(false)";        
    } 

~~~

### Voorbeeld 2 met getallen
~~~php

    $leeftijd = 28;

    //true or false?
    echo "<hr>";    
    if ($leeftijd > 28) {
        echo "$leeftijd > 28 is waar(true)";
    } 
    else {
        echo "$leeftijd > 28 is niet waar(false)";        
    } 
    echo "<hr>";    
    if ($leeftijd >= 28) {
        echo "$leeftijd >= 28 is waar(true)";
    } 
    else {
        echo "$leeftijd >= 28 is niet waar(false)";        
    } 
    echo "<hr>";    
    if ($leeftijd < 28) {
        echo "$leeftijd < 28 is waar(true)";
    } 
    else {
        echo "$leeftijd < 28 is niet waar(false)";        
    } 
    echo "<hr>";    
    if ($leeftijd <= 28) {
        echo "$leeftijd <= 28 is waar(true)";
    } 
    else {
        echo "$leeftijd <= 28 is niet waar(false)";        
    } 

~~~

### Voorbeelden met and (&&) en or (||)

&& (and) en || (or) worden gebruikt om meerdere voorwaarden te kunnen combineren

Voorbeelden van een combinatievragen (voorwaarden) zijn:

1. Is de leeftijd lager dan 18 __of__ is de leeftijd hoger dan 65?
2. Is de leeftijd lager dan 18 __en__ is de woonplaats Den Bosch?
3. Is de leeftijd lager dan 18 __of__ is de woonplaats Den Bosch?
4. Is de leeftijd hoger dan 18 __en__ lager dan 65?

Vertaling naar php-code:
~~~php

 $leeftijd = 17;
    $plaats = "Vught";

    echo "leeftijd is $leeftijd en plaats is $plaats";
    // voorbeeld 1 van hierboven
    echo "<hr>";    
    if ($leeftijd <18 || $leeftijd >65) {
        echo "<br>Je bent of jong of heel oud";
    } 
    else {
        echo "<br>Je bent een volwassen persoon";        
    } 

    //voorbeeld 2 van hierboven
    if ($leeftijd <18 && $plaats == "Den Bosch") {
        echo "<br>Je bent een jonge Bosschenaar";
    } 
    else {
        echo "<br>Je bent oud en je komt niet uit Den Bosch";        
    } 

    //voorbeeld 3 van hierboven
    if ($leeftijd <18 || $plaats == "Den Bosch") {
        echo "<br>Je bent een jong persoon of je woont in Den Bosch";
    } 
    else {
        echo "<br>Je bent niet jong en je bent geen Bosschenaar";        
    }

~~~

