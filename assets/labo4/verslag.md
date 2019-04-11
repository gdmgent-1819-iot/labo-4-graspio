*Internet Of Things MMP-NMD Morgane Bekaert en Anna De Langhe*
# Verslag Cloudio/GraspIO

### Doelstellingen:
* Wat is Cloudio/GraspIO
* Wat bevat Cloudio/GraspIO
* Wat kan je doen met Cloudio/GraspIO
* Projecten aanmaken

### Inhoudstafel:
* Introductie GraspIO
* Download Software
* Aansluiting GraspIO aan Raspberry
* GraspIO Studio
* Verbinding Wifi-netwerk

## Introductie GraspIO
![](labo4\1GraspIOelements.jpg)

1. **Temperatuur Sensor**  
Dit is een klein apparaatje waarin de fysische grootheid temperatuur - aangegeven in graden Celsius of Fahrenheit - wordt omgezet in een uit te lezen elektrisch signaal.
2. **IR Sensor/ Infrarood Sensor**   
Dit is een sensor die gebruik maakt van infrarood licht. Deze kan gebruikt worden om bewegingen te detecteren. De GraspIO Cloudio heeft een maximum waarnemingsafstand van 30 cm.  
![](labo4\2IRblock.jpg)  
    1. In het eerste vakje zie je het icoontje. Hier kan je kiezen tussen analoog of digitaal. Bij analoog kan je de analoge waarden laten lezen en vergelijken met de drempelwaarde tussen 0 - 999
    2. In het 2e vakje is er de keuze tussen interne IR sensor of externe sensor, aangesloten op één van de drie poorten op het bord.
    3. In het 3e vakje kan je het operant teken beslissen:
        * groter dan: >
        * kleiner dan: <
        * groter of gelijk aan: ≥
        * kleiner of gelijk aan: ≤
        * gelijk aan: ==
        * niet gelijk aan: !=
    4. In het 4e vakje vind je indien je voor analoog gekozen hebt de plaats waar je de waarde kan geven, die je dus tussen 0-999 kan ingeven.
    Heb je gekozen voor digitaal, dan kan je kiezen tussen de drempel toestanden die zullen worden vergeleken met de toestand die jouw IR-sensor in digitale modus ontvangt.
3. **Digitale switch**  
Een digitale schakelaar verwijst naar een drukknop die AAN (of UIT) staat wanneer deze wordt ingedrukt en UIT (of AAN) staat wanneer deze niet is ingedrukt. Wanneer de schakelaar wordt ingedrukt, zijn twee punten in het circuit aangesloten en is het circuit voltooid. Er dient echter te worden opgemerkt dat een drukknop slechts AAN (of UIT) staat totdat de gebruiker de schakelaar indrukt.
Deze switch kan in digitale modus worden gebruikt om de toestanden (hoog of laag) van de ingangen van een digitale schakelaar te ontvangen. De sensor kan de ingebouwde tactiele schakelaar (SW) zijn, of een externe sensor die aangesloten is op één van de poorten S1, S2 of S3.  
![](labo4\4Switchblock.jpg)
    1. Bij het icoontje in het eerste vakje kan je niets doen. 
    2. Daarnaast staat een vakje met “SW” dit staat voor de Switch. Hier kan je kiezen welke Port. Je hebt de switch van de GraspIO zelf maar je kan ook de 3 poorten aansluiten die naar een externe switch verwijzen.
    3. Het 3e vakje is het operant teken.
        * gelijk aan: ==
        * niet gelijk aan: !=
    4. Dan heb je nog het laatste vakje, daar kies je de status. Hoog of laag. We konden de optie “Read” gebruiken om real-time waarden van de geselecteerde poort te lezen en te ontvangen
De switch zal zich altijd bevinden in een if statement of dergelijke
4. **Licht sensor**  
Een lichtsensor genereert een uitgangssignaal dat de intensiteit van het licht aangeeft door de stralingsenergie in het lichtspectrum te meten. Het is een passief apparaat dat deze "lichtenergie" omzet in een elektrische signaaluitgang. Deze sensor kan worden gebruikt om analoge ingangen (gehele getallen in het bereik van 0 tot 999) van een lichtsensor te ontvangen. De sensor kan de ingebouwde omgevingslichtsensor zijn, of een externe sensor die is aangesloten op één van de poorten S1, S2, S3.  
![](labo4\5Lightblock.jpg)
    1. Bij het icoontje in het eerste vakje kan je niets doen. 
    2. Daarnaast staat een vakje met “LT” dit staat voor de Light. Hier kan je kiezen welke Port. Je hebt de lichtsensor van de GraspIO zelf maar je kan ook de 3 poorten aansluiten die naar een externe licht sensor verwijzen
    3. In het 3e vakje kan je het operant teken beslissen:
        * groter dan: >
        * kleiner dan: <
        * groter of gelijk aan: ≥
        * kleiner of gelijk aan: ≤
        * gelijk aan: ==
        * niet gelijk aan = !=
    4. In het laatste konden we een drempelwaarde van een geheel getal instellen om te vergelijken. Ook hier is de optie “Read” weer aanwezig.
5. **OLED scherm**  
Het OLED-blok wordt gebruikt om tekst, sensorwaarden en emojis op de OLED weer te geven. U kunt de inhoud van het blok instellen als aangepaste tekst (maximaal 100 tekens), realtime sensorwaarden die worden verzameld van de sensoren (aan boord of extern) die op het bord zijn aangesloten, of als een emoji geselecteerd uit een verzameling beschikbare emojis.  
![](labo4\6Oledblock.jpg)  
Hierin kan je kiezen voor het type: 
    * sensors
    * tekst
    * emoji
6. **Buzzer**  
Een zoemer (Engels: buzzer of beeper) is een elektromechanisch of elektronisch onderdeel dat onder spanning een luide zoem- of pieptoon opwekt, afhankelijk van de toonhoogte. Er bestaan elektromagnetische en piëzo-elektrische zoemers. Zoemers worden onder andere toegepast in alarmapparaten, telefoontoestellen, magnetrons, wekkers en in auto's bij veiligheidsgordels. Zoemers bestaan al heel lang en werden vroeger vaak in plaats van de ouderwetse elektrische deurbel gebruikt.
De buzzer op de Graspio is een piëzo-elektrische zoemer.  
![](labo4\7Buzzerblock.jpg)  
Bij de buzzer is het heel simpel,je kan op de buzzer de status aan en de status uit zetten.
7. **RGB led**  
Cloudio bevat RGB led's op de kaart.
RGB led's bestaan uit een rode, een groene en een blauwe led. Door elk van deze drie onafhankelijk van elkaar aan te passen, kunnen deze een breed scala aan kleuren produceren  
![](labo4\8Ledblock.jpg)  
Er kan eender welk kleur gekozen worden. Bij costom kan je eigen rood, groen en blauw toevoegen of aftrekken.
Ook hier is het simpel. De status is een kleur of de status is uit.
___

## Download software 

Bij het opstarten van de GraspIO moeten we natuurlijk ook een aantal softwares downloaden. Te beginnen met Etcher software. Deze software is nodig om GraspIO Software over te plaatsen naar de SD kaart van de Raspberry. Download en plaats deze op de computer.
Een tweede installatie is de GraspIO OS, sla dit op op de computer.

![](labo4\3Flash.jpg)

De software GraspIO OS moet op de SD kaart terecht komen. Dit deden wij als volgt:
1. Eerst moesten we starten met het plaatsen van de SD-kaart in de computer.  

<img src="labo4\9PiSD.JPG" width="500">  

2. Dan moesten we gaan zoeken in welk station (drive) ons SD kaart terecht komt in de computer.
3. Dan het opstarten en het open van Etcher
4. Kies voor selecteer afbeelding (select image)  
![](labo4\10Etcher.jpg)
5. Zoek naar de GraspIO waar je deze hebt opgeslagen en klik de afbeelding (image) open.
6. Selecteer dan “Select drive” om het juiste station te selecteren. Hier toon je aan waar jouw SD kaart zich bevindt. 
7. Als je zeker bent van het juiste station kies je voor Flash. Dan zal de GraspIO worden geplaatst (geknipt) op het station, jouw SD kaart.
8. Natuurlijk altijd eindigen met de SD kaart veilig te verwijderen!

De SD kaart van Raspberry is nu klaar voor gebruik van Cloudio OS
___

## GraspIO aansluiten (op Raspberry)
Na dat onze SD kaart klaar was om gebruik te maken van het Operating System moesten we nog zorgen dat onze GraspIO juist werd aangesloten.
1. Zorg dat de Sensehat verwijderd is van de Raspberry Pi  
<img src="labo4\11SenseHat.jpg" style="transform:rotate(-90deg)" width="500px">  
2. We zorgden we ervoor dat de Raspberry geen stroom kon ontvangen en dan plaatsten we de SD kaart terug.
3. Het is belangrijk dat de afstandhouder (spacer) is aangesloten op de Cloudio voordat je deze op de Raspberry Pi monteert.  
<img src="labo4\12spacer.jpg" width="500px">
4. Plaats nu de Cloudio op de GPIO-header van de Raspberry Pi. (rij pinnetjes aan de bovenkant van de Raspberry). Wanneer je een Raspberry Pi 0/0W gebruikt, moet je de meest linkse pinnen van de Cloudio monteren op de meest linkse pinnen van de Raspberry Pi. 
5. Druk voorzichtig op de pinnen zodat ze goed vastzitten.
<img src="labo4\13place.jpg" width="500px" style="transform:rotate(-90deg)"><img src="labo4\13place2.jpg" width="500px" style="transform:rotate(-90deg)">

Op dit ogenblik is de Raspberry klaar om stroom te ontvangen. Indien uw Raspberry Pi geen Wifi heeft, moet je een wifi-dongle aansluiten. Dit was voor ons niet van toepassing. Om de Raspberry Pi en de Cloudio aan te zetten moet u de voeding aansluiten op de micro-USB-poort. Als dit gebeurd is en de installatie is voltooid dan zal er op het OLED-scherm een welkomstboodschap verschijnen 
___


## GraspIO Studio
Voor ons onderzoek merkten we op dat er ook nog een app bestaat voor GraspIO namelijk: GrapsIO Studio. Hiermee kan je verbinding maken met de GraspIO. Door deze app wordt het veel efficiënter om gebruik te maken van GraspIO. Alles wordt visueler gebracht. Dus hebben we via de App Store de app GraspIO Studio gedownload. Deze is gratis.
___

## Verbinding wifi-netwerk 
Voordat we kunnen beginnen met het gebruiken van onze Cloudio, moeten we deze eerst verbinden met een wifi-netwerk en dit toevoegen aan ons account. Deze wifiverbinding kunnen we dan gebruiken om meerdere Cloudio boards aan het account op de GraspIO app toevoegen. Om de GraspIO te verbinden met een wifi-netwerk kunnen we twee methoden gebruiken. Via USB-verbinding ofwel via de hotspot.  
<img src="labo4\14Verbind.png" width="500px">


### USB twinkle 
De USB is een standaardmethode om de GraspIO te verbinden met uw account & een wifi-netwerk. Hierbij wordt gebruik gemaakt van een USB-kabel, zo kunnen we de wifigegevens overdragen tussen de Cloudio en een mobiel apparaat. Hierdoor kan de Cloudio dan verbinding maken met een extern wifi-netwerk en kan het er ook mee verbonden blijven. Voor deze methode hebben we een USB-kabel nodig zodat we een mobiel apparaat kunnen verbinden met de Raspberry Pi. Het connecteren met de USB gebeurt volgens volgende stappen. 

1. Verbind je mobiel apparaat met de Cloudio via een USB-kabel  
<img src="labo4\14Verbind2.jpg" width="500px">
2. Maak een account aan.
3. Ga naar "Account".
4. Kies voor "USB Twinkle" en selecteer één van de Raspberry Pi's.
5. Dan krijg je mooie instructies op de applicatie. Eerst sluit je de USB aan op jouw gsm en aan de Raspberry. Na 2 keer op next te drukken moet je op "Confirm" drukken om te bevestigen dat de USB is aangesloten.  
<img src="labo4\14Verbind3.png" width="500px">
6. Het kan zijn dat de gsm vraagt of je de computer vertrouwt. Dan moet je op vertrouwen drukken.  
<img src="labo4\14Verbind4.jpg" width="500px">
6. Hierna moeten we op de GraspIO de GIO-schakelaar indrukken. Je zal zien dat er een USB-logo verschijnt op het OLED-schermpje. Dit komt tevoorschijn wanneer de Cloudio verbinding probeert te maken met je apparaat. Indien deze verbinding gelukt is zal het schermpje ‘Apple device found’ weergeven.  
<img src="labo4\14Verbind5.jpg" width="500px">
6. Op de app op je mobiele apparaat zal er een lijst tevoorschijn komen met netwerken waarmee de Cloudio verbinding kan maken.
7. Dan is het de bedoeling dat je het netwerk waarmee je wilt verbinden selecteert, wanneer je die geselecteerd hebt dan moet je het wachtwoord ingeven en doorgaan naar de volgende stap.
<img src="labo4\14Verbind6.jpg" width="500px">
8. Na het invoeren van het wachtwoord moet je wachten tot de Cloudio verbinding heeft gemaakt met het netwerk.
<img src="labo4\14Verbind7.jpg" width="500px">
9. Als de verbinding succesvol is verlopen zal je op de app een scherm zien die weergeeft dat de verbinding is geslaagd.
<img src="labo4\14Verbind8.jpg" width="500px">
10. Als laatste moet je je USB-kabel verwijderen/loskoppelen en je bord een naam geven.  
<img src="labo4\14Verbind9.jpg" width="500px">

Het kan natuurlijk altijd zijn dat er een error is. Dit kan aan verschillende dingen liggen. Bijvoorbeeld kan het zijn dat jouw wifi dit niet ondersteunt anderzijds dat je geen kabel hebt, zo kunnen er nog problemen optreden. Bij ons lukte het in de les niet om onze GraspIO te verbinden met een wifi-netwerk, doordat we problemen hadden om het wachtwoord in te voeren bij de wifi-netwerken op school. Wij raakten dus maar tot en met stap 7. Daarom verkozen wij de tweede methode om de verbinding te maken.  
<img src="labo4\14Verbind10.jpg" width="500px">

### Hotspot Twinkle
Indien je een mobiel netwerk hebt op je apparaat kan je de Hotspot Twinkle methode gebruiken om Cloudio te verbinden met je account en het netwerk. 

1. Als eerste selecteer je deze methode in de app op je mobiel apparaat 
Het is de bedoeling dat je de GIO-schakelaar lang indrukt. Dan krijg je een lijst op het OLED.
<img src="labo4\15Hotspot5.jpg" width="500px" style="transform:rotate(-90deg)" >
2. Bovenaan de lijst selecteer je ‘Hotspot Twinkle’, je kan dit selecteren door lang op de GIO-schakelaar te drukken. 
3. Wanneer je dit geselecteerd hebt zal er op het OLED een wachtwoord verschijnen, deze hebben we nodig in de verdere stappen om met de hotspot verbinding te maken.
4. Nu moeten we een hotspot maken op ons mobiel apparaat. Er zal een knop configureren komen op het app-scherm, op deze moeten we drukken, dan komen we terecht in de instellingen van ons mobiel apparaat. 
5. Nu moeten we de mobiele data inschakelen.
6. Ook de persoonlijke hotspot moeten we aanzetten, bij wachtwoord vullen we het wachtwoord in dat tevoorschijn kwam op ons OLED
<img src="labo4\15Hotspot.jpg" width="200px" >
7. Na het inschakelen van onze persoonlijk hotspot gaan we terug naar de GraspIO app en wachten we tot de hotspot is opgezet.
8. Nu moeten we de Cloudio verbinden met onze mobiele hotspot. Dit doen we door opnieuw lang te drukken op de GIO-schakelaar, zo kunnen we de beschikbare netwerken waarmee we verbinding kunnen maken bekijken. We kunnen door de lijst scrollen door kort op de GIO-schakelaar te drukken, tussen de verschillende hotspots zien we de hotspot staan die we in de vorige stappen hebben ingesteld.
9. Wanneer we de hotspots hebben geselecteerd moeten we wachten tot de Cloudio verbinding heeft gemaakt en de verbindingsstatus wordt weergegeven op de OLED.
10. Als we verbonden zijn met de hotspot zien we op ons mobiele apparaat een lijst met beschikbare wifi-netwerken waarmee we kunnen verbinden.
11. Het is de bedoeling dat we het wifi-netwerk waarmee we de cloudio willen verbinden selecteren, dan moeten we het wachtwoord van dit netwerk ingeven 
12. Op het app scherm moeten we wachten tot de verbinding is voltooid, wanneer de verbinding is voltooid zullen we dit zien op het OLED.
<img src="labo4\15Hotspot3.jpg" width="500px" style="transform:rotate(-90deg)" >
13. Nadat dit bericht op het OLED is verschenen, zal je op het app scherm op ‘Succesful’ moeten klikken 
___
## Voorbeeld
Voor we van start gingen zagen we dat er voor ons een paar voorbeelden werden gemaakt. Dit was voor ons interessant om daar even door te gaan. Zo maakten we kennis met de GraspIO Studio App. 

<img src="labo4\16Examples.jpg" width="500px">

Eén van de voorbeelden zullen we nu overlopen.

### Hi5
**Doelstelling:**  
We spraken eerder over de IR-sensor. Bij het voorbeeld Hi5 wordt er gebruik gemaakt van de IR-sensor. Wanneer we het voorbeeld starten met runnen zal de buzzer beginnen piepen en zien we een Emoji. Wanneer ons hand dicht in de buurt kwam van de IR-sensor,zagen we een “High-Five” emoji en stopte de buzzer. 

**Interne benodigdheden:**  
* IR-sensor
* Buzzer
* OLED-scherm


**Aangemaakt project**  
<img src="labo4\16examples2.jpeg" width="200px">
<img src="labo4\16examples3.jpg" width="500px">
<img src="labo4\16examples4.jpg" width="500px">
___
## Eigen Applicaties

### **Good Morning**
_*Eerste project*_ 

**Doelstelling**  
Het is ochtend en je wilt dat het licht aangaat zonder de lichtknop aan te raken. Je kan je gsm pakken en aan je gsm vragen om het licht aan te leggen.
Ook kan dit als je het licht terug wilt uit zetten.
Dit kan je op het OLED scherm zien 

**Interne benodigdheden**  
* Ledlichtje (stelt de lamp voor)

**Externe benodigdheden**
* GraspIO app
* Voice control (telefoon) 

**Aangemaakt project**  
<img src="labo4\17project.png" width="200px">  
Wanneer we op de cirkel drukken en “Good morning” zeggen gaat het gele ledlichtje branden en komt er op het OLED-scherm “Good morning!”. Wanneer we terug op de cirkel drukken en “Good night” zeggen dan zal het ledlicht uitgaan en komt er “Good night!” tevoorschijn op het OLED-scherm. 

Project is gestart met runnen  
<img src="labo4\17project2.jpg" width="500px">  

Druk op de knop en zeg "Good morning".  
<img src="labo4\17project3.jpg" width="500px">  

De voice control neemt de herkenbaarheid op en zal een actie uitvoeren. Namelijk de led aanleggen en op het OLED scherm zal "good morning" tevoorschijn komen.  
<img src="labo4\17project4.jpg" width="500px">  

Druk op de knop en zeg "Good night".  
<img src="labo4\17project5.jpg" width="500px">  

De voice control neemt de herkenbaarheid op en zal een actie uitvoeren. Namelijk de led uit doen en op het OLED scherm zal "good night" tevoorschijn komen.  
<img src="labo4\17project6.jpg" width="500px">  

##**Wekker**  
_*Tweede project*_

**Doelstelling:**  
Het is ochtend en je wilt dat er een geluid afspeelt en een lichtje gaat branden wanneer het 7u30 is. Als je wilt snoozen houd je je hand voor de IR-sensor. Wanneer de wekker dan terug afgaat druk je op de switch schakelaar om hem volledig te doen stoppen. 

**Interne benodigdheden**  
* Ledlichtje (stelt de lamp voor)
* Buzzer 
* Switch schakelaar 
* IR-sensor 

**Externe benodigdheden**
* GraspIO app

**Aangemaakt project**  
<img src="labo4\18project.png" width="200px">
<img src="labo4\18project2.png" width="200px">
<img src="labo4\18project3.png" width="200px">

Op het juiste uur zal de buzzer afgaan en zal er op het OLED-scherm een emoji verschijnen. Wanneer je je hand voor de IR-sensor houdt zal de buzzer stoppen met afgaan en zal het ledlicht stoppen met branden voor 10 minuten en zal er een slapende emoji komen op het OLED-scherm. Dit is dus de ‘snooze’ van de wekker. Na 10 minuten gaat de buzzer opnieuw afgaan en het ledlicht branden. Wanneer we dan de switch schakelaar indrukken zal hij meteen de buzzer stoppen en het led licht uitdoen en komt er een zonnetje tevoorschijn op het OLED-scherm.  

Je bent aan het slapen en de wekker staat klaar om 7u30 's morgens.  
<img src="labo4\18project4.jpg" width="500px">

Het is 7u30. De wekker gaat af. Zowel de buzzer gaat af als het ledje.  
<img src="labo4\18project5.jpg" width="500px">

Houd je hand naast de sensor. Als je hand dicht genoeg is zal je de klok op snooze zetten. Je kan je hand weer weghalen van de sensor. Hij zal 10 minuten op sluimeren staan.
<img src="labo4\18project6.jpg" width="500px">
<img src="labo4\18project7.jpg" width="500px">

Na 10 minuten gaat hij terug af.  
<img src="labo4\18project8.jpg" width="500px">

Druk op de Switch knop om de wekker te stoppen.
<img src="labo4\18project9.jpg" width="500px">
<img src="labo4\18project10.jpg" width="500px">

## **Automatisch licht**  
_*Derde project*_

Het derde project hebben we zelf niet tot stand kunnen brengen. In dit project werkten we met IFTTT. Dit staat voor If This Than That. Met dit kunnen we projecten maken waarbij de sensoren op het GraspIO-board kunnen worden gebruikt als Triggers om te gebruiken bij het maken van applets op IFTTT. Ook de randapparatuur van het bord en de opgeslagen projecten kunnen worden gebruikt als acties tijdens het maken van applets op IFTTT. 
Dat klonk voor ons zeer verwarrend. Hierbij stelden we ons toch enkele vragen.
Wat is een Applet?
Een Applet verbindt twee/meer apps of apparaten met elkaar. Het stelt je in staat om iets te doen wat die apps of apparaten niet in hun eentje kunnen doen. 

Om applets op IFTTT te maken, moet u gebruik maken (of creëren) van 
* diensten die van plan zijn om op IFTTT te gebruiken. (ex Amazon Alexa, Philips Hue, etc.)
* IFTTT-account voor GraspIO

Hier volgt er weer een stappenplan hoe je IFTTT en GraspIO linkt.
1. Log uit bij Graspio Studio
2. Daarna moet je “verbind met email” selecteren
3. Dan kies je helemaal onderaan “LOG IN NOW”
4. Kies daarna de optie “wachtwoord vergeten”
5. Voer uw geregistreerde e-mail-ID in waar u een authenticatie OTP ontvangt. Zorg dat je hetzelfde email-ID gebruikt als op het account van jou IFTTT
6. Ga dan verder met de stappen van een nieuw wachtwoord.

Dan gaan we door met het 3e project. Dit konden we natuurlijk niet realiseren omdat we geen externe verbindingen hadden, maar vonden dit zeker belangrijk om in ons verslag te steken.

**Doelstelling:**  
Wanneer het te donker wordt gaan de lichten in het huis branden.

**Interne benodigdheden:**  
* Lichtsensor verbonden met GraspIO
**Externe benodigdheden:**   
* Lampen in huis verbonden met de app "Hue"  
<img src="labo4\19project.jpg" width="500px">  

**Aangemaakt project** 
Eerst moet je een nieuw project aanmaken in de GraspIO studio.
In dat project moet er niet al te veel gemaakt worden. In Advanced kan je kiezen tussen een paar opties, namelijk:
Voice
Schedule
Monitor
IFTTT
Uiteraard kiezen we voor IFTTT en slepen we deze in ons project. Dan zagen we het volgende:  
<img src="labo4\19project3.png" width="200px">  
In de onderste Trigger kan je dan de lichtsensor erin slepen.  
<img src="labo4\19project2.png" width="200px">  
Om te zorgen dat dit nu van kracht gaat moet je deze gaan runnen. 
Je zal de volgende Alert krijgen. Deze vertelt ons dat we een Applet moeten creëren op IFTTT. Dus dat is wat we als volgt zullen doen.  
<img src="labo4\19project4.png" width="200px">  
Als we IFTTT openden zagen we het volgende scherm:  
<img src="labo4\19project5.jpg" width="200px">  
Om een nieuwe Applet te creëren moet je op het plusje bovenaan drukken.
Dan zie je een duidelijk scherm "if This Than That".  
<img src="labo4\19project6.jpg" width="200px">  
Klik op de "this" om Trigger te maken.
Ga in de zoekbalk opzoek naar GraspIO.  
<img src="labo4\19project7.jpg" width="200px">  
Daarna kan je kiezen tussen 2 opties:
* trigger the Analog sensors
* trigger the Digital sensors  
<img src="labo4\19project8.jpg" width="200px">  
Deze kan je zelf beslissen. Hier gaan we door in de trigger the Analog sensors. Dan zal hij automatisch opzoek gaan naar een Trigger die is aangemaakt. Je zal iets in de aard terugvinden als “Cloudio IFTTT_Light_<_350”. Dat betekent dat hij onze juiste trigger heeft gevonden.
Daarna kan je op de "that" klikken om een actie te laten uitvoeren. Bij de "that" kan je kiezen welke app iets moet doen bij een bepaalt iets. Hier gaan we door met de app “Hue”. In de app "Hue" zal je bepaalde lichten kunnen kiezen. 
Wanneer je dat geïnstalleerd hebt en op next drukt heb je een nieuwe applet. Als je deze op “On” zet is jouw applet in actie.
Als je de lichtsensor dan zou bedekken zullen de lichten die verbonden zijn met de app “Hue” uitgaan.

## **Je hebt een e-mail van...**  
_*Vierde project*_

Ons laatste project hebben we ook getest. Hier gaan we ook te werk met IFTTT, maar deze keer is ons GraspIO niet een trigger maar een action. 

**Doelstelling:**
Wanneer er een e-mail in jouw inbox komt zal er door de speaker worden uitgesproken van wie je een e-mail ontvangen hebt.

**Externe benodigdheden:**
* Box aangesloten op GraspIO
* E-mail verbonden met e-mail applicatie

We starten terug met het aanmaken van een project in GraspIO Studio. In dat project slepen we weer een IFTTT in ons bord, maar deze keer kiezen we in de plaats van Trigger, Action.   
<img src="labo4\20project.png" width="200px">  
Daarna runnen we weer het project.
Terug in de app IFTTT starten we een nieuwe applet.
Bij de "this" kiezen we voor de app van jouw e-mail dit kan Gmail, mail, Outlook, Officemail, … zijn.  
Daar kan je kiezen voor de trigger als er een nieuwe mail in jouw box komt. Bij ons voorbeeld is dit met Office 365 mail. Daar heb je de keuze “Any new email”.  
<img src="labo4\20project2.png" width="200px">  
Dan moesten we de action kiezen wat voor ons dus de GraspIO is. 
Daar krijg je heel wat verschillende keuzes van acties.  
<img src="labo4\20project3.png" width="200px">  
Eerst voerden we een test uit met de “Control RGB LED”. Daar kan je kiezen voor het bord dat je gemaakt hebt in de GraspIO en welk kleur van lichtje dat je wilt zien als je een e-mail krijgt.  
<img src="labo4\20project4.png" width="200px">  
Dan hadden we onze applet. Als we deze op ON zetten werkte dit.  
<img src="labo4\20project5.png" width="200px">  
<img src="labo4\20project6.png" width="200px">  

Als dit lukte konden we dit proberen met een externe box die jou verteld dat je een e-mail ontvangen hebt. Bij the “than that” kies je terug voor GraspIO maar in de plaats van de action “Control RGB” kan je kiezen voor “Speak the entered text”.  
Bij de optie “Text” krijg je een een knop Add Ingredient. Daar kan je bijvoorbeeld “SenderName” kiezen.  
<img src="labo4\20project8.png" width="200px">  
<img src="labo4\20project7.png" width="200px">  
Dan zal hij dit toevoegen in jouw tekst. Bijvoorbeeld “Je hebt een e-mail ontvangen van SenderName”.  

<img src="labo4\20project9.png" width="200px">

Start de applet en vanaf nu zal je altijd direct weten wanneer je een e-mail ontvangt.  

Bronnen:
* https://guide.grasp.io/blocks/input-blocks/ir#description 02.04.2019  
* https://guide.grasp.io/adding-a-new-board#usb-twinkle 02.04.2019 / 03.04.2019  
* https://guide.grasp.io/hotspot-twinkle 03.04.2019  
_*bijna alle informatie komt uit de GraspIO guide*_
* https://ifttt.com/applets/98002232d-if-any-new-email-then-turn-the-ifttt-led-blue 03.04.2019 