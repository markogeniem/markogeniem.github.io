title: Opettajien koodikoulu

author:
	name: Marko Lenkkeri
	url: http://www.geniem.com/
	twitter: markogeniem
	email: marko@geniem.com
output: index.html
theme: select/cleaver-select-theme

--

# Opettajien koodikoulu #2
## Ohjelmoinnin ja koodikoulun perusteita
## http://markogeniem.github.io/jatkokoulu/

--

### Tärkeimmät 2 asiaa ensin

- Kesto 4h
- Kahvitauko klo 14

--

### Geniem

http://www.geniem.com/

* Verkkosivuja
* Palveluja
* Konsultointia
* Verkkosovelluksia
* Mobiilisovelluksia

--

### Kurssi

Kaksi lähiopetuspäivää:
- [Perusteet](http://markogeniem.github.io/koulu/)
- [Kehittyneemmät tekniikat](http://markogeniem.github.io/jatkokoulu/)

Käytännön harjoittelu:
- Oppilaille
- Kurssia käymättömälle kollegalle

--

### Kurssi

Oma koodikoulun ohjauskokeilu ja sen raportointi = verkkotyöskentelyjakso:
- ReadIT-järjestelmä

--

### Tänään

Päämäärät:
- jatketaan Turtle Royn kanssa
- kerrataan
- pohditaan ohjelmoinnin opettamista
 - käydään läpi koodikoulun järjestäminen
- kirjaudutaan ReadIT-järjestelmään

--

### Turtle Roy

Kerrataan perusteet: http://www.koodikirja.fi/luku1/
Turtle Roy: http://turtle-roy.herokuapp.com

--

### Turtle Roy

Peruskomennot
- piirtäminen
- värit ja teksti
- tallentaminen ja lataaminen
- äänet

--

### Turtle Roy

Piirtäminen
- ```fd 50```
- ```rt 90```
- ```lt 45```
- ```clear```
- ```home```

--

### Turtle Roy

Piirtäminen
- ```penup```
- ```pendown```

--

### Turtle Roy

Värit ja teksti
- ```color "red"```
- ```bg "green"```
- ```text "Moikka maailma!"```
- ```font 10```

--

### Turtle Roy

Tallentaminen ja lataaminen
- ```login "nimi"```
- ```save "nimi"```
- ```open "nimi"```
- ```ls```

--

### Turtle Roy

Äänet
- ```say "Hello world"```
- ```play c 500```
- Mieti tarkkaan
- Muista testata toimiiko selaimella

--

### Turtle Roy

Näppäimistötaikoja
- hakasulult ```alt gr``` -näppäimellä ja 8- tai 9-näppäimillä.
- macilla hakasulut oikeanpuoleinen ```alt``` ja 8 tai 9
- aaltosulut ```alt gr``` -näppäimellä ja 7- tai 0-näppäimillä
- macilla aaltosulut ```shift```, ```alt``` ja 8 tai 9.

--

### Turtle Roy

Sekvenssit
- peräkkäin suoritettavia käskyjä
- ```s [clear, fd 90, rt 90, fd 90, rt 90, fd 90, rt 90, fd 90, rt 90] ```

--

### Turtle Roy

Toistot
- käsky, jota toistetaan määrätty määrä
- ```r 4 (fd 50)```


--

### Turtle Roy

Funktiot (nimettyjä käskyjä)
- ```let nelio = r 4 (s [fd 50, rt 90])```
- ```nelio```

Vaihtoehtoisesti myös
- ```let kulma = s [fd 50, rt 90]```
- ```let nelio = r 4 kulma```
- ```nelio```

--

### Turtle Roy

https://github.com/raimohanska/turtle-roy laajempaa käskylistausta ja alkuperäinen lähdekoodi.

--

### Miten ohjelmointia opetetaan?

Lähde ja hyvää lukemistoa: http://koodi2016.fi/opetus.html

--

### Miten ohjelmointia opetetaan?

Koodauksen opetus on ajattelun opettamista! (ohjelmoinnillinen ajattelu)
- ongelman purkaminen osiin (lego-harjoituksesta tuttua)
- kaavojen ja toistuvien sääntöjen tunnistaminen (syy-seuraussuhteet)
- algoritmien luominen (= kuvaus jonkin tehtävän suorittamiseksi tarvittavista toimenpiteistä)
- ratkaisun yleistäminen ja automatisointi

--

### Miten ohjelmointia opetetaan?

Ohjelmointia oppii tekemällä!
- 1-2 luokilla leikkien avulla (oppilaat ohjelmoi opettajaa/toisiaan...)
- 3-6 luokilla visuaaliset ohjelmointiympäristöt/piirtäminen Turtle Roylla/
koodauspelit/applikaatiot
- 7-9 luokilla ohjelmointikielet

--

### Miten ohjelmointia opetetaan?

![Taidot esimerkin kautta](img/taidot-esimerkki.png)

--

### Miten ohjelmointia opetetaan?

![Algoritminen ajattelu](img/algoritminen-ajattelu.png)

<small>*https://github.com/raimohanska/opettajien-koodikoulu/</small>

--

### Koodikoulun rakenne ja järjestäminen

Miten järjestää koodikoulutunti oman oppilasryhmän kanssa? 
http://koodikoulu.github.io/koodikoulu/

- etukäteisvalmistelu
- alkusanat
- intro
- lämmittelyleikki
- Turtle Roy: perusasiat + koodaus
- tunnin päätös (+ halutessa todistukset)

--

### Koodikoulun rakenne ja järjestäminen

Tarkastuslista 

- laitteet (tabletit sopivat huonosti)
- verkkopääsy
- tunnukset
- äänet
- koko sovelluksen toiminta
- tehtävät, ratkaisut, tyypilliset ongelmat

--

### Haasteet

Mitä ongelmia ohjelmoinnin opettamisessa voi tulla eteen?
Miten haasteet ratkaistaan?
Mistä löytyy tuki opettajalle? (opetus, softa, rauta)

--

### Lasten huomiointi

Ylimääräistä kivaa:
- [Tehtävä- ja diplomimateriaaleja koodikerhosta](https://drive.google.com/drive/u/0/folders/0B1C8IjvRApfgeXIzZUx5UXBSMlk)
- [Koodikoulun diplomit](http://koodikoulu.github.io/koodikoulu/)
- muuta?

--

### juniorKoodari

Materiaali 9 - 12 -vuotiaille alakoululaisille

http://rosa.utu.fi/juniorkoodari/etusivu/materiaalit/

Hyödyntää Turtle Royta, kuten Koodikirja.

--

### juniorKoodari

[Tehtävä #1](http://rosa.utu.fi/juniorkoodari/etusivu/materiaalit/#t1)
- valmis pohja
- kuljeta Roy alusta loppuun
- sekvenssit, toistot
- huomaa kommentit

--

### juniorKoodari

[Tehtävä #2](http://rosa.utu.fi/juniorkoodari/etusivu/materiaalit/#t2)
- piirrä annettu kuvio
- sekvenssit, toistot, funktiot
- hyvä ratkaisu piilotettuna
- oppilaille ratkaisua ei kannata suorilta näyttää

--

### juniorKoodari

[Tehtävä #3](http://rosa.utu.fi/juniorkoodari/etusivu/materiaalit/#t3)
- piirrä annettu kuvio
- sekvenssit, toistot, funktiot, ehtolauseet
- uuden opettelua

--

### juniorKoodari

[Tehtävä #4](http://rosa.utu.fi/juniorkoodari/etusivu/materiaalit/#t4)
- piirrä annettu kuvio
- sekvenssit, toistot, funktiot
- enemmän tekemistä, tosi vaikea ilman funktioita

--

### juniorKoodari

[Tehtävä #5](http://rosa.utu.fi/juniorkoodari/etusivu/materiaalit/#t5)
- valmis pohja, visuaalisesti erottuva ja kiva tehtävä
- sekvenssit
- mahdollisuus ajella autolla, kts vastauksesta ohje kursorin muuttamiseen

--

### juniorKoodari

[Tehtävä #6](http://rosa.utu.fi/juniorkoodari/etusivu/materiaalit/#t6)
- piirrä annettu kuvio
- sekvenssit, toistot, funktiot, ehtolauseet
- erittäin vaikea ilman funktioita

--

### juniorKoodari

Pääpointit tehtävissä
- ymmärrä toistuvien osien hahmottaminen
- ymmärrä toistot, sekvenssit ja funktiot
- poista manuaalinen toisto

--

### Verkkotyöskentelyjakso

Verkkotyöskentelyjakso alkaa toisen lähiopetusiltapäivän jälkeen.
Ympäristönä ReadIT. Ideana pitää yksi tai useampi oppitunti oppilaille koodikoulun mukaisesti, ja dokumentoida se.

Tutorina toimii:

Heikki Hutri
hohutr@utu.fi

-- 

### Verkkotyöskentelyjakso

http://rosa.utu.fi/koodikoulut/

- luo tunnus
- kirjaudu sisään
- anna kurssisi kurssiavain "Turku_I" tai "Tampere_I" (ilman lainausmerkkejä)
- muut hankkeen koulutukset saat näkyviin "TTtiedonhaku" ja "TTtietoturva" -avaimilla
(voit tutustua näihin ja suorittaa nekin halutessasi, niistä saat 2 op tietotaidot -kurssitodistuksen, tarkemmat infot kurssista: http://rosa.utu.fi/kick/tietotaidot/)

--

### Kysymyksiä tästä materiaalista?

kalle@geniem.com

artturi@geniem.com

marko@geniem.com

-- 

### Loppu

Kysymyksiä?

Kommentteja?

Haasteita tai ideoita?

--

### Linkkejä

http://www.koodikoulu.fi/

http://www.koodi2016.fi/

http://www.koodikirja.fi/luku1/

http://rosa.utu.fi/juniorkoodari/


