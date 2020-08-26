#### [kleurcode]rgba(85, 39, 176,1)

# Opdracht 2 over UNIONS, EXCEPT, INTERCEPT 

## Nieuwe keywords 

## Voorbeeld met UNION keyword

- Maak van de laatse 5 jaren per jaar een top 3 van de films met titel, releasedatum, oscarnominaties en genre

## Voorbeeld met EXCEPT, INTERCEPT keyword

SELECT ProductID   
FROM Production.Product ;  
--Result: 504 Rows  

SELECT ProductID   
FROM Production.Product  
INTERSECT  
SELECT ProductID   
FROM Production.WorkOrder ;  
--Result: 238 Rows (products that have work orders)  

SELECT ProductID   
FROM Production.Product  
EXCEPT  
SELECT ProductID   
FROM Production.WorkOrder ;  
--Result: 266 Rows (products without work orders)  

## Opdrachtomschrijving opdracht 2

//TODO