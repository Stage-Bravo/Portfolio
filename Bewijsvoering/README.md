# Stageverloop
In dit document beschrijf ik het verloop van mijn stage en de werkzaamheden die ik heb uitgevoerd. Ik werk met sprints van telkens 2 weken, die ik opzet in GitHub. Na elke sprint evalueer ik wat ik heb bereikt en maak ik een retrospectief om te reflecteren op wat er goed en minder goed ging tijdens die sprint.

## Inhoudsopgave
[Sprints](https://github.com/Stage-Bravo/Portfolio/tree/main/Bewijsvoering#sprints)<br>
[Persoonlijke ontwikkeling](https://github.com/Stage-Bravo/Portfolio/tree/main/Bewijsvoering#persoonlijke-ontwikkeling)<br>
[Verloopstage](https://github.com/Stage-Bravo/Portfolio/tree/main/Bewijsvoering#verloopstage)<br>

## Sprints 
Voor het plannen van mijn sprints maak ik een bord in GitHub, waarop ik de planning voor de komende 2 weken opstel. Ik gebruik hierbij vier kolommen: TODO, In Progress, Feedback en Done. Hieronder laat ik een voorbeeld zien van hoe een sprintplanning eruitziet.

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/7cd8a00b-3ad5-44ca-b29f-04dcb6a69a35)
 
Bij sommige items die ik in de planning heb aangemaakt heb ik omschrijving erbij gezet waardoor ik beter weet wat ik bedoelde en dan kunnen anderen het ook beter begrijpen wat ik in de planning omschrijf. Hieronder zie je daar een voorbeeld van. 

 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/1b4d302b-99ec-463b-884c-a4731ea635ab)

 Na elke sprint maak ik een [retrospective](https://github.com/Stage-Bravo/Portfolio/blob/main/Retrospective.md) waarin ik reflecteer op wat er goed ging en wat beter kon in de sprint. Hierdoor weet ik na elke sprint waar ik mee moet doorgaan en waar ik meer op moet letten, in de hoop elke sprint vooruitgang te boeken en uiteindelijk een beter eindproduct op te leveren.
 
## Persoonlijke ontwikkeling
Ik heb een bestand gemaakt waarin ik beschrijf hoe ik me op persoonlijk vlak heb ontwikkeld tijdens mijn stage. Dit heeft te maken met hoe ik heb geleerd te werken binnen een bedrijf. [HIER]( https://github.com/Stage-Bravo/Portfolio/blob/main/Bewijsvoering/Persoonlijke_ontwikkeling.md) kun je dit bestand bekijken.

## Verloopstage
In de eerste week heb ik een algemene planning voor mijn stage gemaakt in mijn projectplan. De planning is zo opgesteld dat ik eerst onderzoek doe, waarna ik de opgedane kennis kan toepassen in mijn uitwerking. De planning ziet er als volgt uit:
Fasering |	Effort | 	Start |	Gereed
--- | --- | --- | --- 
1 |	Onderzoek	|	Week 1	| Week 6
2	| Applicatie onderzoek	|	Week 7 |	Week 7
3	| API-laag maken	|	Week 8 |	Week 16
4	| Afronden	|	Week 17	| Week 18

### Sprints 1, 2 en 3
Het eerste wat ik heb gedaan op mijn stage is het maken van het [projectplan](https://github.com/Stage-Bravo/Portfolio/blob/main/Overige%20Documenten/Projectplan.pdf). Daarin heb ik de eerste 6 weken gepland aan mijn onderzoek. Dit omvat een onderzoek naar wat een API is en wat de beste manier is om een API op te zetten. [HIER](https://github.com/Stage-Bravo/Portfolio/blob/main/Onderzoek/Onderzoeksrapport.pdf) is het onderzoeksrapport te vinden. <br>

Omdat het onderzoeksrapport sneller dan verwacht af was, heb ik verschillende API-frameworks geëvalueerd om te bepalen welk framework het beste bij dit project past. Daarnaast heb ik de beveiliging opgezet om een voorsprong te nemen op mijn planning. [HIER](https://github.com/Stage-Bravo/PHP-API-Framworks) kun je mijn testen met verschillende frameworks vinden. Hiermee wilde ik mijn onderzoek valideren en kreeg ik een voorsprong op de volgende fase van mijn stage.

Het applicatieonderzoek heb ik uitgesteld, omdat de bestaande applicatie geen OOP of MVC gebruikt, waardoor functies niet herbruikbaar zijn. Voor het maken van API’s heb ik een apart project opgezet.

### Sprint 4
In deze sprint ben ik begonnen met het ontwikkelen van het project. Na mijn onderzoek naar de beste manier om een API op te zetten, heb ik mijn testversie gepakt en verder ontwikkeld. Voor een meer gedetailleerde beschrijving van mijn werk en keuzes kun je mijn [Project Beschrijving](https://github.com/Stage-Bravo/Portfolio/blob/main/Bewijsvoering/Project_beschrijving.md) zien. Hier leg ik uit wat ik doe en waarom ik dat doe. 

De endpoints die ik deze sprint heb ontwikkeld, zijn onder andere voor het inloggen, zodat je een JWT-token terugkrijgt, en een functie om de JWT-token te valideren. Deze functies heb ik getest op een test-API. Hieronder zie je hoe deze functies worden aangeroepen.

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/93221d29-ca24-42fa-bc93-343d9de20f3a)
 
De functie moet worden aangeroepen via /token, waarbij de headers email en wachtwoord moeten worden meegestuurd. Deze zijn nodig om te controleren of de gebruiker toegang heeft tot de API’s en in welke WBE hij hoort. Er wordt een dependency injection gebruikt voor het aanroepen van functies in andere lagen. Uiteindelijk wordt de functie maakToken aangeroepen in de class tokenCollectie, die dan direct via de API wordt geretourneerd. Zo ziet de class tokenCollectie eruit, die zich in de laag logic bevindt.

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/2005481c-168e-4d7e-9b8c-80413b1e8bc5)

Nu we een token kunnen maken, moet ook gecontroleerd worden of de meegestuurde token geldig is. Hiervoor is de class token aangemaakt en die ziet er zo uit. Hier wordt gecontroleerd of de token geldig is en of de API nog geldig is en niet te lang geleden is gemaakt.

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/6fe30947-3a0b-425f-a071-8e6554bcc4e2)

Daarnaast heb ik het project van een localhost naar een lokale server op het bedrijf verplaatst. Hierdoor kan ik nabootsen hoe de API's reageren op een publieke server. Hierdoor hoef ik bijna geen aandacht meer te besteden aan cross-origin handling. Hiervoor heb ik de volgende code geschreven.

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/688fa263-cda6-44ff-9319-cad5e4bd7c82)

Met deze code geef ik de route naar het project aan, die ook meegegeven moet worden in de URL van de API. Deze route zal veranderd worden wanneer het project op een server staat. Daarnaast geven we een aantal access controls aan waar de API-call aan moet voldoen.

In deze sprint heb ik ook een verbinding met de database tot stand gebracht via mysqli, waarbij geen gebruik wordt gemaakt van PDO. De verbinding wordt gemaakt in een aparte class en ziet er zo uit.

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/cad899fb-222d-494a-ba0a-6150704ead97)

Omdat de bestaande applicatie niet met OOP werkt en er weinig structuur in zit, heb ik het applicatieonderzoek uitgesteld. Nu ik verder ben in het project, heb ik beschreven hoe de applicatie er nu uitziet vergeleken met hoe we het op school hebben geleerd. Ik heb de voor- en nadelen van beide methoden opgeschreven en beschreven hoe de API in het project is ontworpen. Het onderzoek kun je [HIER](https://github.com/Stage-Bravo/Portfolio/blob/main/Onderzoek/Onderzoeksrapport.pdf) vinden.

### Sprint 5
In sprint 5 heb ik het project uitgebreid door endpoints te maken voor het ophalen van gegevens en een functie te maken die de user ID uit de JWT-token haalt. Deze functie vergemakkelijkt het achterhalen van de gebruiker die de token gebruikt. Hieronder zie je hoe deze functie eruitziet.
 
 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/ee2b261b-6ac3-4161-a98a-170be33139e1)

Hier laat ik kort zien welke endpoints ik heb toegevoegd aan mijn project. Deze endpoints zijn gekozen vanwege hun eenvoud, zodat er goed gekeken kon worden naar de beste manier om de basis goed op te zetten. Zo wordt de endpoint aangemaakt.
 
 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/50a905ad-7f2c-492f-879b-5d6e3b7640bc)

Hierin wordt de volgende functie aangeroepen in de wbeCollectie class.
 
 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/7feb8c76-4365-425a-b516-c35719b453d2)

In deze functie wordt eerst gecontroleerd of er een token is meegestuurd, waarna wordt gekeken of die token geldig is. Vervolgens wordt gecontroleerd of de gebruiker toegang heeft tot de WBE. Dit doen we door de gebruikers-ID mee te sturen, die we uit de JWT-token halen, waarbij ook de WBE meegestuurd moet worden. Zo ziet de functie heeftGebruikerTotWbe eruit. 

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/094761b6-c1af-4504-ad44-42146dbd9edc)

In deze functie maak ik eerst een verbinding met de database waar ik de naam van mee stuur. Als er iets niet goed gaat met de verbinding komt het in de catch en dan wordt een error meegestuurd. Wanneer de verbinding is gemaakt met de database gaan we via een select query en als we een row terug krijgen sturen we true terug naar de logic laag en kan de volgende functie aangeroepen worden.

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/7bcccc41-b1f3-483e-b7fd-cbb7a5db481c)

Hierin wordt de verbinding met database opnieuw gemaakt waarnaar er alle gegevens van de combinatie gereturnd worden. De uitleg waarom ik geen pdo gebruik kun je [HIER](https://github.com/Stage-Bravo/Portfolio/blob/main/Bewijsvoering/Project_beschrijving.md) vinden. 

Daarnaast heb ik verbeterpunten toegepast aan mijn [onderzoeksrapport](https://github.com/Stage-Bravo/Portfolio/blob/main/Onderzoek/Onderzoeksrapport.pdf). Ik heb van mijn assessor feedback gekregen op mijn onderzoek en die feedback heb ik in mijn onderzoek verwerkt. 

Naast dat ben ik ook bezig geweest met hoe ik mijn stage uitgebreider kan maken. Dit is omdat er met een gesprek met mijn assessor er twijfels kwamen wat ik nog kan laten zien om alle leeruitkomsten goed te kunnen behalen. Daarom gaan we contact leggen met het bedrijf dat de API’s zou gaan gebruiken om te kijken hoe we het kunnen uitbreiden.

### Sprint 6
Tijdens deze sprint heb ik samen met mijn assessor een nieuwe planning gemaakt omdat de planning van de afgelopen sprints niet optimaal was en er meer gedaan moest worden. We hadden drie weken ingepland voor deze sprint, maar ik was al na twee weken klaar en ben daarna met een nieuwe sprint begonnen.

Ik ben begonnen met het interactief maken van Swagger. Hoewel Swagger al geïmplementeerd was, kreeg je bij het aanroepen van een API geen respons terug. Dit kwam omdat de URL naar de verkeerde host was ingesteld. Daarnaast moest de route naar de API worden aangepast omdat het project naar een lokale server was verplaatst.

Vervolgens heb ik een API ontwikkeld waarmee foto's naar een server kunnen worden gestuurd. Dit was op verzoek van de opdrachtgever, zodat ze wisten hoe ze zelf zo'n API konden maken. Deze API heb ik geïntegreerd met de API voor het opslaan van markers. Hierdoor kon ik direct een functionele API maken die later gebruikt kan worden. De eerste API is voor het uploaden van een marker en het ophalen van de foto. De structuur van deze API ziet er als volgt uit.

 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/0c97467f-b48d-43fc-a12e-242e0037e493)

Om de foto op te slaan, heb ik verschillende functies gemaakt in de class markerCollectie. Hier zijn enkele voorbeelden van deze functies.

 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/0f4fd29d-e405-4f3d-aaf5-c0d7dcd18831)

Deze functies zorgen voor het proces van het maken en opslaan van de foto. Eerst wordt gecontroleerd of het uploaden is gelukt. Vervolgens wordt de naam van de foto opgehaald en een nieuwe naam gegenereerd om naamconflicten te voorkomen. Deze functie ziet er als volgt uit. 

 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/499e803a-bdc2-4877-a628-8f2e07ca56f8)

Als de naam is gegenereerd, wordt gecontroleerd of deze naam al bestaat. Indien dit het geval is, wordt een nieuwe naam gegenereerd. Vervolgens wordt de foto opgeslagen met de functie fotoOpslaan, die de foto op de server opslaat in plaats van in de database om geheugenproblemen te voorkomen. De functie voor het opslaan van de foto ziet er zo uit:

 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/97e2e8cf-991b-47d2-a2a0-1014c55e0ead)

In hier zie je hoe ik ervoor zorg hoed de foto wordt opgeslagen. We kijken of het bestand een png of een jpg is en als dat niet zo is wordt er een foutmelding teruggestuurd en een false zodat we weten dat het een foutmelding is. Dan pakken we de foto en dan slaan we die op bij de route die we hebben gegeven met de naam die we geven plus de goeie bestands value. Die data sturen we ook terug zodat we weten dat alles goed is gegaan en dan kunnen we de bestandsnaam opslaan in de database. 

Naast deze API hebben we ook een API gemaakt waar we de marker plus de foto op kunnen vragen. De API ziet er bijna hetzelfde uit als de andere API’s die we hebben aangemaakt want we sturen namelijk json bestand terug maar hoe we de foto mee sturen laat ik nu wel hier zien. We halen namelijk de bestandsnaam op uit de database die we dan kunnen gebruiken om de goeie foto op te halen van de server. Het ziet er dan zo uit. 
 
 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/c087eaa5-d49c-4903-b40f-97d30eb71000)

Dit is de regel waar we de foto bijvoegen aan een array file. Hierin zie je 2 dingen gebeuren, een base64_encode en een file_get_contents. De file_get_contents haalt de foto van de server en door de base64_encode te gebruiken wordt er van de foto een encoded tekst gemaakt. Hierdoor kunnen we het via json meesturen via de API. De gebruiker kan het dan bijvoorbeeld via javascript decoden. Hier zat niet de volledige tijd in van het maken van het maken van de API maar er moes ook getest worden of je de foto krijgt als je het weer decode. Dit heb ik via javascript/jquery gedaan waardoor ik zeker weet dat de API werkt en bruikbaar is. Zo ziet het eruit om de foto te openen in jquery/javascript.
 
 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/214f9ab0-6705-4be2-ae0e-8e11c4dbf4b7)

Ik heb PHPUnit gebruikt om unit tests te schrijven voor de publieke functies in de logic-laag.  Hierover heb ik een uitleg gemaakt in de [project beschrijving](https://github.com/Stage-Bravo/Portfolio/blob/main/Bewijsvoering/Project_beschrijving.md) waar ik ook een voorbeeld geef van een unit test. Daarnaast heb ik de code verbeterd door functies in de juiste classes te plaatsen en de dependency injection correct uit te voeren. Dit ontdekte ik tijdens het maken van de tests.

Ik heb overleg gehad over welke endpoints nodig zijn om het project tot een goed einde te brengen en mijn leeruitkomsten uitgebreid aan te tonen. Verder ben ik bezig geweest met het verbeteren van mijn portfolio en heb ik een server opgezet om de API’s te hosten. Ik ben ook begonnen met het automatiseren van het uploaden van de API’s naar de server.

### Sprint 7
Deze sprint was iets korter vanwege Hemelvaart, waardoor ik twee dagen minder had om te werken.

We hebben nieuwe endpoints toegevoegd voor het maken en ophalen van afschot. Hiervoor heb ik een tabel in de database gemaakt om het afschot op te slaan. De API's hiervoor zijn vergelijkbaar met de marker-API's, met enkele aanpassingen voor de verschillende data. Ik heb ook unit tests geschreven voor de functies in de logic-laag.

Daarnaast ben ik ook begonnen met het maken van [project beschrijving](https://github.com/Stage-Bravo/Portfolio/blob/main/Bewijsvoering/Project_beschrijving.md) waar ik mijn keuzes beschrijf die ik heb gemaakt. Hier ga ik wat meer in op de technieken die ik gebruik en waarom ik voor die techniek heb gekozen. 

Ik had een probleem met de libraries die ik gebruik voor mijn project vanwege een update naar een oudere versie. Dit zorgde ervoor dat het project niet meer werkte en ik een dag kwijt was om het op te lossen. Dit was een goede les om altijd een back-up te maken.

Verder heb ik een server opgezet om de applicatie te hosten en onderzocht of ik lokaal GitHub kon gebruiken voor CI/CD, maar dit bleek niet mogelijk te zijn.

### Sprint 8
In deze sprint heb ik vooral gewerkt aan het opzetten van het project op de server. Dit ging gepaard met enkele onverwachte problemen en een dag minder werk vanwege Pinksteren. Ik ben begonnen met het afmaken van dit document en het project op de server te zetten via FileZilla.

Toen kwam ik erachter dat swagger niet meer werkte en heb daar een aantal dingen moeten veranderen. Ik heb een html pagina gemaakt waardoor je online naar een swagger pagina kunt kijken. De html van die pagina ziet er zo uit.

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/2e206f2a-7b13-4cf7-8002-db6bd57b9f65)

En dan ziet het resultaat er zo uit.

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/1d671de4-7c7a-413f-8173-367b15d48e45)
 
Om dit voor elkaar te krijgen heb ik vrij lang moeten zoeken naar het juiste resultaat. De json en yaml bestanden die ik genereer via mijn eigen script zijn niet goed en krijg een error dat het bestand verkeerd is. Door op de site van swagger het yaml bestand in te voeren en te downloaden werkt het nu wel. Waarom het dan wel werkt weet ik niet want er is geen code aangepast of toegevoegd. Het enige verschil dat ik kan zien is dat het bestand van swagger in kb’s iets groter is.

Naast dat heb ik nog een probleem gehad met swagger. Als je data meestuurde via swagger kreeg de API de data niet binnen. Dit kwam omdat de server geen data wilde ontvangen die via een header meegestuurd werd. Dat probleem heb ik kunnen oplossen door in de .htaccess file deze regel heb toegevoegd. 
```
Header set Access-Control-Allow-Origin "*"
```

Daarnaast moest ik de naam 'authorization' aanpassen omdat deze niet werd ondersteund door Swagger.

Ik ben verder gegaan met het maken van een script om het project automatisch naar de server te uploaden. Dit kostte veel tijd omdat het uploaden traag ging. Het grootste probleem was dat het project te groot was om in één keer te uploaden, dus moest ik enkele mappen uitsluiten. Ik wilde ook dat het script alleen uploadde als alle tests slaagden, maar dit was niet mogelijk met de versie van PHP die ik gebruik.  [HIER](https://github.com/Stage-Bravo/Portfolio/blob/main/Bewijsvoering/Project_beschrijving.md) leg ik uit hoe ik het scriptje heb gemaakt en welke keuzes ik daarbij heb gemaakt.

## Conclusie
Tijdens mijn stage heb ik veel geleerd over het ontwikkelen van API's en het werken binnen een bedrijf. Door het werken in sprints heb ik geleerd om mijn werk te plannen en reflecteren op mijn voortgang. Ik ben trots op wat ik heb bereikt en kijk uit naar mijn volgende uitdaging.

## Referenties
[Onderzoeksrapport](https://github.com/Stage-Bravo/Portfolio/blob/main/Onderzoek/Onderzoeksrapport.pdf) <br>
[Project Beschrijving](https://github.com/Stage-Bravo/Portfolio/blob/main/Bewijsvoering/Project_beschrijving.md) <br>
[Persoonlijke Onwikkeling]( https://github.com/Stage-Bravo/Portfolio/blob/main/Bewijsvoering/Persoonlijke_ontwikkeling.md)<br>
