## Opdracht 260 DOM en CSS aanpassingen!

`` Opleveren: Plaats al je gemaakte bestanden (.js, .html ) in een een rar met naam OPDRACHT260.rar en upload deze in je portfolio. Laat daarna de opdracht zien aan de docent om deze af te tekenen. Onthoud bij het uploaden dat we inmiddels in Periode 2 zitten.``

> Tip: Pak de presentaties erbij van de afgelopen week 5 en 6!

> Download het template bestand <a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.16%20JAV%5D%20Javascript/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2002/Productie/03.%20Scripts/Opdracht260.zip">hier</a>.

### Een introductie in de opleiding "Applicatie Ontwikkelaar"

**Opdracht**

Op de aangeleverde website gaan we via Javascript en jQuery teksten en wat CSS updaten. Het is dus de bedoeling dat na een klik op de button een aantal teksten en CSS aangepast gaan worden. 
Deze website is overigens door iemand anders gemaakt, dus hij is niet zoals jij hem gewend bent. Hier moet je later ook mee leren omgaan!

### Deel 1: Openen en uitpakken website
1. Download de template website <a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.16%20JAV%5D%20Javascript/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2002/Productie/03.%20Scripts/Opdracht260.zip" target="_blank">hier</a>.
2. Pak de template website uit
3. Open deze in WebMatrix via de File -> Open -> Open as Folder optie

### Deel 2: Website aanpassen
Laat de onderstaande dingen gebeuren via jQuery zodra er op de button "Verander de pagina!" geklikt wordt (zie onderstaande afbeelding)

1. Verander de eerste titel in 'Opleiding applicatieontwikkelaar'
2. Verander de tweede titel in 'Waar kan ik werken?'
3. Voeg een extra paragraaf toe na de alinea met 'Als applicatieontwikkelaar...' met de tekst: 'Ook de overheid is vaak een goede werkgever. Secundaire arbeidsvoorwaarden zijn meestal goed.'
4. Maak van 'Praesent sed est' een h3 element. met de tekst 'Hoe ziet de opleiding eruit?'
5. Voeg voor de eerste paragraaf na 'Hoe ziet de opleiding eruit' een nieuwe paragraaf toe met de tekst: 'De overstap die je maakt van vmbo-T of Have is rdelijk groot. Er wordt van je verwacht dat je zelfstandig te werk gaat en gaat het er minder schools aan toe dan je gewend was.'
6. Verander van iedere h2 element de tekstkleur in rood
7. Voeg in je styling toe: ```.zwartopwit { 
	background: #fff;
	color: #000;
}
```
en voeg deze klasse toe met jQuery aan alle elementen met id="kerntaken"
8. Verander de achtergrondkleur van blauw naar een andere  kleur, en verander ook de kleur van de tekst, zodat alle tekst wel goed leesbaar blijft
9. Open de site in je browser en klik op de button "Verander de pagina!"


*De teksten moeten veranderen zodra er op de button (in rood) geklikt is!*
![Voorbeeld](https://raw.githubusercontent.com/ictacademiekw1c/opdrachten-repository/master/javascript/p2/productie/Afbeeldingen/opdracht260.png)
  

---
## Opdracht 261 jQuery CSS, onClick en append, prepend etc

`` Opleveren: Plaats al je gemaakte bestanden (.js, .html ) in een een rar met naam OPDRACHT261.rar en upload deze in je portfolio. Laat daarna de opdracht zien aan de docent om deze af te tekenen. Onthoud bij het uploaden dat we inmiddels in Periode 2 zitten.``

### Bewegende elementen, nieuwe elementen en elementen verwijderen

> Tip: Pak de presentaties erbij van de afgelopen week 5 en 6!

> Download het template bestand <a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.16%20JAV%5D%20Javascript/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2002/Productie/03.%20Scripts/Opdracht261.zip">hier</a>.

**Opdracht**

We gaan een website maken waarop de gebruiken kan spelen met DIV blokken. Hij kan nieuwe blokken plaatsen (zwart of rood) en hij kan het laatst geplaatste blok ook weer laten verwijderen.
Daarnaast kan de bezoeker de blokken "besturen"  door allemaal tegelijk naar links, rechts, boven of onder te laten bewegen! Jouw opdracht is het, om het de gegeven template zo uit te bouwen dat de bezoeker het plaatje wat helemaal onderaan deze opdracht staat kan namaken!

Dit gaan we allemaal doen door middel van jQuery, dus pak de presentaties erbij voor voorbeelden!

### Deel 1: Openen en uitpakken website
1. Download de template website <a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.16%20JAV%5D%20Javascript/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2002/Productie/03.%20Scripts/Opdracht261.zip" target="_blank">hier</a>.
2. Pak de template website uit
3. Open deze in WebMatrix via de File -> Open -> Open as Folder optie
4. Voeg jQuery en een extern JS bestand toe!
5. Zet alle CSS code de je kunt vinden op deze pagina over naar een extern CSS bestand en lees deze CSS even door, zodat je ongeveer weet wat er aan styling is
6. Open de website om te kijken of hij eruit ziet zoals onderstaande afbeelding:

![Voorbeeld van de lege website](https://raw.githubusercontent.com/ictacademiekw1c/opdrachten-repository/master/javascript/p2/productie/Afbeeldingen/opdracht261_2.png)

#Deel 2: Toevoegen van blokken
Zorg ervoor dat de 3 meest rechste buttons doen wat er als commentaar in de HTML beschreven is (zie afbeelding hieronder). Je gaat dus de "Nieuwe rood blok", "Nieuw zwart blok" en "Verwijder eerste blok"
**Tip:** Pak de presentaties erbij om code voorbeelden terug te kijken!

*Lees goed het commentaar in de HTML!*
![De buttons die je moet programmeren](https://raw.githubusercontent.com/ictacademiekw1c/opdrachten-repository/master/javascript/p2/productie/Afbeeldingen/opdracht261_3.png)


#Deel 3: Besturing van de blokken
Zorg ervoor dat de blokken bestuurt kunnen worden door middel van de 4 buttons die hiervoor aangemaakt zijn. In de afbeelding hieronder zie je over welke buttons we het hebben!. Lees het commentaar goed in de HTML.
Om ALLE blokken tegelijk 15px naar boven te besturen heb je onderstaande jQuery code nodig:

```$("#wrapper .block").animate({top: "+=15px"});```

Om ALLE blokken tegelijk 15px naar beneden te sturen heb je onderstaande jQuery nodig:
```$(".block").animate({top: "-=15px"});```

Bedenk zelf de jQuery code om de blokken naar links en rechts te sturen!

*Lees goed het commentaar in de HTML!*
![De buttons die je moet programmeren](https://raw.githubusercontent.com/ictacademiekw1c/opdrachten-repository/master/javascript/p2/productie/Afbeeldingen/opdracht261_4.png)

# Deel 4: Nabouwen van een plaatje
Je bent klaar met de opdracht zodra je onderstaand plaatje kunt namaken (door de buttons te gebruiken uiteraard)!

![De buttons die je moet programmeren](https://raw.githubusercontent.com/ictacademiekw1c/opdrachten-repository/master/javascript/p2/productie/Afbeeldingen/opdracht261.png)

