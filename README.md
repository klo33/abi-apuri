# AbixApuri

AbixApuri (ent. AbittiApuri) on ilmainen ja avoin käyttöliittymälaajennus Ylioppilastutkintolautakunnan 
[oma.abitti.fi]-koepalveluun. **AbixApuri** toimii Firefox- ja Chrome-selaimissa erillisen ladattavan laajennoksen [GreaseMonkey][1]/[TamperMonkey][2]). 

## Ominaisuudet

1. WYSIWYG-editori tehtävitekstien muokkaamiseen
  * mahdollistaa tekstin muotoilun sekä muotoillun tekstin ja kuvien liittämisen suoraan tehtävänantokenttiin esim. Wordistä.
2. Vanhojen tehtävien uudelleenkäyttö kopioimalla tehtävä vanhasta kokeesta
3. Tehtävien järjestely kokeen sisällä intuitiivisesti raahaamalla.

## Asentaminen

1. Firefox-selaimessa lataa [GreaseMonkey][1]-lisäosa. Chrome-selaimessa lataa [TamperMonkey][2]-lisäosa.
2. Lataa [AbixApuri-skriptilaajennos][3]-javascript osoitteesta [github.com/klo33/abi-apuri/raw/master/src/AbittiApuri-skripti.user.js][3]. Jos laajennos on asennettu selaimeen sen pitäisi ehdottaa asennusta.
3. Osoitteessa [oma.abitti.fi] varmista, että skripti on päällä. Huom! Skripti on aktiivinen **vain** muokkaustilassa, ei listanäkymässä.

### Muutokset
#### v0.0.3 (19.5.2017)
- Lisätty järjestystoiminnallisuus

### Tunnetut ongelmat
+ Chrome-selaimessa TamperMonkey'ssa kuvien liittämisessä leikepöydältä on vielä ongelmia. Firefox-GreaseMonkey-yhdistelmällä toimii.

### Lisenssi ja vastuuvapaus

Lisäosan kehittäjällä ei ole mitään yhteyksiä Ylioppilastutkintolautakuntaan, eikä lisäosa ole YTL:n kehittämä. Tarkoituksellisesti lisäosa ei tee mitään pahantahtoista YTL:n tai kolmannen osapuolen palvelulle. Huomaa kuitenkin, että skriptikoodia ei ole laajasti testattu, joten käyttö omalla vastuulla. Jos olet epäilevä, niin käytä erillistä testitunnusta.

Lisäosa ei siirrä mitään informaatiota YTL:n [oma.abitti.fi]-palvelun ulkopuolella, mutta lähettää aktiivisesti rajapintakutsuja kyseiseen palveluun kyseisen sivun "päälle liimattuna osana" sekä lataa skriptitiedostoja internetistä (toiminnallisuuksiin liittyvät laajennuksia). Sinänsä toiminnallisuuksien ei pitäisi rikkoa yhtään mitään YTL:n eikä käyttäjän tiedoista, mutta skripti tekee muutoksia koetietoihin, mikä onkin sen käyttötarkoitus.

AbixApuri (ent. AbittiApuri) on julkaistu [GPLv3]-lisenssillä. Lyhyesti, laajennusskripti on ilmainen käyttää, sen lähdekoodi on julkinen ja sitä saa muokata. Muokkauksissa ja käytössä pitää lähde ja alkuperäinen lisenssi mainita sekä julkaista koodi myös GPL:n alaisuudessa. AbixApuri-skriptiä käytetään omalla vastuulla, eivätkä kehittäjät vastaa mistään skriptin aiheuttamasta vahingosta.

### Yhteystiedot
Lisätiedot ja palaute Joni Lehtola, [etunimi.sukunimi@kauniaistenlukio.fi]

[1]:https://addons.mozilla.org/fi/firefox/addon/greasemonkey/
[2]:https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo
[3]:https://github.com/klo33/abi-apuri/raw/master/src/AbittiApuri-skripti.user.js
[GPLv3]:https://www.gnu.org/licenses/gpl-3.0.en.html
[oma.abitti.fi]:https://oma.abitti.fi
