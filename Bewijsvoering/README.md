# Stageverloop
In dit document omschrijf ik hoe het verloop van de stage is gegaan en wat ik allemaal heb gedaan. Ik werk met sprints van telkens 2 weken. De sprints die zet ik op in Github en na elke sprint kijk ik wat ik heb gehaald en maak ik een retrospective van wat er goed en minder goed die sprint ging. 

## Inhoudsopgave
[Sprints](https://github.com/Stage-Bravo/Portfolio/tree/main/Bewijsvoering#sprints)<br>
[Persoonlijke ontwikkeling](https://github.com/Stage-Bravo/Portfolio/tree/main/Bewijsvoering#persoonlijke-ontwikkeling)<br>
[Verloopstage](https://github.com/Stage-Bravo/Portfolio/tree/main/Bewijsvoering#verloopstage)<br>

## Sprints 
Om mijn sprints in te plannen maak ik een bord in Github waar ik mijn planning van de komende 2 weken opstel. Hiermee maak ik 4 koppen aan, TODO, In Progress, Feedback en Done. Hieronder laat ik een voorbeeld zien van hoe een sprint planning eruitziet.

![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/7cd8a00b-3ad5-44ca-b29f-04dcb6a69a35)
 
Bij elk item dat ik in de planning heb aangemaakt heb ik omschrijving erbij gezet waardoor ik beter weet wat ik bedoelde en dan kunne anderen het ook beter begrijpen wat ik in de planning omschrijf. Hieronder zie je daar een voorbeeld van: 

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
 
De functie moet aangeroepen worden door /token te gebruiken. We vragen om de headers email en wachtwoord mee te sturen. Die hebben we namelijk nodig om te kijken of de gebruiker toegang heeft tot de API’s en in welke WBE hij hoort. Er wordt dan een dependecy injection gebruikt voor het aanroepen van functies in andere lagen. We roepen dan uiteindelijk een de functie maakToken aan in de class tokenCollectie die we dan gelijk gereturnd via de API. 

Zo ziet de class tokenCollectie eruit die in de laag logic zit. 
 

Naast dat heb ik het project van een localhost naar een lokale server die op het bedrijf gebruikt wordt verplaats. Hierdoor kan ik nabootsen hoe de API's reageren op een publieke server. Hierdoor hoef ik geen aandacht meer te besteden aan cross handelingen. 


Het applicatie onderzoek heb ik uitgesteld omdat er niet met OOP gewerkt is en er verder weinig structuur in zit. Nu dat ik verder ben in het project heb ik opgeschreven hoe de applicatie er nu uitziet vergeleken hoe we het op school aangeleerd krijgen. Hier heb ik de voor- en nadelen van opgeschreven van beide kanten. Naast dat heb ik beschreven hoe de API in het project gedesigneerd is. Het onderzoek kun je [HIER](https://github.com/Stage-Bravo/Portfolio/blob/main/Onderzoek/Onderzoeksrapport.pdf) vinden.

### Sprint 5
In sprint 5 ben ik vooral bezig geweest met het uitbreiden van het project. Hiermee heb ik de endpoints gegevens ophalen gemaakt en heb ik een functie gemaakt die de user id uit de JWT-token haalt. Daarnaast heb ik verbeterpunten toegepast aan mijn onderzoeksrapport. In deze sprint ben ik ook verder bezig geweest om het applicatie onderzoek uit te breiden. 

Naast dat ben ik ook bezig geweest met hoe ik mijn stage uitgebreider kan maken. Dit is omdat er met een gesprek met mijn assessor er twijfels kwamen wat ik nog kan laten zien om alle leeruitkomsten goed te kunnen behalen. Daarom gaan we contact leggen met het bedrijf dat de API’s zou gaan gebruiken om te kijken hoe we het kunnen uitbreiden.

### Sprint 6
Naast dat ben ik veel bezig geweest met hoe ik mijn stage uitgebreider kan maken zodat ik alle leeruitkomsten uitgebreid kan gaan aantonen. Dit heb ik gedaan door te vragen welke endpoint er nodig zijn om dit project tot een goede uitkomst te krijgen. Naast dat ga ik de API’s op een server runnen en daarbij ga ik kijken of ik dit automatisch kan laten lopen via Github waarbij ik gebruik maak van ci/cd. 

### Sprint 7
 
