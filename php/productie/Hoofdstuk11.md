# Hoofdstuk 11 Formulier 

## 12.1 Wat ga je leren ?

- Hoe krijg je formuliergegevens binnen in PHP
- De methods get en post
- action
- verborgen formulier velden

## Voorbeelden

- stap 1 html form
~~~php
<form method="get" action="voorbeeld1.php">
    <input type="submit" name="verzend">
</form>
~~~

voorbeeld1.php:
~~~php
    //Wat zit er in $_GET?
    var_dump($_GET);
~~~

- stap 2 html en input type="text"
- stap 1 html form
~~~php
<form method="get" action="voorbeeld1.php">
    <label>Getal 1: </label><input type="text" name="getal">
    <input type="submit" name="verzend">
</form>
~~~

voorbeeld1.php:
~~~php
    //Wat zit er in $_GET?
    //var_dump($_GET);

    echo $_GET['naam'];
~~~

## Opdracht onderzoekje

Welke formulier velden ken je? Voeg ze toe aan het formulier en kijk hoe je ze binnen krijgt in het ontvangende php script.








