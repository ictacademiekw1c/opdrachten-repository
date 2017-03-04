#### [kleurcode]rgba(204,67,54,1)

#  Hoofdstuk 16 - Toepassingsopdracht  

## 16.1 Black Jack

Wat is Black Jack en hoe wordt het gespeeld?

[Wikipedia over blackjack](https://nl.wikipedia.org/wiki/Blackjack)

## 16.2 Black Jack versie online met PHP

### 16.2.1 Eerste opzet

Nu vraag je je af hoe moet ik nu Black Jack gaan programmeren?

Je kan beginnen door een array te initialiseren met de volgende waarden:
~~~php
$aNumbers = array('aas','twee','drie','vier','vijf','zes','zeven','acht','negen','tien','boer','vrouw','heer');

$aStok = array( "schoppen" => $aNumbers
,"klaveren" => $aNumbers
,"harten" => $aNumbers
, "ruiten" => $aNumbers);

~~~
Een combinatie van een associatieve array (de kleuren) en een numerieke array (de kaarten aas, 2, 3, ... t/m koning)
Als je een foreach en een while lus programmmeert dan kun je alle kaarten laten zien:
~~~php
  echo "<div>";
    foreach ($aStok as $kleur => $kaarten) {
        $tel = 0;
        while ($tel < count($kaarten)) {
            echo "<span>".$kleur." ".$kaarten[$tel]."</span>  ";
            $tel++;
        }
        echo "<hr>";
    }
    echo "</div>";
~~~

Test dit zelf uit in stap0.php (in een nieuwe map hoofdstuk16).

### 16.2.2 Opdracht 

Nu heb je gelezen hoe de spelregels zijn van het echte spel black jack, maar ga je een eigen versie maken in php waarin 1 speler 
speelt tegen de computer. Hoe ga je de puntentelling doen en met hoeveel stokken ga je spelen?
Om het eenvoudiger te houden is het aan te raden om slechts met 1 stol te spelen (52 kaarten).

### 16.2.3 Visualisatie van de kaarten

Om het leuker en echter te maken wil je natuurlijk de kaarten als plaatjes laten zien. Je kan 52 verschillende afbeeldingen gebruiken maar je kan ook 1 afbeelding gebruiken waar alle afbeeldingen naast elkaar op staan.
Dat scheelt het laden van afbeeldingen als je andere kaarten wil laten zien. Dit noemen ze een sprite.

[Download de kaarten sprite](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/p3/images/cards.png?raw=true)

Maar hoe toon je nu 1 specifieke kaart?

