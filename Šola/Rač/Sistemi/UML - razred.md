Razred vsebuje 3 razdelke
1. ime razreda
2. struktura (atributi)
3. obnašanje (operacije)

struktura:
(dostopnost) ime: tip (multiplikator) = (privzeta vrednost)

obnašanje:
(dostopnost) naziv (parametri) : vrednost

> [!NOTE] Dostopnost
> +public
> \#protected
> -private
> \\izpeljana vrednost


**Povezave** zagotavljajo komunikacijsko pot med različnimi objekti
Modelirane s črtami, pri čemer različne vrste črt predstavljajo različne vrste povezav:
- asociacija
	- agregacija
	- Kompozicija
- odvisnost
- generalizacija
- realizacija

**Agregacija** posebna oblika asociacije, ki modelira povezavo "celota-del" med agregatom 

**Kompozicija** je oblika agregacije z močnim lastništvom in enako življenjsko dobo kot celota. deli ne morejo živeti dlje kot celota / agregat.

| **Števnosti**                |         |
| ---------------------------- | ------- |
| nedoločena                   |         |
| natanko en                   | 1       |
| nič ali več (več, neskončno) | 0..*    |
|                              | *       |
| eden ali več                 | 1..*    |
| nič ali eden                 | 0..1    |
| določeno območje             | 2..4    |
| Več, različnih območji       | 2, 4..6 |
