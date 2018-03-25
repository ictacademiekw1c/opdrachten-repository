###[kleurcode]rgba(77,182,172,1)

##Void setup en loop##

###Void Setup(){ … }###

In het blok “Void setup “ staat tussen de accolades {} de informatie. Hier staat wat we allemaal gaan gebruiken. De setup wordt maar één keer ingelezen en vervolgens onthouden.


```Arduino C++
void setup()
{
  // Tussen de accolades wordt de code één keer uitgevoerd.
  // Dit kan handig zijn om bijvoorbeeld te zeggen waar een led aangesloten is.
}

```

###Void loop(){ … }###

In het blok “Void loop” staat de informatie ook tussen de accolades {}. In deze informatie staat wat we allemaal gaan doen. De “Void loop” wordt niet één keer ingelezen, maar iedere keer herhaald. Binnen het blok “Void loop” kun je kleinere blokjes maken, die staan dan ook weer binnen twee accolades. Het aantal accolades is dus altijd even. Bij het schrijven van een programma kun je natuurlijk wel eens een accolade vergeten. Als je in de sketch naast een accolade gaat staan laat het programma zien waar de tweede staat, dit ter controle.


```Arduino C++
void loop()
{
  // Alle code tussen de accolades in de loop worden eeuwig herhaald.
  // Dit kan bijvoorbeeld handig zijn om een lampje te laten knipperen.
}
// Alle code buiten de accolades zijn niet geldig en geven een ERROR

```