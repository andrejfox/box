DML skupina zajema SQL stavke za manipulacijo s podatki.
-SELECT \<izbira>
-INSERT \<dodajanje nove vrstice>
-DELITE \<brisanje vrstice>
-UPDATE \<spreminjanje vrstice>
Sintaksa SELECT stavka je najbolj kompleksna

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
```