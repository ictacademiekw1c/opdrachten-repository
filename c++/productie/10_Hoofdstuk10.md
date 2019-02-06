####[kleurcode]rgba(255,192,0,1)

#HOOFDSTUK 10#
In hoofdstuk 10 wordt het volgende onderwerp uitgewerkt in de opdracht:
- Gebruik van een array om de data van het kennisgrammatica diagram in op te slaan.


##ARRAYS##
Een array is een zogeheten datastructuur waarin je veel waarden van hetzelfde type kunt opbergen. "Veel" betekend dat het aantal elementen in de array kunnen varieren van enkel tot vele tienduizenden.
Je moet echter al bij de declaratie aangeven hoeveel elementen er zijn. 

###Declaratie###
een voorbeeld van een declaratie van een C-array die a heet en waarin vijf int-waarden kunnen worden opgeborgen ziet er zo uit:

``` C++
// Declaratie
int a[5];
```
schematisch ziet deze array er in het geheugen van de computer uit als in de volgend figuur.

```
| index   | inhoud | element    |
|         |        | naam       |
|---------|--------|------------|
|   0     |   22   | a[0]       |
|   1     |   12   | a[1]       | 
|   2     |    5   | a[2]       |
|   3     |    7   | a[3]       |
|   4     |   16   | a[4]       |
```
De array bestaat uit 5 elementen. Om de elementen van een array van elkaar te kunnen onderscheiden zijn ze genummerd. Elk element heeft een eigen nummer, de *index* van dat element. 

Met behulp van de naam van de array en de index krijgt elk element zijn eigen naam. In dit voorbeeld *a[0], a[1], a[2], a[3], a[4],*. De vierkante haken die je in deze notatie gebruikt heten de subscript-operator of index-operator.

###Initialisatie###
``` C++
// Initialisatie
int a[5] = { 12, 23, 34, 45, 56 } ;
//of
int a[] = { 12, 23, 34, 45, 56 } ;
```

###Toekennen###
``` C++
// Toekennen
int b;
b = a[2];
//of
cout << a[1];
```
C++ Compiler heeft geen Array checking. Gebruik dus altijd een constante om de lengte van het Array aan te geven.

``` C++
const int MAXARRAY = 5;
```

###Aanroep in functies###
```
// declaratie
int registratie[3];
int b;

// prototype
void InvoerenLeerling(int []);
int WeergevenNummerLeerling(int []);


// implementatie
void InvoerenLeerling(int x[]);
{
    x[0] = 12345;
}

int WeergevenNummerLeerling(int y[])
{
   return y[2];
}

int main()
{
    InvoerenLeerling{registratie);
    b = WeergevenNummerLeerling(registratie);
}
```
###Kopieren van arrays###
```
for (int 1=0; i<10;i++)
{
     x[i]=y[i]; // Kopieer de inhoud van elk element van y op dezelfde index in x
}
```


###Voor- en nadelen van C-arrays###
1. Een C-array heeft een vaste grootte die je al in de broncode moet vastleggen.
2. Een C-array kun je niet op een vanzelfsprekende manier kopieren.
3. Je kunt niet op een vanzelfsprekenende manier twee C-arrays met elkaar vergelijken.


##TWEEVOUDIGE ARRAY##
Een tweevoudige of tweedimensionale array bestaat uit rijen en kolommen  waarin je gegevens van hetzelfde type kunt opslaan. Het is gebruikelijk om in zo'n array de gegevens van tabellen of matrices in op te bergen.

De declaratie van een tweevoudige array van gehele getallen kan er zo uitzien:

```
int voorraad[3][4];
```
De array voorraad heeft 2 indexen. Gebruikelijk is om eerst het aantal rijen te noemen en daarna het aantal kolommen.

voorraad[0][0] - Element linksboven
voorraad[2][3] - Element rechtsonder

### initialisatie tweevoudig array ###

```
int voorraad[3][4] =
{
     {12,6,3,2},
     {9,13,7,0},
     {7,4,8,5},
}
```
