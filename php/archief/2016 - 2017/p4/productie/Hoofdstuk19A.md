#### [kleurcode]rgba(19, 36, 180, 0.9)

# Vervolg Hoofdstuk 19 Database connectie PHP

## 19.12 Wijzigen van een joke in de ijdb database

Wil je een grap wijzigen in de database dan gebeurt dat in meerdere stappen:
1. Haal de te wijzigen joke grap uit de database met de query:<br>
~~~mysql
SELECT * FROM joke WHERE id = <id van de te wijzigen grap>
~~~

2. Zet alle gegeven in een formulier, inclusief het id-nummer, zodat de gebruiker ieder veld kan wijzigen.

3. In het action script van het formulier moeten de POST of GET parameters, afhankelijk van de method van het formulier, worden opgevangen
 en de waardes in een update statement gezet.

 De update statement is: 
 ~~~mysql
        UPDATE joke 
		   SET joketext=<de waarde uit het formulier>, jokeclou=<de waarde uit het formulier> 
         WHERE id=<de waarde uit het formulier>
 ~~~
 
 ### 19.12.1 Ophalen van 1 specifieke grap
 
 Dit is de PHP-code die je nodig hebt om 1 grap op te halen:
 
 ~~~php
    // de id krijg je mee vanuit de GET parameter
     $id = $_GET['id'];
     try
     {
         //Ophalen van de grap op basis van de primary key
 	    $sql = 'SELECT * FROM joke WHERE id='.intval($id);
         $result = $pdo->query($sql);
         $row = $result->fetch(PDO::FETCH_ASSOC);
         $jokeclou = $row['jokeclou'];
         $joketext = $row['joketext'];
     }
     catch (PDOException $e)
     {
 	    echo 'Er is een probleem met ophalen van grap: ' . $e->getMessage();
 	    exit();
     }
 
 ~~~
 
 ### 19.12.2 Plaats de opgehaalde joke in een formulier
 
 ~~~php
 <!DOCTYPE html>
 <html lang="en">
     <head>
         <link type="text/css" rel="stylesheet" href="../../css/style.css">
         <meta charset="utf-8" />
         <title>Beheer grap</title>
     </head>
     <body>
      <header><h1>Wijzigen grap</h1></header>
      <div id="wrapper">
      <p>$msg</p>
             <form method='get' action='update.php'>
             <input type='hidden' name='id' value='<?php echo $id ?>'>
             <label>Inleiding</label>
             <textarea name="joketext"><?php echo $joketext ?></textarea>
             <label>Clou</label>
             <textarea name="jokeclou"><?php echo $jokeclou ?></textarea>
 	        <input type='submit' value='verzend' name='verzend'>
             </form>
        </div>
     </body>
 </html>
 
 ~~~
 ### 19.12.3 Vang de submit waarden op en verwerk ze in een update statement
 
~~~php
    $id = $_GET['id'];
    $joketext = $_GET['joketext'];
    $jokeclou = $_GET['jokeclou'];

    try {
		    $sql = 'UPDATE joke 
				    SET joketext=:joketext, jokeclou=:jokeclou 
                    WHERE id=:id
				    ';
			
		    //het statement wordt toegevoegd aan een pdo statement object
		    $s = $pdo->prepare($sql);
		
		    //koppelen van parameters in de query string met de te inserten waardes
		    $s->bindValue(':joketext', $joketext, PDO::PARAM_STR);
		    $s->bindValue(':jokeclou', $jokeclou, PDO::PARAM_STR);
		    $s->bindValue(':id', $id, PDO::PARAM_INT);

		    //Nu kan de query worden uitgevoerd
		    $s->execute();		
    }
    catch (PDOException $e)
    {
	    die('Fout bij het wijzigen van een rij: ' . $e->getMessage());
	
    }
~~~

## 19.13 Opdracht 193 Opstap naar volledig beheer van grappen

Pas je opdracht191.php aan zodanig dat de volgende visuele weergave krijgt:<br>

![beheer](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/p4/images/overzicht.png?raw=true)
  
  
## 19.14 Opdracht 194 Wijzigen van een grap

Programmeer nu ook echt je update.php waarin je 1 grap selecteert uit de database, deze in een formulier zet, en na 
wijziging door de gebruiker en verzending de grap ook echt met een update statement in de database.
<br>Vergeet nu ook niet de filter_var() functie te gebruiken voor het verwijderen van ongewenste input.
<br>Alle code snippets zijn hierboven al geplaatst. Je hoeft het alleen maar in de goede volgorde en met de juiste if else
constructie in elkaar te zetten.

<br>__Tip voor de opbouw van je code__:<br>
``In update php toon je dus een formulier als alleen de id in de GET parameter zit, 
maar doe je een update als je alle velden via het formulier binnenkrijgt. Als je geen id binnenkrijgt, moet je niks doen..``

## 19.15 Opdracht 195 Verwijderen van een grap

- Zorg ervoor dat je vanuit opdracht191.php nu ook één grap kan verwijderen.

- Programmeer dus ook een delete.php waarin je je DELETE statement op de tabel joke uitvoert.

- Laat na het succesvol verwijderen weer het overzicht van grappen zien.<br>

Met de volgende regel kun je je pagina meteen laten doorsturen.
~~~php
  header('location: opdracht191.php');
~~~
