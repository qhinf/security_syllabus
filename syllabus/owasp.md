OWASP Top 10
=============

Wat is de OWASP Top 10?
-----------------------
De OWASP Top 10 is een lijst van de 10 meest voorkomende 
beveiligingsproblemen in webapplicaties. De lijst wordt 
elke drie tot vier jaar aangepast door het Open Worldwide
Application Security Project (OWASP), en wordt door veel 
webdevelopers gebruikt om hun applicaties zo veilig mogelijk
te maken.

OWASP Top 10 2024
-----------------
Dit is de lijst in 2024:

1. Slecht Toegangsbeheer
Toegangsbeheer wordt gebruikt om gebruikers toegang, 
maar vooral belangrijker, geen toegang te geven aan 
bepaalde onderdelen van een website. Als dit niet correct 
is geïmplementeerd, kan het zo zijn dat een gebruiker 
toegang kan krijgen tot geheime informatie over de website, 
of zelfs informatie over andere gebruikers.

1. Slechte cryptografie
Slechte cryptografie bestaat uit heel veel verschillende 
problemen. Het zou bijvoorbeeld kunnen zijn dat een 
webapplicatie een slecht encryptiealgoritme gebruikt, 
dat geheime sleutels niet goed opgeslagen worden of 
dat sommige encryptie helemaal niet gebruikt wordt.

1. Injecties
Injecties zijn een veelvoorkomende kwetsbaarheid. 
Een injectie laat een aanvaller een stukje code 
naar een server of database sturen, waardoor deze 
iets uitvoeren wat eigenlijk niet de bedoeling was. 
Meestal komen deze problemen voor als er niet goed 
gecheckt wordt wat een gebruiker kan invullen op 
bepaalde stukken van de website. Denk dan bijvoorbeeld 
aan de mogelijkheid om letters te typen in een enquêtevraag 
waar je alleen getallen moet invullen (zoals je leeftijd).

1. Onveilig design
Dit probleem vat eigenlijk alle andere problemen samen, 
maar gaat vooral om de designstap van een webapplicatie, 
en niet over de implementatiestap. 

1. Veiligheidsmisconfiguraties
Kwetsbaarheden door misconfiguraties liggen vaak helemaal 
aan de webdeveloper zelf. Het houdt in dat bepaalde vereiste 
stappen niet uitgevoerd zijn, zoals bijvoorbeeld standaard 
inloggegevens veranderen of debuginformatie achterlaten. 

1. Zwakke en verouderde onderdelen
Veel websites zijn gebouwd op frameworks en libraries. Dit 
zijn eigenlijk ook gewoon stukjes code, en als deze niet 
geüpdatet worden, wordt de kans steeds groter dat er een 
veiligheidsprobleem gevonden gaat worden. Dit betekent dan 
dat dit veiligheidsprobleem ook in de website zit van de 
webdeveloper.

1. Slechte identificatie en authenticatie
Slechte identificatie en authenticatie gaan over slechte inloggegevens, zoals wachtwoorden. Denk dan bijvoorbeeld aan "123456789" als wachtwoord, of andere voorbeelden hier (https://mailsafi.com/blog/top-200-most-common-passwords/)

1. Slechte software en data-integriteit
Dit beveiligingsprobleem heeft niet zozeer met de webdevelopers zelf te maken, maar met software en data die ze gebruiken voor hun applicatie. Een stuk software kan bijvoorbeeld een update krijgen waar een (beveiligings)probleem in zit, en dit kan grote gevolgen hebben, zoals bijvoorbeeld de CrowdStrike storing van afgelopen juli (https://tweakers.net/nieuws/224584/microsoft-crowdstrike-storing-trof-8-komma-5-miljoen-windows-apparaten.html).

1. Slechte toezicht en boekhouding
Met slecht toezicht en boekhouding hebben webdevelopers geen idee wat er allemaal gebeurt op hun applicatie. Normaal worden toezicht en boekhouding gebruikt om aanvallen te voorkomen of actief tegen te werken, maar als dit er niet is, is het moeilijk om dit tegen te houden.

1. Server-side Request Vervalsing
Met dit beveiligingsprobleem kan een aanvaller zich voordoen als een server van de webapplicatie. Meestal is er beveiliging zodat alleen een server bij bepaalde informatie of data kan komen, maar nu kan de aanvaller dit dus ook.

Zie dit (https://www.reflectiz.com/blog/owasp-top-ten-2024/) voor nog meer voorbeelden.
