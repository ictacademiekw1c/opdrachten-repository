####[kleurcode]rgba(77,182,172,1)

#Besturingsstructuren#

### if (conditie) {….}###

Bij deze opdracht wordt gecontroleerd of de conditie die tussen de haakjes staat waar is. Als dat zo is wordt de actie uitgevoerd die tussen de accolades staat. Zo niet, dan wordt de actie overgeslagen.
Voorbeeld:

``` ArduinoC++
if(val == 1)
{
	digitalWrite(LED,HIGH); // als de waarde val 1 is gaat de LED aan
}
```

### if….else###

Hier wordt gekozen tussen twee condities. Als de ene waar is, doe {…..} anders doe {——}
Voorbeeld:

``` ArduinoC++
if(inputPin == HIGH)
{
	//voer actie A uit;
}
else
{
	//voer actie B uit;
}
```
Je kan het nog verder uitbreiden. Let goed op de haakjes en puntkomma’s.
Voorbeeld:

``` ArduinoC++
if(inputPin < 500)
{
	//Voer actie A uit;
}
else if (inputPin <= 1000)
{
	//voer actie B uit;
}
else
{
	//voer actie C uit;
}
```

### for (variabele; voorwaarde; vermeerdering of vermindering;)

Laat je een stukje programma een bepaald aantal keren uitvoeren.
Voorbeeld:

``` ArduinoC++
for(int i = 0; i < 10; i ++)
{
	/*    Voer 10 keer iets uit.    i begint bij 0 en eindigt bij 10  */
}
```
### while (variabele)

Lijkt wel wat op de for loop. Doe iets zolang aan een bepaalde voorwaarde voldaan wordt. Wordt er niet aan de voorwaarde voldaan dan wordt het blokje overgeslagen.
Voorbeeld:
``` ArduinoC++
var = 0;
while(var < 200)
{	// doe iets 200 keer
	var ++;
}
```