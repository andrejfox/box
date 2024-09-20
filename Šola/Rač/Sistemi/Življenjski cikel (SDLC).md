ang.: SDLC – Software Development Life Circle

V teoriji naletimo na bolj ali manj podrobno razdelane faze v “življenju” nekega programa. Govorimo o **življenjskem ciklu programa**. Ena od možnih opredelitev življenjskega cikla programa:
1. **študija izvedljivosti**
2. **definicija in analiza**
▪ opredelitev osnovne ideje in ciljev, analiza problema
3. **načrtovanje**
▪ razbijanje problema na podprobleme, izbira najboljših algoritmov, planiranje vhodnih in izhodnih podatkov ter njihovega zgleda, uporaba raznih diagramskih tehnik, npr. diagramov poteka
▪ v tej fazi problem v bistvu že dokončno rešimo
4. **implementacija (programiranje)**
▪ pretvorba rešitve v izbrani programski jezik (kodiranje)
5. **preverjanje in testiranje**
▪ testiranje pravilnosti in učinkovitosti in po potrebi vračanje na zgodnejše faze
6. **vzdrževanje**
▪ odpravljanje neodkritih napak, posodabljanje
7. **(ukinitev)**
---
**Študija izvedljivosti predhodi** odločitvi o začetku projekta razvoja:
▪ kaj je obseg predlaganega projekta?
▪ ali je projekt tehnično izvedljiv?
▪ kakšne bodo koristi od projekta?
▪ kakšni so stroški, časovnica?

Študija izvedljivosti pelje k odločitvi: **gremo** ali **ne gremo** v izvedbo
projekta.

---
**Analiza in specifikacija zahtev**
**Zahteve** definirajo funkcionalnosti sistema iz vidika naročnika: **kaj**
**naročnik potrebuje in ne kaj je povedal, da potrebuje!**
Osnovni cilj je **opis problema**, ki ga je potrebno rešiti in definiranje
zahtev skladno s:
▪ **podanim problemom**,
▪ **okoljem**, katerem je sistem namenjen (npr. strojna oprema, programska oprema,
uporabniki, zakonodaja, ...).
Osnovni dokument te faze je **specifikacija zahtev**. Zahteve se lahko
določijo v samostojni študiji ali lahko nastanejo inkrementalno.

---
**Načrtovanje**
**Načrt** (ang. design) opisuje sistem iz vidika razvijalca:
▪ kako naj sistem dela tisto, kar bi moral?
**Načrt sistema:** vzpostavlja arhitekturo, ki ustreza zahtevam po
strojni in programski opremi.
**Načrt programa:** predstavlja programske funkcionalnosti v takšni
obliki, da se lahko pretvorijo v enega ali več izvršljivih programov.
Osnovni dokument je načrt sistema oz. **tehnična specifikacija**
**(načrt)**.

 ----
**Izgradnja**
To je faza pri kateri se **programirajo** moduli sistema.
Osnovni cilj je narediti **berljivo, zanesljivo, za nadgradnje** **enostavno ter dobro dokumentirano programsko kodo.**
Poudarek ni na učinkovitosti, čeprav je tudi ta pomemben vidik
programiranja.
Rezultat te faze je program, ki se **lahko izvaja** (in ne prevaja, kakor
menijo eni razvijalci :)

---
**Testiranje**
Testiranje pomeni **izvajanje programa z namenom iskanja**
**pomanjkljivosti** v programski opremi.
V novejših modelih razvoja se vse več prepleta s fazo izgradnje.
Načrtovanje testnih aktivnosti začne s fazo specifikacije zahtev.
Pravilo: **vsako pomanjkljivost je bolj poceni odpraviti, če je**
**najdemo čim bolj zgodaj v razvojnem ciklu.**

---
**Namestitev in vzdrževanje**
Po dobavi/namestitvi v produkcijsko okolje naročnika sledi faza
vzdrževanja.
Osnovni namen vzdrževanja je:
▪ odprava vseh pomanjkljivosti skritih napak (odkritih po dobavi).
▪ prilagajanje sistema spremenjenim zahtevam.
▪ izboljševanje sistema.
Cilj te faze je **zagotoviti nemoteno izvajanje** programske opreme pri
uporabniku.