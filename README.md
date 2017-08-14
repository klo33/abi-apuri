# AbixApuri

**AbixApuri** (ent. AbittiApuri) on ilmainen ja avoin käyttöliittymälaajennus Ylioppilastutkintolautakunnan 
[oma.abitti.fi]-koepalveluun. **AbixApuri** toimii Firefox- ja Chrome-selaimissa erillisen ladattavan laajennoksen ([GreaseMonkey][1]/[TamperMonkey][2]) avulla. 

**AbixApuria** voi myös käyttää natiivin selainlaajennuksen avulla, josta tietoa alempana.

## Ominaisuudet

1. Tehtävätekstien muokkaus laajennetulla editorilla (WYSIWYG)
   * mahdollistaa tekstin muotoilun sekä muotoillun tekstin ja kuvien liittämisen suoraan tehtävänantokenttiin esim. Wordistä.
   * Chromessa kuvien liittäminen suoraan leikepöydältä ei toimi, mutta kuvia ja mediaa voi lisätä Lisää kuva -napilla
2. Vanhojen tehtävien uudelleenkäyttö kopioimalla tehtävä vanhasta kokeesta
3. Tehtävien järjestely kokeen sisällä intuitiivisesti raahaamalla.
4. Kopion ottaminen vanhasta kokeesta uudelleenkäytettäväksi

## Asentaminen

1. Firefox-selaimessa lataa [GreaseMonkey][1]-lisäosa. Chrome-selaimessa lataa [TamperMonkey][2]-lisäosa.
2. Lataa [AbixApuri][3] menemällä osoitteeseen [klo33.github.io/abixapuri/src/AbiApuri-skripti.user.js][3]. Jos 1-kohdan lisäosa on asennettu selaimeen oikein sen pitäisi ehdottaa asennusta. Hyväksy asennus.
3. Mene osoitteeseen [oma.abitti.fi] normaalisti. Tarvittaessa varmista GreaseMonkeys apina-kuvakkeesta tai TamperMonkeyn "ruutu"-kuvakkeesta, että AbixApuri on päällä.

Jos et halua asentaa ym. laajennoksia voit vaihtoehtoisesti asentaa oman selainlaajennoksen [Chromeen][5] tai [Firefoxiin][4], mutta tämä prosessi on monimutkaisempi. Tästä tietoa alempana.

Huomaa, että AbixApurin toimintaa haittaa, mikäli Bittiniilo on aktiivisena selaimessa. Suosittelemme sen poistamista käytöstä, ohjeet tähän alempana.

### Muutokset
#### v0.1.2 (8.8.2017)
- Virheenkorjauksia
  * korjattu kokeen tuontiin liittyvä ongelma
  * lisäkorjauksena v0.1.1 tullut ongelma korjattu
- Lisätty huomautus, jos Bittiniiloa käytetään yhtäaikaa
#### v0.1.0 (28.5.2017)
- Chrome-tuki
- CKEditor päivitetty versioon v4.7 ja lisätty lisäosia
- Tuki tehtävän kopioinnille
- Päivitetty ulkoasua ja korjattu bugeja mm. järjestelytoiminnossa
#### v0.0.3 (22.5.2017)
- Lisätty järjestystoiminnallisuus
  * Ei toimi vielä alatehtävissä
- Lisätty viivästetty tallennus, jos kuvia liittää suuria määriä
- Eroteltu YTL:n toivomuksesta selkeämmin lisätyt elementit ja YTL:n elementit sekä tieto, että lisäosa on latautunut

### Selainlaajennokset
- [Firefoxille][4]
- [Chromelle][5]

#### Miksi haluan käyttää erillisiä selainlaajennoksia?
Tietooni on tullut, että AbixAjurin juridisesta asemasta on heitetty epäilyksiä, viitaten siihen, että GreaseMonkey ja TamperMonkey eivät olisi luotettavia. Molemmat lisäosat ovat vakiintuneita ja hyvämaineisia, erityisesti viimeaikoina kun niiden skriptien asetuksia on pystynyt rajaamaan tarkemmin.

Erillisen laajennuksen käyttö poistaa nämä epäilyt. Erityisesti tämä koskee Firefoxin laajennusta, joka on allekirjoitettu heidän laajennussertifikaatillaan.

#### Miksi selainlaajennokset eivät ole selaimien laajennoksien omilla sivustoilla?

Laajennoksen lataavat YTL:n ulkopuolista koodia (CKEditor ja jäsennyksen käyttöliittymäkoodi sekä erikoisfontin renderöintikoodi), joka ei ole selainlaajennoksissa sallittua. Kaikki muut on erittäin helppo ja nopea saada toimimaan myös laajennoksen sisällä, mutta CK-Editor vaatisi aika paljon työtä, jotta sen pystyisi toiminnallisesti saamaan siihen asuun joka ei lataa mitään ohjelmakoodia YTL:n verkkosivujen ulkopuolelta.

Juuri nyt tähän ei olla ryhtymässä, joten laajennoksia ei tule selainkauppoihin ihan lähiaikoina.

### Tuki ja ongelmatilanteet
Uusista huomatuista virheistä ja ongelmista kannattaa raportoida ensisijaisesti [GitHubin projektin virheseurantaan](https://github.com/klo33/abixapuri/issues).

AbixApuri on avointa ohjelmistoa, jossa ei ole varsinaista käyttötukea, mutta toki autan parhaani mukaan, jos tarve on suuri.
Apuja voi kysellä minun sähköpostini lisäksi [Tietokoneet YO-kirjoituksissa Facebook-ryhmästä](https://www.facebook.com/groups/339542799419574/).

### Ohjeet AbixAburin tai Bittiniilon poisasentamiseksi
AbixApurin toiminnallisuutta haittaa Bittiniilon aktiivisena olo. Mikäli et ole ostanut maksullista Bittiniilon lisenssiä, ei se auta kokeenlaadinnassa, jolloin se kannattaa poistaa käytöstä.

#### Bittiniilon kytkeminen pois käytöstä
- Chromessa sivuvalikosta (...-ikoni) *Lisää työkaluja* -> *Laajennukset*
Ota ruksi pois Bittiniilon *Käytössä* sarakkeesta. Jos haluat poistaa Bittiniilon kokonaan, voit valita myös roskakorin.
Mikäli vain poistit laajennukset käytöstä, on se helppo palauttaa käyttöön valitsemalla *Ota käyttöön*.

- Firefoxissa valikossa (kolme vaakaviivaa) valitse *Lisäosat* ja tarvittaessa sivuvalikosta *Laajennukset*. Bittiniilon kohdalla paina *Poista käytöstä* napista.
#### AbixApurin kytkeminen pois käytöstä
- Chromessa kun olet oma.abitti.fi-osoitteessa valitse TamperMonkey-laajennuksen kuvake (pyöreäreunainen neliö, jossa kaksi aukkoa) ja AbixApurin kohdalta käännä on->off. Tarvittaessa päälle kytkentä samoin.
- Firefoxissa oma.abitti.fi-osoitteessa GreaseMonkey-laajennuksen kuvakkeesta (apinakuvake) alasnuoli -> ota valinta pois AbixApurin kohdalta. Tarvittaessa kytke uudelleen päälle ja päivitä verkkosivu.

### Tunnetut ongelmat
+ Chrome-selaimessa TamperMonkey'ssa kuvien liittämisessä leikepöydältä on vielä ongelmia. Firefox-GreaseMonkey-yhdistelmällä toimii.
+ Viivästetyn tallennuksen ollessa aktiivinen, koetehtävien järjestelytoiminto kyllä pyrkii tallentamaan kokeen, mutta potentiaalisesti voi joutua tilanteeseen, että viimeisimmät muutokset menetetään.

### Lisenssi ja vastuuvapaus

Lisäosan kehittäjällä ei ole yhteyksissä Ylioppilastutkintolautakuntaan, eikä lisäosa ole YTL:n kehittämä. Tarkoituksellisesti lisäosa ei tee mitään pahantahtoista YTL:n tai kolmannen osapuolen palvelulle. Huomaa kuitenkin, että skriptikoodia ei ole laajasti testattu, joten käyttö omalla vastuulla. Jos olet epäilevä, niin käytä erillistä testitunnusta.

Lisäosa ei siirrä mitään informaatiota YTL:n [oma.abitti.fi]-palvelun ulkopuolella, mutta lähettää YTL:n Abitti-palveluun rajapintakutsuja kyseisen sivun "päälle liimattuna osana" sekä lataa skriptitiedostoja internetistä (toiminnallisuuksiin liittyvät laajennuksia). Sinänsä toiminnallisuuksien ei pitäisi rikkoa yhtään mitään YTL:n eikä käyttäjän tiedoista, mutta skripti tekee muutoksia avoinna olevan kokeen tietoihin, mikä onkin sen käyttötarkoitus. Muihin kokeisiin laajennus ei tee muutoksia.

AbixApuri (ent. AbittiApuri) on julkaistu [GPLv3]-lisenssillä. Lyhyesti, laajennusskripti on ilmainen käyttää, sen lähdekoodi on julkinen ja sitä saa muokata. Muokkauksissa ja käytössä pitää lähde ja alkuperäinen lisenssi mainita sekä julkaista koodi myös GPL:n alaisuudessa. AbixApuri-skriptiä käytetään omalla vastuulla, eivätkä kehittäjät vastaa mistään skriptin aiheuttamasta vahingosta.

    AbixApuri - Lisäosa oma.abitti.fi-palveluun
    Copyright (C) 2017 Joni Lehtola

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see [http://www.gnu.org/licenses/]

### Yhteystiedot
Lisätiedot ja palaute Joni Lehtola, etunimi.sukunimi@kauniaistenlukio.fi

[1]:https://addons.mozilla.org/fi/firefox/addon/greasemonkey/
[2]:https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo
[3]:https://klo33.github.io/abixapuri/src/AbiApuri-skripti.user.js
[4]:https://github.com/klo33/abixapuri/blob/master/dist/abixapuri-0.1.2-an+fx.xpi?raw=true
[5]:https://github.com/klo33/abixapuri/blob/master/dist/AbixApuri-loader-0.1.2.crx?raw=true
[GPLv3]:https://www.gnu.org/licenses/gpl-3.0.en.html
[oma.abitti.fi]:https://oma.abitti.fi
