####[kleurcode]rgba(239,108,0,1)####

##C# Programma structuur##

###Algemene C# regels .###

* C# is hoofdlettergevoelig.
* Alle statements en expressies moeten worden afgesloten met een puntkomma. (**;**)
* Het programma start executie bij de *Main* methode  (Hoofdletter M)
* De bestandsnaam van een klasse moet *dezelfde* naam hebben als de klasse zelf.

**Basis structuur console applicatie - New York City Marathon**

**NYCM.cs**

```C#
/************************** Module Header *******************************\
Project:		New York City Marathon
Auteur:			Bart Linsen
Aanmaakdatum:   3 april 2017 
Module naam:	NYCM.cs

Omschrijving:	Hoofdprogramma New York City Marathon

\************************************************************************/
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace NewYorkCityMarathon_Hfst23
{
    class NYCM
    {
        static void Main(string[] args)
        {
        }
    }
}
```

* De eerste regels van het programma bestaan uit *using System;* 
  Het keyword *using* wordt gebruikt om de System namespace in het programma op te nemen.(#include in C++) Een programma heeft meestal meerdere using statements.

* Na het using blok volgt de *namespace* declaratie. Een *namespace* is een collectie van klassen. De NewYorkCityMarathon_Hfst23 *namespace* bevat de klasse NYCM.

* De volgende regel bevat de *class* declaratie, de klasse NYCM bevat data en methods definities die het programma gebruikt. Klassen bevatten over het algemeen meerdere *methoden*. *Methoden* definieren het gedrag van een klasse. Op dit moment heeft de *Program* klasse maar een *methode* *Main*

* De volgende regel definieerd de *Main* methode, dit is het toegangspunt voor alle C# programma's. De *Main* methode bepaalt wat de class doet wanneer de klasse wordt opgestart. De Main methode is gedefinieerd als static, zodat er geen instantie hoeft te worden gecreeerd van het toegangspunt. De *Main* methode mag maar een keer voorkomen in een C# programma.

* De lijn ``` /* .... */ ``` wordt door de compiler genegeerd en hier kun je daarom commentaar in plaatsen.




**De volledige console implementatie - New York City Marathon:**

**NYCM.cs**
```C#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace NewYorkCityMarathonHfst23
{
    class NYCM
    {
        static void Main(string[] args)
        {
            // Constructie van object deelnemer1
            Deelnemer deelnemer1 = new Deelnemer();

            deelnemer1.Invoeren(); // Invoeren deelnemer deelnemer1 structuur
            deelnemer1.Weergeven(); // Weergeven deelnemer deelnemer1 structuur 

            // Wacht tot de gebruiker een toets indrukt
            Console.ReadKey(); 
        }
    }
}
```
- Een object moet worden aangemaakt, geconstrueerd, met behulp van het new statements
  ```<Klasse naam> <object naam> = new <Klasse constructor>();```
- Aanroep van een method van een object.
  ```<object naam>.<methode naam>;```
- De laatste regel ```Console.ReadKey();``` zorgt ervoor dat het programma wacht voor een toets aanslag en voorkomt dat het scherm sluit en je de finale tekst op het scherm niet kunt lezen.

**Deelnemer.cs**

```C#
/************************** Module Header *******************************\
Project:		New York City Marathon
Auteur:			Bart Linsen
Aanmaakdatum:    3 april 2017 
Module naam:	Deelnemer.cs

Omschrijving:	Definitie klasse Deelnemer

\************************************************************************/
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace NewYorkCityMarathonHfst23
{
    class Deelnemer
    {	// Attributen
        private string deelnemerNaam;
        private int rugNummer;
        public int chipNummerH201; //Hoofdverzameling Hfd:201 en Uniciteit 

        // Constructor
        public Deelnemer()
        {	// Hoofdverzameling chipNummer bevat een niet leeg indicatie
            chipNummerH201 = 0;
        }
        // Methods - Implementatie
        public void Invoeren()
        {   
            string gebruikersInput; // lokale variabele voor try-catch

            Console.Write("Geef de naam van de deelnemer: ");
            deelnemerNaam = Console.ReadLine();

            Console.Write("Voer zijn rugnummer in: ");
            gebruikersInput = Console.ReadLine();
            try
            {
                rugNummer = Convert.ToInt32(gebruikersInput);
            }
            catch
            {
                rugNummer = 0;
                Console.WriteLine("Geen juist rugnummer ingevoerd");
            }

            Console.Write("Voer zijn chipnummer in: ");
            gebruikersInput = Console.ReadLine();
            try
            {
                chipNummerH201 = Convert.ToInt32(gebruikersInput);
            }
            catch
            {
                chipNummerH201 = 0;
                Console.WriteLine("Geen juist chipnummer ingevoerd");
            }
        }

        public void Weergeven()
        {   //UI
            Console.WriteLine("\nDeelnemer {0} heeft het rugnummer {1} en het chipnummer {2}", deelnemerNaam, rugNummer, chipNummerH201);
        }
    }
}
```

- **Int32.TryParse()** of **try{} catch{}** constructies maken het mogelijk om een datatype conversie uit te voeren van string naar int en indien dit niet lukt, netjes af te vangen in je programma en de gebruiker te informeren. 

  In het voorbeeld is het try catch voorbeeld uitgewerkt. Let op dat een variabele die je zet in de try tak ook in de catch tak gevuld moet worden. Beide beslistaken moeten de variabele vullen.

  Hier een voorbeeld met *Int32.TryParse()*:

  ```C#
  Console.Write("Voer zijn chipnummer in: ");
  gebruikersInput = Console.ReadLine();
  while (!Int32.TryParse(temp, out chipNummerH201))
  {
  	// Ga net zo lang door totdat de ingevoerde string kan worden omgezet naar een int
      Console.WriteLine("Geen juist chipnummer ingevoerd");
      temp = Console.ReadLine();
  }
  ```

  




##Interessante bronnen##
[C# program structure](https://www.tutorialspoint.com/csharp/csharp_program_structure.htm) - Tutorial point

[try {} catch {}](https://www.dotnetperls.com/catch) - dotnetperls

[TryParse](https://www.dotnetperls.com/parse) - dotnetperls

[How To Concatenate Strings In C#](https://www.c-sharpcorner.com/article/6-effective-ways-to-concatenate-strings-in-c-sharp-and-net-core/) - C# Corner