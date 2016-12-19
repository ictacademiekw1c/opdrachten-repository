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
    <option value="b">Tilburg</option>
    <option value="c">Breda</option>
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

## 11.3 Opdracht 111 formuliervelden validatie

### Opdrachtomschrijving 111
In de volgende video wordt een formulier getoond, waarin met php gecontroleerd wordt wat de gebruiker heeft ingevuld.
In een goed werkende applicatie krijgt de gebruiker feedback/terugkoppeling als niet de gewenste input door de gebruiker is gegeven.

Bestudeer het gedrag in deze video en breid het formulier zo uit dat hetzelfde gedrag wordt vertoond als in de video.

[Bekijk hier de video van het formulier](https://mix.office.com/watch/14j36qfov0w4g)

### Opzet programmastructuur
Begin met de volgende html/php code:
~~~php
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Formulier en $_GET</title>
         <style>
            section {
                width:  40%;
                margin:  auto;
                padding:  1em;
                border: 1px solid black;
            }
        </style>
    </head>
    <body>      
        <section>      
        <form method="get" action="opdracht111.php">
            <label>Getal 1: </label><input type="text" value="<?php echo $getal ?>" name ="getal">
            <input type="submit" name="verzend" value="verzend">
        </form>
        <p><?php echo $msg; ?></p>
        </section>
    </body>
</html>
~~~

### Stappenplan 111

- Je krijgt meteen een foutmelding dat $getal en $msg niet bestaan. Initialiseer getal op null en msg op "Vul een getal in tussen de 10 en de 20.".
- Maak een if else constructie met isset() en $_GET zodat je kan testen of het formulier verzonden is.
- Indien het formulier verzonden is test dan of er iets is ingevuld in het veld getal met de functie empty()
- Test vervolgens of het ingevulde getal groter is dan 10 en tegelijkertijd kleiner is dan 20.
- Test of je de juiste melding krijgt bij goede en foute invoer.

### Visuele weergave en gedrag 111

[Bekijk hier de video van het formulier](https://mix.office.com/watch/14j36qfov0w4g)

### Beoordelingscriteria 111
- Comprimeer opdracht111.php als opdracht111.rar en upload het naar je portfolio
- Je php-script toont een volledige en geldige html pagina
- Je code bevat commentaar; vooral op plekken waar het moeilijk wordt of waar jij problemen had
- Je maakt gebruik van de method get
- Voor de validatie gebruik je de functies isset() en empty()







