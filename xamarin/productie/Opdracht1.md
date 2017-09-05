# Opdracht 1

## 0. Opdrachtomschrijving

- Installatie en configuratie
- Hello World App

De opdracht bestaat uit bovenstaande 2 onderdelen. 

### 0.1 Zet in je visual studio team services pagina de volgende sprint (sprint 1)

Deze sprint heeft als einddatum 1 week later dan het moment dat de opdracht in de klas is uitgelegd.
![Sprint 1](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/sprint1.png?raw=true)

Zet in je teams services pagina 

## 1. Installatie en configuratie van software onderdelen 

### 1.1 Installatie Visual Studio 2017 Enterprise

Je laptop draait op Windows 10 en je hebt Visual Studio 2017 Enterprise geinstalleerd.
De enterprise versie kun je downloaden vanaf Microsoft Imagine voorheen Dreamspark, waarbij alle leerlingen een account hebben.

Als je Visual Studio 2017 installeert moet je alle opties aanvinken volgens de volgende afbeelding:

Ook als je Visual Studio 2017 al hebt geinstalleerd kun je via de VS Installer programma controleren of je alle onderdelen die je nodig wel hebt geinstalleerd.

Onder de workloads moeten de volgende onderdelen zijn aangevinkt:
![Installer screendump 1](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/installer1.png?raw=true)

![Installer screendump 2](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/installer2.png?raw=true)

### 1.2 Android SDK Manager (VS2017)

Je hebt in de Android SDK alle software voor de versie lollipop (of hoger) bijgewerkt en geinstalleerd.

![Android SDK](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/androidsdk.jpg?raw=true)

Je hebt in de Android SDK onder de folder tools alle software geinstallleerd.

Je hebt in de Android SDK onder de folder extras: Android Support Repository en Google USB Driver geinstalleerd.

### 1.3 NuGet packetmanager (VS2017)

Je hebt in de NuGet packetmanager in visual studio Xamarin.Forms geinstalleerd/geupdate.

![NuGet package Xamarin.Forms](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/xamforms.jpg?raw=true)

### 1.4 Testen van de App: Android Emulator of Android Device
 
#### 1.4.1 Emulator

__Virtualisatie__

Je hebt [hyper-V](https://msdn.microsoft.com/nl-nl/virtualization/hyperv_on_windows/quick_start/walkthrough_install) in windows 10 aangezet.

Zie ook deze installatie [video](https://developer.xamarin.com/videos/?v=Installing_Xamarin_on_Windows).

Je hebt in Visual Studio [Android Player](https://www.visualstudio.com/en-us/features/msft-android-emulator-vs.aspx) een (mobiele) device aangemaakt die minimaal de Android versie Lollipop (welk versienummer en/of API level is dat ?) heeft.

![visual studio android player](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/vsplayer.jpg?raw=true)

Als alternatief voor de visual studio player is [Xamarin  player](https://developer.xamarin.com/releases/android/android-player/).

Als tweede alternatief voor een android player kun je ook [genymotion](https://www.genymotion.com/thank-you-freemium/) gebruiken.

Natuurlijk kun je je Android App ook installeren en testen op je eigen android telefoon.


#### 1.4.2 Device

## 2 Opdrachtomschrijving tweede onderdeel

Bouw je hello world Android App volgens onderstaande visuele weergave
 
### 2.1 Visuele weergave

![Hello world opdracht](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/helloworld.jpg?raw=true)

### 2.2 Stappen

- Maak een nieuwe solution vanuit het team explorer venster, waarin de focus staat op je eigen visual studio team services pagina. 
Klik hier op New Solution.

![New Solution](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/newsolution.png?raw=true)

In het geopende venster:
- Klik op Cross-Platform en Cross Plaform App(Xamarin)
- Geef een goede naam voor de App

![New Project](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/newproject.png?raw=true)

- Vervolgens kies de opties volgens de volgende afbeelding:

![App Options](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/appoptions.png?raw=true)
 
- Start de Visual Studio Emulator

![Visual Studio Emulator](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/vsemulator.png?raw=true)

- Zodra de emulator is opgestart, start dan de debug volgens de afbeelding:

![Start debug proces](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/startdebug.png?raw=true)

### 2.2 Beoordelingscriteria

- Je App draait foutloos op een device of op je eigen android device. (Android versie maakt nog even niet uit)
- Je hebt een nieuwe (cross-platform) project gestart, Blank App, Xamarin.Forms (Shared)
- Je hebt de tekst en kleur aangepast volgens de visuele weergave
- Je hebt alle taken in je team services pagina op done gezet
- Je hebt op je team services pagina a.saebu@kw1c.nl toegevoegd als teammember
