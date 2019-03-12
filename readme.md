# GnuPG (GPG)
GPG on OpenPGP-standardin vapaa, avoimen lähdekoodin toteutus. Se tuottaa isoja, turvallisia avaimia ja sillä on erittäin ystävällinen käyttöliittymä.<br />

# GnuPG on RFC4880:n (tunnetaan myös nimellä PGP) määrittelemä OpenPGP-standardin vapaa toteutus. GnuPG: n avulla voit salata ja allekirjoittaa tietosi ja viestisi; Siinä on monipuolinen avaintenhallintajärjestelmä sekä kaikkien julkisten avainten hakemistojen käyttömoduulit.

Käyttö<br />
________________________________________
Voit luoda avaimen ajamalla %gpg --gen-key , muista seurata ohjeita. <br />

    Valitse avaintyyppi, DSA and ElGamal (oletus) ovat yleensä sopivat.

    Valitse avaimen koko, minimi on 1024, 4096 on paras. (1024 on oletusarvo)

    Valitse avaimen viimeinen käyttöpäivämäärä. Tämä on täysin vapaaehtoista, mutta yhtään tärkeämmille järjestelmille tai käyttötarkoituksille, avaimen viimeinen käyttäpäivämäärä on hyvä asettaa.

    Valitse käyttäjänimi (Oma, keksitty, sukunimi, tms) ja sähköpostiosoitteesi, kommenttikenttä on vallinnainen.

    Kun kehotetaan valitsemaan salasana, tee siitä tarpeeksi pitkä, jotta se olisi turvallinen, mutta varmista, että muistat sen.

    Tiedot annettuasi, GPG luo sinulle avainparin, julkinen ja yksityinen. (Public key / Private key)

# HUOM: Kun käytät luotua avainparia, ole erittäin tarkkana ettet anna tai aseta kenellekkään yksityistä avaintasi, julkinen avain on se millä salataan liikenteesi ja yksityinen avain on se jolla puretaan salaus!
_________________________________________
Luo peruutusavain ajamalla %gpg --gen-revoke ja seuraa ohjeita. Tulosta luotu peruutusavain ja säilytä se jossain turvallisessa paikassa, mieluiten muistitikulla tai paperilla. <br />
_________________________________________

Tulosta/vie avain komennolla %gpg --armor --export "<oma nimi>". Kopioi tuloste ja vie se vaikka tekstitiedostoon jonka olet luonut. <br /> 
	
Muista tulostaa avain ASCII-panssaroinnilla, muutoin avain tulostuu binäärisenä, joka vaikeuttaa sen sisällyttämistä muihin ohjelmiin (esim. sähköposti). 
_________________________________________

Komennolla %gpg --list-keys voit tulostaa kaikki avaimet jotka kuuluvat avainrenkaaseesi. <br />

Jos haluat tulostaa vain tietyt tai pienen osan avainrenkaasi sisällöstä, voit antaa komennolle %gpg --list-keys ARVO tulostaaksesi vain avaimet joilla on ARVO parametri, joka voi olla vaikka henkilön etunimi tai sukunimi (parametrin kirjainkoolla ei väliä, eli N ja n tulostavat samat avaimet).
_________________________________________

Tiedoston allekirjoittamista varten aja %gpg --clearsign <tiedostonimi> Huomaa: %gpg --sign <tiedostonimi> tulostaa ulostulon binäärisenä. <br />

	Jos haluat tarkistaa allekirjoituksen, aja %gpg --verify <tiedostonimi> Allekirjoittajan julkinen avain tulee olla avainrenkaassasi jotta voit tarkistaa allekirjoituksen.

	Salataksesi tiedoston aja %gpg --encrypt <tiedostonimi>

	Allekirjoittaaksesi salauksen aja %gpg --sign --encrypt <tiedostonimi> Sinulta kysytään kenelle allekirjoitat salatun tiedoston.
	Purkaaksesi salauksen aja %gpg --decrypt <tiedostonimi> 
