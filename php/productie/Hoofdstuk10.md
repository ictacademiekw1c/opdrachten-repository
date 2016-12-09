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

## 10.4 Opdracht 100 arrays

### Opdrachtomschrijving 100
Declareer een array $cijfers met al je cijfers van alle vakken die je in periode 1 hebt gehad.

Programmeer een __while lus__ en bereken/bepaal in de lus de volgende zaken:<br>
- Het aantal cijfers
- Het laagste cijfer
- Het hoogste cijfer
- Het gemiddelde cijfer afgerond 2 cijfer achter de komma
- Het aantal onvoldoendes

``Je mag geen functies gebruiken die nog niet eerder zijn voorgekomen in de php-lessen in periode 1 of 2``

Wel mag je gebruiken: count() of sizeof() en round() en je mag zoveel variabelen gebruiken als je zelf wil.

### Visuele weergave 100

- Je cijfers zijn: 2, 7, 6.7, 8.8, 10, 1, 7.5
- Je hebt 7 cijfers gehaald
- Het hoogste cijfer is: 10
- Het laagste cijfer is: 2
- Het gemiddelde is: 6.14
- Het aantal onvoldoendes: 2

### Beoordelingscriteria 100
1. Comprimeer opdracht100.php als opdracht100.rar en upload het naar je portfolio
2. Je php-script toont een volledige en geldige html pagina
3. Je code bevat commentaar; vooral op plekken waar het moeilijk wordt of waar jij problemen had
4. Je mag geen special functies gebruiken die het hoogste, laagste of gemiddelde getal voor je direct bepalen.

## 10.5 Opdracht 101 arrays

### Opdrachtomschrijving 100
Declareer een array $namen met alle voornamen van alle leerlingen uit je klas.

Programmeer een __while lus__ en bereken/bepaal in de lus de volgende zaken:<br>
- Bepaal de kortste naam
- Wat is de langste naam
- Welke namen hebben een a 
- Welke namen eindigen op een n
- Welke namen hebben de meeste klinkers
- (Extra) Welke naam heeft de minst voorkomende medeklinkers?

``Je mag geen functies gebruiken die nog niet eerder zijn voorgekomen in de php-lessen in periode 1 of 2``

Wel mag je gebruiken: strlen(), substr() en strpos() en je mag zoveel variabelen gebruiken als je zelf wil.

### Visuele weergave 101

### Beoordelingscriteria 101
1. Comprimeer opdracht101.php als opdracht101.rar en upload het naar je portfolio
2. Je php-script toont een volledige en geldige html pagina
3. Je code bevat commentaar; vooral op plekken waar het moeilijk wordt of waar jij problemen had
4. Je mag geen special functies gebruiken die letters zoeken in een woord en posities teruggeven
5. Je moet een while lus gebruiken.

## 10.6 Opdracht 102 (ifelse - while - functies - algoritmes)

### Opdrachtomschrijving 102
Bepaal alle priemgetallen tussen 2 en 20. [Wat is een priemgetal?](https://nl.wikipedia.org/wiki/Priemgetal)

### Visuele weergave 102
__De priemgetallen tot 20 zijn: 2, 3, 5, 7, 11, 13, 17, 19__

### Beoordelingscriteria 102
1. Comprimeer opdracht102.php als opdracht102.rar en upload het naar je portfolio
2. Je php-script toont een volledige en geldige html pagina
3. Je code bevat commentaar; vooral op plekken waar het moeilijk wordt of waar jij problemen had
4. Je moet een while lus gebruiken.
5. Je moet een functie isPriem() maken, die teruggeeft (return) of een getal (parameter) een priemgetal is of niet.

