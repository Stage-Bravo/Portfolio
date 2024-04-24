# Voortgang Stage Project

## Inhoudsopgave

## Introductie
In dit bestand ga ik beschrijven wat ik voor het project gemaakt heb en welke keuzes ik daarbij heb gemaakt. Hiermee wil ik mijn voortgang laten zien die ik heb gemaakt op mijn stage. 

## Algemeen programmeren
Voor dit project heb ik een aantal keuzes gemaakt en die wil ik in het stuk beschrijven.
### OOP
Bij mijn stage bedrijf wordt er geen gebruik gemaakt van OOP. Dit wil ik doormiddel van dit project laten zien hoe het werkt en wat de voordelen daarvan zijn. 
### MVC
Ik wil doormiddel van MVC te gebruiken laten zien hoe je een MVC-applicatie opstelt en wat de voordelen daarvan zijn. Hierdoor zal het bedrijf de kennis hebben om een MVC-applicatie op te kunnen stellen voor misschien een toekomstig project. 
### Nederlandse taal
Vanwege hoe Mijn Jachtveld is gemaakt heb ik besloten om te programmeren in het Nederlands. Dit doe ik omdat ik niet te veel wil afwijken van hoe ze hier doen programmeren. 

## API’s 
In het project heb ik een aantal API’s ontwikkeld. Een van die API’s wordt een JWT-token gemaakt, hierdoor kan ik later controleren of degene rechten heeft om gebruik te maken van de API’s. Voor meer informatie of JWT-tokens klik HIER. Hieronder laat ik de API zien die de JWT-token aanmaakt:
![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/4cf0e9cc-3b0f-4adf-93b3-6a64c949482e)

Hier kun je de API genaamd token zien. Je kunt hier zien dat het een GET API is met de route /token. De eerste 2 regels in de API zijn de data ophalen uit de header van de API. Daarna gaan we de JWT-token ophalen in de class token als de gegevens goed zijn. Daarna gaat de token teruggestuurd worden via de body.

## JWT-token
We hebben het er net over gehad dat we een API hebben aangeroepen waar we een JWT-token maken, hier gaan we kijken hoe we de JWT-token doen aanmaken. Hieronder zie je hoe de JWT-token wordt aangemaakt.
 ![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/c807b7e6-c184-4543-b97a-5a6f5ce33f34)

Als eerste wat hier wordt gekeken is of de inlog gegevens goed zijn zodat de gebruiker überhaupt een token mag krijgen. Daarna wordt de token aangemaakt waarbij de gebruikers id wordt toegevoegd die we encrypten voor de veiligheid. Aan de token wordt de tijd toegevoegd van hoelang de token geldig mag zijn en dan wordt de tijd en datum toegevoegd van wanneer de token wordt aangemaakt. 

Dat is hoe de Token wordt aangemaakt maar nu gaan we kijken hoe we kijken of de token geldig is. Hieronder staat een schermafbeelding van hoe ik dat heb gedaan. 
![image](https://github.com/Stage-Bravo/Portfolio/assets/103424907/e8bc140e-cde9-4de8-bbc3-efaa8dde2aca)
 
Als eerste onderdeel kijken we of de JWT-token uit 2 delen bestaat en als dat zo is halen we die 3 delen uit elkaar. Dan decoden we de header en de payload zodat we weten wat daarin zit. Dan kijken we eerst of het een JWT-token is met de goeie gegevens erin en daarna kijken we of de token nog geldig is in tijd. 
