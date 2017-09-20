# Sprint/Opdracht 3 Phoneword App

## Phoneword exercise in EdX Course

> Ga naar Module 3 Pages and Views > Hands-On Exercises > Goals.
Volg de [EdX HandsOn Exercises Module 3 Walkthrough](https://courses.edx.org/courses/course-v1:Microsoft+DEV215x+1T2016/courseware/04c272628e46433fa77f081f050ed9f4/ac997ad219294470a9d9e4109f517012/?activate_block_id=block-v1%3AMicrosoft%2BDEV215x%2B1T2016%2Btype%40sequential%2Bblock%40ac997ad219294470a9d9e4109f517012) en bouw de phoneword app zoals is beschreven. Volg de cursus t/m Module 4 tot de "end of course evaluation".

<br>``Let op: De walkthrough loopt nog door tot in module 4``

![Phoneword App](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/phoneword.png?raw=true)

## Leerdoelen
- Anatomie van een Xamarin.FORMS App zonder xaml
- Layout en views/user controls 
- Platsporm specifieke code schrijven met een DependencyService 

## Phoneword geschiedenis
[Phoneword geschiedenis op wikipedia](https://en.wikipedia.org/wiki/Telephone_keypad)


## Android specifieke code PhoneDialer.Droid.cs

Onderstaande klasse heb je nodig in je Droid project om de App ook echt in een Android te kunnen laten bellen.
[PhoneDialer.Droid.cs](https://gist.github.com/saebuabu/6321aa71487811f20c5ac29b9640d7e3)

## Beoordelingscriteria
1. Je kunt de programmastructuur van de App uitleggen; zet commentaar bij programmacode en leg uit in eigen woorden wat de verschillende classes en methoden doen.
2. Je hebt een eigen icon gebruikt voor de App.
3. Je hebt extra functionaliteit toegevoegd in de vorm van validatie en feedback in het invoersscherm

   > Implementeer:
   - telefoonnummer moet precies uit 10 tekens bestaan
   - telefoonnummer moet met een 0 beginnen
   - Sta alleen letters, cijfers en het - toe
   - Geef duidelijke terugkoppeling als de invoer niet juist is 

4. De App moet toestemming hebben om te kunnen bellen en heb je de toestemming toegevoegd aan de AndroidManifest.xml
5. Plaats elk vertaalde phoneword in een listview onderin het scherm. Zorg ervoor dat er unieke waardes worden getoond in de listview.
6. Je hebt een sprint 3 gemaakt in je VS team services met als backlogitems Module 3 en Module 4 van de edx workshop en het bouwen van de Phoneword App als apart backlog item. Verdeel het bouwen van de phoneword App in subonderdelen die ongeveer even groot/moeilijk zijn zodat je je werk beter kan inplannen.
