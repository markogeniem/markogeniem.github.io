# Yleinen tietosuoja-asetus ja verkkosovellukset

## Yleiset tiedot

https://markogeniem.github.io/

Marko Lenkkeri

Software Architect

Geniem Oy

# Tietosuoja-asetus teknologian kannalta

## Yhteydet

* palvelinten välillä
* käyttäjien ja palvelinten välillä
* ulkoisten käyttäjien välillä

<div class="notes">
Mihin teknologisiin elementteihin asetus vaikuttaa?
</div>

## Varastot

* varmuuskopiot
* välimuistit
* tiedonsiirrot

<div class="notes">
Mihin teknologisiin elementteihin asetus vaikuttaa?
</div>

## Oikeudet

* käsittelijät 
* estot

<div class="notes">
Murehdittava myös teknologiapuolella sovellus- ja järjestelmätason pääsyt.

-adminit
-kannat
-järjestelmät
</div>

## Dokumentit

* valmiuksien osoittaminen
* prosessien osoittaminen

<div class="notes">
Auditoinnin perusteet, dokumentointi, osoitusvelvollisuus.
Esimerkki seuraavassa slidessä.
</div>

## Auditointi

* ketä teki?
* mitä teki?
* koska teki?
* mille teki?

<div class="notes">
Esimerkki. Muista Läpinäkyvyys Villen jutuista. Kuukauden kuluessa tiedot toimenpiteistä. Todennettavissa.
</div>



# Järjestelmän suunnittelu käyttäjän oikeuksien kannalta

## Suostumus tietojen keräämiseen

* poisvedettävissä
* opt-in, ei opt-out

## Tietojen kerääminen

* minimointi
* osoitusvelvollisuus

## Omien tietojen siirto

* tiedot tarjottava koneluettavassa muodossa
* saatavissa käyttäjän pyynnöstä
* käyttäjää koskeva henkilötieto
* käyttäjän syöttämä henkilötieto
* käyttäjään yhdistettävä tieto

<div class="notes">
Itselleen tai toiselle rekisterinpitäjälle/käsittelijälle.

Koneluettava? JSON, XML, CSV - ihan sama.

Automaatio helpottaa elämää.
</div>

## Omien tietojen poisto

* poistettava pyydettäessä
* suurempi ongelma olemassaolevissa järjestelmissä

<div class="notes">
Poisto vanhassa voi rikkoa sisällön täysin. 

Relaatiokannat.
</div>

## Omien tietojen päivittäminen ja ajantasaisuus

* ei vanhentunutta henkilötietoa
* henkilötiedot päivitettävissä

<div class="notes">
Ulkoiset datalähteet, backupit, jne. 

Backupeista lisää myöhemmin.
</div>

## Rajoitukset ja suostumukset

* suostumus tietojen keräämiseen
* suostumus tietojen käsittelyyn
* alaikäisiltä kerättävä data (13v-16v)
* vanhempien suostumus

<div class="notes">
Esim oikeudellisen vaateen takia voidaan ohittaa käsittelyesto.

Miten todentaa vanhempien suostumus? 

2014 Facebook käyttäjiä arvioitu n. 180k 16v ja alle.
</div>

## Automaatio

* profilointi
* päätelmät

<div class="notes">
Kerrottava mitä tehty, Käyttäjä voi vastustaa.

Ei saa perustua erityisiin henkilötietoryhmiin, esim etnisyys.
</div>

# Pilvipalveluiden ja SaaS-palveluiden rooli

## Pilvipalvelut {data-background-image="gdpr/img/awsarch.png" data-background-size=contain}

## Sijainti

* ETA-alueen ulkopuolinen data
* hajautettu data

<div class="notes">
Jos ulkopuolelle: Komission hyväksyntä, Käyttäjän suostumus, asianmukaiset suojatoimet.
</div>

## Varmuuskopiointikäytännöt

* mitä oikeasti säilytetään
* miten säilytetään
* turvalliset poistot

<div class="notes">
Näkyvät ja näkymättömät backupit, laitteiden poistot.
</div>

## Tiedonsiirto

* mitä kautta ja minne?
* siirtovaatimukset

<div class="notes">
Tietoturva siirrossakin.

Vastuu päättyy jos käyttäjä pyytänyt siirron, ei jos osa järjestelmää.
</div>

## Jäämät

* palasia datasta
* täysin oma ongelmansa

<div class="notes">
Enemmän seuraavaksi.
</div>

# Datajäämien haasteet

## Välimuistit

* datan palasia
* poistot
* näkymät
* suhteellinen vaiva

<div class="notes">
Välimuistit:

-Kooditaso
-Kääntötaso
-Palvelut
-Selaimet
-Kannat
</div>

## Varmuuskopiot

* varmuuskopioiden palauttaminen
* vanhentuneet tiedot

<div class="notes">
Vikatilanteet voivat aiheuttaa ongelmia. 
Palauttaminen voi ylikirjoittaa muuttuneita tietoja.
Erillinen säilyttäminen ja kahdennukset.
</div>

# Tietoturva osa tietosuoja-asetusta

## Hyväksi havaitut menetelmät

* tietojen säilöntä
* tietojen muokkaus
* tunnistautuminen

<div class="notes">
-Salaaminen
-Hashit
-Pääsyrajoitukset
-Vahva tunnistautuminen ja vahvistusmailit
</div>

# Käyttäjän näkökulma

## Omat tiedot saatavilla

* näen mitä kerätään
* näen mitä on kerätty
* näen mitä tiedoilla tehdään
* pystyn vaikuttamaan

<div class="notes">

</div>

## Tietoturvanäkemykset

* tietomurtojen vaikutusten minimointi
* murroista tiedottaminen

<div class="notes">
-Ei niin isoa uhkaa muiden palvelujen turvallisuudelle
-Saa oikeasti tietoa eikä sitä pimitetä
</div>

# The End
 
## Kysymyksiä?

## Yhteystiedot

marko.lenkkeri@geniem.com

@markogeniem

http://geniem.fi/

