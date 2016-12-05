# Hoofdstuk 10 Arrays

## 10.1 Wat ga je leren ?

- Numerieke arrays
- Declareren van arrays
- Nieuwe elementen toevoegen
- Arrays en loops
- Arrayfuncties

## 10.2 Uitleg arrays w3schools

[PHP arrays](http://www.w3schools.com/Php/php_arrays.asp)

## 10.3 Voorbeelden

Arrays kunnen alle soorten datatypes bevatten.
~~~php
//alleen getallen
$lijstje = array(1,5,7,24,-14,24,333,256,123);
~~~

Arrays kunnen ook strings bevatten:
~~~php
$namen = array("Emiel", "Jurre", "Jason", "Martijn","Tijn", "Mike");
~~~

of een mix van datatypes:
~~~php
$mix = array(1,2,"sla",true,"01-01-2016",-56,2.34);
~~~

De lengte van een array (het aantal elementen in een array) kun je opvragen met de __sizeof()__ of __count()__ functie.

Ieder element kun je afzonderlijk opvragen via zijn index-waarde: <br>

~~~php
echo $lijstje[0]; //print de waarde 1
echo $lijstje[4]; //print de waarde -14
echo $namen[1]; //print de naam Jurre

//eerst het aantal elementen opvragen
$aantal = count($lijstje);

echo $lijstje[ $aantal -1 ]; // print 123
~~~

Met de volgende constructie kun je elementen toevoegen aan een array:<br>
~~~php
    $aantal = count($lijstje); //9
    $lijstje[] = 450;
    echo count($lijstje); //10
~~~

While constructies met arrays:
~~~php 
    //het aantal elementen in de array
    $aantal = count($lijstje);
    $tel = 0;

    while ($tel < $aantal) {
            echo $lijstje[$tel]."<br>";
            $tel++;
    }
~~~



