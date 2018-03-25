###[kleurcode]rgba(77,182,172,1)

# Digitale functies#

Arduino heeft speciale functies voor de digitale pinnetjes.

### pinMode(pin, mode)###

Stelt een bepaalde pin in als output of als input.
Voorbeeld:

``` Arduino C++
pinMode(7, INPUT); // Maakt van pin 7 een input. 
```
### digitalWrite(pin, value)###

Zet een bepaalde pin hoog (HIGH) of laag (LOW).
Voorbeeld:

``` Arduino C++
digitalWrite(9, HIGH); // Zet pin 9 aan.
```

### digitalRead(pin)

Leest of een pin hoog of laag staat.
Voorbeeld:

``` Arduino C++
val = digitalRead(8);
// Geeft de waarde HIGH (wel
// spanning) of LOW (geen
// spanning) van pin 8
```