#### [kleurcode]rgba(19, 36, 160, 0.9)

# Hoofdstuk 20 Database connectie PHP met de lokale MSSQL server via odbc

## 20.1 Lokale connectie

Tot nu toe hebben we onze php-code niet lokaal kunnen testen, omdat we geen lokale MySQL database hebben draaien.
Voor ASP en het vak database SQL is er echter wel een MSSQL server database geinstalleerd en wordt deze server ook automatisch gestart
wanneer je laptop wordt opgestart.

Het ligt nu voor de hand om ook te kijken of we ook een connectie kunnen leggen met een MSSQL database en tabel, en of we daar ook 
op dezelfde manier gegevens kunnen selecteren, toevoegen en verwijderen.

## 20.2 Stappen om de connectie naar MSSQL lokaal op te zetten 

### 20.2.1 Database en table in SQL Server Management studio
Voordat we een connectie kunnen leggen moeten we natuurlijk ook een ijdb database en een joke tabel aanmaken in deze lokale omgeving.
Open je SQL Server Management studio en maak hierin een ijdb database aan en een joke tabel met dezelfde velden als de joke tabel op
de c9 server. Voeg ook alvast een goeie grap in via deze beheertool.

### 20.2.1 Een Data Source Name (DSN) aanmaken 


Volg de stappen die in de volgende video (de video start met het opstart scherm van het programma odbc data sources, dat reeds op je laptop is geinstalleerd)  
worden getoond:
[Uitleg via een screenvideo](https://mix.office.com/watch/19twfepzm461o)

In de video wordt een odbc DSN met de naam __phpmssql__ aangemaakt. Deze naam heb je straks ook nodig in je php-script.

### 20.2.2 De extensie php_pdo_odbc.dll aan php.ini toevoegen

Om een odbc koppeling te gebruiken heb je nog de extensie php_pdo_odbc.dll in de configuratieinstellingen van de php-interpreter.

Zoek in je php.ini of de volgende regels erin staan:<br>
~~~ini
; Directory in which the loadable extensions (modules) reside.
; http://php.net/extension-dir
; extension_dir = "./"
; On windows:
extension_dir = "ext"

; en op een andere plek
extension=php_pdo_odbc.dll
~~~

Het kan zijn dat de vorige regels wel reeds aanwezig waren in je php.ini, maar dan met een ; ervoor. Verwijder in dit geval de ; (met ; wordt aangegeven dat het NIET gebruikt wordt).
Als de regels niet bestonden zet de regels er dan in op een plek waar ook andere extensies zijn aangezet (extension=...).

Nu ben je klaar om de connectie met php op te gaan zetten naar de lokale mssql database.

### 20.2.2 Een aparte connectieodbc.php script aanmaken

Maak een aparte connectieodbc.php aan en zet daarin de volgende code:
~~~php
//vooraf eerst een DSN aanmaken in ODBC data-sources applicatie
//en php_pdo_odbc.dll als extension toevoegen aan php.ini
try {
        $pdo = new PDO("odbc:phpmssql");
}
catch (PDOException $e)
{
        echo $e->getMessage();
}
echo "connectie naar lokale mssql database is gelukt";
~~~

##20.2 Opdracht 196 Lokale connectie

Volg alle bovenstaande stappen en test je lokale connectie. Krijg je de melding "connectie naar lokale mssql database is gelukt"?
Laat dit zien aan de docent.



