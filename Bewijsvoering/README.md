# Stageverloop
In dit document omschrijf ik hoe het verloop van de stage is gegaan en wat ik allemaal heb gedaan. Ik werk met sprints van telkens 2 weken. De sprints die zet ik op in Github en na elke sprint kijk ik wat ik heb gehaald en maak ik een retrospective van wat er goed en minder goed die sprint ging. 

## Inhoudsopgave
[Sprints](https://github.com/Stage-Bravo/Portfolio/tree/main/Bewijsvoering#sprints)<br>
[Persoonlijke ontwikkeling](https://github.com/Stage-Bravo/Portfolio/tree/main/Bewijsvoering#persoonlijke-ontwikkeling)<br>
[Verloopstage](https://github.com/Stage-Bravo/Portfolio/tree/main/Bewijsvoering#verloopstage)<br>

## Sprints 
Om mijn sprints in te plannen maak ik een bord in Github waar ik mijn planning van de komende 2 weken opstel. Hiermee maak ik 4 koppen aan, TODO, In Progress, Feedback en Done. Hieronder laat ik een voorbeeld zien van hoe een sprint planning eruitziet.

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/7cd8a00b-3ad5-44ca-b29f-04dcb6a69a35)
 
Bij somige items die ik in de planning heb aangemaakt heb ik omschrijving erbij gezet waardoor ik beter weet wat ik bedoelde en dan kunne anderen het ook beter begrijpen wat ik in de planning omschrijf. Hieronder zie je daar een voorbeeld van: 

 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/1b4d302b-99ec-463b-884c-a4731ea635ab)

 Na elke sprint maak ik een [retrospective](https://github.com/Stage-Bravo/Portfolio/blob/main/Retrospective.md) waardoor over wat er goed ging en wat er beter kon in de sprint. Hierdoor weet ik na elke sprint waar ik mee moet doorgaan en waar ik meer op moet letten. Daardoor hoop ik elke sprint op vooruit te gaan waardoor ik uitijndelijk een beter eindproduct kan opleveren. 

## Persoonlijke ontwikkeling
Ik heb een bestand gemaakt waarbij ik op heb geschreven hoe ik me op een persoonlijk vlak heb verbeterd. Dit heeft te maken met hoe ik me heb ontwikkeld hoe je bij een bedrijf moet werken. [HIER]( https://github.com/Stage-Bravo/Portfolio/blob/main/Bewijsvoering/Persoonlijke_ontwikkeling.md) kan naar het bestand gekeken worden. 

## Verloopstage
In de eerste week heb ik in mijn projectplan een algemene planning gemaakt voor mijn stage. De planning heb ik zo gemaakt zodat ik eerst een kan onderzoeken zodat ik daarna de kennis van het onderzoek mee kan nemen in mijn uitwerking. De planning die ik heb gemaakt ziet er zo uit:
Fasering |	Effort | 	Start |	Gereed
--- | --- | --- | --- 
1 |	Onderzoek	|	Week 1	| Week 6
2	| Applicatie onderzoek	|	Week 7 |	Week 7
3	| API-laag maken	|	Week 8 |	Week 16
4	| Afronden	|	Week 17	| Week 18

### Sprints 1, 2 en 3
De eerste 6 weken ben ik zoals gepland bezig geweest het onderzoek. Dit is een onderzoek waarbij ik kijk wat een API is en wat de beste manier is om een API op te zetten. [HIER](https://github.com/Stage-Bravo/Portfolio/blob/main/Onderzoek/Onderzoeksrapport.pdf) het onderzoeksrapport. <br>

Omdat ik goed en snel door het onderzoeksrapport ben gegaan heb ik een aantal API frameworks opgesteld voor te kijken welke het beste bij dit project past. Naast dat heb ik de beveiliging op gesteld zodat ik gelijk een voorsprongetje heb gehad op mijn planning. [HIER](https://github.com/Stage-Bravo/PHP-API-Framworks) kan gevonden worden wat ik allemaal heb gedaan om te testen met verschillende frameworks. Hiermee wilde ik mijn onderzoek voor mijzelf valideren en daardoor kreeg ik gelijk een voorspring op de volde fase van mijn stage.

Het applicatie onderzoek heb ik uitgesteld omdat ik gekeken heb naar de bestaande applicatie geen OOP en geen MVC. Hierdoor kan ik geen functies hergebruiken dus om API’s te maken moet ik een geheel apart project maken wat ik ook heb gemaakt. 

### Sprint 4
In deze sprint ben ik begonnen met het maken van het project. Na mijn onderzoek waarbij ik heb gekeken hoe ik het beste een API kan opzetten heb ik mijn test versie gepakt en heb de beste versie verder ontwikkeld. Om te zien wat ik daar allemaal in heb gemaakt en welke keuzes ik heb gemaakt kun je mijn [Project Beschrijving](https://github.com/Stage-Bravo/Portfolio/blob/main/Bewijsvoering/Project_beschrijving.md) zien. Hier ga ik dieper in op wat ik doe en waarom ik dat doe. 

De endpoints die ik deze sprint heb gemaakt voor het project zijn het inloggen zodat je een JWT-token terugkrijgt. Daarnaast heb ik een functie gemaakt waarbij de JWT-token wordt gevalideerd. Die functie heb ik getest op een test API die ik nu niet meer gebruik. Hieronder zie je hoe die functies aangeroepen worden.

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/93221d29-ca24-42fa-bc93-343d9de20f3a)
 
De functie moet aangeroepen worden door /token te gebruiken. We vragen om de headers email en wachtwoord mee te sturen. Die hebben we namelijk nodig om te kijken of de gebruiker toegang heeft tot de API’s en in welke WBE hij hoort. Er wordt dan een dependecy injection gebruikt voor het aanroepen van functies in andere lagen. We roepen dan uiteindelijk een de functie maakToken aan in de class tokenCollectie die we dan gelijk gereturnd via de API. Zo ziet de class tokenCollectie eruit die in de laag logic zit. 

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/2005481c-168e-4d7e-9b8c-80413b1e8bc5)

Nu er we een token kunnen maken moet er ook gekeken worden dat als iemand een token meestuurt of die token dan ook geldig is. Hiervoor is de class token aangemaakt en die ziet er zo uit.  
Hier zie je hoe er gekeken wordt of de token geldig is. Daarnaast wordt er in deze functie gekeken of de API nog geldig is dat de API niet te lang geleden is gemaakt. 

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/6fe30947-3a0b-425f-a071-8e6554bcc4e2)

Naast dat heb ik het project van een localhost naar een lokale server die op het bedrijf gebruikt wordt verplaats. Hierdoor kan ik nabootsen hoe de API's reageren op een publieke server. Hierdoor hoef ik bijna geen aandacht meer te besteden aan cross handelingen. Daarvoor het ik het komende stukje code voorgeschreven.

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/688fa263-cda6-44ff-9319-cad5e4bd7c82)

Met deze code geef ik als eerste de route naar het project aan. Deze route moet ook meegegeven worden in de url van de API. Deze route zal veranderd worden wanneer het project op een server staat. Daarnaast geven we een aantal acces controls aan waar de API-call aan moet voldoen. 

In deze sprint heb ik er ook voor kunnen zorgen dat er een verbinding is gekomen met de database. De verbinding wordt gemaakt via mysqli en er wordt daarom geen gebruik gemaakt van een pdo. De verbinding wordt gemaakt in een aparte class en dat ziet er zo uit. 

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/cad899fb-222d-494a-ba0a-6150704ead97)

Het applicatie onderzoek heb ik uitgesteld omdat er niet met OOP gewerkt is en er verder weinig structuur in zit. Nu dat ik verder ben in het project heb ik opgeschreven hoe de applicatie er nu uitziet vergeleken hoe we het op school aangeleerd krijgen. Hier heb ik de voor- en nadelen van opgeschreven van beide kanten. Naast dat heb ik beschreven hoe de API in het project gedesigneerd is. Het onderzoek kun je [HIER](https://github.com/Stage-Bravo/Portfolio/blob/main/Onderzoek/Onderzoeksrapport.pdf) vinden.

### Sprint 5
In sprint 5 ben ik bezig geweest met het uitbreiden van het project. Hiermee heb ik de endpoints gegevens ophalen gemaakt en heb ik een functie gemaakt die de user id uit de JWT-token haalt. Die functie heb ik extra gemaakt waardoor zodat het makkelijk wordt om erachter te komen wie gebruik maakt van de token. Hieronder kun je zien hoe die functie er uit ziet.
 
 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/ee2b261b-6ac3-4161-a98a-170be33139e1)

Nu laat ik in het kort zien welke endpoint ik heb toegevoegd aan mijn project. Voor deze endpoint is gekozen om de eenvoudigheid waardoor er goed gekeken kon worden naar wat de beste manier is de basis goed op te kunnen zetten. Hier wordt de endpoint aangemaakt.
 
 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/50a905ad-7f2c-492f-879b-5d6e3b7640bc)

Hierin wordt de volgende functie aangeroepen in de wbeCollectie class.
 
 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/7feb8c76-4365-425a-b516-c35719b453d2)

In de functie die wordt aangeroepen kijken we eerst of er een token is meegestuurd waarna we gaan kijken of die token geldig is. Daarna kijken we of de gebruiker toegang heeft tot de wbe. Dit doen we door de gebruikers id mee te sturen die we uit de JWT-token halen waarbij ook nog de wbe meegestuurd moet worden. Zo ziet de functie heeftGebruikerTotWbe eruit. 

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/094761b6-c1af-4504-ad44-42146dbd9edc)

In deze functie maak ik eerst een verbinding met de database waar ik de naam van mee stuur. Als er iets niet goed gaat met de verbinding komt het in de catch en dan wordt een error meegestuurd. Wanneer de verbinding is gemaakt met de database gaan we via een select query en als we een row terug krijgen sturen we true terug naar de logic laag en kan de volgende functie aangeroepen worden.

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/7bcccc41-b1f3-483e-b7fd-cbb7a5db481c)

Hierin wordt de verbinding met database opnieuw gemaakt waarnaar er alle gegevens van de combinatie gereturnd worden. De uitleg waarom ik geen pdo gebruik kun je [HIER](https://github.com/Stage-Bravo/Portfolio/blob/main/Bewijsvoering/Project_beschrijving.md) vinden. 

Daarnaast heb ik verbeterpunten toegepast aan mijn [onderzoeksrapport](https://github.com/Stage-Bravo/Portfolio/blob/main/Onderzoek/Onderzoeksrapport.pdf). Ik heb van mijn assessor feedback gekregen op mijn onderzoek en die feedback heb ik in mijn onderzoek verwerkt. 

Naast dat ben ik ook bezig geweest met hoe ik mijn stage uitgebreider kan maken. Dit is omdat er met een gesprek met mijn assessor er twijfels kwamen wat ik nog kan laten zien om alle leeruitkomsten goed te kunnen behalen. Daarom gaan we contact leggen met het bedrijf dat de API’s zou gaan gebruiken om te kijken hoe we het kunnen uitbreiden.

### Sprint 6
Deze sprint heb ik met mijn assessor de planning gemaakt omdat de planning van de afgelopen sprints wat minder was ene er meer moes gaan gebeuren. We hebben voor die sprint 3 weken uitgetrokken alleen was ik al na 2 weken klaar en ben daarna een nieuwe sprint begonnen.

In deze sprint ben ik begonnen met Swagger interactief maken. Swagger had ik al geïmplementeerd in het project maar als je een API aanriep kreeg je niks terug. Dit kwam omdat de url naar de verkeerde host in was gesteld. Daarnaast moest de route naar de API ook veranderd worden omdat het project naar een lokale server is verplaats. 

Daarna ben ik begonnen met een API te maken waarbij foto’s naar een API gestuurd kunnen worden. Dit was op verzoek van de opdrachtgever zodat ze zelf weten hoe er zoon API kunnen maken. Deze API heb ik verwerkt met de API-marker opslaan. Dit heb ik zo gedaan zodat er gelijk een functionele API erbij gemaakt kon worden die later nog gebruikt kan worden. De eerste API is het uploaden van een marker en we de foto ophalen ziet er zo uit.

 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/0c97467f-b48d-43fc-a12e-242e0037e493)

Om de foto op te slaan hebben zijn er een aantal functies gemaakt. Dit heb ik in de class markerCollectie gedaan. Hier laat ik de functies zien die ervoor zorgen dat de foto’s worden opgeslagen.

 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/0f4fd29d-e405-4f3d-aaf5-c0d7dcd18831)

Deze functie regelt het proces van het maken en het opslaan van de foto. Eerst wordt er gekeken of het uploaden is gelukt, daarna gaan we de naam van foto ophalen. Dan gaan we een naam genereren van de foto die we op gaan slaan. Dit doen we omdat als iemand een foto uploadt met dezelfde naam er een error komt en de foto niet wordt opgeslagen. De functie die dat regelt ziet er zo uit. 

 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/499e803a-bdc2-4877-a628-8f2e07ca56f8)

Als deze naam is gegenereerd gaan we kijken of deze naam toch al bestaat en als dat zo is wordt er een nieuwe naam gegenereerd. Dan wordt de foto opgeslagen en die functie fotoOpslaan aangeroepen waarmee de foto op de server wordt opgeslagen. Dit doen we op de server en niet op de database omdat te veel geheugen is voor de database en hij dan te snel vol raakt en hij er te traag van wordt. Dit is de functie die de foto opslaat. 

 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/97e2e8cf-991b-47d2-a2a0-1014c55e0ead)

In hier zie je hoe ik ervoor zorg hoed de foto wordt opgeslagen. We kijken of het bestand een png of een jpg is en als dat niet zo is wordt er een foutmelding teruggestuurd en een false zodat we weten dat het een foutmelding is. Dan pakken we de foto en dan slaan we die op bij de route die we hebben gegeven met de naam die we geven plus de goeie bestands value. Die data sturen we ook terug zodat we weten dat alles goed is gegaan en dan kunnen we de bestandsnaam opslaan in de database. 

Naast deze API hebben we ook een API gemaakt waar we de marker plus de foto op kunnen vragen. De API ziet er bijna hetzelfde uit als de andere API’s die we hebben aangemaakt want we sturen namelijk json bestand terug maar hoe we de foto mee sturen laat ik nu wel hier zien. We halen namelijk de bestandsnaam op uit de database die we dan kunnen gebruiken om de goeie foto op te halen van de server. Het ziet er dan zo uit. 
 
 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/c087eaa5-d49c-4903-b40f-97d30eb71000)

Dit is de regel waar we de foto bijvoegen aan een array file. Hierin zie je 2 dingen gebeuren, een base64_encode en een file_get_contents. De file_get_contents haalt de foto van de server en door de base64_encode te gebruiken wordt er van de foto een encoded tekst gemaakt. Hierdoor kunnen we het via json meesturen via de API. De gebruiker kan het dan bijvoorbeeld via javascript decoden. Hier zat niet de volledige tijd in van het maken van het maken van de API maar er moes ook getest worden of je de foto krijgt als je het weer decode. Dit heb ik via javascript/jquery gedaan waardoor ik zeker weet dat de API werkt en bruikbaar is. Zo ziet het eruit om de foto te openen in jquery/javascript.
 
 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/214f9ab0-6705-4be2-ae0e-8e11c4dbf4b7)

Nu we een aantal functies hebben gemaakt moet het ook getest worden of alles werkt. Dit wordt gedaan via phpunit waar we unit testen voor php code kunnen maken. Alleen de publieke functies in de logic laag worden getest. Hierover heb ik een uitleg gemaakt in de [project beschrijving](https://github.com/Stage-Bravo/Portfolio/blob/main/Bewijsvoering/Project_beschrijving.md) waar ik ook een voorbeeld geef van een unit test. 

Voor de rest heb ik de code verbeterd die ik heb geschreven. Er waren functies in verkeerde classes en de dependency injection was verkeerd uitgevoerd. Dit kwam omdat ik een verkeerde stukje code van internet heb gebruikt en hierachter kwam met het maken van de testen. 

Naast dat ben ik veel bezig geweest met hoe ik mijn stage uitgebreider kan maken zodat ik alle leeruitkomsten uitgebreid kan gaan aantonen. Dit heb ik gedaan door te vragen welke endpoint er nodig zijn om dit project tot een goede uitkomst te krijgen. Naast dat ga ik de API’s op een server runnen en daarbij ga ik kijken of ik dit automatisch kan uploaden. 

Daarnaast ben ik begonnen om mijn portfolio een stuk te gaan verbeteren en daar ben ik de sprint hierna verder mee bezig gegaan.

### Sprint 7
Deze sprint is iets korter dan de andere omdat in deze sprint hemelvaar viel en daarom heb ik 2 dagen minder gehad om aan deze sprint te werken. 

In de vorige sprint hebben we als eerste gekeken welke endpoints erbij moeten gaan komen en twee van die endpoints zijn het maken en ophalen van afschot. Hiervoor heb ik in de database een tabel aan moeten met waar het afschot wordt opgeslagen. Het maken van de API ziet er bijna hetzelfde uit als de marker API’s omdat ze hetzelfde doel hebben alleen is het net iets andere data die in een ander tabel moeten. Voor de functies in de logic laag zijn ook testen voor gemaakt. 

In deze sprint ben ik ook begonnen met het maken van [project beschrijving](https://github.com/Stage-Bravo/Portfolio/blob/main/Bewijsvoering/Project_beschrijving.md) waar ik mijn keuzes beschrijf die ik heb gemaakt. Hier ga ik wat meer in op de technieken die ik gebruik en waarom ik voor die techniek heb gekozen. 

Deze sprint heb ik ook een probleem gehad met de libraries die ik gebruik voor mijn project. Dit kwam omdat ik een package deed updaten naar een oudere versie waardoor het hele project niet meer werkte. Ik had natuurlijk geen back-up gemaakt waardoor ik minimaal een dag kwijt ben geweest om het op te lossen. Dit is een goeie les geweest voor de volgende keer om wel een back-up te maken.

Er is ook voor gezorgd dat er een server is waar ik de applicatie op kan gaan hosten. Naast dat heb ik gekeken of ik lokaal GitHub kon gaan gebruiken om gebruik te kunnen maken van ci./cd maar dat kan niet en daarom moet ik een alternatief ervoor gaan zoeken. 

### Sprint 8
In deze sprint ben ik vooral bezig geweest met alles rond het project op de server zetten. Dit kwam omdat dat er nog extra problemen bij kwamen die ik van tevoren niet zag aankomen. Daarnaast heeft deze sprint ook een dag minder gehad vanwege Pinksteren. Maar in het begin van deze sprint ben ik begonnen met het afmaken van dit bestand. Dit heeft me veel tijd gekost om het op een goeie manier op te zetten.

Daarna ben ik begonnen met het project op de server te zetten. Hiervoor heb ik FileZilla omdat het hier op het stagebedrijf wordt gebruikt. De server is voor mij opgezet en heb de gegevens ervoor gekregen waardoor ik heb kunnen inloggen op de server. Toen heb ik nog de inlog gegevens van de database moeten veranderen naar een database die op een server staat. 

Toen kwam ik erachter dat swagger niet meer werkte en heb daar een aantal dingen moeten veranderen. Ik heb een html pagina gemaakt waardoor je online naar een swagger pagina kunt kijken. De html van die pagina ziet er zo uit.

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/2e206f2a-7b13-4cf7-8002-db6bd57b9f65)

En dan ziet het resultaat er zo uit.

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/1d671de4-7c7a-413f-8173-367b15d48e45)
 
Om dit voor elkaar te krijgen heb ik vrij lang moeten zoeken naar het juiste resultaat. De json en yaml bestanden die ik genereer via mijn eigen script zijn niet goed en krijg een error dat het bestand verkeerd is. Door op de site van swagger het yaml bestand in te voeren en te downloaden werkt het nu wel. Waarom het dan wel werkt weet ik niet want er is geen code aangepast of toegevoegd. Het enige verschil dat ik kan zien is dat het bestand van swagger in kb’s iets groter is.

Naast dat heb ik nog een probleem gehad met swagger. Als je data meestuurde via swagger kreeg de API de data niet binnen. Dit kwam omdat de server geen data wilde ontvangen die via een header meegestuurd werd. Dat probleem heb ik kunnen oplossen door in de .htaccess file deze regel heb toegevoegd. 
```
Header set Access-Control-Allow-Origin "*"
```

Naast dat had ik nog een ander probleem waarbij de naam authorization niet wordt ondersteunt door Swagger waardoor ik over die naam aan moest passen bij swagger maar ook bij de API’s. 

Nadat ben ik verdergegaan met het maken van een script waarbij het project geüpload wordt naar de server. Dit heeft veel tijd gekost omdat het uploaden niet snel werkte. Het grootste probleem daarbij was dat het project te groot was om helemaal te uploaden waardoor ik een aantal folders in een ignore moet zetten. Daarbij wilde ik ook iets toevoegen waarbij het alleen geüpload wordt als alle testen slagen maar dat is niet mogelijk in de php versie die ik gebruik. [HIER](https://github.com/Stage-Bravo/Portfolio/blob/main/Bewijsvoering/Project_beschrijving.md) leg ik uit hoe ik het scriptje heb gemaakt en welke keuzes ik daarbij heb gemaakt.
