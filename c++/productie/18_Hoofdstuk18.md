####[kleurcode]rgba(255,192,0,1)

#HOOFDSTUK 18#

In hoofdstuk 18 wordt de volgende onderwerpen uitgewerkt in de opdracht:

- Gebruik van klassen om de data  van het kennisgrammatica diagram en de functies die hier toegang tot hebben, in op te slaan;
- Gebruik van scope operator om de implementatie van methoden buiten de klasse te kunnen plaatsen.

##KLASSEN##

Klassen vormen de basis van object georienteerd programmeren. Elke klasse heeft functies waar ieder object van die klasse gebruik van kan maken. Elk object bevat ook gegevens, de *attributen* van het object en deze attributen zijn, net als de functies, ook in de klasse gedefineerd.

Kort gezegd:

* Een klasse is een omschrijving voor objecten;
* In een klasse zijn attibuten en functies gedefinieerd;
* Een object is een ding dat gemaakt is volgens die omschrijving;
* Elk object kan gebruikmaken van de functies en gegevens (attributen) die in de klasse zijn gedefinieerd.

##KLASSENDIAGRAM##
Een klassendiagram is een van de vele zogeheten *UML-diagrammen*. UML is de afkorting van *Unified Modeling Language*. UML is een beeldtaal waarmee verschillende aspecten van een programma  kunt weergeven.

In een klassendiagram wordt de klasse door middel van een rechthoek, die uit drie gedeelten gestaat.

```uml
 -------------------
|  Leerling         |  <-- Naam van de klasse.
|-------------------|
| l_nm : string     |
| l_nr : int        |  <-- Attributen van de klasse.
| k_nm : string     |
|-------------------|
| Invoeren() : void |  <-- Functies (methods) van de klasse.
| Weergeven(): void |
 -------------------
```

* In het bovenste deel staat de naam van de klasse,
* In het middelste deel staan de attributen en
* in het onderste deel staan de namen van de functies.

##IMPLEMENTATIE##
**kop**

In de broncode begint de defenitie van een klasse met de kop van de klasse die bestaat uit het woord *class* gevolgd door de naam van de klasse. De defenitie eindigt met een puntkomma:

```c++
class Leerling
{

};
```
Achter de kop en voor de puntkomma staat tussen de accolades de *body* van de klasse, die de feitelijke inhoud bevat. In de meeste gevallen staan in de body een paar attributen en een aantal functies.

**attributen**

De attributen van de klasse definieer je in de body van de klasse op de volgende wijze.

```c++
class Leerling
{
	private:
		string l_nm;
		string k_nm;

	public:
		int l_nr;
};
```

Door middel van het woord *private* met een dubbele punt geef je aan dat de attributen die erop volgen zijn afgeschermd voor de buitenwereld. Ze zijn dus niet benaderbaar voor code buiten de klasse.
Alleen functies die in de klasse zijn gedefinieert, hebben toegang tot de attributen. 
Naast de lokale en globale variabelen is er dus nog een derde soort variabele. Een variabele (attribuut) die alleen bestaat binnen een klasse.

Naast de *private* attributen is het ook mogelijk aan te geven of de attributen wel beschikbaar zijn voor de code buiten de klasse dit wordt geven we aan met het woord *public*.

In een UML klassendiagram wordt het *private* of *public* zijn van een attribuut aangegeven met een minteken of een plusteken.

```uml
 -------------------
|  Leerling         |
|-------------------|
|- l_nm : string    |
|+ l_nr : int       |
|- k_nm : string    |
|-------------------|
| Invoeren() : void |
| Weergeven(): void |
 -------------------
```

**constructor**

De attributen in de klasse vormen het geheugen van het object. Om deze attributen een beginwaarde te geven bij het aanmaken van het object (*initialiseren*) is het mogelijk om hiervoor de *constructor* te gebruiken.

Een *constructor* is een soort functie die:

* *dezelfde naam* heeft als de klasse waartoe hij behoort;
* wordt uitgevoerd zodra je een *nieuw* object van die klasse maakt;
* in de meeste gevallen zorgt voor *initialisatie* van de attributen van het object;
* geen *return* waarde heeft, ook geen *void*.

Als een klasse geen constructor heeft , maakt de compiler automatisch een *defaultconstructor* aan. Een *defaultconstructor* doet niets anders dan een object construeren. De attributen in het object krijgen *geen* speciale waarde. Er vindt dus geen *initialisatie* van de attributen plaats.

**methoden**

Het is niet voldoende om gegevens op te slaan in een object. Je moet die gegevens ook kunnen wijzigen of er iets mee kunnen doen. Daarom heb je functies nodig. Via de functies zijn alle attributen van de klasse benaderbaar 
Om het hergebruik van klassen te vergroten is het gebruikelijk  om het *prototype* van de klasse (defenitie) en de *implementatie* van de functies van elkaar te scheiden.
In functies die in klassen worden gedefnieerd noemen we *methoden*

In de klasse komt van een methode dan alleen zijn *prototype* of *declaratie* te staan. De *implementatie* van de body van de methode komt buiten de klasse te staan. 
Met de **scope- operator ::** maakt de compiler  duidelijk bij welke klasse de implementatie hoort.

```c++
class Leerling
{
	private:
		string l_nm;
		string k_nm;

	public:
		int l_nr;
	
	// constructor
	Leerling() {}
	
	// methoden (prototype)
	void Invoeren();
	
	void Weergeven();
};

// implementatie
void Leerling::Invoeren()
{

}

void Leerling::Weergeven()
{

}
```

##TOEPASSING##
Een klasse kun je niet direct gebruiken om hier data in op te slaan. Een klasse is een bouwtekening (datatype) om een object mee te construeren. De declaratie is als volgt:

```c++
#include Leerling.h

int main()
{
	Leerling leering1;
	
	leerling1.Invoeren();
	leerling1.Weergeven();
	
	cout << "Het leerlingnummer is: " << leerling1.l_nr;
}
```