# UML schematechmieken

## USE CASE en Activiteiten diagrammen

## Klasse diagrammen

Zie ook het hoofdstuk Informatica m.b.t. naming conventions

### Relaties tussen klassen

- Associaties
    - Bijzondere associatie: __Reflexieve__ associatie
    - Associatieklasse 
    
    ``Modelleer een associatieklasse bij een associatie als er attributen of methoden bij de associatie horen ie niet bij een van de betrokken klassen horen``
 
    Eigenschappen van een associatie:
    - Naam
    - Rol
    - Multipliciteit
    *, 0..1, 0..*, 1..*
    - Navigeerbaarheid
        - 1 richting als de ene klasse kennis heeft van de andere

``Modelleer een associatie tussen klassen als tenminste een van de klassen kennis over de andere klassen vasthoudt.``

``Beschrijf namen van associaties in gebruikerstaal``

``Modelleer geen aggregaties``

``Modelleer een compositie als een klasse onderdeel is van een andere klasse, en nooit als onderdeel van een andere klasse mag gelden``

//TODO blz 360 en verder uit het boek van Hoogendoorn          
Regels voor het omzetten van een klasse diagram naar een database diagram (=Bachman diagram)
