#### [kleurcode]rgba(156,39,176,1)

# Hoofdstuk 3 - Stringfuncties

## Wat ga je leren?
Er zijn een aantal standaard php functies die handig zijn bij string variabelen.
- strlen()
- trim()
- strtolower()
- strtoupper()
- str_replace()

## Voorbeeld van strlen() 
~~~php
//bepaal de lengte van een string

$mijnnaam = "Saebu";
$collega  = "Spierings";
$collega2 = "de Reus";
$collega3 = "Gijsbrechts"

echo strlen($mijnnaam);
echo "<br>";
echo strlen($collega);
echo "<br>";
echo strlen($mijnnaam) + strlen($collega);

~~~

## Voorbeeld van trim() 
~~~php
//alle alle spaties uit een string

$sAchter = "spaties      ";
$sVoor = "               weghalen.";

$sAchter = trim($sAchter);
echo $sAchter. trim($sVoor);

~~~

---
## Voorbeeld van strtolower(), strtoupper() en ucfirst()
~~~php
//omzetten van kleine letters naar grote en omgekeerd

//voorbeeld 1
$sLuidkeels = "Ik houd niet van GESCHREEUW";
echo strtolower($sLuidkeels);

//voorbeeld 2
$sLuidkeels = "Ik houd niet van GESCHREEUW";
$sZachtjes = strtolower($sLuidkeels);
$sNetjes = ucfirst($sZachtjes);
echo $sNetjes;

//voorbeeld 3
$sLuidkeels = "Ik houd niet van GESCHREEUW";
echo ucfirst( strtolower( $sLuidkeels ) );

~~~

## Voorbeeld van str_replace() 

~~~php
//vervangen van stukken tekst met andere tekst
$sLuidkeels = "Ik houd niet van GESCHREEUW.";

//vervang niet in de zin door wel
$sLuidkeels = str_replace("niet", "wel", $sLuidkeels);

echo $sLuidkeels;

~~~

---

## Opdracht30 spelen met strings
### Opdrachtomschrijving opdracht30

Declareer 10 variabelen voor 10 medeleerlingen uit je klas en initialiseer ze op de juiste waarde.

Bepaal met strlen() wat de lengte van iedere string is van iedere variabele en toon de namen van je medeleerlingen
in volgorde van lengte. 

### 3.4.2 Visuele weergave 
//Uitwerking met bovenstaande variabelen
> Saebu (lengte 5)<br>
> de Reus (lengte 7)<br>
> Spierings (lengte 9)<br>
> Gijsbrechts (lengte 11) 

### 3.4.3 Beoordelingscriteria
1. Sla dit script op als opdracht30.php in de map Hoofdstuk3
2. Het script levert geen fouten of waarschuwingen op in de browser


---