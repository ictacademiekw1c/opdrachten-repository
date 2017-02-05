#### [kleurcode]rgba(156,39,176,1)

# Hoofdstuk 3

---
## Opdracht 3.1
---

### Download
<a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.14%20HTM%5D%20HTMLCSS/Productie/02.%20Opdrachten/Hoofdstuk%203/Opdracht%203.1.pdf" target="_blank">Download opdracht 3.1</a>

### Onderwerpen
*   Module header
*   Commentaar 
*   Syntax SQL

### Benodigde bestanden
*   <a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.26%20SQL%5D%20SQL%20%20Databases/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2003/Productie/02.%20Opdrachten/Hoofdstuk03/Resources/opdracht%203.1.sql" target="_blank">Download opdracht3.1.sql </a> 

### Help
*   Module header
```sql
/*
~    Opdracht:       opdrachtnaam
~    Auteur:         naam van de maker
~    Aanmaakdatum:   startdatum + tijd
~    Bestandsnaam:   bestandsnaam
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
*   <a href="http://www.w3schools.com/sql/sql_comments.asp" target="_blank">Commentaar </a> 
```sql
-- Vanuit master heb je de juiste rechten om een nieuwe database aan te maken
USE MASTER;
GO

-- Maak database aan
CREATE DATABASE <Database naam>;

-- Verwijder database 
DROP DATABASE <Database naam>;

-- Gebruik database 
USE <database naam>;
GO

-- Maak tabel aan
CREATE TABLE <tabel naam>
(
~	<kolumnaam>     <datatype>,
~	<kolumnaam>     <datatype>,
~   <kolumnaam>     <datatype>,
~   <kolumnaam>     <datatype>
)
-- 


```