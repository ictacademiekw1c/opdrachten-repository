####[kleurcode]rgba(255,192,0,1)

#HOOFDSTUK14#
In hoofdstuk 14 worden de volgende onderwerpen uitgewerkt in de opdracht:
- Gebruik van *structs* om de data van het kennisgrammatica diagram in op te slaan
- Gebruik van het *reference*-argumenten in plaats van *value*-argumenten.


##STRUCT##
Een struct is een groep gegevenselementen die onder één naam zijn gegroepeerd. Deze gegevenselementen, ook wel *members* genoemd, kunnen verschillende typen en verschillende lengten hebben. *structs* kunnen in C ++ worden gedeclareerd met behulp van het volgende syntax:

```
struct type_naam
{
	member_type1 member_naam1;
	member_type2 member_naam2;
	member_type3 member_naam3;
	.
	.
} object_namen;
```

###Declaratie###
een voorbeeld van een declaratie van een C-struct die product heet en waarin een *int* en *double* waarden kunnen worden opgeborgen ziet er zo uit:

``` C++
//declaratie
struct product 
{
  int gewicht;
  double prijs;
};

product appel;
product banaan, meloen;
```

schematisch ziet deze *struct* er in het geheugen van de computer uit als in de volgend figuur.

```
|  member   |  type  | inhoud |   member    |
|           |        |        |    naam     |
|-----------|--------|--------|-------------|
| gewicht   | int    |   10   | a.gewicht   |
| prijs     | double |    2   | a.prijs     | 
```
De *struct* bestaat uit 2 *members*. Iedere *member* is van een ander *datatype*. Om de *members* van een *struct* van elkaar te kunnen onderscheiden hebben ze een eigen unieke naam. 

###Toekennen###
Met behulp van de naam van de *struct* en de naam van de *member* kun je de elementen individueel uitlezen en schrijven. In dit voorbeeld apple.gewicht, appel.prijs. De punt tussen de *struct*-naam en de *member*- naam heet de *punt*-operator.

``` C++
// Declaratie
struct product 
{
  int gewicht;
  double prijs;
} appel, banaan, meloen;

int main()
{
	appel.gewicht = 1000;
	appel.prijs = 2,99;
	
	banaan.gewicht = 500;
	banaan.prijs = 1,69
	
	meloen.gewicht = 750
	meloen.prijs = 2,39
}
```
**Kopieren van een struct**

```
struct Artikel
{
	string omschrijving;
	int nummer;
	double prijs;
}

Artikel artikel1;
artikel1.omschrijving = "driewieler";
artikel1.nummer = 101;
artikel1.projs = 72.35;

artikel2 = artikel1;
```

Na de toekenning hebben de *members* van artikel2 precies dezelfde waarden als de *members* van artikel1

###Structure als argument van een functies###
Net als andere variabelen kan een *struct* een *argument* zijn van een functie. en net als bij andere variabelen kan zo'n *argument* op drie manieren voorkomen, namelijk als 
- value-argument
- [reference](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.08%20C++%5D%20C++/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2007/Productie/04.%20Aanvullend/Reference-argument_AanDeSlagMetC++_2002.pdf);
- pointer;


```
\\Declaratie
struct Artikel
{
	string omschrijving;
	int nummer;
	double prijs;
}

void Print(Artikel);

main()
{
	Artikel artikel;

	artikel.omschrijving = "cd-speler"
	artikel.nummer = 20021;
	artikel.prijs = 335;

	Print(artikel);
}

void Print(Artikel a)
{
	cout	<< a.omschrijving << " , " 
			<< a.nummer << " , "
			<< a.prijs
			<< endl;
}

```

**Een reference-argument voor een structure**
Bij het aanroepen met *print(artikel)* in het voorbeeld wordt het formele argument *a* een kopie van het actuele argument *artikel1*. Het kopieren kost tijd en geheugenruimte en is onnodig: de functie kan net zo goed zijn werk doen met een refence-argument, dus zo:

```
void Print (Artikel &)
```
Door deze wijzigingen is het argument *a* geen kopie, maar een *alias* voor het actuele argument *artikel*. Dit betekent dat *print()* de inhoud van *artikel* kan wijzigen.

```
void Print (Artikel &a)
{
	.....
}

```
Voor een print-functie is het onnodig en ongewenst en je kunt met behulp van een *const reference-argument* vookomen dat zoiets gebeurt:

```
void Print (const Artikel &a)
{
	.....
}

```
Het voorbeeld zou dus op de volgende manier kunnen worden uitgewerkt.

```
struct Artikel
{
	string omschrijving;
	int nummer;
	double prijs;
}

void Print(const Artikel &);
void Invoer(Artikel &);

main()
{
	//Declaratie
	Artikel artikel1;

	Invoer(artikel1);
	Print(artikel1);
}
void Invoer(Artikel &a)
{
	a.omschrijving = "cd-speler"
	a.nummer = 20021;
	a.prijs = 335;
}

void Print(const Artikel &a)
{
	cout	<< a.omschrijving << " , " 
			<< a.nummer << " , "
			<< a.prijs
			<< endl;
}
```

----------------------
#Pointers vs reference (engels)#

A pointer can be re-assigned any number of times while a reference cannot be re-seated after binding.
Pointers can point nowhere (NULL), whereas reference always refer to an object.
You can't take the address of a reference like you can with pointers.
There's no "reference arithmetics" (but you can take the address of an object pointed by a reference and do pointer arithmetics on it as in *&obj + 5*).
To clarify a misconception:

The C++ standard is very careful to avoid dictating how a compiler must implement references, but every C++ compiler implements references as pointers. That is, a declaration such as:

```
int &ri = i;
```
if it's not optimized away entirely, allocates the same amount of storage as a pointer, and places the address of i into that storage.
So, a pointer and a reference both occupy the same amount of memory.

As a general rule,

- Use references in function parameters and return types to define useful and self-documenting interfaces.
- Use pointers to implement algorithms and data structures.

Interesting read:

- [C++ FAQ lite](http://yosefk.com/c++fqa/ref.html).
- [References vs. Pointers](https://www.embedded.com/electronics-blogs/programming-pointers/4023307/References-vs-Pointers).
- [An Introduction to References](https://www.embedded.com/electronics-blogs/programming-pointers/4024641/An-Introduction-to-References).
- [References and const](https://www.embedded.com/electronics-blogs/programming-pointers/4023290/References-and-const).
