# Hoofdstuk 4 - Nog meer stringfuncties

## 4.1 Wat ga je leren?
Je leert het gebruiken en toepassen van nog een aantal string functies:

### Zoeken van een string in een andere string waarbij je de positie terugkrijgt waar die is gevonden.
- strpos() 
- strrpos()
- stripos()
- strripos()

### Van een string een stukje (substring) knippen (substr()) of vervangen (substr_replace())
- substr()
- substr_replace()

## 4.2 Uitleg en voorbeelden strpos() en varianten

~~~php

$sZin = "Dit is een zin. dit is een tweede zin. Dit een derde."

/*
strpos zoekt vanaf de linkerkant en stopt als het gevonden is
strrpos zoekt vanaf de rechterkant en stopt als het gevonden is
stripos als de eerste maar dan zonder onderscheid van hoofd of kleine letters
strripos als de tweede maar dan zonder onderscheid van hoofd of kleine letters
*/

echo strpos ($sZin, "$dit"). "<br>";
echo strrpos ($sZin, "$dit"). "<br>";
echo stripos ($sZin, "$dit"). "<br>";
echo strripos ($sZin, "$dit"). "<br>";

~~~
## 4.3 Uitleg en voorbeelden substr() en substr_replace()

~~~php

~~~

---
## 4.4 Opdracht 40

### Omschrijving 40

### Visuele weergave 40

### Programmastructuur 40

### Beoordelingscriteria 40
---

---
## 4.5 Opdracht 41

### Omschrijving 41

### Visuele weergave 41

### Programmastructuur 41

### Beoordelingscriteria 41
---