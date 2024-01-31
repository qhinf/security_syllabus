OSI Model
============

Voorkennis: {doc}`networking`

Het OSI-model is een manier van abstractie waardoor problemen in een
netwerkomgeving gemakkelijker te achterhalen zijn. Een laag in het model
geeft functie aan de laag erboven en krijgt functie door de laag
eronder. Er zijn 7 lagen zoals beschreven in ISO 7498-1. (International
Standardisation Organisation, de organisatie die alle standaarden
noteert en bewaart onder een ISO-nummer)

Waarom is dit nuttig?
---------------------

Wanneer er problemen zijn met een netwerk, kan het soms heel moeilijk
zijn om te weten waar deze problemen liggen. Ook wanneer je een
programma met netwerkfunctionaliteit schrijft, is het erg lastig te
achterhalen waar een fout kan zitten. Als netwerkbeheerder is het
essentieel om de functie juist te kunnen uitvoeren en systeembeheerders
kunnen met hulp van dit model zorgen dat de wifi altijd werkt.

Dit is ook niet uitsluitend voor netwerken, dit model kan toegepast
worden op elke vorm van digitale communicatie van apparaten onderling.

Wanneer je kennis hebt van dit model maakt het ook het hacken
makkelijker, aangezien je een netwerk op 7 lagen kan kraken.

Wat zijn de lagen?
------------------

De lagen worden hier beschreven van hoog naar laag, waardoor je een
beter begrip krijgt van de hardware erachter.

### Laag 7: Application

Deze laag zit het dichtst bij de gebruiker. Elk programma dat
netwerkfunctionaliteit aanbiedt zit in deze laag (bijv. Chrome en
Firefox). Alle vormen van serversoftware zitten bijvoorbeeld ook in deze
laag. De API’s zijn high-level, wat betekent dat er met relatief simpel
te begrijpen en weinig regels code heel veel op hardware niveau gedaan
wordt.

### Laag 6: Presentation

Deze laag is de brug tussen data op netwerkniveau en applicatieniveau.
Zo zet deze laag het verzoek om een website te bezoeken om in een echt
verzoek wat naar de webserver gaat en te begrijpen is voor de website.

Cryptografie zit ook in deze laag, de data wordt versleuteld
‘gepresenteerd’ aan een ander apparaat en daar in laag 6 weer omgezet in
data die de Application layer begrijpt.

### Laag 5: Session

Elk apparaat dat wil spreken met een ander, moet eerst een band leggen.
Dit wordt een session genoemd en alles wat te maken heeft met zo’n band
gebeurt in deze laag. Zo wordt er hier overlegd tussen apparaten hoe
lang ze wachten op communicatie van elkaar.

### Laag 4: Transport

Om een band tussen apparaten te kunnen leggen, moet er al een vorm van
communicatie zijn. Ook om überhaupt te kunnen praten met andere
apparaten moet er een ‘taal’ zijn die gesproken wordt. De meest bekende
vorm van zo’n transportsysteem is TCP (Transmission Control Protocol),
die gebouwd is op het IP (Internet Protocol). Samen worden ze TCP/IP
genoemd. TCP en UDP poorten werken op laag 4, ip adressen op laag 3.

### Laag 3: Netwerk

In de netwerklaag zit de meeste routerfunctionaliteit. Deze is
verantwoordelijk voor het rondsturen van pakketten. Wanneer een apparaat
in Europa wil praten met een ander apparaat in Amerika, gaat dit verkeer
eerst door heel veel routers er tussenin. Er zijn soms wel duizenden
andere apparaten waar het verkeer eerst doorheen gaat voordat het zijn
bestemming bereikt. Dit is ook de laag waar een apparaat een eigen adres
krijgt om verkeer op te ontvangen. Netwerkengineers vinden dit de meest
interessante laag.

### Laag 2: Data Link

De data link-laag zorgt voor directe communicatie tussen twee apparaten,
maar zorgt ook voor de foutcorrectie van laag 1. Er zijn hier twee
sublagen, namelijk de MAC (Media Access Control) laag en de LLC (Logical
Link Control) laag. De meeste switches werken op deze laag. Een switch
is netwerkapparatuur dat van een ethernetpoort meerdere maakt. Zo kunnen
er grote en gecompliceerde netwerkstructuren gemaakt worden, terwijl er
maar een kabel naar de centrale router toe gaat.

### Laag 1: Physical

Dit is het rauwste van het rauwste. De aller diepste laag zorgt voor de
fysieke transport van de data. Dat kan bijvoorbeeld over radiogolven
gaan, of 802.11 draadloos signaal, of een internet kabel. Elke vorm van
digitale communicatie wordt op een manier verzonden en is de
verantwoordelijkheid van deze laag. Meestal wanneer er een probleem is
in een netwerk, wordt deze laag als eerste bekeken. “Heb ik de internet
kabel er wel goed in zitten?” of “Ben ik wel verbonden met wifi?” zijn
de vragen die hier perfect bij passen.

Hoe onthoud ik dit?
-------------------

De zin *“A Penguin Said That Nobody Drinks Pepsi”* vergeet je nooit meer
en bevat alle eerste letters van het model. *“A Priest Saw Two Nuns
Doing Pushups”* is ook een zin die hier gebruikt kan worden.

Links
-----

Kijk hier eens als je nog meer wilt weten:

- [Uitleg met plaatjes op Lifewire](https://www.lifewire.com/layers-of-the-osi-model-illustrated-818017)
- [Video door TechTerms](https://www.youtube.com/watch?v=vv4y_uOneC0)
- [Kijk eens op Wikipedia!](https://nl.wikipedia.org/wiki/OSI-model)