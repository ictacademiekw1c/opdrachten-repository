# Hoofdstuk 4 - Nog meer stringfuncties

## 4.1 Wat ga je leren?
Je leert het gebruiken en toepassen van nog een aantal string functies:

### Zoeken van een string in een andere string waarbij je de positie terugkrijgt waar die is gevonden.
- strpos() 
- strrpos()
- stripos()
- strripos()

### Van een string een stukje (substring) knippen (substr()) of vervangen (substr_replace())
- substr()
- substr_replace()

### zero-based
Tellen begint bij 0.

## 4.2 Uitleg en voorbeelden strpos() en varianten

~~~php
$sZin = "Dit is een zin. dit is een tweede zin. Dit een derde.";

/*
strpos zoekt vanaf de linkerkant en stopt als het gevonden is
strrpos zoekt vanaf de rechterkant en stopt als het gevonden is
stripos als de eerste maar dan zonder onderscheid van hoofd of kleine letters
strripos als de tweede maar dan zonder onderscheid van hoofd of kleine letters
*/

$dit = "dit";

echo strpos ($sZin, "$dit"). "<br>";
echo strrpos ($sZin, "$dit"). "<br>";
echo stripos ($sZin, "$dit"). "<br>";
echo strripos ($sZin, "$dit"). "<br>";

~~~
## 4.3 Uitleg en voorbeelden substr() en substr_replace()

### Voorbeeld substr()
~~~php
echo substr('abcdef', 1);     // bcdef
echo substr('abcdef', 1, 3);  // bcd
echo substr('abcdef', 0, 4);  // abcd
echo substr('abcdef', 0, 8);  // abcdef
echo substr('abcdef', -1, 1); // f
~~~


### Voorbeeld substr_replace()

[Bekijk de examples 1,2 en 3](http://www.w3schools.com/php/func_string_substr_replace.asp)

## 4.4 Opdracht 40

### Omschrijving 40
Kopieer de code uit paragraaf 4.2 in een script met naam opdracht40.php.
Ga na of je begrijpt wat er op het scherm wordt getoond.

### Beoordelingscriteria 40
1. Je kan de uitkomst/de uitvoer van het script uitleggen 

---
## 4.5 Opdracht 41

### Omschrijving 41
Zet de volgende zin in een string variabele:
~~~php
$mop = "Weekend! Waarom gaat een Belg op vrijdag door het raam naar buiten? Het weekend staat voor de deur.";
~~~
Gebruik vervolgens voor iedere regel de substr() functie om de volgende uitvoer te krijgen die je ziet in de Visuele weergave.
### Visuele weergave 41

    - Weekend!
    - Belg
    - deur.
    - .
    - Waarom gaat een Belg op vrijdag door het raam naar buiten? Het weekend staat voor de deur.
    - Het weekend staat voor de deu

### Beoordelingscriteria 41
1. Voor iedere regel uitvoer is substr() gebruikt
2. Het programma toont geen waarschuwingen of errors
3. Voor iedere substr() wordt er commentaar gebruikt om de code uit te leggen

---
## 4.6 Opdracht 42 - van Belg naar blondje

### Omschrijving 42
Verander onderstaande mop in stappen met een van de functies uit dit hoofdstuk. Per verandering wordt aangegeven welke functie gebruikt moet worden.

> Weekend! Waarom gaat een Belg op vrijdag door het raam naar buiten? Het weekend staat voor de deur.

Na de laatste verandering is de mop veranderd in:

> Waarom gooit een blondje tijdens een spelletje de dobbelsteen tegen het plafond? Wie het hoogst gooit, mag beginnen.

### Visuele weergave 42

~~~php
    Weekend! Waarom gaat een Belg op vrijdag door het raam naar buiten? Het weekend staat voor de deur.
    //Gebruik: substr() om de $mop om te zetten naar:
    Waarom gaat een Belg op vrijdag door het raam naar buiten? Het weekend staat voor de deur.
    
    //Gebruik: str_replace() om de $mop om te zetten naar:
    Waarom gaat een blondje op vrijdag door het raam naar buiten? Het weekend staat voor de deur.
    
    //Gebruik: substr_replace() om de $mop om te zetten naar:
    Waarom gooit een blondje op vrijdag door het raam naar buiten? Het weekend staat voor de deur.
   
   //Gebruik: str_replace() om de $mop om te zetten naar:
    Waarom gooit een blondje tijdens een spelletje door het raam naar buiten? Het weekend staat voor de deur.
    
    //Gebruik: str_replace() om de $mop om te zetten naar:
    Waarom gooit een blondje tijdens een spelletje door het raam naar buiten? .
    positie 'door' is: <positie> lengte mop: <lengte>
    
    //Gebruik: substr_replace() met een negatieve waarde (zie voorbeeld 3 in de gelinkte pagina) om $mop om te zetten naar:
    Waarom gooit een blondje tijdens een spelletje de dobbelsteen tegen het plafond? Wie het hoogst gooit, mag beginnen.
~~~

### Beoordelingscriteria 42
1. Voor iedere regel uitvoer wordt de aangegeven functie gebruikt
2. Na iedere verandering is $mop gewijzigd en wordt deze ge-echo-d.
3. Het programma toont geen waarschuwingen of errors
4. Voor iedere verandering van de mop wordt commentaar gebruikt.
---