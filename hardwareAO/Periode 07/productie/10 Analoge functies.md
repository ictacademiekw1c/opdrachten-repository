#### [kleurcode]rgba(77,182,172,1)

#Analoge functies#

### analogRead(pin)###

Leest het voltage (tussen 0 en 5 volt) dat staat op een analoge input pin (pin 0 t/m 5 zijn analoge pinnen) en geeft daarvoor een waarde tussen 0 en 1023.
Voorbeeld:

``` ArduinoC++
val = analogRead(2);
// Meet de spanning op pin2
// en geef een waarde (val)
```

### analogWrite(pin, value)###

Een Arduino is een digitaal apparaat en kan alleen wel of geen stroom zetten op een pin. De pinnen 3, 5, 6, 9, 10 en 11 ondersteunen PWM (pulse width modulation). Deze pinnen kunnen heel snel aan en uit gezet worden waardoor ze analoog lijken. De value kan een getal zijn tussen 0 en 255 die omgeschaald wordt naar een spanning tussen 0 en 5 V.
Voorbeeld:

``` ArduinoC++
analogWrite(9, 128);
// Dim een led op pin 9 met 50%
```