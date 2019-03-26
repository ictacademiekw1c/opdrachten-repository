#### [kleurcode]rgba(255,192,0,1)

# HOOFDSTUK 19

In hoofdstuk 19 wordt de volgende onderwerpen uitgewerkt in de opdracht:

- Overerving (Inheritance ) van klasses
- Overerving modi

## Overerving

Het vermogen van een klasse om eigenschappen en kenmerken van een andere klasse over te nemen, wordt *Overerving* genoemd. *Overerving* is een van de belangrijkste kenmerken van object georiënteerd programmeren. (OOP)

**Subklasse**: de klasse die eigenschappen van een andere klasse overneemt, wordt *Sub*-klasse of *Derived* klasse genoemd.

**Superklasse**: de klasse waarvan de eigenschappen worden overgenomen door de subklasse, wordt de *Base* klasse of de *Super* klasse genoemd.

### Waarom en wanneer overerving gebruiken?

Neem een groep voertuigen. Uit deze groep van voertuigen wil je klassen maken voor Bus, Auto en Vrachtwagen. De methoden brandstofHoeveelheid(), aantalPersonen(), remmen() zijn hetzelfde voor alle drie de klassen. Als we deze klassen zouden maken zonder overerving dan moeten we al deze functies in elk van de drie klassen implementeren, zoals weergegeven in de onderstaande afbeelding:

```
| 	Class Bus				|	Class Auto				|	Class Vrachtwagen		|
|---------------------------|---------------------------|---------------------------|
| 	brandstofHoeveelheid()	|	brandstofHoeveelheid()	|	brandstofHoeveelheid()	|
|	aantalPersonen()		|	aantalPersonen()		|	aantalPersonen()		|
|	remmen()				|	remmen()				|	remmen()				|

```

Je kunt duidelijk zien dat bovenstaande proces resulteert in dubbele duplicatie van dezelfde code. Dit vergroot de kans op fouten en dubbele gegevens, wat je juist met klasses wilt voorkomen. Om dit soort situaties te voorkomen, wordt *overerving* gebruikt. Als we een klasse Voertuig maken en deze drie functies erin opnemen en de rest van de klassen van de voertuigklasse erven, kunnen we eenvoudig de duplicatie van gegevens vermijden en de herbruikbaarheid vergroten. Kijk naar het onderstaande diagram waarin er een overerving is van de drie klassen uit de voertuigklasse:

```
							|	Class Voertuig			|
							|---------------------------|
							|	brandstofHoeveelheid()	|
							|	aantalPersonen()		|
							|	remmen()				|
							|---------------------------|
							/			|				\
						   /			|				 \
						  /				|				  \ 
						 /				|					\
						/				|					 \

| 	Class Bus				|	Class Auto				|	Class Vrachtwagen		|
|---------------------------|---------------------------|---------------------------|

```

Gebruiken we overerving, dan schrijven we de functies maar een keer op in plaats van drie keer. omdat de drie *sub*-klassen (Bus, Auto en Vrachtwagen) de functionaliteit erven van de *base* klasse. (Voertuig) 

**Implementatie van overerving in C++**: Voor het creëren van een sub-klassedie een overerving heeft van een base klasse geld de volgende syntax.
**Syntax**:

```c++
class sub-klassenaam : access_mode base-klassenaam
{
  // body van de sub-klasse
};
```

Hier is *sub-klassenaam* de naam van de sub-klasse, *access_mode* is de modus waarin je deze *sub*- klasse wilt erven, bijvoorbeeld:  *public*, *private* enzovoorts en *base_klassenaam* is de naam van de base klasse waarvan u de sub- klasse wilt erven. .
**Opmerking:** een afgeleide klasse krijgt niet de toegang tot private data members . De afgeleide klasse neemt echter wel het alle members en functies van het volledig bovenliggend object over. Dus ook de private members die in deze *base* klasse zijn door gedeclareerd.

```c++
// C++ programma als voorbeeld voor overerving (Inheritance)

#include <std.h> 
using namespace std; 

//Base klasse 
class Ouder 
{ 
	// Declaratie
	public: 
	int idOuder; 
}; 

// Sub klasse met een overerving van Base klasse(Ouder) 
class Kind : public Ouder 
{ 
	// Declaratie
	public: 
	int idKind; 
}; 

//main function 
int main() 
{ 
		// Constructie
		Kind object1; 
		
		// Een object van de klasse Kind heeft alle data members
		// en alle member functies van de klasse Ouder 
		// Initialisatie
		object1.idKind = 7; 
		object1.idOuder = 91;
        
        // UI
		cout << "Het Id van het kind is " << object1.idKind << endl; 
		cout << "Het Id van de ouder is " << object1.idOuder << endl; 
		
		return 0; 
} 
```

Output:

```
Het Id van het kind is 7
Het Id van de ouder is 91
```

### Modes van overerving

**public mode:** als we een sub-klasse afleiden uit een *public* base klasse. De *public* members van de base klasse worden *public* members in de afgeleide sub-klasse en *protected* members van de base klasse worden *protected* members van de afgeleide sub-klasse.

**Protected mode:** als we een sub-klasse afleiden uit een *protected* base klasse. Zowel de public als de  protected members van de base klasse worden *protected* members in de sub-klasse.

**Private mode:** als we een sub-klasse van een private base klasse afleiden. Zowel de public als de protected members van de base klasse worden private members van de afgeleide sub-klasse.

**Opmerking:** de private members in de base klasse kunnen niet rechtstreeks worden benaderd in de afgeleide sub-klasse, terwijl protected members rechtstreeks kunnen worden benaderd. Klassen B, C en D bevatten bijvoorbeeld allemaal de variabelen x, y en z in het onderstaande voorbeeld. Het is alleen maar kwestie van toegang.

```c++
// C++ implementatie als voorbeeld dat een afgeleide sub-klasse
// niet de toegang de toegang van de private data members erft.
// Echter, de afgeleide sub-klasse erft wel het gehele parent object

class A 
{ 
public: 
	int x; 
protected: 
	int y; 
private: 
	int z; 
}; 

class B : public A 
{ 
	// x is public 
	// y is protected 
	// z is niet toegankelijk vanuit B 
}; 

class C : protected A 
{ 
	// x is protected 
	// y is protected 
	// z is niet toegangelijk vanuit C 
}; 

class D : private A // als je niks expliciet aangeeft maakt de compiler
					// data members privatefor classes 
{ 
	// x is private 
	// y is private 
	// z is not toegankelijk vanuit D 
}; 
```

Hieronder een tabel met de samenvatting van de drie toegangs-modi. De tabel toont ook de access  definitie van de members van de base klasse in de afgeleide sub-klasse wanneer de sub-klasse is afgeleid in public, protected en private modus:

| Base klasse  members<br />Access specifiers | Type overerving     |                     |                     |
| ------------------------------------------- | ------------------- | ------------------- | ------------------- |
|                                             | Public              | Protected           | Private             |
| Public                                      | *Public*            | *Protected*         | *Private*           |
| Protected                                   | *Protected*         | *Protected*         | *Private*           |
| Private                                     | *Niet toegankelijk* | *Niet toegankelijk* | *Niet toegankelijk* |

