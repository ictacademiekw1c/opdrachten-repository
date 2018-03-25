[kleurcode]rgba(77,182,172,1)

# Constanten

Een aantal woorden zijn bij de Arduino gekoppeld aan speciale, constante waardes. Let op de hoofdletters en kleine letters.

### **HIGH** en **LOW**

Worden gebruikt om een Arduino pin aan of uit te zetten.
Voorbeeld:
```Arduino C++
digitalWrite(13, HIGH); // dit betekent: zet 5 volt op pin 13
```

### **INPUT** en **OUTPUT**

Bepalen of een pin een input (spanning meten) of output (spanning geven) is.
Voorbeeld:

```Arduino C++
pinMode(13, OUTPUT); // pin 13 is een output. 
```
### **true** en **false**

Controleren of iets waar of niet waar is. False (niet waar) is 0. Alle waardes die niet nul zijn beschouwt de Arduino als true (waar).
Voorbeeld:

```Arduino C++
if(b == true){   // doe iets tussen de accolades als b true als waarde heeft } |
```