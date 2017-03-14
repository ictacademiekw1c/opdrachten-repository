## Opdracht 350 De temperaturen via AJAX inlezen

`` Opleveren: Plaats al je gemaakte bestanden (.js, .html ) in een een rar met naam OPDRACHT350.rar en upload deze in je portfolio. Laat daarna de opdracht zien aan de docent om deze af te tekenen. Onthoud bij het uploaden dat we inmiddels in Periode 3 zitten.``

**Opdracht:**

We gaan een site maken die de huidige temperaturen in minimaal 7 steden van Nederland laat zien. Dit gaan we doen door gebruik te maken van de gratis webservice genaamd "Open Weather Map". We kunnen deze webservice via AJAX inlezen.
We gaan voor 7 steden (3 steden moet je zelf bedenken) de temperaturen inlezen en we gaan deze laten zien in een kaart.

> Protip: Pak <a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.16%20JAV%5D%20Javascript/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2003/Productie/01.%20Reader/Reader%203%20-%20AJAX.pdf" target="_new">reader 3 (AJAX)</a> erbij. Deze opdracht is namelijk wat lastiger als je niet weet hoe *objecten* en *JSON* werkt.

 **Stappen:** 
 1. Download de <a href="https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.16%20JAV%5D%20Javascript/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2003/Productie/03.%20Scripts/Huiswerkopdrachten/Opdracht%20350.zip" target="_blank">template</a> en pak deze uit
 2. Zorg ervoor dat je in de kaart van NL, boven de steden die hieronder in de tabel staan tekst kan plaatsen (via een DIV of SPAN) 
 3. Bedenk zelf nog 3 steden en plaats hier ook een DIV of SPAN boven op de kaart, zodat je hier ook tekst in kan plaatsen
 4. Zodra de gebruiker op de knop "Update" klikt, moeten de temperatuur van de betreffende steden in de kaart getoond worden (via AJAX)
 5. Kom je er niet uit? Lees de reader. Met name de sectie "JSON" is hier erg handig!
 5. That's it!
 
 **Ron's extra tips:**
 1. Bekijk de API URL alvast in je browser om een idee te hebben hoe de JSON is opgebouwd
 2. Kijk heel goed hoe de JSON is opgebouwd. Hier zul je waarschijnlijk veel tijd aan kwijt zijn
 3. Maak een test AJAX request (wel met een van de onderstaande API URLS) aan en gebruik hier *$.parseJSON()*. Plaats daarna het *debugger;* keyword en kijk in je Inspector naar de uitkomst
 4. Gebruik je Console en *debugger* zo goed mogelijk!
  
 **Extra opdracht:**
 1. Zorg ervoor dat ook er ook <a href="http://www.ourdesignz.com/wp-content/uploads/2014/12/Weather-icon.png" target="_blank">icoontjes</a> getoond worden
 2. Alle data hiervoor is te vinden in de JSON van Open Weather Map!
 
### URL's voor de temperaturen
<table>
    <tr>
        <th>Stad</th>
        <th>API URL</th>
    </tr>
    <tr>
        <td>
            Amsterdam
        </td>
        <td>
            http://api.openweathermap.org/data/2.5/weather?q=Amsterdam&appid=8d294e9544f1f24d1ec04c7e8839cba9&units=metric
        </td>
    </tr>
    <tr>
        <td>
            Groningen
        </td>
        <td>
            http://api.openweathermap.org/data/2.5/weather?q=Groningen&appid=8d294e9544f1f24d1ec04c7e8839cba9&units=metric
        </td>
    </tr>
    <tr>
    <td>
        <td>
            Vlissingen
        </td>
        <td>
            http://api.openweathermap.org/data/2.5/weather?q=Vlissingen&appid=8d294e9544f1f24d1ec04c7e8839cba9&units=metric
        </td>
    </tr>
    <tr>
        <td>
            DenBosch
        </td>
        <td>
            http://api.openweathermap.org/data/2.5/weather?q=DenBosch&appid=8d294e9544f1f24d1ec04c7e8839cba9&units=metric
        </td>
    </tr>
</table>

### Visueel voorbeeld:
<img style="width: 40%" src="https://raw.githubusercontent.com/ictacademiekw1c/opdrachten-repository/master/javascript/p3/productie/Afbeeldingen/350-1.png">

 **Beoordelingscriteria:**
1. De temperatuur van de onderstaande steden is te zien op de kaart
    - Amsterdam
    - Vlissingen
    - Den Bosch
    - Groningen
2. De temperatuur van nog 3 andere steden is ook zichtbaar
3. De temperatuur staat gepositioneerd ongeveer op de plek waar de steden liggen
4. Bij een klik op de "Update" button worden de temperaturen opnieuw ingeladen via AJAX
5. Er worden in totaal minimaal 7 losse AJAX requests gemaakt (voor iedere stad één)

---

## Opdracht 351
