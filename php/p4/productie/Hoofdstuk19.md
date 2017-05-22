#### [kleurcode]rgba(19, 36, 200, 0.9)

# Hoofdstuk 19 Database connectie op een c9 server.

Professionele websites die gebouwd zijn in PHP en waarbij heel veel gegevens centraal moeten worden opgeslagen maken gebruik van een database.
Een database service (applicatie) draait vaak op een aparte server,maar soms ook op dezelfde server als de webserver. Een professionele website kan niet zonder een database en ook niet zonder een server-side programmmeertaal als PHP/ASP.

Een webapplicatie kan niet alleen met clientside software (javascript) runnen omdat je altijd serverside software nodig hebt om de database te kunnen raadplegen.

## 19.1 Database connectie op een c9 webserver met een MySQL database
 
![architectuur](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/p4/images/dbserver.gif?raw=true)
 
Een database programma is een aparte applicatie (service) die losstaat van een webserver en waarmee je allereerst een connectie moet opzetten voordat je er gegevens uit kan halen of opslaan.
In de bovenstaande afbeelding wordt een MySQL database getoond. Tot nu toe hebben jullie kennisgemaakt met een Microsoft SQL database. 
Een MySQL database heeft veel overeenkomsten met een MS SQL database. Beide databases verstaan dezelfde vraagtaal 'SQL'.

## 19.2 Leerdoelen

1. Het kunnen hosten en testen van je php-script op een webserver (op het portaal c9.io) in de cloud.
2. Online kunnen zetten van je nieuwe en gewijzigde php scripts (met commandline git instructies) die je hebt gecommit en gepushed naar www.github.com.
3. Een MySQL database kunnen opzetten op de c9 webserver, en via PHPMyAdmin een database en een tabel kunnen aanmaken.
4. In PHP een database connectie kunnen opzetten.
5. Via php code SQL statements uitvoeren op de MySQL database en de resultaten kunnen opvangen (associatieve array) en weergeven in een html-pagina.

## 19.3 Hoe ga je aan de slag?

We gaan aan de slag met de leerdoelen in de volgorde zoals ze genoemd zijn. 
Ieder leerdoel zal worden uitgelegd door de leraar. Ieder leerdoel heeft ook minimaal 1 opdracht. 
Omdat er veel stappen nodig zijn om het uiteindelijke doel te bereiken, wordt er geadviseerd om in koppels te werken. Je mag natuurlijk ook in je eentje werken, 
maar als je er in je eentje niet uitkomt zul je worden gekoppeld aan een mede-leerling.

## 19.4 Leerdoel 1: Hosten en testen van je phpsemester2 code op een c9 server

1. Ga naar [c9 portaal](http://c9.io) login met je github account en open je c9 workspace.

![open c9 workspace](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/p4/images/c9.png?raw=true)

Nadat je workspace is opgestart zie je hetvolgende beeld:<br>

![Startscherm](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/p4/images/c9start.png?raw=true)

Open vanuit het menu een nieuwe terminal.<br>

![Nieuwe terminal](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/p4/images/terminal.png?raw=true)

Type achter de $-prompt de git commando:<br>

 ~~~linux

 wolkanc:~/workspace (master) $ git clone https://github.com/wolkanc/phpsemester2.git

~~~

Waar hierboven wolkanc staat moet je eigen gebruikersnaam zijn op github.com. Daarna wordt je gevraagd om je login en wachtwoord in te vullen van de github.com site. <br>

Is dat gelukt dan heb je je phpsemester2 repository op de c9 server workspace binnengehaald.
<br>
![clone](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/p4/images/clone.png?raw=true)

Om het te kunnen testen moet je de webserver nog opstarten:
Klik op run project
<br>

![clone](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/p4/images/run.png?raw=true)

Kopieer de URL naar je browser en dan kun je iedere pagina via de c9 server uittesten.

__OPDRACHT__
- Volg alle stappen hierboven en laat aan je docent zien dat je phpsemester2 code nu ook werkt op een URL in het c9 domein.
- Als je met zijn tweeen werkt heb je mekaar geholpen zodat ieder individueel zijn eigen phpsemester2 repository heeft staan op ieders c9 workspace.

## 19.5 Leerdoel 2: Online zetten/updaten van je php code op c9.

Als je nu nieuwe code gaat schrijven in PHPStorm staat het natuurlijk niet automatisch online op de c9 workspace.
Volg de volgende stappen om dat voor mekaar te krijgen. 
1. Maak een nieuwe directory aan in PHPStorm met de naam hoofdstuk19
2. Maak daar een nieuwe php-script aan met de naam test.php
3. Zet daar in de volgende test php-code:

~~~php
<!DOCTYPE html>
<html lang="en">
<head>
    <link type="text/css" rel="stylesheet" href="../css/style.css">
    <meta charset="utf-8" />
    <title>Opdrachten overzicht PHP periode 4</title>
</head>
<body>
<header><h1>Test online op c9</h1></header>
<div id="wrapper">
    <h2>Hoofdstuk 19</h2>
    <p>
        <?php
            echo "Test php op c9";
        ?>
    </p>
</div>
</body>
</html>
~~~

4. Commit en push deze directory en nieuwe php script.
5. Ga vervolgens naar je c9 workspace en open een terminal venster
    - ga eerst naar de phpsemester2 directory met het commando: __cd phpsemester2__
    - en type daar op een prompt in een terminal window: __git pull__

__OPDRACHT__
<br>
Volg alle stappen hierboven en test of je nieuwe script nu ook werkt op de c9 server.
<br>__Let op:__ Om je nieuwe script te kunnen testen moet je je URL ook uitbreiden met de directory en scriptnaam (<basisURL>/hoofdstuk19/test.php).

## 19.6 Leerdoel 3: Opzetten van een MySQL database op de c9 workspace

De MySQL database staat niet standaard aan op de c9 machine, maar die kunnen we wel eenvoudig installeren en configureren.

Dit zijn de stappen die je moet volgen op de c9 server. Je moet hiervoor weer een aantal commando's uitvoeren achter de prompt in een terminal window.

Installeren van mysql doe je met:
~~~linux
mysql-ctl install
~~~

Vervolgens kun je phpmyadmin installeren met:
~~~linux
phpmyadmin-ctl install
~~~

Opstarten van de database:
~~~linux
mysql-ctl start
~~~

Nadat je phpmyadmin hebt geinstalleerd krijg je een link waarmee via phpmyadmin het beheer kan doen van de MySQL database.
De link ziet er alsvolgt uit: __https://[workspacename]-[username].c9users.io/phpmyadmin__. 
Login met je Cloud9 gebruikersnaam en een lege wachtwoord.

Log in op je phpmyadmin. Je ziet hetvolgende scherm:<br>

Maak een nieuwe database aan met de naam ijdb (international jokes database).

![database](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/p4/images/database.png?raw=true)

Kies de database en voer dan de volgende sql-statements uit:

~~~sql

CREATE TABLE IF NOT EXISTS `joke` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `joketext` text NOT NULL,
  `jokeclou` text NOT NULL,
  `jokedate` datetime NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB  DEFAULT CHARSET=utf8 AUTO_INCREMENT=1 ;

INSERT INTO `joke` (`id`, `joketext`, `jokeclou`, `jokedate`) VALUES
(1, 'Een dwerg loopt een bar binnen\r\n– Wat is blauw en ruikt naar rode verf?', 'Blauwe verf!!!', '2017-01-30 13:01:32');
~~~

![tabel](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/p4/images/table.png?raw=true)

Hiermee wordt er 1 tabel aangemaakt met de naam joke en wordt er 1 grap toegevoegd, zodat we al tenminste 1 grap uit de database kunnen selecteren met onze php-script.

__Opdracht__
- Je hebt de database ijdb aangemaakt
- Je hebt de tabel aangemaakt en je hebt er 1 mop aan toegevoegd
- Laat dit zien aan de docent

## 19.7 Leerdoel 4: Een connectie met MySQL ijdb opzetten in een PHP script.

Maak een script __connectie.php__ en zet hierin:
~~~php
<?php
// try catch constructie voor opvangen van foutsituaties
try
{
    $pdo = new PDO('mysql:host=localhost;dbname=ijdb','<gebruikersnaam c9>');
    $pdo->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
    $pdo->exec('SET NAMES "utf8"');
}
catch (PDOException $e)
{
    echo 'Connectie met database mislukt: ' . $e->getMessage();
    exit;
}

echo 'Database connectie is gelukt.';
?>
~~~

__Opdracht__<br>
- Test dit uit op je lokale machine en wat krijg je nu te zien als je het script connectie.php uitvoert?
- Commit en push het naar github.com en zet het weer vervolgens op de c9 server met een git pull commando. Wat krijg je nu te zien als je het script uitvoert in de browser?
- Laat de docent zien dat je uiteindelijk een database connectie hebt kunnen opzetten met de MySQL database.

## 19.8 Huiswerkopdracht 190
- Doe alle bovenstaande opdrachten in de leerdoelen 1 t/m 4 en laat het resultaat zien aan de docent.

### 19.8.1 Beoordelingscriteria
- Je hebt een werkende MySQL database draaien op c9
- Je hebt de database ijdb daarin aangemaakt
- Je hebt de tabel joke aangemaakt met 1 rij erin
- Je kan je connectie script uitvoeren vanuit jouw c9 URL
- Je hebt je phpsemester2 naar c9 gehaald (eenmaal) met de __git clone__ commando
- Je hebt je phpsemester2 repository ververst op c9 met het commando: __git pull__ 


## 19.9 Leerdoel 5: SQL statements uitvoeren op de ijdb database in PHP op de c9 server.

### 19.9.1 Een select statement uitvoeren op de joke tabel.

Om een select statement uit te kunnen voeren moeten we ook de connectie statements van te voren ook uitvoeren.
Omdat meerdere scripts ook andere sql statements uitvoeren hebben we daar ook dezelfde statements nodig.
Daarom is het handig 1 connectie.php te gebruiken en die in verschillende scripts met de include commando aan het script toe te voegen.

Maak een nieuw script __opdracht191.php__ en begin met het includen van connectie.php (uit leerdoel 4).

~~~php
//vervolgens kunnen we een select statement uitvoeren met de volgende code
include('connectie.php');

try
{
	$sql = 'SELECT * FROM joke';
	$result = $pdo->query($sql);
}
catch (PDOException $e)
{
	echo 'Er is een probleem met ophalen van grappen: ' . $e->getMessage();
	exit();
}

// Uitlezen van een resultaat set en toewijzen aan een associatieve array ( veld => waarde )
// Elk nieuw element in de array $row is op zich ook weer een associatieve array
// zolang als er nog rijen zijn wordt de lus herhaald en iedere keer wordt er een associatieve rij aan $row toegevoegd
while ($row = $result->fetch(PDO::FETCH_ASSOC)) {
   print_r($row);
}

~~~
__Opdracht__
- Neem bovenstaande code over zoals is beschreven en test het uit op je c9 server.

Je krijgt die ene grap te zien die in de tabel joke al was toegevoegd. De uitvoer is echter niet erg mooi. 

## 19.10 Opdracht 191 Select statement en uitvoer weergeven in tabel

1. Pas de code in opdracht191.php aan zodanig dat de volgende visuele weergave wordt getoond:<br>
![overzicht](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/p4/images/ijdb1.png?raw=true)
2. Voeg via de phpmyadmin (zie leerdoel 2) nog 2 (echte leuke) grappen toe. 
3. Laat aan de docent zien dat de uitvoer nog steeds netjes is.

### 19.9.2 Een insert statement uitvoeren op de joke tabel.
Met de volgende code kun je een nieuwe grap toevoegen in de joke tabel.
~~~php
include "connectie.php";
$joketext = "Een werknemer stonk en een collega vroeg: 'Douche je na de seks ? Ja, zei hij.'";
$jokeclou = "'Dan moet je misschien eens seks hebben?'";
try {
            //insert statement met placeholders voor de waardes
		    $sql = 'INSERT INTO joke 
				    (joketext, jokeclou, jokedate) 
				    VALUES 
				    (:joketext, :jokeclou, NOW() );';
			
		    //het statement wordt toegevoegd aan een pdo statement object
		    $s = $pdo->prepare($sql);
		
		    //koppelen van parameters in de query string met de te inserten waardes
		    $s->bindValue(':joketext', $joketext, PDO::PARAM_STR);
		    $s->bindValue(':jokeclou', $jokeclou, PDO::PARAM_STR);

		    //Nu kan de query worden uitgevoerd
		    $s->execute();
		    $id = $pdo->lastInsertId();
		    //De id is nu bekend (auto increment veld)
            echo "De grap is toegevoegd met id: ".$id; 
		
    }
    catch (PDOException $e)
    {
	    die('Fout bij inserten van een rij: ' . $e->getMessage());
	    exit;
    }
~~~

__Lesopdracht__<br>
Zet bovenstaande code in __insert.php__; initialiseer de variabelen met een nieuwe goeie grap en run het script.
Bevestig voor jezelf dat de grap is toegevoegd door daarna het script opdracht191.php te runnen, of rechtstreeks met
phpmyadmin in de tabel joke te kijken.

## 19.11 Opdracht 192 Toevoegen van een grap vanuit een formulier.

Als je gebruikers de mogelijkheid wil bieden om zelf grappen toe te voegen heb je een formulier nodig. 

__Opdrachtstap 1:__<br>
Maak het script formulier.php waarin je 2 velden zet om de joketext en jokeclou in te vullen.
Zet er ook een submitbutton die ervoor zorgt dat het formulier wordt verzonden naar het script __insert.php__.
De form tag heeft de attributen method en action. Zorg ervoor dat deze de juiste waarden hebben.

> [Theorie html form tag](https://www.w3schools.com/html/html_forms.asp)

__Opdrachtstap 2:__<br>

``Als je nu in het formulier de method get hebt gebruikt, 
<br>dan krijg je waardes binnen in de variabele $_GET.
Maar als je de method post gebruikt dan krijg je het binnen in de $_POST variabele.``

Pas insert.php nu zodanig aan dat de ingevulde grap in het formulier wordt toegevoegd aan de tabel joke.<br>
Werkt dit ga dan verder met <br>
__Opdrachtstap 3:__<br>

Breidt __insert.php__ uit met een stukje validatie. Als 1 van de velden joketext of jokeclou niet is ingevuld,<br>
mag de grap niet worden ingevoerd. Je moet worden teruggestuurd naar het formulier met de melding dat alle velden verplicht moeten worden ingevuld.

``Maak op de juiste manier gebruik van de isset() en empty() functies.``

__Opdrachtstap 4__:<br>

Als je wilt voorkomen dat er in de graptekstelden rare tekens, HTML of bijvoorbeeld SQL of javascript bevatten moet je 
de get- of post- parameters nog filteren op schadelijke of ongewenste invoer. 

Test het zelf eens in je formulier door html tags  en of javascript in een grap in te voeren. 
Hoe wordt dit in de database opgeslagen en hoe ziet de uitvoer van opdracht191.php er nu uit?

``Je begrijpt nu dat je je invoer echt moet filteren op ongewenste invoer.``

Filteren doe je op de volgende manier: <br>
~~~php
$jokeclou = filter_var($_GET['jokeclou'], FILTER_SANITIZE_STRING);
$joketext = filter_var($_GET['joketext'], FILTER_SANITIZE_STRING);
~~~




