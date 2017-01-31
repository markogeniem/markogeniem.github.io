# Yleinen tietosuoja-asetus ja verkkosovellukset

## Yleiset tiedot

https://markogeniem.github.io/

Marko Lenkkeri

Software Architect

Geniem Oy

# Tietosuoja-asetus teknologian kannalta

## Yhteydet

* Yhteydet palvelinten välillä
* Yhteydet käyttäjien ja palvelinten välillä
* Yhteydet ulkoisten käyttäjien välillä

<div class="notes">
Mihin teknologisiin elementteihin asetus vaikuttaa
</div>

## Varastot

* Varmuuskopiot
* Välimuistit
* Tiedonsiirrot

<div class="notes">
Mihin teknologisiin elementteihin asetus vaikuttaa
</div>

## Oikeudet

* Käsittelijät 
* Estot

<div class="notes">
Murehdittava myös teknologiapuolella sovellus- ja järjestelmätason pääsyt
-Adminit
-Kannat
-Järjestelmät
</div>

## Dokumentit

* Valmiuksien osoittaminen
* Prosessien osoittaminen

<div class="notes">
Auditoinnin perusteet, dokumentointi, osoitusvelvollisuus
Esimerkki seuraavassa
</div>

## Auditointi

* Ketä teki?
* Mitä teki?
* Koska teki?
* Mille teki?

<div class="notes">
Esimerkki. Muista Läpinäkyvyys Villen jutuista. Kuukauden kuluessa tiedot toimenpiteistä. Todennettavissa.
</div>



# Järjestelmän suunnittelu käyttäjän oikeuksien kannalta

## Suostumus tietojen keräämiseen

* Poisvedettävissä
* Opt-in, ei opt-out

## Tietojen kerääminen

* Minimointi
* Osoitusvelvollisuus

## Omien tietojen siirto

* Koneluettavassa muodossa oleva data
* Saatavissa käyttäjän pyynnöstä
* Käyttäjää koskeva henkilötieto
* Käyttäjän syöttämä henkilötieto

<div class="notes">
Itselleen tai toiselle rekisterinpitäjälle/käsittelijälle
Koneluettava? JSON, XML, CSV - ihan sama.
Automaatio helpottaa
</div>

## Omien tietojen poisto

* Poistettava pyydettäessä
* Suurempi ongelma olemassaolevissa järjestelmissä

<div class="notes">
Poisto vanhassa voi rikkoa sisällön täysin. Relaatiokannat.
</div>

## Omien tietojen päivittäminen ja ajantasaisuus

* Ei vanhaa/viallista henkilötietoa
* Henkilötiedot päivitettävissä

<div class="notes">
Ulkoiset datalähteet, backupit, jne. Backupeista lisää myöhemmin.
</div>

## Rajoitukset ja suostumukset

* Suostumus tietojen keräämiseen
* Suostumus tietojen käsittelyyn
* Alaikäisiltä kerättävä data (13v-16v)
* Vanhempien suostumus

<div class="notes">
Esim oikeudellisen vaateen takia voidaan ohittaa käsittelyesto.
Miten todentaa vanhempien suostumus? 
2014 Facebook arvioitu n. 180k 16v ja alle
</div>

## Automaatio

* Profilointi
* Päätelmät

<div class="notes">
Kerrottava mitä tehty, Käyttäjä voi vastustaa
Ei saa perustua erityisiin henkilötietoryhmiin, esim etnisyys
</div>

# Pilvipalveluiden ja SaaS-palveluiden rooli

## Sijainti

* ETA-alueen ulkopuolinen data
* Hajautettu data

<div class="notes">
Jos ulkopuolelle: Komission hyväksyntä, Käyttäjän suostumus, asianmukaiset suojatoimet
</div>

## Varmuuskopiointikäytännöt

* Mitä säilytetään oikeasti, ja miten
* Turvalliset poistot

<div class="notes">
Näkyvät ja näkymättömät backupit, laitteiden poistot
</div>

## Tiedonsiirto

* Mitä kautta ja minne?
* Siirtovaatimukset

<div class="notes">
Tietoturva siirrossakin
Vastuu päättyy jos käyttäjä pyytänyt siirron, ei jos osa järjestelmää
</div>

## Jäämät

* Palasia datasta
* Täysin oma ongelmansa

<div class="notes">

</div>

# Datajäämien haasteet

## Välimuistit

* Datan palasia
* Poistot, näkymiset
* Suhteellinen vaiva

<div class="notes">

</div>

## Varmuuskopiot

* Varmuuskopioiden palauttaminen
* Vanhentuneet tiedot

<div class="notes">

</div>

# Tietoturva osa tietosuoja-asetusta

## Hyväksi havaitut menetelmät

* Tietojen säilöntä
* Tietojen muokkaus
* Tunnistautuminen

<div class="notes">

</div>

# Käyttäjän näkökulma

## Omat tiedot saatavilla

* Näen mitä kerätään
* Näen mitä on kerätty

<div class="notes">

</div>

## Tietoturvanäkemykset taatummat

* Pienempi vaikutus tietomurroilla
* Taatumpi tiedottaminen murroista

<div class="notes">

</div>

# The End
 
## Kysymyksiä?

## Yhteystiedot

marko.lenkkeri@geniem.com

@markogeniem

http://geniem.fi/

