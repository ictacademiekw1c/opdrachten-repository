# Theory Pulse Width Modulation

Pulse Width Modulation (afgekort PWM) is een techniek om het vermogen of de positie naar een actuator te regelen.   We kunnen het bijvoorbeeld gebruiken om de lichtsterkte van een LED of de stand van een servo mee te regelen .

De diagram hieronder laat het signaal zien van een van de PWM pinnen van de Arduino.

-------------------
![PWM](https://www.arduino.cc/en/uploads/Tutorial/pwm.gif)

-------------------
Ongeveer elke 1/500 van een seconde produceert de PWM-uitvoer een puls. De lengte van deze puls wordt bepaald door de functie 'analoogWrite'. Dus 'analogWrite(0)' produceert helemaal geen puls en 'analogWrite(255)' produceert een puls die de hele tijd duurt tot de volgende puls moet worden uitgevoerd, zodat de output eigenlijk altijd aan is.

Als we in de analogWrite een waarde opgeven die ergens tussen 0 en 255 ligt, produceren we een puls. Als de uitvoerpuls slechts 5% van de tijd hoog is, krijgt wat we aansturen maar 5% van het volledige vermogen.

Als de uitvoer echter 90% van de tijd op 5V staat, krijgt de belasting 90% van de geleverde stroom. Het menselijk oog is niet in staat om het knipperen van de LED's met deze snelheid waar te nemen, voor ons lijkt het dus alsof de helderheid veranderd.