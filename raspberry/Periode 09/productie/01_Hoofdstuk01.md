####[kleurcode]rgba(244,67,54,1)

# Hoofdstuk 1: Werkend krijgen van de Pi


##1.1 Inleiding

Een Raspberry Pi computer kost zo’n 40 euro. Deze lage prijs is één van de redenen voor de grote populariteit.  Echter, er zijn ook nog wat andere onderdelen nodig om met de Pi te kunnen werken. Hierdoor loopt de prijs eerder tegen de 90 euro (en meer als je geen scherm beschikbaar hebt). 

In bijlage 1 van dit boek vind je een overzicht van alle hardware die in dit boek wordt gebruikt. Sommige onderdelen zijn essentieel, bijvoorbeeld een USB stick of SD kaart, maar andere onderdelen worden maar in één van de paragrafen gebruikt , zoals de LoRa module in Project 2  of de Compute Module uit project 3. Schaf deze onderdelen pas aan als je zeker weet dat je het desbetreffende project gaat uitvoeren.

De onderstaande onderdelen worden gebruikt in alle hoofdstukken.:

1. Raspberry Pi 3B+
2. voeding (5 Volt USB adapter en USB 2.0 kabel A Male naar Micro B Male)
3. behuizing (doosje) voor Raspberry Pi
4. SD kaart (of USB stick) met operating system Raspbian
5. hdmi kabel voor verbinden Raspberry Pi en scherm
6. tussenstukje voor hdmi en ingang beeldscherm (als beeldscherm een hdmi ingang heeft dan is een hdmi/hdmi snoer voldoende)
7. beeldscherm
8. USB muis
9. USB toetsenbord

##1.2	Installeren Raspberry Pi

Bekijk allereerst de Raspberry Pi goed en vergelijk deze met onderstaand plaatje. Ga nog niet de componenten aansluiten.

![RPi overzicht](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.34%20RASP%5DRaspberry%20Pi%20Challenge/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/04.%20Aanvullend/Images/overzicht-Raspberry-Pi.jpg)

De SD kaart aansluiting wordt over het algemeen een kaart geplaatst waarom het besturingssysteem voor de RPi staat. Vaak is dit Raspbian (een Linux variant). Het besturingssysteem is nodig om de RPi op te starten.

Sinds Raspberry Pi versie 3 is het ook mogelijk om de RPi te *booten* (op te starten) met Raspbian op een USB stick. Aangezien SD kaarten af-en-toe corrupt raken bij het aan- en uitzetten van de RPi gebruiken we in dit boek de USB stick voor booten van de Pi.

De USB poorten worden ook gebruikt om een muis en toetsenbord aan te sluiten.

Connectie met een netwerk zoals internet kan via de ethernet aansluiting, maar vanaf RPi versie  3 is er ook ingebouwd een wifi mogelijkheid. Uiteriaard kan ook een USB poort gebruikt worden om een externe wifi adapter te plaatsen. 

Beeld en geluid wordt naar de monitor verzonden via een HDMI kabel. Sommige monitoren hebben geen HDMI ingang. In dat geval is een tussenstukje nodig (bijv. hdmi-vga of hdmi-dvi)

De  GPIO pinnen ga je pas gebruiken in hoofdstuk 5. Hierop kunnen bijvoorbeeld lampjes of sensoren worden aangesloten.  

##1.3 Installatie van Raspbian

Raspbian is het besturingssysteem speciaal gemaakt voor de Raspberry Pi. Het is een variant van Linux.  Dit is een van de meest succesvolle besturingssystemen., rond de 60% van de servers werkt met Linux. Het is overigens ook mogelijk om een ander besturingssysteem te gebruiken. In hoofdstuk 13 wordt Windows IoT gebruikt.

Versies 1 en 2 van de RPi kunnen alleen opstarten als het besturingssysteem op een SD kaart. Vanaf versie 3 werkt Raspbian op een USB stick ook, maar voor versie 3b is het nodig om eerst op te starten met een SD kaart en vervolgens enige aanpassingen te doen op de Pi. De nieuwste versie (3B+) werkt direct met een USB stick met Raspbian. 

Aangezien SD kaarten af-en-toe corrupt raken bij het aan- en uitzetten van de RPi gebruiken we in dit proejct de USB stick voor booten van de Pi.

Let op: niet alle merken USB sticks kunnen worden gebruikt. De volgende werken in ieder geval wel:[[1\]](#_ftn1) 

- Sandisk Cruzer Fit 16GB
- Sandisk Cruzer Blade 16GB
- Samsung 32GB USB 3.0 drive
- MeCo 16GB USB 3.0
- Toshiba Transmemory U202 16GB (verkrijgbaar in *'t Winkeltje* KW1C)

Het is mogelijk om SD kaarten te kopen waarop Raspbian al aanwezig is[[2\]](#_ftn2),maar de meeste mensen zullen de software zelf dowloaden en installeren. Hiervoor moet je onderstaande stappen volgen. Wil je gebruik maken van een micro SD kaart dan heb je natuurlijk een SD sleufhouder nodig.

**Stap 1)** Download het gewenste besturingssysteem op de site [https://www.raspberrypi.org/downloads](https://www.raspberrypi.org/downloads)

 Op deze pagina kan je verschillende besturingssystemen downloaden. De echte beginner kan de NOOBS versie downloaden. De lezer van dit boek kan ook een beginner zijn, maar omdat we toewerken naar een hoger niveau gaan we direct aan de slag met Raspbian.

![Download Page](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.34%20RASP%5DRaspberry%20Pi%20Challenge/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/04.%20Aanvullend/Images/Raspbian%20Download%20page.png)

Kies hier voor Raspbian ( vervolgens kies je
voor de ‘*Raspbian with deskop*’ versie, niet voor de Lite versie).

**Stap 2)** Waarschijnlijk heb je een .zip file gedownload. Pak deze vervolgens uit (unzip). Dit kan bijvoorbeeld met met 7-zip voor Windows of Unarchiver voor Mac.

**Stap 3)** Het uitgepakte image moet daarna worden neergezet op de USB stick of SD kaart.[[3\]](#_ftn3) Dit kan je doen met het programma [Etcher](https://etcher.io/) of [Win32DiskImager](https://sourceforge.net/projects/win32diskimager/files/Archive/).

**Stap 4)** Doe je USB stick (of SD kaart) in je computer en start Etchter, Je krijgt dan die scherm:

![Etcher1](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.34%20RASP%5DRaspberry%20Pi%20Challenge/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/04.%20Aanvullend/Images/Etcher1.jpg)

**Stap 5)** Vervolgens kies voor je juiste image en de juiste drive en klikt op Flash. Na enige tijd is de SD kaart  of USB stick klaar:

![Etchter2](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.34%20RASP%5DRaspberry%20Pi%20Challenge/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/04.%20Aanvullend/Images/Etcher2.jpg)

**Stap 4 en 5** kunnen ook uitgevoerd worden met Win32DiskImager. 

![W32DiskImager](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.34%20RASP%5DRaspberry%20Pi%20Challenge/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/04.%20Aanvullend/Images/W32DiskImager.png)

##1.4 Opstarten RPi voor de eerste keer.

Je gaat nu alle componenten aan elkaar koppelen. Het inpluggen van de voeding doe je als laatste. 

Afhankelijk van de Raspberry Pi versie gebruik je een SD kaart of USB stick met Raspbian. 

- Raspberry Pi versies 1 en 2 werken uitsluitend met een SD kaart.
- Raspberry Pi versie 3B start je allereerst met een SD kaart en vervolgens voer je de acties uit zoals beschreven in toelichting 1 (aan het eind van deze paragraaf). 
- Raspberry Pi 3B+ start je direct met een USB stick.

Na het opstarten krijg je waarschijnlijk de vraag om een aantal acties te doen (Before you start using it, there are a few things te set up). 

Klik op ‘*Next*’ en kies vervolgens voor ‘*Nederland*’ bij country en klik weer op ‘*Next*‘

Vervolgens mag je het wachtwoord aanpassen. Zolang je geen ‘geheime’ gegevens op de RPi zet dan zou ik dit voorlopig op het standaard wachtwoord ‘raspberry’ houden, zodat je jezelf niet buitensluit omdat je het wachtwoord niet meer weet. 

Je kan ook de wifi instellen en Raspbian upgraden. 

**Toetsenbord**

Een veelvoorkomend probleem is dat standaard een Engels toetsenbord is (de Raspberry Pi komt uit het Verenigd Koninkijk).   In Nederland worden meestal toetsenborden met een Amerikaanse indeling verkocht. Als sommige tekens (zoals @ of “ ) niet op het scherm verschijnen als je ze intypt dan moet je waarschijnlijk het sturingsprogramma voor toetsenborden aanpassen. Dit doe je als volgt:

1) Klik op het Raspberry ikoontje en kies voor ‘*Preferences*'. Vervolgens klik je op ‘*Mouse and Keyboard Settings*’ (zie afbeelding)

![Desktop Prefences](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.34%20RASP%5DRaspberry%20Pi%20Challenge/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/04.%20Aanvullend/Images/Desktop%20-%20preferences.jpg) 

2) Bij het tabblad ‘*Keyboard*’ kies je bij Layout voor ‘*English (US)*’ (als je inderdaad een Amerikaans toetsenbord hebt).

![Desktop Prefences -keyboard](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.34%20RASP%5DRaspberry%20Pi%20Challenge/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/04.%20Aanvullend/Images/Desktop%20-%20preferences.keyboard.jpg)

Na een reboot controleer je of  tekens zoals **@** of  **“**  inderdaad op het scherm verschijnen.

In het volgende hoofdstuk krijg je de basis van Linux uitgelegd..

##1.5 Maak RPi versie 3B klaar voor booten met USB

Zoals uitgelegd in paragraaf 1.3; de Raspberry Pi versies 3B en 3B+ werken ook met Raspbian op een USB stick. Voor versie 3B is het echter nodig om eerst een keer met een SD kaart op te starten en wat aanpassingen te doen. Deze aanpassingen zijn hieronder beschreven: [[4\]](#_ftn4)

**Stap 1)** start de RPi met een SD kaart en ga naar Terminal. Dit doe je door te klikken op het ikoontje linksboven:

![img](https://elo.kw1c.nl/CMS/Studie/811%20ICT-Academie/811%20VakkenInhoud/%5BB.34%20RASP%5DRaspberry%20Pi%20Challenge/25187%20%C2%A0%20Applicatie-%20en%20mediaontwikkelaar/Periode%2009/Productie/04.%20Aanvullend/Images/Prompt.jpg)

**Stap 2)** In terminal type je de volgende regel:

```
sudo apt-get update && sudo apt-get upgrade
```
hiermee zorg je dat Raspbian helemaal up-to-date is.

**Stap 3)** In terminal type je nu de volgende regel:

```
echo program_usb_boot_mode=1 | sudo tee -a /boot/config.txt
```

Je voegt hiermee de regel `program_usb_boot_mode=1` toe aan het bestand  '*/boot/config.txt*'. Hiermee zorg je er voor dat de Pi ook met USB kan booten.`

In hoofdstuk 2 krijg je meer uitleg over dit soort Linux opdrachten.

**Stap 4)** Na de reboot controleer je of de USB mogelijkheid inderdaad aangezet is. Dit doe je met de opdracht:

```
vcgencmd otp_dump | grep 17
```

Krijg je als antwoord *17:3020000a* dan werkt het inderdaad. Krijg  je een ander antwoord, bekijk dan wat er fout gaat.

------

[[1\]](#_ftnref1) [https://www.raspberrypi.org/blog/pi-3-booting-part-i-usb-mass-storage-boot](https://www.raspberrypi.org/blog/pi-3-booting-part-i-usb-mass-storage-boot)
[[2\]](#_ftnref2) Bijvoorbeeld bij sossolutions.nl
[[3\]](#_ftnref3) Zie ook: [https://www.raspberrypi.org/documentation/installation/installing-images/README.md](https://www.raspberrypi.org/documentation/installation/installing-images/README.md)
[[4\]](#_ftnref4) bron: [https://www.raspberrypi.org/documentation/hardware/raspberrypi/bootmodes/msd.md](https://www.raspberrypi.org/documentation/hardware/raspberrypi/bootmodes/msd.md)

