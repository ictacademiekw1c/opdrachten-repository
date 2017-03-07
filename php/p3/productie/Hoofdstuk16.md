#### [kleurcode]rgba(204,67,54,1)

#  Hoofdstuk 16 - Toepassingsopdracht  

[Meervoudige intelligentietest](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.22%20PHP%5D%20PHP/Productie/02.%20Opdrachten/Meervoudige_intelligentie_-_vragenlijst_leeg.xlsx)

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
Om het eenvoudig te houden is het aan te raden om slechts met 1 stok te spelen (52 kaarten).

Hoe wordt jouw eigen Black Jack online game? Beschrijf de spelregels zoals jij het wil gaan maken. Laat je inspireren door de uitleg op de wikipagina.

### 16.2.3 Visualisatie van de kaarten

Om het leuker en echter te maken wil je natuurlijk de kaarten als plaatjes laten zien. Je kan 52 verschillende afbeeldingen gebruiken maar je kan ook 1 afbeelding gebruiken waar alle afbeeldingen naast elkaar op staan.
Dat scheelt het laden van afbeeldingen als je andere kaarten wil laten zien. Dit noemen ze een sprite.

[Download de kaarten sprite](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/p3/images/cards.png?raw=true)

Maar hoe toon je nu 1 specifieke kaart?

Met css styling kun je 1 specifieke afbeelding tonen:
~~~css
            p {
                margin: 3px;
                width: 79px;
                height: 123px;
                float: left;
                background-image: url('cards.png');
            }

            .schoppen {
                background-position-x: -79px;
            }

            .twee {
                background-position-y: -369px;
            }
~~~

~~~html
    <p class="schoppen twee"></p>
~~~

Komt eruit te zien als schoppen 2? Test dit zelf uit.
