## Opdracht 250 jQuery rooster

`` Opleveren: Plaats al je gemaakte bestanden (.js, .html ) in een een rar met naam OPDRACHT250.rar en upload deze in je portfolio. Laat daarna de opdracht zien aan de docent om deze af te tekenen. Onthoud bij het uploaden dat we inmiddels in Periode 2 zitten.``

### Een website voor je rooster voor maandag en dinsdag

>> Download het template bestand <a href="">hier</a>.

**Opdracht**

We gaan een website bouwen, waarin (via jQuery) je rooster getoond ingetoond wordt voor de maandag en de dinsdag. Via een button kun je kiezen welke dag je te zien krijgt. Gelukkig voor jullie krijg je al de HTML aangeleverd van een leeg rooster. De Javascript en jQuery om dit rooster daarna te vullen mogen jullie zelf schrijven!

**Beoordelingscriteria**
1. Je hebt een extern JavaScript bestand gebruikt
2. Je hebt de jQuery library ingeladen
3. Zodra je de pagina opent, zie je een leeg rooster. Pas na het klikken op een van de buttons, krijg je de informatie te zien
3. De informatie over je rooster wordt via Javascript / jQuery inladen in de HTML
4. Je hebt minimaal de jQuery functie *.html()* gebruikt en *fadeIn()*, *fadeOut()*





---

## Opdracht 251 jQuery selectoren

`` Opleveren: Plaats al je gemaakte bestanden (.js, .html ) in een een rar met naam OPDRACHT251.rar en upload deze in je portfolio. Laat daarna de opdracht zien aan de docent om deze af te tekenen. Onthoud bij het uploaden dat we inmiddels in Periode 2 zitten.``

### Een katten fansite pimpen met jQuery

**Opdracht**

Onze buurman "Henk" heeft een katten website. Hij heeft aan jou gevraagd om deze wat te pimpen door gebruik te maken van jQuery. 
We gaan dit doen door wat dingen toe te voegen aan de HTML en zelf de JS code schrijven, zodat we allerlei verschillende selectoren kunnen uitproberen! De bedoeling is dus dat we de aangegeven effecten te zien krijgen zodra een gebruiker de website opent

>> Download de website van buurman Henk <a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.16%20JAV%5D%20Javascript/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2002/Productie/03.%20Scripts/Opdracht241.zip" target="_blank">hier</a>.

### Deel 1: Opzetten HTML & CSS
1. Download de bovenstaande website en pak deze uit. Open deze daarna in WebMatrix via de File -> Open -> Open as Folder. Zie onderstaande afbeelding.
2. Voeg de jQuery library toe
3. Koppel een extern JS bestand
4. Voeg een extern CSS bestand toe en laat deze de volgende dingen doen
	- Verberg alle elementen (behalve de &lt;button&gt;) via *display: none*
5. Klaar? Ga verder met deel 2


### Deel 2: Effecten bij openen van website
Hieronder zie je een tabel van de effecten die we graag op bepaalde elementen willen zien. 
Zorg ervoor dat via de onderstaande gegeven selectoren de jQuery effecten uitgevoerd worden. Je moet dus soms iets in de HTML aanpassen of toevoegen en daarna de benodigde Javascript zelf maken!.

<table><tr>
<th>**Element**</th>
<th>**Selector**</th>
<th>**jQuery functie**</th>
<th>**Opmerking**</th>
</tr>
<tr>
<td>H1 titel</td>
<td>*.welcome*</td>
<td>*fadeIn()*</td>
<td>Deze hebben we alvast in de HTML toegevoegd voor je!</td>
</tr>

<tr>
<td>H2 titel</td>
<td>*#subTitle*</td>
<td>*.slideToggle(4000)*</td>
<td></td>
</tr>

<tr>
<td>P paragraaf</td>
<td>*.paragraph1*</td>
<td>*.slideToggle()*</td>
<td></td>
</tr>

<tr>
<td>Alle IMG elementen</td>
<td>Zelf bedenken!</td>
<td>*.fadeIn(4000)*</td>
</tr>

</table>
<br><br>

### Deel 3: Button
1. Zorg ervoor dat wanneer iemand op de button klikt, de H3 en OL lijst ingefade komen. Maak hierbij gebruik van:
	- onclick event
	- Tip: Maak een functie aan die de *fadeIn()*'s doet!
	- Tip: Kijk goed welke elementen je met de CSS verborgen hebt! Wellicht loop je hier tegen problemen aan
2. Klaar!

<br>
<br>
<br>
*Zie hier hoe je een bestand opent binnen WebMatrix, zodat je deze "Launch in browser" kunt doen*
![Hoe een bestand te openen in webmatrix, zodat deze te openen is](https://raw.githubusercontent.com/ictacademiekw1c/opdrachten-repository/master/javascript/p2/productie/Afbeeldingen/Opdracht241_1.png)