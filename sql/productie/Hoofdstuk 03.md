#### [kleurcode]rgba(156,39,176,1)

# Hoofdstuk 3

---
## Opdracht 3.1
---

### Download
<a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.26%20SQL%5D%20SQL%20%20Databases/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2003/Productie/02.%20Opdrachten/Hoofdstuk03/Opdracht%203.1.pdf" target="_blank">Download opdracht 3.1</a>

### Onderwerpen
*   Module header
*   Commentaar 
*   Syntax SQL

### Benodigde bestanden
*   <a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.26%20SQL%5D%20SQL%20%20Databases/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2003/Productie/02.%20Opdrachten/Hoofdstuk03/Resources/opdracht%203.1.sql" target="_blank">Opdracht3.1.sql </a> 

### Help
*   Module header

```sql
/*
     Opdracht:       opdrachtnaam
     Auteur:         naam van de maker
     Aanmaakdatum:   startdatum + tijd
     Bestandsnaam:   bestandsnaam
*/
```

*   <a href="http://www.w3schools.com/sql/sql_comments.asp" target="_blank">Commentaar </a> 

```sql
-- Deze regel staat in commentaar!

/*  
     Deze
     regels
     staan
     ook
     in
     commentaar!
*/
```

---
## Opdracht 3.2
---

### Download
<a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.26%20SQL%5D%20SQL%20%20Databases/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2003/Productie/02.%20Opdrachten/Hoofdstuk03/Opdracht%203.2.pdf" target="_blank">Download opdracht 3.2</a>

### Onderwerpen
*   Database maken
*   Database verwijderen
*   Tabel maken
*   Tabel verwijderen
*   Datatypen

### Benodigde bestanden
*   Je hebt voor deze opdracht geen bestanden nodig.

### Help
*   <a href="http://www.w3schools.com/sql/sql_create_db.asp" target="_blank">Database maken </a> 
*   <a href="http://www.w3schools.com/sql/sql_drop.asp" target="_blank">Database verwijderen </a> 
*   <a href="http://www.w3schools.com/sql/sql_create_table.asp" target="_blank">Tabel maken </a> 
*   <a href="http://www.w3schools.com/sql/sql_drop.asp" target="_blank">Tabel verwijderen </a> 
*   <a href="https://www.techonthenet.com/sql_server/datatypes.php" target="_blank">Datatypen </a> 
*   Voorbeeldcode

```sql
-- Vanuit master heb je de juiste rechten om een nieuwe database aan te maken
USE MASTER;

-- Maak database aan
CREATE DATABASE <Databasenaam>;
GO

-- Verwijder database 
DROP DATABASE <Databasenaam>;

-- Gebruik database 
USE <databasenaam>;

-- Maak tabel aan
CREATE TABLE <tabelnaam>
(
    <kolumnaam>     <datatype>,
    <kolumnaam>     <datatype>,
    <kolumnaam>     <datatype>,
    <kolumnaam>     <datatype>
);

-- Verwijder tabel
DROP TABLE <tabelnaam>;

```