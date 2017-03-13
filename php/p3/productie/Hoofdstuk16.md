#### [kleurcode]rgba(204,67,54,1)

#  Hoofdstuk 16 - Toepassingsopdracht: Black Jack 
Tussendoortje:
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

### 16.2.2 Visualisatie van de kaarten

Om het leuker en echter te maken wil je natuurlijk de kaarten als plaatjes laten zien. Je kan 52 verschillende afbeeldingen gebruiken maar je kan ook 1 afbeelding gebruiken waar alle afbeeldingen naast elkaar op staan.
Dat scheelt het laden van afbeeldingen als je andere kaarten wil laten zien. Dit noemen ze een sprite sheet.

**Download de black jack kaarten sprite sheet**
[![Download de black jack kaarten sprite sheet](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/p3/images/cardsx.png?raw=true)](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/p3/images/cards.png?raw=true)

Maar hoe toon je nu 1 specifieke kaart?

De hoogte en breedte van iedere kaart in de sprite sheet is 78px breed en 122px hoog.

Met css styling (background-position) kun je 1 specifieke afbeelding tonen:
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

In de html heb je een p-tag nodig met de 2 klassen voor de kleur en de kaart.

~~~html
    <p class="schoppen twee"></p>
~~~

Komt eruit te zien als schoppen 2? Test dit zelf uit.

### 16.2.3 Spelverloop 

In de volgende UML activity diagram wordt visueel beschreven hoe het spelverloop is bij een spelletje Black Jack tegen de computer.

Zoals je kunt zien in het diagram kan het spel anders verlopen afhankelijk van verschillende spelsituaties.

[![Spelverloop Blackjack](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/p3/images/blackjackx.png?raw=true)](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/p3/images/blackjack.png?raw=true) 

[Wat is een UML activity diagram](https://nl.wikipedia.org/wiki/Activiteitendiagram)

### 16.2.4 Startcode

In de volgende startcode is al een deel van het spelverloop geimplementeerd.
 
[Download je startcode](https://gist.github.com/saebuabu/89aa96ad9fd75cb4b3a664d26bd4b879)

Test dit stukje code en probeer de verschillende onderdelen te begrijpen hoe bepaalde dingen zijn geprogrammeerd.
In de klas zal de docent de werkende startcode demonstreren. 

### 16.2.5 Opdracht 160 week 13-17 maart

Programmeer minimaal 1 onderdeel, die je zelf kiest, uit het activiteiten diagram in ###16.2.4, die in de startcode (###16.2.4) ontbreekt.

**Beoordelingscriteria**
- Je hebt alle bestaande code van commentaar voorzien, zodat je aantoont dat je de code begrijpt
- Je eigen code bevat beschrijvende commentaar
- Je hebt minimaal 1 onderdeel toegevoegd aan het blackjack spel
- Maak gebruik van sessievariabelen om spel informatie (geld, totaalspeler, totaalcomputer) op te slaan.
- Oplevering uiterlijk 20 maart (via commits en pushes)

### 16.2.6 Opdracht 161 week 20-24 maart

Programmeer minimaal 2 onderdelen uit het activiteiten diagram in ###16.2.4

**Beoordelingscriteria**
- Je eigen code bevat beschrijvende commentaar
- Je code bevat beschrijvende commentaar
- Je hebt minimaal 2 onderdelen toegevoegd aan het blackjack spel
- Maak gebruik van sessievariabelen om spel informatie op te slaan.
- Oplevering uiterlijk 27 maart (via commits en pushes)

### 16.2.7 Bonusopdracht 162 week 13-24 maart

Programmeer blackjack zodanig dat alle onderdelen uit het activity diagram (###16.2.4) zijn geprogrammeerd.

**Beoordelingscriteria**
- Je bent uitgegaan van de startcode of je hebt hebt je eigen black jack versie gemaakt
- Je code bevat beschrijvende commentaar
- Je hebt alle onderdelen toegevoegd aan het blackjack spel
- Maak gebruik van sessievariabelen om spel informatie op te slaan.
- Oplevering uiterlijk 27 maart (via commits en pushes)

**Opleveringen**
Blackjack moet in de week van 27 maart persoonlijk worden nagekeken bij de docent. 