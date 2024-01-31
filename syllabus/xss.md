Cross-site scripting
=======================

Basis Javascript
----------------

Met voorkennis van Javascript kan je dit overslaan

Javascript is een taal die vooral wordt gebruikt in web development. Het
is een stuk code die in de browser van de client zelf runt. Zo kan je
web apps bouwen die efficiënter zijn omdat de server niet alles hoeft te
berekenen maar je een groot gedeelte af kan staan aan de clients zelf.
Tegenwoordig is Javascript niet meer weg te denken en is een van de
grootste programmeertalen in de wereld.

Javascript kan je leren op:

1. [https://www.codecademy.com/learn/introduction-to-javascript](https://www.codecademy.com/learn/introduction-to-javascript)
1. [https://www.w3schools.com/js/](https://www.w3schools.com/js/)
1. [https://en.wikibooks.org/wiki/JavaScript](https://en.wikibooks.org/wiki/JavaScript)

Javascript wordt op een website vaak geladen met een `<script>`
tag, maar kan ook op andere manieren geladen worden door bijvoorbeeld
een image of button tag.

Wat is cross-site scripting?
----------------------------

Omdat Javascript als HTML element geplaatst kan worden, kan er op
plekken waar de gebruiker een bericht kan achterlaten HTML meegestuurd
worden met het bericht. Zo ook, de script tag. Telkens wanneer dit
bericht gezien wordt door anderen, wordt er dus code uitgevoerd op dat
apparaat.

Een goed voorbeeld hiervan is de Self-Retweeting Tweet. Dit was een
simpele Tweet die er heel onschuldig uitzag, maar er was veel meer aan
de hand.

```html
<script class="xss">
    $('.xss').parents().eq(1).find('a').eq(1).click();
    $('[data-action=retweet]').click();
    alert('XSS in Tweetdeck');
</script>How are you doing?
```

Voor een persoon die deze Tweet zonder inspecteer element bekijkt, is
alleen de “How are you doing?” te zien. Maar, zonder dat de persoon er
zelf op geklikt heeft, is de Tweet al geretweet.

De code werkt als volgt:

1.  Een `script` tag met de styling class `"xss"` wordt gemaakt.

2.  De tag boven de script tag, dus die van de Tweet, wordt geselecteerd
    met jQuery.

3.  Vervolgens wordt er in de DOM gezocht naar een `a` element die een
    `data-action=retweet` heeft.

4.  Daar wordt `.click()` op uitgevoerd en de Tweet is geretweet.

Als je meer wilt weten over deze tweet dan is er hier een video van Tom
Scott: [https://www.youtube.com/watch?v=zv0kZKC6GAM](https://www.youtube.com/watch?v=zv0kZKC6GAM)

Het gevaar
----------

Dit lijkt heel onschuldig, maar XSS kan hele serieuze gevolgen hebben.
Telkens wanneer je inlogt op een website krijg je een cookie. Deze
cookie zegt dat jij bent ingelogd en hoe lang dat nog geldig is voordat
je opnieuw moet inloggen. Deze cookies zijn alleen ook te zien met
Javascript. Zo kunnen je persoonlijke gegevens dus in gevaar komen.

Ook kan er met Javascript een websocket connectie gemaakt worden,
waardoor er data kan worden verzonden naar een andere computer.

Als iemand kwaad zou willen, kan er dus een stuk script geschreven
worden waardoor je cookies worden opgeslagen in een variabele om
vervolgens verzonden te worden naar een aanvaller. Deze aanvaller kan
dan alles met jouw account alles wat jij ook kan, totdat de sessie
verloopt. Dit kan bij banken catastrofaal zijn.

Oefening
---------------------------------------

Op de volgende site krijg je 6 puzzels die je moet oplossen door XSS toe
te passen. Je kan direct om hints vragen of de code zien die ze
verwachten. [https://xss-game.appspot.com/level1](https://xss-game.appspot.com/level1)


Links
-----

Kijk hier eens als je nog meer wilt weten:

- [Uitleg van Imperva (onderdeel van Thales, die van de defensiesystemen)](https://www.imperva.com/learn/application-security/cross-site-scripting-xss-attacks/)
- [Nog een video met Tom Scott, op Computerphile](https://www.youtube.com/watch?v=L5l9lSnNMxg)