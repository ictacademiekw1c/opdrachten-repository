# Hoofdstuk 6 - Getallen deel 1

## 6.1 Wat ga je leren ?

In dit hoofdstuk gaan we het hebben over getallen en strings en hoe ze worden opgeslagen in de computer. We leren wat bits en bytes zijn en wat het binaire stelsel is.

Verder gaan we ons focussen op getallen.
### Gehele getallen
- Wat zijn Integers.
- Verschil tussen integers en strings
- Rekenen met integers
- Toekenningsoperatoren
- Vermeerderings++ en verminderingsoperatoren--

### Gebroken getallen
- Floats
- De afrondfuncties round(), floor() en ceil() 

## 6.2 Bits en bytes, opslag van gegevens

Verschillen en overeenkomsten tussen getallen en strings:
- Met getallen kun je rekenen - operatoren: + - * / % 

- Zowel strings als getallen worden opgeslagen in de computer in bits en bytes (een reeks van 0 en 1). Alleen de manier waarop verschilt.
    - De ruimte die een getal in gebruik neemt in het geheugen is afhankelijk van het datatype (integer of float) 
    - Bijv een een geheel getal in PHP neemt 16 bits geheugenruimte in. Wat kun je daarin kwijt?
    - Bekijk allereerst deze video:
    - [![Uitleg bits and bytes](http://img.youtube.com/vi/EXYd9q2Ibn8/0.jpg)](http://www.youtube.com/watch?v=EXYd9q2Ibn8)
- Van een string neemt ieder karakter/letter neemt 1 byte(8 bits) in beslag
    - Iedere letter komt overeen met een getal uit de ASCII tabel, bekijk de volgende video
    - [![Uitleg ASCII](http://img.youtube.com/vi/0VqcOSC10Yw/0.jpg)](http://www.youtube.com/watch?v=0VqcOSC10Yw)

- [Bestudeer deze wiki pagina over binaire getallen](https://nl.wikipedia.org/wiki/Binair)

- [Als je meer wil weten over de werking (en geschiedenis) van computers en de transistor (nullen en enen) in het bijzonder...](http://ed.ted.com/lessons/how-transistors-work-gokul-j-krishnan)

---
## 6.3 Opdracht 60 Bits en bytes

### Omschrijving 60

1. Hoe wordt jouw naam (in kleine letters) in de computer opgeslagen?
    - Wat zijn de ASCII getallen voor ieder karakter
    - Wat zijn de binaire waardes
    - Hoeveel bits of bytes zijn ervoor nodig?

2. Wat is het grootste getal dat je kan opslaan in 32bits?
    a. Als je alleen maar gehele positieve wil bewaren
    b. Als je ook negatieve gehele getallen wil opslaan. 

### Beoordelingscriteria 60
1. Je hebt een word document aangemaakt met de vragen en antwoorden opdracht60.docx
2. Je bent in staat ieder getal om te zetten naar een binair getal
3. Je weet wat een ASCII tabel is je weet waarvoor het wordt gebruikt.

---

## 6.4 Integers (gehele getallen)

Met getallen kun je rekenen:

### Voorbeeld 1
~~~php
echo $getal1 = 13;
echo "<br>";
echo $getal2 = 2;

//de verschillende rekenkundige operatoren
$plus = $getal1 + $getal2;
$min = $getal1 - $getal2;
$keer = $getal1 * $getal2;
$delen = $getal1 / $getal2;
$modulus = $getal1 % $getal2;

echo "<br".$plus;
echo "<br".$min;
echo "<br".$keer;
echo "<br".$delen;
echo "<br".$modulus;
echo "<br".$macht;
~~~

### Voorbeeld 2

~~~php
//een variabele veranderen ten opzichte van zijn oude waarde
$getal = 15;
//de waarde is nu 15
$getal = $getal + 5;
// de waarde is veranderd in 20
//Maar er is ook een verkorte notatie mogelijk
$getal += 5;
//waarde is 5 hoger dan de vorige => 25

//dit kan ook met de andere operatoren
$getal *= 2;
//het getal is 2 * de oude waarde => 50

//zo heb je nog een derde manier om getallen met 1 op te hogen of juist te verminderen
$getal++;  //om de waarde met 1 op te hogen

$getal--; // om de waarde met 1 te verlagen
~~~
---

## 6.5 Floats (gebroken getallen)
Gebroken getallen (floats) worden genoteerd met de . (punt) als decimale punt. (Dus niet de komma.)

~~~php
<?php
//float is een gebroken getal; alle getallen die geen integers zijn
$getal = 2/3;
echo $getal; // 0.66666666666667 Let op! het is geen komma

//afronden op 2 getallen na de komma
echo "<br>";
echo round($getal,2);

//afronden naar boven
echo "<br>";
echo ceil($getal); //1

//afronden naar beneden
echo "<br>";
echo floor($getal); //0

?>
~~~

## 6.6 Opdracht 61

### Opdrachtomschrijving 61

Volg de code in voorbeeld 1 hierboven. Pas deze code aan zodat:
- De getallen uit een get-parameter worden gehaald
- De visuele weergave is zoals in de afbeelding die hieronder volgt
- De pagina een geldige html document is (alle content bevindt zich in de body; er worden bijv h1 en p en br gebruikt voor de structuur

### Visuele weergave 61
![Visuele weergave 61](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/images/opdracht61.PNG?raw=true)

### Beoordelingscriteria 61
1. Visuele weergave als hierboven
2. Geldige html
3. Er is gebruik gemaakt van php-commentaar.
4. Je maakt gebruik van get-parameters om de getallen door te geven
5. Je maakt gebruik van de isset() functie (zie hoofdstuk 5 laatste paragraaf) om te voorkomen dat je foutmeldingen krijgt als er geen get-parameters worden doorgegeven.

---
## 6.7 Opdracht 62

### Opdrachtomschrijving 62
Wat is de uiteindelijke waarde van de variabele $getal?

~~~php
$getal = 20021964; // Neem je geboortedatum - 20 geb 1964 
$leeftijd = 52; //Neem je leeftijd

$getal++;

$getal /=$leeftijd;

$getal = ceil($getal);

$getal--;

$getal +=50;

$getal /=3;

$getal = $getal % 15;
~~~


### Beoordelingscriteria 62

1. Je kunt uitleggen wat de waarde is na iedere regel code/verandering.
2. Je hebt in commentaar erachter gezet wat de waarde is.
3. Bewaar het script als opdracht62.php en upload het gerarde bestand.
4. Neem als beginwaardes je eigen geboortedatum (01011998 <= 1 jan 1998) en leeftijd