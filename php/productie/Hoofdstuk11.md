# Hoofdstuk 11 Formulier 

## 11.1 Wat ga je leren ?

- Hoe krijg je formuliergegevens binnen in PHP
- De methods get en post
- action
- verborgen formulier velden

## Voorbeelden

- stap 1 formulier.html form
~~~php
<form method="get" action="opracht110.php">
    <input type="submit" name="verzend">
</form>
~~~

voorbeeld1.php:
~~~php
    //Wat zit er in $_GET?
    var_dump($_GET);
~~~

- stap 2 html en input type="text"
~~~php
<form method="get" action="opdracht110.php">
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

## 11.2 Opdracht 110 formuliervelden

### Opdrachtomschrijving 110

Breidt het formulier uit met de volgende invoer velden:
~~~html
<label>Keuze: </label>
<input type="checkbox" name="keuze" value="1">

<label>Plaats: </label>
<select name="plaats">
    <option value="a">Den Bosch</option>
    <option value="b">Den Bosch</option>
    <option value="c">Den Bosch</option>
</select>

<label>Geslacht: </label>
<input type="radio" name="geslacht" value="m">M<br>
<input type="radio" name="geslacht" value="v">M<br>

<input type="hidden" name="geheim" value="onbekend">

<textarea name="tekst">Wat heeft U te zeggen...</textarea>

<input type="password" name="wachtwoord" value="">
~~~

Programmeer vervolgens in opdracht110.php
- de waardes van de verschillende formuliervelden 

### Visuele weergave 110

``De geprinte waardes in de visuele weergave komen overeen met wat er is ingevuld in het formulier``

De waarde van plaats is : .....<br>
De waarde van keuze is : .....<br>
De waarde van geslacht is : .....<br>
De waarde van geheim is : ......<br>
De waarde van tekst is : ......<br>
De waarde van wachtwoord is : ......<br>

### Beoordelingscriteria 110
- Comprimeer opdracht110.php als opdracht110.rar en upload het naar je portfolio
- Je php-script toont een volledige en geldige html pagina
- Je code bevat commentaar; vooral op plekken waar het moeilijk wordt of waar jij problemen had








