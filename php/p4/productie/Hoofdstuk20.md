#### [kleurcode]rgba(19, 36, 160, 0.9)

# Hoofdstuk 20 Database connectie PHP met de lokale MSSQL server via odbc

## 20.1 Lokale connectie

Tot nu toe hebben we onze php-code niet lokaal kunnen testen, omdat we geen lokale MySQL database hebben draaien.
Voor ASP en het vak database SQL is er echter wel een MSSQL server database geinstalleerd en wordt deze server ook automatisch gestart
wanneer je laptop wordt opgestart.

Het ligt nu voor de hand om ook te kijken of we ook een connectie kunnen leggen met een MSSQL database en tabel, en of we daar ook 
op dezelfde manier gegevens kunnen selecteren, toevoegen en verwijderen.

## 20.2 Lesopdracht 

Voordat we een connectie kunnen leggen moeten we natuurlijk ook een ijdb database en een joke tabel aanmaken in deze lokale omgeving.
Open je SQL Server Management studio en maak hierin een ijdb database aan en een joke tabel met dezelfde velden als de joke tabel op
de c9 server. Voeg ook alvast een goeie grap in via deze beheertool.