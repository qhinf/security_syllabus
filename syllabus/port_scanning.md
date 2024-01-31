Port scanning
================

Ports
-----

Wanneer een server op een netwerk een service aanbiedt, draait deze
service op een port. Zie een port als een huisnummer in een straat. Je
wil communiceren met die ene persoon die op dat huisnummer woont.
Wanneer er een verbinding tussen apparaten wordt gelegd gebeurd dit
altijd over een port.

De meest bekende ports op TCP zijn:

|80  |HTTP (Webserver, levert web pagina’s)|
|-----|----------------------------------------------------|
|443|HTTPS (Webserver, maar dan met TLS encryptie)|
|22|SSH (Serverbeheer op afstand met een remote shell)|
|21|FTP (Filesharing)|
|993|IMAP (Om mail op te ontvangen)|
|587|SMTP (Om beveiligd mail op te versturen)|

Port scanner
------------

Als security professional wil je natuurlijk weten welke ports er open
staan en dus welke services een server levert. Om hier snel achter te
komen zijn er port scanners. Deze verbinden op elke mogelijke port om
erachter te komen of deze een service open heeft.

Er zijn verschillende typen port scan, deze verbinden op verschillende
manieren met de poorten. Sommige van deze typen port scan zijn te
detecteren door een firewall en dus ook af te weren. Andere types zijn
onherkenbaar voor een firewall, maar deze zijn ook minder nauwkeurig in
het detecteren welke service er draait.

Een voorbeeld van een port scanner is [https://www.advanced-port-scanner.com/](https://www.advanced-port-scanner.com/)
Deze kan je downloaden en uitproberen op je eigen netwerk tegen bijvoorbeeld 
het IP-adres van je router.

Port scannen van een willekeurige computer op het inter wordt als een offensieve actie beschouwd. Dit is het computer-equivalent van bij alle deuren van de straat kijken welke open staat. Dit levert je een mogelijke aanklacht van huisvredebreuk of in dit geval computervredebreuk op.

Je mag voor deze module wel port scannen op [https://ctf.q-highschool.nl/](https://ctf.q-highschool.nl/).

Directory fuzzing
---
Wanneer je eenmaal een HTTP(S)-server gevonden hebt op een poort, kan het interessant zijn om te kijken welke mappen en bestanden toegankelijk zijn. Zelden is het mogelijk om een directory-listing te bekijken. Om toch uit te kunnen vinden welke mappen en bestanden op de server toe- gankelijk zijn is het mogelijk om een zogenaamde _directory fuzzer_ in te zetten. Dit is een programma wat systematisch allerlei mogelijkheden nagaat. Hierbij wordt gebruik gemaakt van vaak gebruikte map- en bestandsnamen. Een zogenaamde brute-force aanval is ook mogelijk. Het voordeel van de brute-force is dat dit zo’n beetje alle mappen en bestanden bloot kan leggen. Nadeel is dat het erg lang duurt (mogelijk zelfs enkele dagen). Dus je zult hier een afweging moeten maken.
De termen die voor deze technologie gebruikt worden zijn _directory fuzzing_ en _URL fuzzing_. De term fuzzing omvat meer dan alleen het vinden van bestanden in een webserver, dat is misschien wel handig om te weten.

Een voorbeeld van een al wat oudere maar nog steeds populaire directory fuzzer is [DirBuster](https://sourceforge.net/projects/dirbuster/). Het programma wordt geleverd met een aantal woordenlijsten met de meeste gebruikte map- en bestandsnamen. Met een kleinere lijst is het programma sneller klaar met het uitproberen van alle mogelijkheden, maar is de kans ook groter dat je interessante pagina's mist omdat die niet in de lijst zaten. Als de `small` lijst van DirBuster je al te lang duurt, kun je ook [deze `tiny` lijst](assets/directory-list-lowercase-2.3-tiny.txt) gebruiken om mee te spelen. Bedenk ook goed in welk type bestanden je geïnteresseerd bent, in welke map die staan, of je ook geïnteresseerd bent in submappen (*recursive* zoeken) en of je op zoek bent naar mappen, bestanden of allebei. De juiste opties aanvinken kan een hoop tijd schelen.

Links
-----

Kijk hier eens als je nog meer wilt weten:

- [Meer over poorten en sockets](http://www.steves-internet-guide.com/tcpip-ports-sockets/)
