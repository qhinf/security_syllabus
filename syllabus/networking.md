Networking
=============

De basis
--------

Wanneer je contact legt met een andere computer, gaat dat over een
netwerk. Een netwerk bestaat uit meerdere computers en een manier van
communicatie tussen deze computers.

Sommige computers zijn servers. Dit type computer levert services aan de
rest van het netwerk. Denk hierbij aan websites, game servers, etc.
Andere zijn routers, deze zorgen ervoor dat de computers elkaar kunnen
bereiken. De grootste groep is echter ‘normale’ computers. Deze noemen
we **clients**. Alle apparaten aangesloten op het netwerk hebben een IP
adres. Dit is een identificatie die je krijgt van je router. Dit ip
wordt meegestuurd in elk bericht wat je doet over het netwerk.

De router thuis is een samensmelting van drie aparte apparaten:

-   Een Router, die het verkeer stuurt naar waar het moet gaan. Deze
    ontvangt data van de pc’s, stuurt het door naar de volgende
    apparaten in het netwerk (bijvoorbeeld een website) en ontvangt de
    data terug van de website. Daarna stuurt hij het terug naar de pc.

-   Een Access Point, die het internet van een kabel naar radiogolven
    omzet. Hiermee heb je wifi zodat je apparaten draadloos ook internet
    hebben.

-   Een firewall, die het thuisnetwerk beschermt en afschermt. Dit zorgt
    ervoor dat alle verbindingen van buitenaf gestopt worden, tenzij ze
    zijn toegestaan binnen de firewall. Het toestaan van deze
    verbindingen wordt port forwarding genoemd.

De routers die verder worden genoemd in deze module, wordt niet de hele
samensmelting mee bedoeld, maar alleen het eerste onderdeel.

In de oudere versie van het internet (maar nog steeds het meest
gebruikt), ipv4, zijn de routers het meest prominent. Dat komt omdat
elke pc verbonden met het internet, eerst langs een of meerdere routers
moet. Op het internet kunnen PC’s elkaar dus niet direct bereiken. Met
de nieuwere versie, ipv6, heeft elke pc een directe verbinding met een
andere. Er zijn geen blokkades of firewalls meer, anders dan die op de
pc geïnstalleerd.

Een manier om ipv4 te visualiseren is om het te vergelijken met een
buurt. In een buurt staan huizen en winkels. Alle gebouwen hebben een
adres waarop pakketjes bezorgd kunnen worden. De hoofdbewoner van het
huis ontvangt pakketjes en verdeelt ze onder de bewoners. Wanneer een
bezorger een adres niet kan vinden, kan hij het vragen aan iemand die
hem doorverwijst (een ‘router’). De winkels leveren diensten aan de
buurt en aan mensen van buiten de buurt.

Met ipv6, is de visualisatie hetzelfde. Alleen nu hebben de gebouwen
geen adres, maar de mensen zelf een apart adres. Zo hebben bewoners van
hetzelfde gebouw hetzelfde begin van het adres, maar elk een apart
gedeelte aan het eind.

Communicatie
------------

De manier van communicatie in een netwerk gebeurd met een ‘protocol’.
Een protocol is simpelweg een set van regels. Deze regels worden
aangehouden om een standaard manier van communicatie te hebben. Zie een
protocol als de grammatica van een taal: er is een vaste zinsopbouw en
vervoeging van woorden.

De hoofd protocollen waar vele andere op gebaseerd zijn, zijn TCP
(Transmission Control Protocol) en UDP (User Datagram Protocol). TCP
checkt dat elk bericht netjes is ontvangen en begint de communicatie met
een driedelige ‘handdruk’. Deze handdruk bevat informatie over de
connectie tussen de twee computers waarop de daarna volgende berichten
worden aangepast. Een handdruk is een proces waarbij twee apparaten
overleggen hoe de verdere communicatie plaats zal vinden.

De TCP handdruk gaat met drie berichten, SYN-SYN/ACK-ACK. Dit staat voor
‘Synchronize’, ‘Acknowledge Synchronize’ en ‘Acknowledge Acknowledged’.
Dus het synchronizatieverzoek wordt bevestigd en de bevestiging wordt
ook bevestigd. Daarmee is een verbinding gelegd. Als deze handshake niet
succesvol wordt uitgevoerd, begint er geen data transmission en is er
dus geen sprake van een verbinding.

MAC-adressen
------------

Zonder dat een apparaat een IP-adres heeft, kan er geen communicatie mee
zijn. Een router geeft een IP-adres aan een apparaat, maar hoe kan dit
zonder dat de router via bijvoorbeeld TCP of UDP met het andere apparaat
kan praten?

Dit gebeurt door middel van MAC-adressen. MAC staat voor Media Access
Control en doet precies waar de naam voor staat. Wanneer een computer
een IP-adres van de router wil ontvangen, doet deze een verzoek met het
DHCP-protocol. Hierbij stuurt de computer een MAC-adres mee, zodat de
router weet waar het bericht naar verzonden moet worden. Dit verzoek
gaat naar alle apparaten die verbonden zijn met dezelfde kabel of
hetzelfde wifi netwerk. Zonder dat een MAC-adres meegezonden wordt, is
er dus volledige chaos en weet geen enkel apparaat voor wie welk bericht
bedoeld is. Een verzoek dat wordt verzonden op het hele netwerk noem je
een **broadcast message**.

De router die ontvangt vervolgens het verzoek en stuurt terug welk
IP-adres de computer krijgt. Om ervoor te zorgen dat niet elk ander
apparaat dit ontvangt en ‘verward’ raakt, stuurt de router het MAC-adres
mee van de ontvanger en van zichzelf. Zo weet het apparaat op welk
MAC-adres de router bereikt kan worden en de router waar het verkeer
naar toe moet voor het apparaat.

Links
-----

Kijk hier eens als je nog meer wilt weten:

- [28-delige videoserie over netwerken](https://www.youtube.com/watch?v=cNwEVYkx2Kk&list=PLDQaRcbiSnqF5U8ffMgZzS7fq1rHUI3Q8)
