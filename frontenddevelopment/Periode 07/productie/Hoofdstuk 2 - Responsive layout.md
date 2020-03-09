#### [kleurcode]rgba(233,30,99,1)

# Hoofdstuk 2 - Responsive Layout en preprocessor css met LESS

---
## 2.1 Basispagina structuur
---

Voordat we beginnen met responsive layout moeten de basis principes voor een goede pagina structuur bekend zijn. Bekijk de volgende video's en oefen ermee als een bepaald onderdeel nog niet helemaal duidelijk voor je is.

- <a target="_blank" href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BK.07%20FrD%5D%20Keuzedeel%20%5BK0722%5D%20Frontend%20development/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2007/Productie/743192_01_01_XR30_12_viewport.mp4">Viewport</a>


- <a target="_blank" href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BK.07%20FrD%5D%20Keuzedeel%20%5BK0722%5D%20Frontend%20development/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2007/Productie/743192_01_02_XR30_required_CSS.mp4">Required css</a>

- <a target="_blank" href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BK.07%20FrD%5D%20Keuzedeel%20%5BK0722%5D%20Frontend%20development/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2007/Productie/743192_01_03_XR30_display_property.mp4">Display property</a>

- <a target="_blank" href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BK.07%20FrD%5D%20Keuzedeel%20%5BK0722%5D%20Frontend%20development/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2007/Productie/743192_01_04_XR30_positioning.mp4">Positioning</a>

- <a target="_blank" href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BK.07%20FrD%5D%20Keuzedeel%20%5BK0722%5D%20Frontend%20development/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2007/Productie/743192_01_05_XR30_floats.mp4">Floats</a>

- <a target="_blank" href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BK.07%20FrD%5D%20Keuzedeel%20%5BK0722%5D%20Frontend%20development/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2007/Productie/743192_01_06_XR30_units.mp4">Units (eenheden)</a>


Gebruik de <a target="_blank" href="https://elo.kw1c.nl/Pages/View.aspx?cp=%2FCMS%2FStudie%2F811%20ICT-Academie%2F811%20VakkenInhoud%2F%5BK.07%20FrD%5D%20Keuzedeel%20%5BK0722%5D%20Frontend%20development%2F25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar%2FPeriode%2007%2FProductie%2FEx_Files_Responsive_Layout">oefenbestanden</a> om met de bovenstaande basisprincipes te oefenen. 

---
## 2.2 Responsive Layout
---

- Waarom <a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BK.07%20FrD%5D%20Keuzedeel%20%5BK0722%5D%20Frontend%20development/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2007/Productie/743192_02_01_XR30_responsive_design.mp4">responsive Design?</a>

- Uitleg <a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BK.07%20FrD%5D%20Keuzedeel%20%5BK0722%5D%20Frontend%20development/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2007/Productie/743192_02_02_XR30_media_queries.mp4">Media queries</a>

- <a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BK.07%20FrD%5D%20Keuzedeel%20%5BK0722%5D%20Frontend%20development/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2007/Productie/03.%20Scripts/743192_02_03_XR30_flexbox.mp4">Gridview en flexbox</a>


Gebruik de <a href="https://elo.kw1c.nl/Pages/View.aspx?cp=%2FCMS%2FStudie%2F811%20ICT-Academie%2F811%20VakkenInhoud%2F%5BK.07%20FrD%5D%20Keuzedeel%20%5BK0722%5D%20Frontend%20development%2F25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar%2FPeriode%2007%2FProductie%2FEx_Files_Responsive_Layout">oefenbestanden</a> om met de bovenstaande basisprincipes te oefenen. 


Bestudeer verder ook de volgende pagina's op w3schools. 
- <a href="https://www.w3schools.com/css/css3_flexbox.asp">display : flexbox</a>
- <a href="https://www.w3schools.com/css/css_grid.asp">display : grid</a>
- <a href="https://www.w3schools.com/css/css3_mediaqueries.asp">Mediaqueries</a>
- <a href="https://www.w3schools.com/css/css_rwd_intro.asp">Responsive Web Design</a> Doorloop alle pagina's via de next button totdat je op de pagina komt over videos (https://www.w3schools.com/css/css_rwd_videos.asp).

---
## 2.3 CSS Pre-Processors met LESS
---

### Less links

<a href="http://lesscss.org/#">CSS pre-processor met LESS</a>
<br>
<a href="https://htmlmag.com/article/an-introduction-to-css-preprocessors-sass-less-stylus">Vergelijking CSS pre-processors met LESS, SASS en Stylus</a>
<br>
<a href="https://www.concretepage.com/css-3/less-css-tutorials-examples">Voorbeelden gebruik less</a>
<br>
<a href="https://www.hongkiat.com/blog/less-color-functions/">Less functions</a>


[![Over LESS op youtube](http://img.youtube.com/vi/YD91G8DdUsw/0.jpg)](http://www.youtube.com/watch?v=YD91G8DdUsw)


---
## Opdracht 2 - Maak gebruik van CSS pre-processor en maak de website responsive
---

### Download
<a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BK.07%20FrD%5D%20Keuzedeel%20%5BK0722%5D%20Frontend%20development/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2007/Productie/02.%20Opdrachten/FD%20-%20Opdracht%202.pdf" target="_blank">Download opdracht 2</a>

### Onderwerpen, o.a:
*   Viewport
*   Grid View
*   Media queries

### Benodigde bestanden
* <a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BK.07%20FrD%5D%20Keuzedeel%20%5BK0722%5D%20Frontend%20development/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2007/Productie/02.%20Opdrachten/Bestanden/HandleidingHosten.pdf" target="_blank">Installatiehandleiding Hosten op Azure</a>

### Help
* <a href="https://www.w3schools.com/whatis/whatis_responsive.asp" target="_blank">W3Schools - What is Responsive Web Design?</a>


---
## Opdracht 3 - Testen
---

De responsive site die ontwikkeld is moet worden getest en aan de hand van de gevonden gebreken worden geoptimaliseerd. <a target="_new" href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BK.07%20FrD%5D%20Keuzedeel%20%5BK0722%5D%20Frontend%20development/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2007/Productie/02.%20Opdrachten/FD%20-%20Opdracht%203.pdf">Download de testopdracht.</a>

__Links__

<a target="_new"  href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BK.07%20FrD%5D%20Keuzedeel%20%5BK0722%5D%20Frontend%20development/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2007/Productie/02.%20Opdrachten/Bestanden/Sjabloon%20Acceptatietest.docx">sjabloon acceptatietest</a>

<a target="_new"  href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BK.07%20FrD%5D%20Keuzedeel%20%5BK0722%5D%20Frontend%20development/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2007/Productie/02.%20Opdrachten/Bestanden/Sjabloon%20testrapport.docx">sjabloon acceptatietestrapport</a>


