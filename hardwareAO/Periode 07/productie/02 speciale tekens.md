####[kleurcode]rgba(77,182,172,1)

#Speciale Tekens#

Arduino gebruikt een aantal verplichte speciale tekens:

1. **; Puntkomma.** Iedere programmaregel moet worden afgesloten met een puntkomma. Een vergeten puntkomma zorgt ervoor dat een
   programma niet werkt.
2. **{} Accolades.** Een accolade geeft het begin en einde van een blok informatie weer. Binnen een blok accolades kunnen meerdere kleine blokken met eigen accolades voorkomen.
3. **// Regel commentaar.** In elke regel kan je // plaatsen. De regel achter de // wordt niet meer gelezen door Arduino. Handig voor uitleg/commentaar. Maar het kan ook gebruikt worden om een programmaregel (tijdelijk) uit te schakelen.
4. **/\*….*/ Commentaarblok.** Als je uitleg of commentaar over meerdere regels wilt schrijven kan je gebruik maken van de tekens voor commentaar blok. Uitleg over het programma is, zeker voor anderen, heel handig.

``` ArduinoC++
int a = 5; // de ; wordt gebruikt na elke regel zodat het programma weet
           // dat er een nieuw stukje code komt hierna

void loop()
{ // openings accolade.
 // dit is een regel commentaar, alleen op één regel kan er iets geschreven worden
 /*
   Met deze tekens kunnen
   meerdere regels commentaar geschreven worden zonder probleem.
   Dit is handig als je veel commentaar wilt schrijven aan het begin.
 */
} // sluitings accolade.
// accolades geven een blok van code aan, alles tussen de code zal uitgevoerd worden.
```

