# Opdracht 2

## Bouwen van pages (schermen) in Xamarin.Forms

## Voorbereiding

1. Doe de cursus op EdX [Xamarin.Forms](https://courses.edx.org/courses/course-v1:Microsoft+DEV215x+1T2016/info) en volg de modules 0 t/m 2.

2. En bestudeer de volgende slides over [Xamarin.Forms slideshow](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.29%20INFi%5D%20Informatica%20instructie/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/xamarinforms/parts/slides.pdf)

3. [Documentatie over welke verschillende pages](https://developer.xamarin.com/guides/xamarin-forms/controls/pages/) je kunt bouwen met Xamarin.Forms.

## Opdrachtomschrijving

Bouw een App met de volgende pages en interactie.

Laat de App starten met een MasterDetailPage waarbij in de 

    - Master pagina 2 buttons worden getoond
        - button1 opent een CarouselPage
        - button2 opent een TabbedPage

    - Detail pagina is dezelfde pagina als de TabbedPage die met button2 in de Master wordt geopend 

Toon in de CarouselPage minimaal 2 afbeeldingen.

Maak in de TabbedPage 3 tabs aan pagina 1, pagina 2 en pagina3 die ieder pagina's openen in een random achtergrondkleur.

Een randomkleur zou je kunnen aanmaken met:
~~~C#
   new Color(random.NextDouble(), random.NextDouble(), random.NextDouble())
~~~

## Visuele weergave

- Detail pagina
![Detail page](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/Opdracht1Detail.jpg?raw=true)

- Master pagina
![Master page](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/opdracht1Master.jpg?raw=true)

- ImageViewer pagina
![ImageViewer page](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/Opdracht1Imageviewer.jpg?raw=true)

## Beoordelingscriteria




