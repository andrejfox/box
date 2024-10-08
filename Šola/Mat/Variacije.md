$n$ elementov, $r$ jih postavimo v vrsto.

**Brez ponavljanja**
$r \leq n$ -> variacije reda $r$ iz $n$ elementov
$V_n^r = \underbrace{n * (n - 1) * \dots * (n - r + 1)}_{r \text{ faktorjev}} = \frac{n!}{(n - r)!}$
Variacije brez ponavlanja so injektivne preslikave iz množice z močjo $r$ v množico z močjo $n$.

$V_n^2 = 20$
$n * (n - 1) = 20$
$(n - 5) (n + 4) = 0$
$n = 5$

$V_{n + 1}^2 = n^2 - n + 12$
$(n + 1) * n = n^2 - n + 12$
$n^2 + n = n^2 - n + 12$
$2n = 12$
$n = 6$

**S ponavljanjem**
${}^{(p)}V_n^r = n^r$
$n$ element, $r$ jih postavimo v vrsto, elementi se lahko ponavljajo
Variacije s ponavljanjem so preslikave iz množice z $r$ elementi v množico z $n$ elementi.
$0, 1$
8 - mestno dvojiško število
$2^8 = 256$

$1, 3, 5, 7, 9$
$n = 5$
se ne ponavljajo:
$5 * 4 * 3 = 60$
$3 * 4 * 3 = 36$

se ponavljajo:
$5^3 = 125$
$3 * 5^2 = 75$

x>3000
x<6000
$0, 1, 2, 3, 4, 5, 6$
$2 * 7 * 7 * 7 - 1 = 685$

n = 15
5 fantov
10 deklet
$5^{15} = veliko$
$4^{15} = malo manj$
$3^{10} * 4^5 = 60466176$

${}^{(p)}V_n^3 = 5 * V_n^2 + 4$
$n^3 = 5 * n(n - 1) + 4$
$n^3 = 5n^2 - 5n + 4$
$n^3 - 5n^2 + 5n - 4 = 0$
$n = 4$

|     | 1   | -5  | 5   | -4  |
| --- | --- | --- | --- | --- |
| 4   |     | 4   | -4  | 4   |
|     | 1   | -1  | 1   | 0   |
| 2   |     | 2   | 2   |     |
|     | 1   | 1   | 3   |     |


