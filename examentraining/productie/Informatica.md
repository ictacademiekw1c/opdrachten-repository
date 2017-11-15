# Informatica

## 1. OOP concepten

__Examenstof__:
- Klassen en overerving
- Properties en attributen (getters en setters)
- Zichtbaarheid (public, protected en private)
- Overloading
- Constructoren en destructoren

- Static klassen, methoden en attributen

- Composities en generalisaties

__Geen examenstof:__
- Abstracts, Interfaces, Structs
- Stereotypen
- Packages
- Meervoudige overerving
- Aggregaties
- Dependencies

## 2. Naming conventions

__Pascal case en camel case__

__Conventies__:
-   Bij voorkeur engelstalig, voor de duidelijkheid soms beter Nederlands
-   Voor de classes enkelvoud, meervoud als het een verzameling is...
-   Gebruik geen keywords als naam
-   Kort namen voor klassen, tabellen, methoden en attributen nooit af
-   Neem de naam van een klasse of tabel niet op in de naam van de attributen van de klasse of tabel
-   Geef een methode die true/false retourneert een naam die de positieve uitkomst beschrijft
```voorbeeld: IsValidGeboortedatum```
-   Gebruik geen underscores

__Attributen__:

~~~c#
[zichtbaarheid] naam : type [=default]
~~~

__Methoden__:
~~~c#
werkwoord + zelfstandig naamwoord
~~~
bijvoorbeeld: SelectForActivityRule

__Niet behandelen:__
- Stereotypen

## 3. n-tier concept software architectuur

- Business laag

- Interactie laag

- Data laag


## 4. Opdrachten ##


### Opdracht 1 - NY Marathon ###


In leerjaar 1 heb je een analyse uitgewerkt van de [NY Marathon](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.01%20ANA%5D%20Analyseren/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2004/Productie/02.%20Opdrachten/1b_NYCMarathon_VN_21aug2012.docx). In deze opdracht moet je deze analyse gaan uitwerken in een C# applicatie in 3-Tier.

- Taak 1. Maak het NY Marathon analyse model af / compleet.

- Taak 2. Vertaal de modellen naar UML klasse diagrammen.
  * Hoofddeelverzamelingen uit je model komen overeen met de klasse diagrammen die je hebt uitgewerkt.

- Taak 3. Werk de NY Marathon in een 3-tier C# applicatie

  * De presentatie laag is geimplementeerd in Windows Forms.
  * De datalaag is geimplemeerd met behulp van een SQL database.
  * Je klasse diagrammen zijn omgezet in Klasses in je C# applicatie

### Download
[NY Marathon analyse opdracht](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.01%20ANA%5D%20Analyseren/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2004/Productie/02.%20Opdrachten/1b_NYCMarathon_VN_21aug2012.docx)

### Onderwerpen
- Analyse omzetten naar code
- 3- Tier
- SQL database 
- Windows Forms

### Benodigde bestanden
- [3Uniciteitenregel_VoordoenNadoen_22aug012.xps](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.01%20ANA%5D%20Analyseren/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2004/Productie/01.%20Reader/3Uniciteitenregel_VoordoenNadoen_14april2011.xps)
- [4Deelverzamelingsregel_VoordoenNadoen_22aug2012.xps](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.01%20ANA%5D%20Analyseren/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2004/Productie/01.%20Reader/4Deelverzamelingsregel_VoordoenNadoen_15april2011.xps)
- [5Gelijkheidsregel_VoordoenNadoen_23aug2012.xps](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.01%20ANA%5D%20Analyseren/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2004/Productie/01.%20Reader/5Gelijkheidsregel_VoordoenNadoen_19jan2012.xps)
