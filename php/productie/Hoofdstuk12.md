
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

## 12.3 Voorbeeld



