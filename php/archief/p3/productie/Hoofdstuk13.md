#### [kleurcode]rgba(234,67,54,1)

#  Hoofdstuk 13 PHPstorm + Github

## 13.0 PHPstorm en versiebeheer

Omdat webmatrix niet meer ondersteund gaat worden zijn we genoodzaakt om een andere editor/ontwikkelomgeving te gaan gebruiken.
De keuze is gevallen op PHPstorm omdat we het een editor is die je helpt om goede php-code te schrijven en je ondersteunt in het hele proces van ontwikkelen van een website of webapplicatie.

PHPstorm heeft ook een goede integratie met github. Github.com is een webportaal waarin programmeurs hun code kunnen hosten en beheren.
De versiebeheer techniek die er gebruikt wordt is GIT, welke in heel veel bedrijven tegenwoordig wordt gebruikt.

Redenen om versiebeheer te gebruiken zijn:
- Vergemakkelijkt samenwerken in een team van programmeurs
- Volledige historie van wijzigingen blijft beschikbaar
- Centrale backup van code
- Je kan altijd terug naar voorgaande versies

Redenen om github te gebruiken in de studieroute PHP:
- Kennismaking met versiebeheer
- Opleveren opdrachten via github
- Geen upload meer nodig naar n@tschool

Volg alle stappen in de volgende handleiding:
[Handleiding PHPStorm](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.22%20PHP%5D%20PHP/Productie/01.%20Reader/PHP%20Handleiding%20PHPStorm%20GitHub.docx)

## 13.1 Opdracht 130 je eerste commit en oplevering

Zet een tabel op in opdracht130.php met alle hoofdstukken uit periode 1 en 2 met de behandelde onderwerpen.
<table><thead>
<tr>
<th>Hoofdstuk</th>
<th align="left">Onderwerpen</th>
</tr>
</thead><tbody>
<tr>
<td>1</td>
<td align="left">Variabelen en waarden</td>
</tr>
<tr>
<td>2</td>
<td align="left">Strings koppelen</td>
</tr>
<tr>
<td>3 t/m 12</td>
<td align="left"></td>
</tr>
</tbody></table>

Zodra je klaar bent met alle hoofdstukken lever je het op via github.
Hoe je dit doet in PHPstorm wordt door de leraar uitgelegd.

De docent laat ook zien hoe je je code op de c9 server kan laten zien.

## 13.2 Opdracht 131 herhaling formulier

Maak een formulier in opdracht131.php met de volgende velden: naam, klas, leerlingnummer, vak, cijfer en een submit knop.
Je kunt gebruik maken van de code die hieronder staat weergegeven. 
Maak vervolgens een nieuw script aan met de naam verzend.php. 

Zet als stap 1 in dit script:
var_dump($_GET);
Launch opdracht131.php en vul alle velden in en druk op de submit knop.

Wat is nu de URL in je adresbalk van je browser ?

Met de var_dump() functie kun je van een samengestelde variabele zien welke waardes er in een variabele zitten. Voorbeeld van een var_dump ziet er als volgt uit:
~~~php
array(6) { ["naam"]=> string(9) "Abu Saebu" 
		["Klas"]=> string(5) "IO1A4" 
		["leerlingnummer"]=> string(8) "36353535" 
		["vak"]=> string(3) "PHP" 
		["cijfer"]=> string(1) "9" 
		["verzend"]=> string(7) "verzend" 
	} 
~~~
Op het scherm zie je nu welke elementen er aanwezig zijn in de $_GET variabele. Je kan ieder element afzonderlijk nu printen door deze op de volgende manier te verwerken:
Voorbeeld voor het veld naam:
~~~php
$naam = $_GET['naam'];
echo $naam; 
~~~
De opdracht is nu: <br>
Print alle velden uit het formulier netjes op het scherm volgens de visuele weergave.

## 13.3 Formulier code
~~~php
<form method='get' action='verzend.php'>
	    <label>Naam: </label><input name='naam' type='text' value=''>
	    <label>Klas: </label><input name='klas' type='text' value=''>
	    <label>Nummer: </label><input name='leerlingnummer' type='text' value=''>
	    <label>Vak: </label><select name='vak'>
		    <option value='PHP'>PHP</option>
		    <option value='javascript'>Javascript</option>
		    <option value='ASP'>ASP</option>
		    <option value='SQL'>SQL</option>
	    </select>
	    <label>Cijfer: </label><input name='cijfer' type='number' value='5'>
	    <input type='submit' value='verzend' name='verzend'>
        </form>
~~~
## 13.4 Visuele weergave

![Visuele weergave 131](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/php/p3/images/opdracht131.jpg?raw=true)

## 13.5 Beoordelingscriteria

- Het html-formuilier heeft als method get
- Het script verzend.php gebruikt de variabele $_GET
- De waardes van de ingevulde velden worden opgehaald met $_GET[‘veld-naam’]
- Het script verzend.php toont een volledige html-pagina
- Het script verzend.php gebruikt /*  commentaar  */ om de code uit te leggen

