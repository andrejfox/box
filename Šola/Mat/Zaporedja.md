 Zaporedje je preslikava iz množice naravnih števil v množico realnih števil.[[Aritmetična Zaporedja]]
 
**Neskončna zaporedja:**
 $f: \mathbb{N} \rightarrow \mathbb{R}$
 $f: n \mapsto f_{(n)}=a_n$
$a_1, a_2, a_3, a_4, \dots,\underbrace{a_n}_{\text{Splošni člen zaporedja}}, \dots$

**Omejena zaporedja:**
 $f: \mathbb{N}_n \rightarrow \mathbb{R}$
  $a_1, a_2, a_3,..., a_n$

**Prikazi zaporedja:**
1. Splošni prikaz:
$a_n = \frac{1}{n}$
2. Nekaj začetnih členov:
$a_1, a_2, a_3,\dots$
3. Rekurzivno zaporedje:
$a_1 = 1$, $a_2 = 1$
$a_{n + 2} = a_n + a_{n + 1}$


Graf zaporedja je množica urejenih parov (1, $a_1$), (2, $a_2$),...
![[zaporedja_graf.png]]

**Lastnosti**
Naraščajoče:$\qquad \qquad \quad \; a_{n + 1} \geq a_n \quad n \in \mathbb{N}$
Strogo naraščajoče:$\qquad a_{n + 1} > a_n \quad n \in \mathbb{N}$
Padajoče:$\qquad \qquad \qquad \;\;\: a_{n + 1} \leq a_n \quad n \in \mathbb{N}$
Strogo padajoče:$\qquad \quad \:\: a_{n + 1} < a_n \quad n \in \mathbb{N}$

**Omejenost**
Zaporedje je omejeno, če je omejeno navzgor in navzdol.
- Navzgor omejeno \[ $a_n \leq M \quad n \in \mathbb{N}$ ]
$M$ - Zgornja meja, neskončno jih je. (Natančna zgornja meja)
- Navzdol omejeno \[ $a_n \geq m \quad n \in \mathbb{N}$ ]
$m$ - Spodnja meja, neskončno jih je. (Natančna spodnja meja)

**Posebna Zaporedja**
- Alternirajoče zaporedje
$a_n = (-2)^n$
$-2, 4, -8, 16, -32,\dots$
$-, +, -, +, -,\dots$