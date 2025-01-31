```
lav04 - blok 6/besedilne datoteke (1)

vaja 11
( draft, 16.1.2025 )

java in sql: ponovitev
osnovno delo z besedilnimi datotekami

Lokalni računalnik zagotavlja SQL storitve preko vrat 3306. Zbirka 'zbrka' storitve vsebuje podatkovno tabelo 'imenik' s
podatki o osebah. 

1. Za izvedbo naloge potrebujemo vzpostavljeno podatkovno zbirko z vsaj 200 podatki o osebah. Spišite javanski program/mehanizem,
   ki bo za potrebe vaje izvedel ustrezen 'fixture', to je, napolnil zbirko zapisov o osebah z N pseudo-realnimi zapis o osebah.

  : lahko je ločen program, ki: a) kreira zbirko, tabelo
                                b) napolni s testnimi podatki
   
2. Za potrebe pošiljanja potrebujemo naslove v formi
   
   Spoštovani/a
   Jožica Novak
   Vegova 4
   Ljubljana 1000
   SI

   Za izpis in izrez naslovov imamo na voljo papir širine 132 znakov (proporcionalna širina) in bi želeli, da se po trije 
   naslovi generirajo vzporedno, da je med njimi horizontalno en stolpec prazen in  da je vertikalno med njimi ena prazna vrstica.
   Vertikalno je na ta list mogoče izpisati 66 vrstic. Med posameznimi listi morajo biti v izpisu po 3 prazne vrstice.
   Formatirano se vsa zadeva zapiše v besedilno datoteko 20250123_izpisNaslovov.txt (če je bila datoteka kreirana na ta datum).
   Če je zapis imena in priimka predolg za predvideno polje, se krajša dolžina imena od konca proti prvi črki. Prva črka imena 
   vedno ostane. Če je zapis še predolg, se krajša priimek od zadnjega dela proti njegovemu začetku.

3. Spremenite zapis podatkov o osebah in mehanizem izpisa, da bo omogočal prijazen izpis Spoštovani v pravem spolu !
 
4. Pridobite vsebino novele Dromidska Podoba (miha remec,1999)
   recimo iz  http://www2.arnes.si/~sudareme/zf/podoba.html

   Spišite javanski program, ki bo prebral dano novelo in izvedel statistiko:
    a- število vrstic
    b- število znakov, število črk
    c- število besed
    č- število povedi
    d- število odstavkov

    e- število različnih besed
    f- pogostost pojavitve posamezne besede
    g- pogostost pojavitve posamezne črke

   Za zadnje tri predlagam zapis s strukturo, ki implementira množico npr. HashMap <beseda,število>

   Poročilo zapiše v poročilo porocilo.txt s formo:

   za
   Nadzorni Učitelj
   Vegova 4, Lj

   Poročilo
     o vsebini datoteke podoba.html z vsebino
     MIha Remec : Dromidska podoba

     a) št vrstic datoteke :
     b)  ..
     c)  ..
     ..

   poročilo izdelal:
   dne 23. 1. 2025
   OsebaIme OsebaPriimek 


 
------------------
 create database zbrka 
    default character set utf8mb4 
	collate utf8mb4_slovenian_ci;
	
use zbrka;

create table imenik(
 id int primary key auto_increment,
 ime varchar(40) not null,
 priimek varchar(50) not null,
 ulica varchar (25),
 hisnaStevilka varchar(4),
 postnaStevilka int,
 kraj varchar(25),
 drzavaIso3166_2 char(2));

insert into imenik values(1,'Jožica','Novak',
'Vegova',4,1000,'Ljubljana','SI');


-------------------------------------
rok za oddajo je 1 teden od objave tega besedila
```