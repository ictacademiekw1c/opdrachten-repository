#### [kleurcode]rgba(224,67,54,1)

#  Hoofdstuk 14 Cookies en sessies

## 14.1 Theorie

### Theorie overzicht

- $_SESSION variabele
   - gegevens zijn server side opgeslagen
   - 1 cookie client side
   
- $_COOKIE variabele
   - geen gegevens server side
   - alle data in aparte cookies opgeslagen(client side)

## 14.2 Reader sessies en cookies

[Open de reader](http://elo.kw1c.nl/CMS/Studie/811 ICT-Academie/811v Vakinhoudelijke MBO  AO/1.11 PHP/95311 AO/Semester 2[Periode 03 en 04]/Productie/Reader 2015/Reader H7.pdf)

## 14.3 Lesopdracht

### Omschrijving
Volg de volgende stappen en geef antwoord op de bijbehorende vragen.

- Maak het script clientsessie.php, zet hierin de volgende code en open het in de browser.

~~~php
setcookie("naam","Levi", time() + 3600);
~~~

- Beantwoord de volgende vragen
   - Hoe heet de cookie?
   - Wat is de waarde van de cookie?
   - Hoe lang is de cookie geldig?
   - Wat is het domein van de cookie?
   - Bestaat de cookie nog als je de browser afsluit en opnieuw opent in het hetzelfde domein?

- Maak vervolgens het script testsessie.php met de volgende code:

~~~php
if (isset($_COOKIE['naam'])) {
    echo "De cookie naam heeft de waarde ".$_COOKIE['naam'];
}
else {
    echo "geen cookie['naam'] gezet.";
}
~~~
- Beantwoord de volgende vragen:
   - Wat is de uitvoer van dit script?
   - Verwijder nu handmatig deze cookie; wat is nu de uitvoer van je script?

- Maak nu het script serversessie.php en zet hierin de volgende code:

~~~php
//als je geen c:\tmp hebt maak dan een tmp directory aan
session_save_path("c:/tmp");
session_start();
$_SESSION['naam'] = "Johan";
~~~

- Beantwoord de volgende vragen:
   - Welk cookie is erbij gekomen en wat is de waarde ervan?
   - Kijk in de directory c:\tmp, wat is daarbij gekomen?
   - Wat is de inhoud van c:\tmp?
   
- Voeg in serversessie.php de volgende code aan het eind toe:
~~~php
$_SESSION['cijfer'] = 7;
~~~

- Beantwoord de vraag?
    - Wat is nu de inhoud van het bestand dat je hiervoor bekeken hebt?

- Voeg in testsessie.php de volgende regels toe:
~~~php
echo "<hr>";

session_save_path("c:/tmp");
session_start();
if (isset($_SESSION['naam'])) {
    echo "Sessie variabele naam heeft de waarde ".$_SESSION['naam'];

} else {
    echo "Er bestaat geen sessie variabele naam";
}
~~~

- Voeg in serversessie.php de volgende code aan het eind toe:
~~~php
$_SESSION['resultaten'] = array(3,6,7,8,2,1,10);
~~~

- Beantwoord de vraag?
    - Wat is nu de inhoud van het bestand dat je hiervoor bekeken hebt?

- Voeg in testsessie.php de volgende regels toe:
~~~php
echo "<hr>";
if (isset($_SESSION['resultaten'])) {
    $resultaten = $_SESSION['resultaten'];
    $tel = 0;
    while ( $tel < count($resultaten)) {
        echo "<br>" . $resultaten[$tel];
        $tel++;
    }
}
~~~

- Beantwoord de vraag?
    - Wat is nu de uitvoer van dit script?
    
    
## 14.4 Opdracht 140

### Omschrijving 140 
Neem het formulier van opdracht 131. 
<br>Laat na verzending van het formulier zien  wat het cijfer is voor het gekozen vak (precies zoals in opdracht 131), alleen moet de gebruiker het formulier meerdere malen kunnen invoeren, zodat de volgende voorbeeld uitvoer zou kunnen onstaan:

<table border="1">
<caption>Rapport van leerling Abu Saebu met nummer 99900398 klas IO1B4</caption>
<tr><th>Vak</th><th>Cijfer</th></tr>
<tr><td>PHP</td><td>7</td></tr>
<tr><td>ASP</td><td>9</td></tr>
<tr><td>Javascript</td><td>5</td></tr>
<tr><td>Database</td><td>7</td></tr>
<tr><td>Gemiddelde</td><td>7</td></tr>
</table>

### Beoordelingscriteria 140
- Er is gebruik gemaakt van sessievariabelen 
- Het formulier heeft als action opdracht141.php (zichzelf)
- In de sessie wordt een variabele met datatype array gebruikt.