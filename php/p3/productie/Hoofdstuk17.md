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
