#### [kleurcode]rgba(244,67,54,1)

# Hoofdstuk 1

## 1.1 Inleiding
In iedere programmeertaal komen variabelen voor. Variabelen hebben een naam een type en een waarde.
Iedere variabele neemt een stukje computergeheugen in beslag en de grootte ervan hangt af van het type en de waarde die je erin wilt opslaan. Als programmeur maak je de variabelen aan die je nodig hebt voor je applicatie, en bepaal je daardoor hoeveel geheugenruimte je programma in beslag neemt.

[![Tedex over computergeheugen](http://img.youtube.com/vi/p3q5zWCw8J4/0.jpg)](http://www.youtube.com/watch?v=p3q5zWCw8J4)

## 1.2 Gegevens, data, informatie, opslag, buffer, geheugen, waarde, getallen, woorden, letters
Data om ons heen:
~~~
17, 45, 3.45, 'Abu Saebu', 'IO1B4'
"12/08/2016", "Dit is de eerste les PHP"
'12:45', ICT-Academie, 'Ronald Meijerink'
'OK1030', 'Onderwijsboulevard 3', "maandag", 
"Nederlands", "PHP", "Ralph Gijsbrechts", "IO1D4","IO1E4"
"Rekenen", "Den Bosch", 60, 45, 'guest'
~~~

## 1.3 Variabelen en waarden
Voorbeelden van variabelen en toegekende waarden
~~~
$leeftijd = 10; // de waarde 10 is van het type getal
$naam = 'Abu';  // de waarde 'Abu' is een string (tekenreeks)
$ervaring = 5.5; // een gebroken getal
$geboortedatum = date();
~~~

- [Regels voor de benaming van php-variabelen](http://www.w3schools.com/php/php_variables.asp)

## 1.4 Datatypes

Voor de theorie verwijzen we je naar de site van w3schools.com:
[Welke datatypes zijn er in php](http://www.w3schools.com/php/php_datatypes.asp)

## 1.5 Hoe toon je de waarde van een variabele?

Met de echo statement kun je de waarde van een variabele op het scherm tonen
~~~php
$naam = 'Pieter-Jan';
echo "Mijn naam is";
echo $naam;

//Hiermee zet je commentaar in je code

//combineer een variabele met tekst

echo "Mijn naam is niet $naam";
~~~

---

## 1.6 Opdracht 01

De opdracht is om het script opdracht0001.php te schrijven, waarin je met php een stuk tekst print die jezelf introduceert.

Het uiteindelijke resultaat van je php-script zal bijvoorbeeld eindelijk het volgende resultaat moeten opleveren.
### 1.6.1 Visuele weergave

> Ik ben Abu Saebu. Ik woon bijna mijn hele leven in 's-Hertogenbosch. Ik heb op school gezeten op het Sint Janslyceum op de Sweelinckplein in Den Bosch. Ik ben 52 jaar, ik ben getrouwd en ik heb 2 kinderen. Mijn hobbies zijn gitaar spelen, piano spelen, muziek luisteren en programmeren. Ik ben docent applicatieontwikkeling en ik geef de vakken PHP, HTML/CSS, Javascript, Database/SQL, C#, Android Apps, Beheer en Bedrijfskunde.

Schrijf een introductietekst over jezelf met je naam, woonplaats, je hobbies, je school, je leeftijd, je hobbies, je thuissituatie en wat je graag wilt worden of wat je graag zou willen doen.
Gebruik voor ieder van deze gegevens een variabele met de juiste datatype en syntax.

### 1.6.2 Opzetten van je programmeercode
Volg de volgende stappen:
1. Maak voor je naam (voornaam en achternaam), je leeftijd, je woonplaats, je hobbies, aantal broers en zussen, en je gewenste beroep pf droom een aparte variabele.
2. Geef iedere variabele de juiste waarde.
3. Schrijf nu je introductietekst en gebruik daarin op de juiste plek de goeie variabele.
4. print de introductietekst met een echo commando. Gebruik &lt;br&gt;
 om je tekst op een volgende regel te zetten.

 >**Vergeet niet**
 - Je code tussen <?php en ?> te zetten.
 - Het einde van een 'zin' te eindigen met een ;
 - Strings in te pakken in quotes of ' ' of " "

 ~~~php
 <?php
 //Zet hieronder je code

 ?>
 ~~~

### 1.6.3 Beoordelingseisen
1. Het script levert geen fouten of waarschuwingen op in de browser
2. De visuele weergave is een duidelijke en correcte tekst.
3. Alle informatie wordt via een variabele met de goeie waarde en datatype weergegeven.
4. Sla het script op als opdracht01.php, pak het in als rar en upload het naar je portfolio.









