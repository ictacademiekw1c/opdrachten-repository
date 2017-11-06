#### [setSubMenuHeader] Opdrachten
# Hoofdstuk 3

## Opdracht 310 document.getElementById()

`` Opleveren: Plaats al je gemaakte bestanden (.js, .html ) in een een rar met naam OPDRACHT310.rar en upload deze in je portfolio. Laat daarna de opdracht zien aan de docent om deze af te tekenen. ``

### document.getElementById()

>> **Tip:** Je kunt voortaan de presentaties de we gegeven hebben via N@tschool terug kijken. Klik op het mapje "Presentaties" en daarna het weeknummer. De presentaties komen online na het einde van iedere week.


>> In deze opdracht ga je een verhaal bedenken waar de gebruiker zelf bepaalde onderdelen (zoals namen, plaatsen, etc) gaat invoeren. Het verhaal mag je volledig zelf bedenken (gebruik je creativeit). Ook mag je het geheel uitbreidden met bv *confirm()*, etc. Je bent hier vrij in, maar je moet wel aan de minimaal gestelde eisen voldoen!

1. Download en unzip het bestand <a href="https://elo.kw1c.nl/CMS/_STUDYROUTE_FOLDERS/33/25187 AO Leerjaar 1 Periode 1/21745/[Bo16 JAV] Javascript [AO o 01]/734D14CA-39E9-44B1-8C5D-9B57DADF6F85/422bf47f/Opdracht310.zip" target="_blank">Opdracht310.zip</a>
2. Zorg ervoor dat in Script.js de naam en minimaal 4 andere vragen stelt (via een *prompt()*) aan de gebruiker
3. Bedank de gebruiker persoonlijk (toon zijn naam) via een *alert()*
4. Zorg ervoor dat je verhaal daarna getoond wordt aan de gebruiker. Je kunt hiervoor het P element met de ID "storyline" vullen. Doe dit via getElementById().innerHTML. Zie de presentaties op N@tschool voor meer informatie hierover.
5. Verander (via JavaScript uiteraard) de src van het img element met ID "image1" naar: http://placekitten.com/g/600/650. Check of je de kat te zien krijgt! Zie de presentaties van Week 6, les 1 voor meer info (Slide #6)
6. Zorg ervoor dat in de Console de datum van vandaag en jouw komen te staan.

--- 

## Opdracht 320 Datatypes

`` Opleveren: Werk de opdracht uit in een Word bestand genaamd opdracht320.docx.
Comprimeer het bestand naar opdracht320.rar en upload het naar je portfolio.``

### Datatypes

Vul onderstaande tabel in door onderstaande literals of expressies toe te kennen aan een variabele.
De vraag voor iedere literal/expressie (per rij) is welke datatype het uiteindelijk oplevert. 

Onze tip is om de code daadwerkelijk uit te voeren in een apart .html bestand of direct in de console van de Inspector.

** Voorbeeldexpressie: **
```javascript
var variable001 = 'javascript';

// Manier 1: via console.log()
console.log(variabele001); //in je console zie je nu ‘javascript’ en kun je concluderen dat het een string is

//Manier 2: met typeof
console.log(typeof variable001);
 
```
Voor dit voorbeeld zou je dus in opdracht3320.docx in je tabel noteren: 
<table>
	<tr>
		<th>**Expressie/literal**</th>
		<th>**Datatype van de uitkomst**</th>
	</tr>
	<tr>
		<td>'javascript'</td>
		<td>string</td>
	</tr>
</table>
		
** Geef van de volgende expressies / literals de datatypes op: **
<table>
	<th>** Wat is het datatype van de volgende expressies/literals ?**
	<tr><td>'javascript'</td></tr>
	<tr><td>1 + 4</td></tr>
	<tr><td>20.3</td></tr>
	<tr><td>2 * 3</td></tr>
	<tr><td>4 + '8'</td></tr>
	<tr><td>2 * (4 + '8')</td></tr>
	<tr><td>'Tieske' + ' ' + 'Verbeek' </td></tr>
	<tr><td>false</td></tr>
	<tr><td>true</td></tr>
	<tr><td>undefined</td></tr>
	<tr><td>'abu'</td></tr>
	<tr><td>89 + 'netherlands'</td></tr>
	<tr><td>'20' * 1</td></tr>
	<tr><td>999.22</td></tr>
</table>
** Mogelijke datatypes: **
<table>
	<tr>
		<td>**string**</td>
		<td>**number**</td>
		<td>**boolean**</td>
		<td>**NaN / undefined**</td>
		<td>**Ongeldig (levert syntaxfout op)**</td>
	</tr>
</table>

---

## Opdracht 330 TRUE or FALSE

### TRUE or FALSE

`` Opleveren: Werk de opdracht uit in een nieuw bestand genaamd opdracht3330.rar
Comprimeer de bestanden naar opdracht330.rar en upload het naar je portfolio.``

Bepaal de uiteindelijke waarde van de onderstaande condities in de tabel.
Ga uit van de volgende declaraties en initialisaties:

```javascript
var a=20, b= 9, c=1, d=null;

var dag1 = ‘maandag’;
var dag2 = ‘dinsdag’;
var dag3 = ‘Dinsdag’;

var score = 100;
```

** Voer daarna de volgende condities uit en bepaal of deze TRUE of FALSE zijn ** 

<table>
	<tr>
		<th>**TRUE or FALSE**</th>
	</tr>
	<tr>
		<td>score === 100</td>
		<td></td>
	</tr>
	<tr>
		<td>score !==100</td>
		<td></td>
	</tr>
	<tr>
		<td>score < 20 || score >50 </td>
		<td></td>
	</tr>
	<tr>
		<td>score > 0 && score > 99 </td>
		<td></td>
	</tr>
	<tr>
		<td>score < 30 || score > 100 || 1==1 </td>
		<td></td>
	</tr>
	<tr>
		<td>a === 20 && b<8 && c<3 </td>
		<td></td>
	</tr>
	<tr>
		<td>a === 20 && b>8 || c<3 </td>
		<td></td>
	</tr>
	<tr>
		<td>a == d </td>
		<td></td>
	</tr>
	<tr>
		<td>dag1 != dag2</td>
		<td></td>
	</tr>
	<tr>
		<td>dag3 == dag2</td>
		<td></td>
	</tr>	
</table>

--- 

## Opdracht 340 parseInt() en isNan

`` Opleveren: Werk de opdracht uit in een nieuw bestand genaamd opdracht340.rar.
Comprimeer de bestanden naar opdracht340.rar en upload het naar je portfolio. Laat het ook aftekenen door de docent``

### Maak een rekenmachine met parseInt(), isNan en parseFloat()

We gaan in deze opdracht een rekenmachine maken die 2 getallen kan vermenigvuldigen met elkaar. De getallen zullen ingevoerd worden door de gebruiker.
De gebruiker krijgt via HTML zijn ingevoerde getallen te zien en de uitkomst van 

1. Download het bestand <a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.16%20JAV%5D%20Javascript/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2001/Productie/03.%20Scripts/Huiswerk/Opdracht340.zip">Opdrachr340.zip</a> en pak deze uit.
2. Lees en maak de 7 opdrachten zoals beschreven in Script.js
3. Check of je rekenmachine aan de onderstaande eisen voldoet
	- Je gebruikt parseInt()
	- Je gebruikt isNan om te controleren of de invoer van de gebruiker daadwerkelijk een getal is
	- HTML elementen "getal1", "getal2" en "uitkomst" worden via document.getElementById() gevuld


>> Kom je er niet uit? Lees hieronder meer
>> parseInt() <a href="http://www.w3schools.com/jsref/jsref_parseint.asp" target="_blank">Lees meer</a><br>
>> isNan() <a href="http://www.w3schools.com/jsref/jsref_isnan.asp" target="_blank">Lees meer</a><br>
>> parseFloat() <a href="http://www.w3schools.com/jsref/jsref_parsefloat.asp"target="_blank">Lees meer</a>

--- 

## Opdracht 350 Zoeken in Strings

`` Opleveren: Werk de opdracht uit in een nieuw bestand genaamd opdracht350.rar.
Comprimeer de bestanden naar opdracht350.rar en upload het naar je portfolio. Laat het ook aftekenen door de docent``

### Zoeken in Strings

In deze opdracht gaan we het een en het ander met een zin en zoekwoorden doen. Dit zal waarschijnlijk een wat langer JavaScript bestanden worden dan wat je gewend bent.
Je gaat veel met IF's werken, dus maak je niet druk als je denkt dat het er teveel zijn.

1. Maak een nieuw leeg .html bestand aan en koppel hier een extern Script.js bestand aan
2. Declareer in Script.js de onder 3 variabelen. Geef zoekwoord1 de waarde "KW1C", de overige mag je zelf een waarde geven.
	- zoekwoord1 (waarde 'KW1C')
	- zoekwoord2 (zelf waarde bedenken)
	- zoekwoord3 (zelf waarde bedenken)
3. Vraag via een *prompt()* aan de gebruiker om een zin in te voeren. Sla deze zin op in een variabele (variabelenaam mag je zelf verzinnen).
4. Check 3 keer via *if* statements, ism *indexOf()* of de zoekwoorden in de zin zitten. 
	- Zit het woord er niet? Alert de tekst 'Helaas. Het woord *zoekwoord* zit niet in de zin' (vervang *zoekwoord* uiteraard door het zoekwoord) 
	- Zit het woord er wel in? Alert de tekst 'Gevonden! Het woord *zoekwoord* zit in de zin.' (vervang *zoekwoord* uiteraard door het zoekwoord)
5. Doe 	nogmaals hetzelfde, maar gebruik overal *lastIndexOf()* in plaats van *indexOf()*
6. Gebruik hierna *substr()*  om de eerste 10 karakters van de zin te tonen via *alert()*
7. *alert()* daarna de zin volledig in hoofdletters via *toUpperCase()*
8. *alert()* daarna de zin volledig in lage letters via *toLowerCase()*
9. Vervang in de zin de 3 zoekwoorden door onderstaande waardes. Gebruik *replace()* hiervoor. *alert()* daarna de aangepaste zin
	- Vervang zoekwoord1 door "Koning Willem 1 College"
	- Vervang zoekwoord2 door "JavaScript"
	- Vervang zoekwoord3 door "harambe"
10. Maak een P tag aan de de HTML met id "zin". Gebruik document.*getElementById()* om de zin te tonen in deze P tag. Let op: vergeet window*.onload()* niet!
11. console.*log()* je naam en de datum van vandaag
12. Klaar! Lever de opdracht in via de in rood bovenstaande instructies. Vergeet niet de opdracht af te tekenen bij de docent!

>> Kom je er niet uit? Lees hieronder meer
>> indexOf()() <a href="http://www.w3schools.com/jsref/jsref_indexof.asp" target="_blank">Lees meer</a><br>
>> lastIndexOf()() <a href="http://www.w3schools.com/jsref/jsref_lastindexof.asp" target="_blank">Lees meer</a><br>
>> toUpperCase() <a href="http://www.w3schools.com/jsref/jsref_touppercase.asp"target="_blank">Lees meer</a><br>
>> toLowerCase() <a href="http://www.w3schools.com/jsref/jsref_tolowercase.asp"target="_blank">Lees meer</a><br>
>> replace() <a href="http://www.w3schools.com/jsref/jsref_replace.asp"target="_blank">Lees meer</a>