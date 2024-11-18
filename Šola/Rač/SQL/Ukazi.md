`CREATE TABLE <shema.> <NazivTabele>` - Nova tabela
`ALERT TABLE` - Modifikacije
`DROP TABLE` - Brisanje
`<ime> <type> <lastnost>`  - stolpec
```sql
CREATE TABLE Oseba (
	EMŠO varchar(13) PRIMARY KEY,
	priimek VARCHAR(10) NOT NULL,
	ime VARCHAR(10) NOT NULL,
	spol CHAR(1) DEFAULT "Ž",
	dat_rojstva DATE
);
#or
CREATE TABLE Oseba (
	EMŠO varchar(13),
	priimek VARCHAR(10) NOT NULL,
	ime VARCHAR(10) NOT NULL,
	spol CHAR(1) DEFAULT "ž",
	dat_rojstva DATE,
	PRIMARY KEY (EMŠO)
);
```