Kirjoita ohjelma, joka ottaa vastaan yhden tai useamman numeron komentoriviparametreina ja tulostaa lukujen summan konsoliin (stdout).

----------------------------------------------------------------------
## VIHJEITÄ

Pääset käsiksi komentoriviparametreihin globaalin `process`-olion avulla. `process`-oliossa on `argv`-niminen kenttä, joka sisältää listan, jossa on ensimmäisenä alkiona indeksissä 0 `node`-binaarin nimi, toisena alkiona indeksissä 1 ohjelmasi täydellinen polku ja sen jälkeisinä alkioina indekseissä 2:sta eteenpäin ohjelmasi komentoriviparametrit. Jos sinulla esimerkiksi on ohjelma

```js
console.log(process.argv)
```
ja ajat sen komennolla `node ohjelma.js`, niin vastauksena on tämäntapainen lista:

```js
[ 'node', '/polku/ohjelmaasi/ohjelma.js', '1', '2', '3' ]
```
Sinun tulee kirjoittaa jonkinlainen silmukka, joka käy läpi numeroita sisältävät komentoriviparametrit, jotta voit laskea ne yhteen. Koska luvut ovat listassa merkkijonoina, ne on muunnettava oikeiksi luvuiksi esimerkiksi laittamalla '+'-merkki niiden eteen, s.o. `+process.argv[2]`.

{appname} kutsuu ohjelmaasi sopivilla parametreilla kun ajat tarkastuksen `{appname} verify program.js`, joten sinun ei tarvitse antaa parametreja omin päin. Jos haluat testata ohjelmaasi ilman tarkastusta, voit ajaa `{appname} run program.js`. Kun käytät käskyä `run`, käytät kuitenkin testiympäristöä, jonka {appname} asettaa kutakin tehtävää varten erikseen.
