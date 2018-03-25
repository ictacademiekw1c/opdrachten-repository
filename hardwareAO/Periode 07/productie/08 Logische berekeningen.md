####[kleurcode]rgba(77,182,172,1)

#Logische berekeningen#

Logische berekeningen (Boolean operators) zijn vergelijkingen waarbij de uitkomst waar of niet waar is. Ze worden vaak gebruikt in if opdrachten om verschillende condities met elkaar te vergelijken:

1. **&&** Logische en (and): if (x>0 && x<5)
   Waar als beide vergelijkingen waar zijn.
2. **||** Logische of (or): if (x>0 || y>0)
   Waar als een van de twee waar is.
3. **!** Logische niet (not): if (!x > 0)
   Waar als de vergelijking niet waar is.
4. **^** Exclusief of (xor):  if ((x>0 || y>0) && (x!=y))
   Waar als slechts een van de twee waar is.

``` ArduinoC++

// and operator
c = false && false;   // false
c = true  && false;   // false
c = false && true;    // false
c = true  && true;    // true
// or operator
c = false \|\| false; // false
c = true  \|\| false; // true
c = false \|\| true;  // true
c = true  \|\| true;  // true
// not
c = ! true;           // false
c = ! false;          // true
// xor operator
c = false ^ false;    // false
c = true ^ false;     // true
c = false ^ true;     // true
c = true ^ true;      // false
```