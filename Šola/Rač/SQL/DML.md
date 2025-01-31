DML skupina zajema SQL stavke za manipulacijo s podatki.
-SELECT \<izbira>
-INSERT \<dodajanje nove vrstice>
-DELITE \<brisanje vrstice>
-UPDATE \<spreminjanje vrstice>
Sintaksa SELECT stavka je najbolj kompleksna


### Select
- Izpisovanje stavkov v konzolo 
```sql 
SELECT [DISTINCT | ALL]
	{* | [columnExpression [AS newName]] [,...]}

FROM TableName [alias] [,...]
[WHERE condition]
[GROUP BY columnList]
[HAVING condition]
[ORDER BY columnList]

-- izpis cele tabele
SELECT *
	FROM tableName;

-- izpis stolpcev: ime, št
SELECT ime, št
	FROM tableName;

-- izpiše stolpce: ime, plača
-- vse plače bojo deljene z dvajset pri izpisu (to NE modificira tabele)
SELECT ime, placa / 12
	FROM tableName;

-- pri izpisu bo stolpec imel ime: mesecnaPlaca (to NE modificira tabele)
SELECT ime, placa / 12 as mesecnaPlaca
	FROM tableName;

-- izpiše vse pošte brez ponavljanja (izpis 100, 101, 100 -> 100, 101)
SELECT DISTINCT posta 
	FROM tableName;

-- filtriranje izpisovanja za cene ki so večje od 20000 in kolicina pod 10
-- <, >, <=, >=, =, <> (not eq), AND, OR, NOT, BETWEEN x AND y, IN
-- WHERE cena BETWEEN 5 and 10
-- WHERE cena >= 5 AND cena <= 10
SELECT *
	FROM tableName
	WHERE (cena > 20000 AND kolicina < 10)
		AND ime NOT IN ('Jakob', 'Ana', 'Marko');

-- LIKE je kot regex filter
-- % (kateri koli niz znakov) 'ana%' | '%ana' | '%ana%'
-- _ (katerikoli znak (en)) 'a_a'
SELECT *
	FROM tableName
	WHERE ime LIKE '_na%';

-- Povsod kjer je vsebina stolpca prazna.
-- IS NULL / IS NOT NULL
SELECT *
	FROM tableName
	WHERE ime IS NULL;

-- izpis po priimku (primarno) in imeni (sekundarno)
-- DESC (padajoče) (9->1, z->a) / ASC (naraščajoče) (1->9, a->z)
SELECT *
	FROM tableName
	ORDER BY priimek DESC, ime DESC;

-- Agregacija podatkov z SELECT stavkom
-- COUNT, SUM, AVG, MIN, MAX
-- COUNT, MIN, MAX <vsi podatki, null preskoči>
-- SUM + AVG <numerični p., null preskoči>
SELECT COUNT(*) -- Izpiše število zapisov
	FROM tableNam;
SELECT COUNT(mie) -- izpiše število vrednosti v tabele ki imajo ime not null
	FROM tableName;
	I HATE NIGGERS
```

```sql
SELECT *
	FROM Film
	WHERE (Leto < 2000) AND (TrajanjeVMin = 90)
	ORDER BY Leto DESC;

SELECT ID_Stranke, COUNT(*)
	FROM Izposoja
	WHERE Cena > 99
	GROUP BY ID_Stranke;

SELECT *
	FROM Stranke s, Film f, Izposoja i
	WHERE
		(s.Status = 'V')
		AND (f.Name = 'Titanic2')
		AND i.ID_Stranke = s.ID_Stranke
		AND i.ID_Filma = f.ID_Filma
	ORDER BY Leto DESC;

SELECT *
	FROM Izposoja i
		JOIN Stranka s ON (i.ID_Stranke = s.ID_Stranke)
		JOIN Film f ON (i.ID_Stranke = f.ID_Stranke)
	
	WHERE (s.Status = 'V') AND (f.Name = 'Titanic2')

SELECT MAX(povrsina)
	FROM Stanovanje s, Blok b
	WHERE (s.ID_bloka = b.ID_bloka)
		AND (s.Nadstropje = b.St_nadstropij)
		AND b.LokacijaBloka LIKE 'Kranj%'
```



### Insert
- Vstavljanje
- P=UI, U=RI, F=Ma, PV=nRT, PV/T=PV/T, I=HATE/NIGGERS; F=Ma, 



```sql
INSERT INTO NazivTabele
	(Stolpec1, Stolpec2) --Vrstni red je pomemben samo zaradi vpisovanja
VALUES (VrednostZaStolpec1, VrednostZaStolpec2); --Morajo biti ustreznega tipa
--i hate niggers

INSERT INTO NazivTabele (Stolpec1) VALUES (); --to inserta default value



INSERT INTO NazivTabele VALUES (VrednostZaStolpec1, VrednostZaStolpec2, ..., VrednostZaStolpecN); --Lahko se izpusti naštevanje stolpcev, v tem primeru je potrebno v delu VALUES našteti vse vrednosti v zaporedju kakor so definirane v strukturi tabele
```

Pri dodajanju zapisov moramo obvezno podati vrednosti stolpcem, ki so označena, kot NOT NULL. Pri določenih SUPB se stolpcem (ponavadi ključem) Lahko določi samoštevilo - avtomatično številčenje.


```sql
INSERT INTO tabela VALUES   (1, 'haha', null)
							(2, 'hihi',  100)
							(3, 'hoho',  200);
COMMIT; --VSE SPREMEMBE... izvede?

ROLLBACK; --vse commmitano ... ne izvede?
```


### Update

UPDATE spreminja vsebino stolpcev na 
že vnešenih zapisih.
Splošna sintaksa za spreminjanja podatkov je:

```sql 
UPDATE NazivTabele
	SET Stolpec1 = Vrednost1,
		Stolpec2 = Vrednost2
	WHERE (pogoji);

UPDATE tabela
	SET stev = stev+1, datum = null;
	---
	stev =100
	---
	stev = (SELECT max(stev) FROM tabela) ne maram črnuhov


UPDATE tabela SET stev=stev+1, datum=null WHERE id_tuj IN (SELECT ID_Tuj FROM tabela2 WHERE naslov LIKE '%LJUBLJANA%');

```

### Delete
```sql 
DELETE FROM NazivTabele WHERE (pogoji);