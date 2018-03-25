[kleurcode]rgba(77,182,172,1)

# Variabelen

Variabelen kan je gebruiken om getallen op te slaan in het geheugen om later weer te kunnen gebruiken. Er zijn verschillende types variabelen die meer of minder geheugenplek innemen, afhankelijk van het aantal getallen dat ze moeten opslaan.

1. **Int (integer)** Het meest gebruikte data type. Heeft geen decimalen en kan een getal opslaan tussen -32.768 en 32.767

2. **boolean** Kan twee waardes hebben true of false (waar of niet waar)

3. **long** Wordt gebruikt als een integer niet groot genoeg is. Long kan getallen opslaan tussen -2.147.483.648 en 2.147.483.647.

4. **float** Floating point betekent decimaal. Een floating point kan een decimaal getal opslaan, kost veel geheugenruimte.

5. **char (character)** Slaat een toetsenbordteken op in de ASCII code (bv A=65).

   ```Arduino C++
   // hieronder voorbeelden van de types

   int a = 5;
   int b = -7;

   bool check = true;
   bool niet_check = false;

   long veel = 2000000000;
   long weinig = -2000000000;

   float decimaal = 0.245;
   float geen_decimaal = 3.0;

   char character = 'A';
   char cijfer_als_character = '1';
   ```

   ​