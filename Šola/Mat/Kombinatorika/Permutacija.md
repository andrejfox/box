#Permutacija je vsaka razporeditev $n$ elementov v kakršno koli vrsto.

**Permutacije brez ponavljanja**
$n$ elementov v vrsto
$P_n = n(n - 1)\dots 1 = n!$
$n!$ -> $n$ fakulteta / $n$ fakultativno
$n! = n * (n - 1)!$
$0! = 1$

$7! = 7 * 6 * 5 * 4 * 3 * 2 * 1$
$8! = 8 * 7!$

Permutacije so bijektivne preslikave množice z močjo $n$.
Bijektivnih preslikav v množici z $n$ elementi je $n!$.

**Permutacije s ponavljanjem**
$ABabc$ -> $5!$
$ABABC$ -> $\frac{5!}{2! * 2!}$
$r_1 + r_2 + \dots + r_k \leq n$
$P_n^{r_1, r_2, \dots, r_k} = \frac{n!}{r_1! * r_2! * \dots * r_k!}$

MALICA
$P_6^2 = \frac{6!}{2!} = 360$

<font color="#ff0000">M</font><font color="#f79646">A</font><font color="#9bbb59">T</font>E<font color="#ff0000">M</font><font color="#f79646">A</font><font color="#9bbb59">T</font>IK<font color="#f79646">A</font>
$P_{10}^{2,2,3} = \frac{10!}{2! * 2! * 3!} = 151200$

V vrsto postavimo:
4 bele
2 modri
5 rumenih
$P_{11}^{2, 4, 5} = \frac{11!}{2! * 4! * 5!} = 6930$

1 2 3 3
$P_4^2 = \frac{4!}{2!} = 12$
$3! = 6$
