#### [kleurcode]rgba(194,67,54,1)

#  Hoofdstuk 17 Array functies

## 17.1 Wat gaan we leren?
PHP heeft standaard veel array functies waarmee je arrays kunt onderzoeken en manipuleren.
We leren:

- Zoeken in arrays op sleutels en waarden
- Sorteer je array op allerlei manieren
- Bouw je een array-schudder (shuffle)
- Maak je van een zin een array met woorden

Een volledige lijst met array functies vind je [hier](http://php.net/manual/en/ref.array.php).

Uit deze lijst van arrays behandelen we de volgende functies:

- array_flip()
- array_search()
- array_key_exists()
- array_keys()
- array_rand()
- array_reverse()
- sort() en asort()
- ksort() en krsort()
- shuffle()
- str_split()
- explode()

##17.2 Voorbeeld array
~~~php
$fruit = array(
     'appel' => 'lekker'
    ,'peer' => 'sappig'
    ,'sinaasappel' => 'zuur'
    ,'kiwi' => 'gezond'
    ,'banaan' => 'zoet'
    ,'meloen' => 'heerlijk'
    ,'kersen' => 'zalig'
);
~~~

##17.3 Lesopdracht

### 17.3.1 Lesopdracht 1

Zoek op php.net op wat de php-functies array_flip(), array_search() en array_key_exists() doen.
Als je de documentatie leest voor een bepaalde functie, let dan op de volgende punten:
- Snap je de uitleg van de werking van de functie?
- Welke parameters kun je doorgeven?
- Welke parameters zijn verplicht/optioneel?
- Welke datatypes hebben de verschillende parameters?
- Heeft de functie een return waarde en zoja? Welk datatype is dat dan?
- Zijn er verder bijzonderheden?

Beantwoordt bovenstaande vragen voor elk van deze functies.
