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

