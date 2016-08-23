#### [setSubMenuHeader] Opdrachten
# Hoofdstuk 3

## Opdracht 311 Datatypes

`` Opleveren: Werk de opdracht uit in een Word bestand genaamd opdracht311.docx.
Comprimeer het bestand naar opdracht311.rar en upload het naar je portfolio.``

Vul onderstaande tabel in door onderstaande literals of expressies toe te kennen aan een variabele.
De vraag voor iedere literal/expressie (per rij) is welke datatype het uiteindelijk oplevert. 

Onze tip is om de code daadwerkelijk uit te voeren in een apart .html bestand of direct in de console van de Inspector (via de F12 toets).

** Voorbeeldexpressie: **
```javascript
var variable001 = 'javascript';
console.log(variabele001); //in je console zie je nu ‘javascript’ en kun je concluderen dat het een string is
//of met typeof
Console.log(typeof variable001); 
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
	<tr><td>'jos' + ' ' + 'Verbeek' </td></tr>
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

## Opdracht 312 Variabelenamen

`` Opleveren: Werk de opdracht uit in een Word bestand genaamd opdracht312.docx.
Comprimeer het bestand naar opdracht312.rar en upload het naar je portfolio.``

Zijn onderstaande variabelenamen geldig of niet geldig? Controleer het aan de hand van de regels die in de reader van dit hoofdstuk zijn beschreven.
Test de geldigheid van onderstaande variabelenamen via de console van de Inspector (via de F12 toets). Noteer daarna je bevindingen in opdracht312.rar.

Volg de stappen:
1. Declareer de variabele naam
2. Geef de variable een waarde (getal of integer);
3. Schrijf de waarde naar het console
4. Krijg je géén foutmelding, dan kun je de conclusie trekken dat de variabelenaam geldig is
5. Zet in het Word bestand of de variabele geldig is of ongeldig en vermeld ook de reden

** Voorbeeldcode **
```javascript
var Teller1;
Teller1 = 10;
```
** Voorbeeld uitwerking in je Word bestand: **
<table>
	<tr>
		<th>**Variabelenaam**</th>
		<th>**Geldige uitkomst? (Ja / Nee)**</th>
		<th>Beredenatie</th>
	</tr>
	<tr>
		<td>Teller1</td>
		<td>Ja</td>
		<td>Teller1 bevat slechts alfanummerieke karakters en bevat geen keywords</td>
	</tr>
</table>

## Opdracht 313 Operatoren

### Operatoren

`` Opleveren: Kopieëer ieder regel uit de onderstaande tabel over naar een nieuw HTML bestand (Opdracht313.html) en voeg na iedere regel een console.log(score) toe.
``

Kijk in het console van je browser wat er wordt geprint, en zet die waarde achter de regel in je code in commentaar.``
** Voorbeeld **
```javascript
var score = 0;
console.log(score); // 0 
```

<table>
	<tr>
		<th>** Operator ** </th>
		<th>** Waarde score? **</th>
	</tr>
	<tr>
		<td>var score = 0;</td>
		<td></td>
	</tr>
	<tr>
		<td>score = 100;</td>
		<td></td>
	</tr>
	<tr>
		<td>score = score - 10;</td>
		<td></td>
	</tr>
	<tr>
		<td>score = score * 10;</td>
		<td></td>
	</tr>
	<tr>
		<td>score++;</td>
		<td></td>
	</tr>
	<tr>
		<td>score++;</td>
		<td></td>
	</tr>
	<tr>
		<td>score += 5;</td>
		<td></td>
	</tr>
	<tr>
		<td>score -=10;</td>
		<td></td>
	</tr>
	<tr>
		<td>score--;</td>
		<td></td>
	</tr>
	<tr>
		<td>score = score + ' sok';</td>
		<td></td>
	</tr>
	<tr>
		<td>score = (parseInt(score) + 30) /10;</td>
		<td></td>
	</tr>
	<tr>
		<td>score /= 2;</td>
		<td></td>
	</tr>
	<tr>
		<td>var score;</td>
		<td></td>
	</tr>
	<tr>
		<td>score += 1;</td>
		<td></td>
	</tr>
	<tr>
		<td>score = score + y;</td>
		<td></td>
	</tr>
	<tr>
		<td>var y = score + 100;</td>
		<td></td>
	</tr>
	<tr>
		<td>score = (y > score);</td>
		<td></td>
	</tr>
	<tr>
		<td>score = !score;</td>
		<td></td>
	</tr>
</table>

** Let op: Het is belangrijk dat je alle bovenstaande codes in 1 HTML bestand plaatst. **

## Opdracht 314 TRUE or FALSE

### TRUE or FALSE

`` Opleveren: Werk de opdracht uit in een nieuw bestand genaamd opdracht314.html.
Comprimeer de bestanden naar opdracht314.rar en upload het naar je portfolio.``

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
		<th>** TRUE of FALSE</th>
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

## Opdracht 315 Built in / Standaard functies

### Built in / Standaard functies

`` Opleveren: Werk de opdracht uit in opdracht315.html
Comprimeer het bestand naar opdracht315.rar en upload het naar je portfolio.``

Ga uit van de volgende code en plaats dit in het body gedeelte van een html-document met de naam OPDRACHT315.html
		
	
```javascript
<script>

var tekst = ‘De Bossche burgemeester Ton Rombouts geneert zich voor de wijze waarop
toeschouwers Jozy Altidore hebben bejegend tijdens de wedstrijd van FC Den Bosch. Dat laat
hij weten in een persoonlijk brief aan de AZ-speler.’;

/*
Schrijf hier je code van de onderstaande opdrachten. Je moet de standaard functies gebruiken
uit de reader van hoofdstuk 3.
*/

<script>
```

Programmeer opdrachten en gebruik de standaard functies uit de reader: 
1. Bepaal de positie van de eerste . (punt) en de positie van de tweede . (punt) in de variabele tekst. Zet de waardes in
de variabelen pos1 en pos2. 

Gebruik bij de volgende 2 opdrachten de variabelen pos1 en pos2 uit opdracht 1 en gebruik hiervoor de functie substr() 

2. Zet de eerste zin uit de variabele tekst in een nieuwe variabele zin1.
3. Zet de tweede zin uit de variabele tekst in een nieuwe variabele zin2
4. Verwijder ‘Ton Rombouts’ uit zin1.
5. Vervang Bossche door BOSSCHE in zin1.
6. Vervang ‘Jozy Altidore’ door ‘de AZ-speler’ in zin 1.
7. Vervang ‘Dat’ in zin2 door ‘Het volgende’
8. Vervang ‘de AZ-speler’ door ‘de voetballer’ in zin1 en in zin2.
9. Print met document.write() eerst zin2 en vervolgens zin1; 

** Dit moet uiteindelijk het resultaat zijn: **
* Het volgende laat hij weten in een persoonlijke brief aan de voetballer. De BOSSCHE burgemeester geneert zich voor
de manier waarop toeschouwers de voetballer hebben bejegend tijdens de wedstrijd van FC Den Bosch. *

`` Opmerking: Gebruik alert() of console.log() om tussentijds te testen wat de waarde is van een variabele ``

## Opdracht 316 Arrays en Array Functies

### Arrays en Array Functies

`` Opleveren: Werk de opdracht uit in een nieuw bestand genaamd opdracht316.html.
Comprimeer beide bestanden naar opdracht316.rar en upload het naar je portfolio.``

Ga uit van de volgende code en plaats dit in het body gedeelte van een html-document.

```javascript
var leerlingen = [‘Mohammed’, ‘Tolga’, ‘Adem’,’Thomas’, ‘Jean’];

document.write(‘<p>De eerste leerling is <strong>’);

document.write(leerlingen[0] + ‘</strong></p>’);
/* schrijf na deze regel je code van opdracht 1 */
/* schrijf na deze regel je code van opdracht 2 */
/* schrijf na deze regel je code van opdracht 3 */
/* schrijf na deze regel je code van opdracht 4 */
/* schrijf na deze regel je code van opdracht 4 */
/* schrijf na deze regel je code van opdracht 5 */ 
```

Opdrachten:
1. Schrijf met document.write() op dezelfde manier als de eerste regel, met de array variabele leerlingen, de volgende
uitvoer:
De laatste leerling in de lijst is **Jean**.

2. Schrijf met document.write() op dezelfde manier als de eerste regel, met de array variabele leerlingen, de volgende
uitvoer:
De tweede leerling in de lijst is **Tolga**.

3. Schrijf met document.write() op dezelfde manier als de eerste regel, met de array variabele leerlingen, de volgende
uitvoer. Gebruik de property .length
De voorlaatste leerling in de lijst is **Thomas**.

4. Verwijder de laatste leerling uit de array met een array-functie. Schrijf met document.write() op dezelfde manier als de
eerste regel, met de array variabele leerlingen, de volgende uitvoer.
De laatste leerling is nu **Thomas**.

5. Voeg de leerlingen Nick en Mike toe aan de array leerlingen. Schrijf met document.write() op dezelfde manier als de
eerste regel, met de array variabele leerlingen, de volgende uitvoer.
De eerste leerling is nu **Nick**.