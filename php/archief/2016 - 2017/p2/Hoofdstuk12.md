
# Hoofdstuk 12 Sessie 

## 12.1 Wat ga je leren ?

- Wat is een sessie
- Hoe maak je een sessie aan
- Hoe zet je een waarde in een sessie
- Hoe haal je een waarde op in de sessie

## 12.2 Uitleg
> In een sessie bewaar je gegevens die je nodig kan hebben gedurende het bezoek van een gebruiker aan een website. Bijvoorbeeld de gebruikersnaam of de producten in een winkelwagen in een webshop.

### Hoe start/gebruik je een sessie?
~~~php
session_start();
~~~

### Hoe zet je bijvoorbeeld de variabele naam in de sessie?
~~~php
$_SESSION['naam'] = "Abu";
~~~

### Hoe echo je een sessie variabele?
~~~php
echo $_SESSION['naam'];
~~~

### Hoe verwijder je een variabele uit de sessie?
~~~php
unset ($_SESSION['naam']);
~~~

## 12.3 Opdracht 120 formulier en sessie

### Opdrachtomschrijving 120

Maak de volgende scripts aan die naar elkaar gaan verwijzen via links of via de action in het formulier.

- formulier.php  
> Een formulier met method post en action naar sessie.php
- sessie.php
> de post variabele naam wordt in de sessie variabele naam gezet
- sessie1.php
> de sessie variabele naam wordt geprint
- sessie2.php
> de sessie variabele naam wordt verwijderd uit de sessie

Haal de scripts op vanuit github: [voorbeeld scripts](https://gist.github.com/saebuabu/57afc5251c820fb36127a946ea130689)

Test de scripts zelf uit. Zou je hier een login systeem van kunnen maken?



