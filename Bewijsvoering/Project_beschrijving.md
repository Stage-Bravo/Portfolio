# Project Beschrijving 

## Inhoudsopgave
[Introductie](https://github.com/Stage-Bravo/Portfolio/blob/main/Progressie_stage/Voortgang_Stage_Project.md#introductie)<br>
[Algemeen programmeren](https://github.com/Stage-Bravo/Portfolio/blob/main/Progressie_stage/Voortgang_Stage_Project.md#algemeen-programmeren)<br>
[API's](https://github.com/Stage-Bravo/Portfolio/blob/main/Progressie_stage/Voortgang_Stage_Project.md#apis)<br>
[JWT-token](https://github.com/Stage-Bravo/Portfolio/blob/main/Progressie_stage/Voortgang_Stage_Project.md#jwt-token)<br>
[Swagger](https://github.com/Stage-Bravo/Portfolio/blob/main/Progressie_stage/Voortgang_Stage_Project.md#swagger)

## Introductie
In dit bestand ga ik beschrijven wat ik voor het project gemaakt heb en welke keuzes ik daarbij heb gemaakt. Hiermee wil ik mijn voortgang laten zien die ik heb gemaakt op mijn stage. 

## Algemeen programmeren
Voor dit project heb ik een aantal keuzes gemaakt en die wil ik in het stuk beschrijven.
### OOP
Bij mijn stage bedrijf wordt er geen gebruik gemaakt van OOP. Dit wil ik door middel van dit project laten zien hoe het werkt en wat de voordelen daarvan zijn. 
### MVC
Ik wil door middel van MVC te gebruiken laten zien hoe je een MVC-applicatie opstelt en wat de voordelen daarvan zijn. Hierdoor zal het bedrijf de kennis hebben om een MVC-applicatie op te kunnen stellen voor misschien een toekomstig project. 
### In het Nederlands programmeren
Vanwege hoe Mijn Jachtveld is gemaakt heb ik besloten om te programmeren in het Nederlands. Dit doe ik omdat ik niet te veel wil afwijken van hoe ze hier doen programmeren. 

## API’s 
In het project heb ik een aantal API’s ontwikkeld. Een van die API’s wordt een JWT-token gemaakt, hierdoor kan ik later controleren of degene rechten heeft om gebruik te maken van de API’s. Voor meer informatie of JWT-tokens klik [HIER](https://github.com/Stage-Bravo/Portfolio/blob/main/Onderzoek/Onderzoeksrapport.pdf). Hieronder laat ik de API zien die de JWT-token aanmaakt:
![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/4cf0e9cc-3b0f-4adf-93b3-6a64c949482e)

Hier kun je zien hoe de API genaamd token gemaakt wordt. Je kunt hier zien dat het een GET API is met de route /token. De eerste 2 regels in de API zijn de data ophalen uit de header van de API. Daarna gaan we de JWT-token ophalen in de class token als de gegevens goed zijn. Daarna gaat de token teruggestuurd worden via de body.

## JWT-token
We hebben het er net over gehad dat we een API hebben aangeroepen waar we een JWT-token maken, hier gaan we kijken hoe we de JWT-token doen aanmaken. Hieronder zie je hoe de JWT-token wordt aangemaakt.
 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/c807b7e6-c184-4543-b97a-5a6f5ce33f34)

Als eerste wat hier wordt gekeken is of de inloggegevens goed zijn, zodat de gebruiker überhaupt een token mag krijgen. Daarna wordt de token aangemaakt waarbij de gebruikers id wordt toegevoegd die we encrypten voor de veiligheid. Aan de token wordt de tijd toegevoegd van hoelang de token geldig mag zijn en dan wordt de tijd en datum toegevoegd van wanneer de token wordt aangemaakt. 

Dat is hoe de Token wordt aangemaakt, maar nu gaan we kijken hoe we kijken of de token geldig is. Hieronder staat een schermafbeelding van hoe ik dat heb gedaan. 
![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/e8bc140e-cde9-4de8-bbc3-efaa8dde2aca)
 
Als eerste onderdeel kijken we of de JWT-token uit 2 delen bestaat en als dat zo is halen we die 3 delen uit elkaar. Dan decoden we de header en de payload zodat we weten wat daarin zit. Dan kijken we eerst of het een JWT-token is met de goeie gegevens erin en daarna kijken we of de token nog geldig is in tijd. 

## Swagger 
Om documentatie te maken voor de API’s maak ik gebruik van Swagger. Hierdoor kan er makkelijk en overzichtelijk gezien worden welke API’s er beschikbaar zijn en wat ze doen. Hierdoor hoeft er geen uitgebreide documentatie gemaakt te worden voor anderen zodat ze we en bespaart het tijd. Naast dat is het handig om de API’s te testen op een overzichtelijke manier en hoef je niet steeds een front-end te maken om de interactie met de API’s te testen. Hieronder laat ik zien hoe je een API doet opzetten in Swagger.
![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/048fb5c2-eac9-44a6-a3b3-84e2e93bb76e)
 
Hierboven zie je hoe je een API documenteert in Swagger. Ik heb de API gepakt waar je een token mee doet aanmaken die ik bij een ander voorbeeld ook al heb gebruikt. De Swagger API moet gemaakt worden in comments. Je gaat erin omschrijven hoe de API er uit ziet, dus je begint met het pad en dan ga je de parameters toevoegen. Je kunt het een naam, beschrijven en requirements waardoor de API duidelijk wordt omschreven. Hieronder kun je zien hoe het er in Swagger er uitziet. 
![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/c8662ac8-e7d3-4b47-bc4e-e617068ade86)

## Testen 
Om te kijken of de functies goed werken die ik heb gemaakt ga ik testen schrijven zodat we weten of er geen errors in de applicatie zitten. Hiervoor wordt phpunit gebruikt en dat is de standaard voor het testen van PHP code. De enige functies die testen omvatten zitten in de logic laag. Hiervoor gebruik ik mockdata zodat er niks aangepast wordt in de database. Hieronder zie je 2 testen als voorbeeld dat ik heb opgesteld waarbij gekeken wordt of er op een goeie manier een token wordt aangemaakt. Hierbij wordt er een keer de goeie gegevens meegegeven en de andere keer worden de verkeerde gegevens meegegeven. 
 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/68e8add6-2f05-4fc7-8f1a-c1b576029004)

Om de testen te runnen moet je via de terminal een command aanroepen die het phpunit bestand doet runnen. Het ziet er dan zo uit als we de test die we net hebben laten zien te runnen.
 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/dee7d71d-039e-466f-9b3f-3f80e3962977)

