SQL Injection
================

Basis SQL
---------

Met voorkennis van SQL, MySQL, SQLite of andere SQL varianten kan je dit
overslaan

SQL is een taal die gebruikt wordt om te communiceren met een database.
Hier wordt veel dieper op ingegaan tijdens de module *Databases*, maar
wordt nu een kleine basis van gegeven. SQL lijkt ontzettend op Engels en
is daarom relatief makkelijk om te leren.

De beste sites om de basis van SQL mee te leren zijn:
1. [https://www.codecademy.com/learn/learn-sql](https://www.codecademy.com/learn/learn-sql)
1. [https://www.w3schools.com/sql/](https://www.w3schools.com/sql/)

Vroeger bestonden er geen frameworks om databases abstracter te maken
(meer high-level). Alles werd destijds handmatig gedaan met (meestal)
PHP en semi-hardcoded (een deel voorgeschreven code wat aangevuld wordt
met de gegevens die een gebruiker invult) SQL statements. Dit zorgt
ervoor dat wanneer er geen input sanitation (het schoonmaken van de
invoer van de gebruiker) is, een hacker zelf een SQL statement kan
meesturen.

Met input sanitation zorgt een programmeur dat de gegevens die een
gebruiker meesturen ook juiste gegevens zijn. Zo voorkomt de programmeur
een crash in zijn programma, of ongewenste bijwerkingen. Bijvoorbeeld
een stuk text meesturen wanneer er om een nummer gevraagd wordt zou dan
afgevangen worden.

Een voorbeeld hiervan is het opvragen van gegevens in een magazijn. Zo
kan een gebruiker zoeken op basis van een item_name wat in het magazijn
zit:

```sql
SELECT item_id, item_name, item_count
FROM stock
WHERE item_id = $userItemID;
```

Omdat een puntkomma de query afsluit en ook direct mogelijkheid geeft om
andere queries te doen, kan een hacker ook andere gegevens opvragen.
Zoals bijvoorbeeld klantgegevens van anderen. Als de hacker zoekt naar
het volgende artikel, krijgt hij de klantgegevens te zien:

![sql-inject-1](assets/image6.png)

Dit komt omdat nu de volgende query wordt verzonden:

```sql
SELECT item_id, item_name, item_count
FROM stock
WHERE item_name=1; SELECT * FROM customers;
```

De hacker krijgt dan het artikel met item_id=1 te zien, maar ook het
hele klantenbestand.

Ook kan een hacker inloggen op elk account met deze manier. Als de
hacker in een inlogform het volgende zou invullen en de authentication
niet goed gedaan is, logt hij in met alleen een gebruikersnaam:

![sql-inject-2](assets/image7.png)

Hierbij is de SQL als volgt geprogrammeerd:

```sql
SELECT user_id
FROM users
WHERE username='$username'
   AND password='$password';
```

Hierdoor wordt het met de injectie:

```sql
SELECT user_id
FROM users
WHERE username='admin'
   AND password=''
    OR 1=1;
```

Geen wachtwoord meer nodig dus, aangezien 1 altijd gelijk staat aan 1 en
er geen andere vorm van login verificatie is. Makkelijk binnenkomen.

Links
-----

Kijk hier eens als je nog meer wilt weten:

- [SQL Injection bij w3schools](https://www.w3schools.com/sql/sql_injection.asp)
- [Video van Computerphile (aanrader!)](https://www.youtube.com/watch?v=ciNHn38EyRc)
