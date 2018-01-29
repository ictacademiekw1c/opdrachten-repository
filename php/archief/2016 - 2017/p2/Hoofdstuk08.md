# Hoofdstuk 8

## 8.1 Wat ga je leren ?

- while loops/lussen
- wanneer begint een lus of repetitie
- wanneer eindigt een lus 
- teller 
- oneindige lus

## 8.2 Wanneer heb je een lus of loop nodig?

Bijvoorbeeld wanneer er veel html-onderdelen worden geprint die zich herhalen, bijvoorbeeld cellen of rijen in een tabel. <br>
De truc is te kijken wat er zich herhaalt en wat er verandert ten opzichte van een vorige herhaling. 
![voorbeeld tabel](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/images/voorbeeld2.jpg?raw=true)

## 8.3 Verschillen en overeenkomsten met if-else

### Overeenkomsten if-else en while

~~~php
// minimale if
if ( conditie ) {

}
else {


}

// while constructie
while ( conditie ) {

}
~~~

- Heeft een conditie nodig, die uiteindelijk true of false oplevert
- Heeft een { } = codeblok nodig die wordt uitgevoerd wanneer de conditie true is
- Je kan if-else constructies en while-lussen **nesten**

### Verschillen if-else en while

- while heeft geen **else**
- if wordt **eenmaal** uitgevoerd en while wordt **herhaaldelijk** uitgevoerd

## 8.4 Uitleg while en do while

[Uitleg while en do while op w3 schools](http://www.w3schools.com/php/php_looping.asp)

## 8.5 Opdracht 80 while lussen

### Opdrachtomschrijving 80

Programmeer een php-script dat de getallen 1 t/m 100 print
- a) Onder mekaar
- b) 10 getallen per rij
- c) 10 getallen per rij, maar print alleen de even getallen
- d) Als opdracht 80b maar dan in een tabel
- e) Aflopend van 100 naar 1 als opdracht 80b en 80d (in een tabel) maar dan alleen de veelvouden van 3. Print wel een lege cel als het getal geen veelvoud is van 3.

### Visuele weergave 80e
![visuele weergave 80e](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/images/opdracht80e.PNG?raw=true)

### Beoordelingscriteria 80
1. Maak voor iedere deelopdracht een apart script. (80a.php, 80b, 80c etc).
2. Comprimeer de bestanden als opdracht80.rar en upload het naar je portfolio
3. Je php-script toont een volledige en geldige html pagina
4. Je maakt gebruik van een while lus en eventueel if-else binnen de while
5. Je code bevat commentaar; vooral op plekken waar het moeilijk wordt of waar jij problemen mee hebt

## 8.6 Opdracht 81 while lussen

### Opdrachtomschrijving 81
De volgende code print de tafel van 5:

~~~php
    //printen van de tabelkop
    echo '<table border="1">
            <tr><th colspan="2">Tafel van 5</th></tr>';
            $teller = 1;    
            //de tafel van 5 in rijen en cellen printen    
            while ($teller < 11) {
                        $uitkomst = $teller * 5;
                        echo "<tr><td>$teller</td><td>$uitkomst</td></tr>";   
                        //teller (1,2,3,4,5,6,7,8,9,10) ophogen zodat de loop stopt bij 10
                        $teller++;         
            }
    //afsluiten van de tabel
    echo    '</table>';
~~~

Kopieer de bovenstaande code en test het uit. <br>
__Breidt de code uit zodat niet alleen de tafel van 5 wordt geprint maar alle tafels van 1 t/m 10.__
<br>Het moet er uit komen te zien als de volgende visuele weergave (tabellen naast elkaar).

### Visuele weergave 81
![visuele weergave 81](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/images/tafels.PNG?raw=true)

### Beoordelingscriteria 81
1. Sla je script op opdracht81.php en upload het als rar in je portfolio
2. Je php-script toont een volledige en geldige html pagina
3. Je maakt gebruik van een while lus en eventueel if-else binnen de while
4. Je maakt gebruik van een geneste while loop
5. Je code bevat commentaar; vooral op plekken waar het moeilijk wordt of waar jij problemen mee hebt

---
__Alternatieve opdrachten (niet verplicht)__
---

## 8.7 Opdracht 81 (alternatief) while lussen
### Alternatieve opdrachten zijn opdrachten voor leerlingen die iets meer uitdaging willen. Als huiswerkopdracht lever je dan de normale opdracht in of de alternatieve opdracht. In dit geval opdracht 81 of opdracht81 alternatief.
### Opdrachtomschrijving 81 alternatief
Hoe maak je een tabel met oplopende cijfers zoals opdracht 80d, maar dan met variabele kolommen en variabele rijen, die je binnen krijgt als GET parameters. Print een tabel met default waardes voor rijen=10 en kolommen=10.

### Visuele weergave 81 alternatief

![visuele weergave 81](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/images/opdracht81alt.PNG?raw=true)

Voor hen die de bovenstaande figuur ook al hebben kunnen deze dan nog proberen.
Plaats een rode kruis in het midden van de tabel.

![visuele weergave 81](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/images/opdracht81alt2.PNG?raw=true)

### Beoordelingscriteria 81 alternatief
1. Sla je script op opdracht81alt.php en upload het als rar in je portfolio
2. Je php-script toont een volledige en geldige html pagina
3. Je maakt gebruik van een while lus en eventueel if-else binnen de while
4. Je maakt gebruik van GET-parameters en default waardes bij het ontbreken ervan.

