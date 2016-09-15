# Opdracht 2

## Bouwen van pages (schermen) in Xamarin.Forms

## Voorbereiding

1. Doe de cursus op EdX [Xamarin.Forms](https://courses.edx.org/courses/course-v1:Microsoft+DEV215x+1T2016/info) en volg de modules 0 t/m 3.

2. En bestudeer de volgende slides over [Xamarin.Forms slideshow](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.29%20INFi%5D%20Informatica%20instructie/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/xamarinforms/parts/slides.pdf)

3. [Documentatie over welke verschillende pages](https://developer.xamarin.com/guides/xamarin-forms/controls/pages/) je kunt bouwen met Xamarin.Forms.

4. [Hoe plaats ik een button op een pagina](https://developer.xamarin.com/guides/xamarin-forms/controls/views/)

## Opdrachtomschrijving

Bouw een App met de volgende pages en interactie.

Laat de App starten met een MasterDetailPage waarbij in de 

    - Master pagina 2 buttons worden getoond
        - button1 opent een CarouselPage
        - button2 opent een TabbedPage

    - Detail pagina is dezelfde pagina als de TabbedPage die met button2 in de Master wordt geopend 

    - Toon in de CarouselPage minimaal 2 afbeeldingen.

    - Maak in de TabbedPage 3 tabs aan pagina1, pagina2 en pagina3 die ieder pagina's openen in een random achtergrondkleur.

Een randomkleur zou je kunnen aanmaken met:
~~~C#
   new Color(random.NextDouble(), random.NextDouble(), random.NextDouble())
~~~

De TabbedPage en de CarouselPage worden gestart vanuit een NavigationPage met:
~~~c
    // De detail pagina wordt ingevuld met de RandomColorpage (=TabbedPage) vanuit een NavigationPage
    Detail = new NavigationPage(new RandomColorPage());
    // RandomColorPage (public class RandomColorPage : TabbedPage) 
~~~
## Programmastructuur

[Voorbeeld Master Detail App met 2 buttons](https://gist.github.com/saebuabu/f1d2df6aff2f683941ee4e3de98e736d)

[Voorbeeld TabbedPage met 2 tabs](https://gist.github.com/saebuabu/89c2a9735d2850f0327daa11780bfd75)

## Visuele weergave

- Detail pagina
![Detail page](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/Opdracht1Detail.jpg?raw=true)

- Master pagina
![Master page](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/opdracht1Master.jpg?raw=true)

Code voor de Master pagina
~~~C#

// Declaraties.
Button spawnTabbedButton = new Button() { Text = "Random Pagina Kleuren" };
Button spawnCarouselButton = new Button() { Text = "Carousel Page" };

//Click event op eerste button impleme
spawnTabbedButton.Clicked += SpawnTabbedButtonClicked; 
// Als er op de knop gedrukt wordt dan wordt de method "SpawnTabbedButtonClicked" uitgevoerd.
//Click event op tweede button ontbreekt

//Contentpagina met een stackLayout en 2 buttons
			Master = new ContentPage()
			{
				Title = "Menu",

//Een StackLayout kan gebruikt worden om meerdere controls onder of naast elkaar te zetten.
				Content = new StackLayout() 
				{
					Children = 
					{ 
						spawnTabbedButton,
						spawnCarouselButton
					}
				}
			};
...

...

    // method "SpawnTabbedButtonClicked" deze opent de RandomColorPage in een NavigationPage
	public void SpawnTabbedButtonClicked(object sender, EventArgs e)
    {
		Detail = new NavigationPage(new RandomColorPage());
	}

~~~

- Carousel pagina
![ImageViewer page](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/Opdracht1Imageviewer.jpg?raw=true)

## Beoordelingscriteria

- Maak voor iedere pagina een aparte class aan geimplementeerd met overerving van (TabbedPage,CarouselPage, MasterDetailPage)
- Afbeeldingen die in de carousel pagina worden getoond zijn lokaal toegevoegd aan de Resources/Drawable map




