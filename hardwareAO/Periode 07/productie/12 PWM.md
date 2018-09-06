Theory (PWM)

Pulse Width Modulation (or PWM) is a technique for controlling power.  We also use it here to control the brightness of each of the LEDs. 

The diagram below shows the signal from one of the PWM pins on the Arduino.

-------------------

Plaatje
-------------------
Ongeveer elke 1/500 van een seconde produceert de PWM-uitvoer een puls. De lengte van deze puls wordt bepaald door de functie 'analoogWrite'. Dus 'analogWrite(0)' produceert helemaal geen puls en 'analogWrite(255)' produceert een puls die de hele tijd duurt tot de volgende puls moet worden uitgevoerd, zodat de output eigenlijk altijd aan is.

Als we in de analogWrite een waarde opgeven die ergens tussen 0 en 255 ligt, produceren we een puls. Als de uitvoerpuls slechts 5% van de tijd hoog is, krijgt wat we aansturen maar 5% van het volledige vermogen.

Als de uitvoer echter 90% van de tijd op 5V staat, krijgt de belasting 90% van de geleverde stroom. Het menselijk oog is niet in staat om het knipperen van de LED's met deze snelheid waar te me,em, voor ons lijkt het dus alsof de helderheid verandert.