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
5. Via php code SQL statements uitvoeren op de MySQL database en de resultaten kunnen opvangen
6. De resultaten van een SQL-statement op een nette manier in PHP kunnen opvangen.

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
5. Ga vervolgens naar je c9 workspace 
    - ga eerste naar de phpsemester2 directory met het commando: __cd phpsemester2__
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

![tabel](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/p4/images/database.png?raw=true)

Hiermee wordt er 1 tabel aangemaakt met de naam joke en wordt er 1 grap toegevoegd, zodat we al tenminste 1 grap uit de database kunnen selecteren met onze php-script.

__Opdracht__
- Je hebt de database ijdb aangemaakt
- Je hebt de tabel aangemaakt en je hebt er 1 mop aan toegevoegd
- Laat dit zien aan de docent

## 19.7 Leerdoel 4: Een connectie met MySQL ijdb opzetten in een PHP script.

Maak een script connectie.php en zet hierin:
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

