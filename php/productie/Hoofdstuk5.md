# Hoofdstuk 5 - Get parameters

## 5.1 Wat ga je leren ?

Wat een Get parameter is. Hoe pas je deze aan in een URL. De eerste manier om iets door te geven aan een script.

Voorwaardelijke code: Hoe maak je in php een if else constructie.

## 5.2 Voorbeeld en uitleg 5.1 

~~~php
// Maak een script aan in de map hoofdstuk 5 met de naam testget.php
// Neem de volgende code over in het script en launch het in je browser
// Wat zie je?
echo $_GET['leeftijd'];

$leeftijd = $_GET['leeftijd'];

if ($leeftijd > 17) {
    echo "Je bent volwassen";
} else {
    echo "Je bent nog een kind";
}


//Pas de URL in je browser aan door ?leeftijd=10 aan het eind toe te voegen
//Wat zie je nu als je nu de pagina opvraagt?
~~~

---
## Opdracht 50

### Omschrijving
Vul hier een omschrijving van de opdracht in.

### Visuele weergave

### Programmastructuur

### Beoordelingscriteria

---
