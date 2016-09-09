#### [kleurcode]rgba(156,39,176,1)

# Hoofdstuk 3 - Stringfuncties

## 3.1 Wat ga je leren?
Er zijn een aantal standaard php functies die handig zijn bij string variabelen.
- strlen()
- trim()
- strtolower()
- strtoupper()
- str_replace()

## 3.2 Voorbeeld van strlen() 
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

## 3.3 Voorbeeld van trim() 
~~~php
//alle alle spaties uit een string

$sAchter = "spaties      ";
$sVoor = "               weghalen.";

$sAchter = trim($sAchter);
echo $sAchter. trim($sVoor);

~~~

---
## 3.4 Voorbeeld van strtolower(), strtoupper() en ucfirst()
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

## 3.5 Voorbeeld van str_replace() 

~~~php
//vervangen van stukken tekst met andere tekst
$sLuidkeels = "Ik houd niet van GESCHREEUW.";

//vervang niet in de zin door wel
$sLuidkeels = str_replace("niet", "wel", $sLuidkeels);

echo $sLuidkeels;

~~~

---

## 3.6 Opdracht30 spelen met strings
### Opdrachtomschrijving opdracht30

Declareer 10 variabelen voor 10 medeleerlingen uit je klas en initialiseer ze op de juiste waarde.

Bepaal met strlen() wat de lengte van iedere string is van iedere variabele en toon de namen van je medeleerlingen
in volgorde van lengte. 

### Visuele weergave 30 
//Uitwerking met bovenstaande variabelen
> Saebu (lengte 5)<br>
> de Reus (lengte 7)<br>
> Spierings (lengte 9)<br>
> Gijsbrechts (lengte 11) 

### Beoordelingscriteria 31
1. Sla dit script op als opdracht30.php in de map Hoofdstuk3
2. Het script levert geen fouten of waarschuwingen op in de browser

---

## 3.6 Opdracht31 spelen met strings
### Opdrachtomschrijving opdracht31

Gebruik voor deze opdracht je introductietekst uit opdracht 20.

Gebruik een of meerdere functies van hierboven om:

1. Zet alle tekstdelen die in je variabelen zitten (bijvoorbeeld $naam) om naar hoofdletters.
2. Maak gebruik van str_replace() om je tekst naar de 3de persoonsvorm te zetten. (Van de ik vorm naar de hij vorm).
3. Bepaal van iedere zin variabele de lengte en zet onder de tekst de volledige lengte van de gehele tekst.

### 3.4.2 Visuele weergave 31

Voorbeeld met mijn eigen tekst:
> Hij is ABU SAEBU. Hij woont bijna zijn hele leven in 'S-HERTOGENBOSCH. Hij heeft op school gezeten op het SINT JANSLYCEUM op de Sweelinckplein in DEN BOSCH. Hij is 52 jaar, hij is GETROUWD en hij heeft 2 kinderen. Zijn hobbies zijn GITAAR SPELEN, PIANO SPELEN, MUZIEK LUISTEREN en PROGRAMMEREN. Hij is DOCENT APPLICATIEONTWIKKELING en hij geeft de vakken PHP, HTML/CSS, JAVASCRIPT, DATABASE/SQL, C#, ANDROID APPS, BEHEER en BEDRIJFSKUNDE.
Deze tekst bevat 370 tekens.


### 3.4.3 Beoordelingscriteria 31
1. Sla dit script op als opdracht31.php in de map Hoofdstuk3
2. Het script levert geen fouten of waarschuwingen op in de browser
3. Je tekst bevat minimaal 5 complete zinnen.
4. De tekst eindigt met het totaal aantal tekens in de zin, die bepaald is met de functie strlen().
---