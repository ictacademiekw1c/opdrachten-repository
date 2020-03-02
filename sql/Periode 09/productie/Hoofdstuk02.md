#### [kleurcode]rgba(85, 39, 176,1)

# Hoofdstuk 2 NoSQL Databases

## 2.1 NoSQL Databases

### KlasseOpdracht Kennis/voorkennis

__Vragen?__

    - Waarom heb ik uberhaupt een database nodig als ik een applicatie bouw?
    - Wat zijn de verschillen tussen een SQL database en een NoSQL database? 
    - Wat is beter/slechter?
    - Bestaan er in de toekomst nog steeds SQL databases? 
    - Welke soorten NoSQL Databases zijn er? 
    - Waarom NoSQL, we hebben toch al SQL? 
    - Welke NoSQL databases zijn er naast mongodb?

### Informatie

<a href="https://www.mongodb.com/nosql-inline" target="_new">Over NoSQL op mongodb.com</a>

## 2.2 MongoDB

### Hoe/waar wordt de data opgeslagen in een MongoDB database?

__Cloud__
<a href="https://www.mongodb.com/cloud/atlas" target="_new">Mongodb database server in the cloud (Atlas)</a>

__Lokaal__
<a href="https://www.mongodb.com/download-center/compass">Mongodb Compass, lokale database server</a>

## 2.3 Informatie

<a href="https://www.c-sharpcorner.com/article/getting-started-with-mongodb-mongodb-with-c-sharp/" target="_new">Mongodb client met C#</a>

<a href="https://gist.github.com/saebuabu/9a20ab663af442b85898b445e0ab687a" target="_new">Voorbeeld code c# connectie in een gist op github inclusief query op mongodb database</a>

<a href="https://www.w3schools.com/nodejs/nodejs_mongodb.asp" target="_new">MongoDB client met nodejs</a>


## 2.4 Inleveropdracht hoofdstuk 2 - Mongodb

- Beschrijf de document layout in BSON/mongodb formaat van je 5 meest favoriete films (titel, lengte, releasedatum, aantal nominaties, aantal oscars, kosten, omzet) uit de movies database, waarbij ook de acteurs, hun rollen, de regisseur, de studio, genre en land wordt meegenomen. Maak hiervan een Word document.
- Zet ook de antwoorden van de klasseopdracht/vragen hierboven in dit document.

__Of__ (wil je liever iets programmeren)

Maak een c# console applicatie waarin je een film (connectie/collection/document als in de bovenstaande gist) kan zoeken op basis van een deel van de titel. Indien gevonden toon je alle gegevens van de gevonden film(s). 
Hierbij de <a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.26%20SQL%5D%20SQL%20%20Databases/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/04.%20Aanvullend/moviesmongo.PNG" target="_new">document-layout</a> van dit document (movies).

Lever dit in in de inleveropdracht van hoofdstuk 2.