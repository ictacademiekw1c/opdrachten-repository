## Opdracht 240 Een website pimpen met jQuery

`` Opleveren: Plaats al je gemaakte bestanden (.js, .html ) in een een rar met naam OPDRACHT240.rar en upload deze in je portfolio. Laat daarna de opdracht zien aan de docent om deze af te tekenen. Onthoud bij het uploaden dat we inmiddels in Periode 2 zitten.``

### Een website pimpen met jQuery

>> Heb je opdracht 6.3 niet gemaakt? Geen probleem, download <a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.16%20JAV%5D%20Javascript/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2002/Productie/03.%20Scripts/Opdracht240.zip" target="_blank">hier</a> de uitwerking.

**Opdracht**

We gaan jullie uitwerking van de HTML/CSS opdracht 6.3 een beetje opleuken (het recept voor Albert Heijn). Dit gaan we doen door gebruik te maken van de kracht van jQuery!
Zo gaan we de grote afbeelding laten in en uit sliden, de H1 en H2 komt infaden en ook doen we iets grappigs met de P elementen. Je eerste stappen in de wereld van jQuery.

### Deel 1: Voorbereiding
1. Kopieer / plak je uitwerking van opdracht 6.3 naar je Javascript huiswerk map. Open de opdracht in WebMatrix. Mocht je de opdracht niet gedaan hebben, dan kun <a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.16%20JAV%5D%20Javascript/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2002/Productie/03.%20Scripts/Opdracht240.zip" target="_blank">hier</a> de uitwerking downloaden.
2. Koppel hier jQuery aan (zoals is uitgelegd in de sheets)
3. Koppel hier een leeg extern JS (bv Script.js) bestand aan
4. Zorg ervoor dat (via CSS) alle H1, H2, IMG en P elementen de style *display: none* krijgen
5. Check of alle H1, H2, IMG en P elementen daadwerkelijk verborgen zijn op je webpagina! We gaan dus al deze elementen via jQuery stuk voor stuk weer tonen
6. Ga door met onderstaand punt 2

## Deel 2: Het toevoegen van jQuery effecten bij pagina laden
1. Neem de ``$(document).ready( function() {   }`` code over van de presentaties (in het lege JS bestand)
2. Nu is het tijd om enkele effecten toe te voegen! Zet onderstaande code tussen de ``$(document).ready( function () {})``` accolades (Zie presentaties voor voorbeeld) 
	- Fade alle H1 elementen in:
	```
	// Fade in van alle H1 elementen op de pagina
	$("h1").fadeIn();
	```
	- Fade alle H2 elementen in (effect duurt 5000 milliseconden):
	```
	// Fade in van alle H2 elementen op de pagina
	$("h2").fadeIn(5000);
	```
	- Fade alle P elementen in en daarna weer uit (effect duurt 2000 milliseconden per stuk)
	```
	// Fade in van alle P elementen op de pagina (2 seconden vertraging)
	$("p").fadeIn(2000);
	
	// Daarna fade out van alle P elementen op de pagina(ook 2 seconden vertraging)
	$("p").fadeOut(2000);
	```
3. Test je webpagina en geniet eventjes van de mooie effectjes! Je kan op deze manier op alle gewenste HTML objecten effecten loslaten
4. Ga door met onderstaande punten van Deel 3

### Deel 3: Het toevoegen van jQuery effecten bij een *event*
1. Maak een nieuwe functie aan genaamd *triggerEffect()*
2. Zet de volgende jQuery code in deze functie
	```
	// Voer slideToggle uit op alle img elementen op de pagina
	$("img").slideToggle();
	```
3. Maak een nieuw BUTTON element aan in de HTML en geef deze een *onclick* event die de functie *triggerEffect()* aanroept
4. Open de webpagina en klik enkele keren op deze button. Je zou een bepaald effect moeten kunnen zien
5. Gefeliciteerd! Je hebt jQquery effecten toegepast op je Albert Heijn gerecht!

>> Wil je meer weten over jQuery effecten? <a href="http://www.w3schools.com/jquery/jquery_ref_effects.asp" target="_blank">Klik hier voor voorbeelden</a>

**Beoordelingcriteria**
1. Je hebt de jQuery library ingeladen
2. Je laat de H1, H2 en P elementen infaden bij het openen van de pagina
3. Je maakt via een *onclick* event een image zichtbaar of juist onzichtbaar via *slideToggle()*
4. Er is voldoende en logisch commentaar geplaatst in de code
5. Je hebt je naam en de datum van maken naar de console gestuurd

---

## Opdracht 241 jQuery selectoren

`` Opleveren: Plaats al je gemaakte bestanden (.js, .html ) in een een rar met naam OPDRACHT241.rar en upload deze in je portfolio. Laat daarna de opdracht zien aan de docent om deze af te tekenen. Onthoud bij het uploaden dat we inmiddels in Periode 2 zitten.``

### Een katten fansite pimpen met jQuery

**Opdracht**

Onze buurman "Henk" heeft een katten website. Hij heeft aan jou gevraagd om deze wat te pimpen door gebruik te maken van jQuery. Dit doen wij natuurlijk maar al te graag!

>> De website van buurman Henk kun je <a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.16%20JAV%5D%20Javascript/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2002/Productie/03.%20Scripts/Opdracht241.zip" target="_blank">hier</a> vinden.

1. Download de bovenstaande website en pak deze uit. Open deze daarna in WebMatrix via de File -> Open -> Open as Folder. Zie onderstaande afbeelding.

2. De rest komt zsm!