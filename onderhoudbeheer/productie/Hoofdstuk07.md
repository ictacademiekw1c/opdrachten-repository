# Hoofdstuk 7 De test pyramide

---
## 7.1
---

In het vorig hoofdstuk is er behandeld wat de verschillende testmethodieken zijn.
Hoe wordt er echter in de praktijk getest? Op een praktische manier kan het testen worden gezien als een pyramide.

<img src="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.06%20BEH%5D%20Onderhoud%20en%20beheer/Productie/04.%20Aanvullend/testPyramid.png" alt="test pyramide">

Hierin zijn de verschillende onderdelen te onderscheiden:

1. De UI tests. Dit is de test van de User Interface. Hierin testen we alle zichtbare schermen van een applicatie en alle mogelijke opties en scenario's die een gebruiker zou kunnen tegenkomen bij het gebruik.

2. De service tests of deze testen worden ook wel component testen genoemd of integratie testen. Hierin wordt getest of verschillende onderdelen van een applicatie nog steeds werken als ze zijn samengevoegd.

3. De Unit tests zijn testen op het laagste/kleinste niveau en test op functie/klasse methode niveau of de input van bepaalde waardes de gewenste output geven.

Hierbij valt op te merken dat:
- Hoe hoger in de pyramide de test meer tijd gaat kosten (langzamer)
- Op het laagste niveau in de pyramide wordt er geisoleerd getest
- Bovenaan de pyrmaide testen we de applicatie als geheel

## 7.2 Opdracht 7 test pyramide

In hoofdstuk 6 hebben we verschillende testmethodieken gezien. Plaats iedere testmethodiek op een plek in de pyramide. Het kan zijn dat een testmethodiek verschillende plaatsen in de pyramide zit. Licht dat toe.

In hoofdstuk 8 gaan we kijken naar de onderzijde van de pyramide. De unit test.


## Links

<a href="https://martinfowler.com/articles/practical-test-pyramid.html" target="_new">Martin Fowler over de test pyramide</a>