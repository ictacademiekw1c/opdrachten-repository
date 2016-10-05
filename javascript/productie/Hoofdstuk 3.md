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

`` Opleveren: Werk de opdracht uit in een Word bestand genaamd opdracht311.docx.
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
Voor dit voorbeeld zou je dus in opdracht311.docx in je tabel noteren: 
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

`` Opleveren: Werk de opdracht uit in een nieuw bestand genaamd opdracht314.html.
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
		<th></th>
		<th>**TRUE of FALSE**</th>
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

## Opdracht 340 parseInt(), isNan en parseFloat()

`` Opleveren: Werk de opdracht uit in een nieuw bestand genaamd opdracht340.html.
Comprimeer de bestanden naar opdracht314.rar en upload het naar je portfolio.``