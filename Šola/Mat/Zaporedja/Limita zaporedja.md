Število $a$ je **limita zaporedja** $a_n$, če je v vsaki poljubno majhni okolici te točke neskončno mnogo členov zaporedja, izven okolice pa kvečjemu končno mnogo členov.

Limito zaporedja $a_n$ označimo: $\lim_{n \to \infty} a_n = 1$

Členi zaporedja $a_n$, ki ležijo v $\varepsilon$-okolici točke $a$, ustrezajo pogoju $|a_n - a| < \varepsilon$, členi izven te okolice pa pogoju $|a_n - a| \geq \varepsilon$, kjer je $\varepsilon > 0$.

**Konvergentno zaporedje** - zaporedje z limito
**Divergentno zaporedje** - nima limite

$\varepsilon$ - okolica števila $a$ je interval $(a - \varepsilon, a + \varepsilon) = O_\varepsilon(a)$
$x \in O_\varepsilon(a)$
$|a - x| < \varepsilon$

Pravila za računanje limit
$$\lim_{n \to \infty} c = c$$
$$\lim_{n \to \infty} \frac{1}{n} = 0$$
$$\lim_{n \to \infty} (a_n \pm b_n) =  \lim_{n \to \infty} a_n \pm \lim_{n \to \infty} b_n$$
$$\lim_{n \to \infty} (a_n * b_n) =  \lim_{n \to \infty} a_n *  \lim_{n \to \infty} b_n$$
$$\lim_{n \to \infty} \frac{a_n}{b_n} =  \frac{\lim_{n \to \infty} a_n}{\lim_{n \to \infty} b_n} \text{, } \quad \lim_{n \to \infty} b_n \neq 0$$
---
**Stikališče**
Število $s$ je **stikališče** zaporedja, če je v vsaki poljubno majhni okolici te točke neskončno mnogo členov zaporedja.

$a_n = \frac{n - 2}{n}$
$-1, 0, \frac{1}{3}, \frac{1}{2}, \frac{3}{5}, \dots$
$n = -1$
$M = 1$
$O_{0.5}(1)$
$O_{0.1}(1)${}
Izven so štirje členi:
$|1 - a_n| < \frac{1}{10}$
$1 - \frac{n - 2}{n} < \frac{1}{10}$
$-\frac{n - 2}{n} < -\frac{9}{10}$

$\lim_{n \to \infty} (\sqrt{n+1}-\sqrt{n-1}) =$
$=\lim_{n \to \infty} \frac{n+1-n+1}{\sqrt{n+1}\sqrt{n-1}}=$
$= \lim_{n \to \infty}\frac{2}{n\sqrt{\frac{1}{n}+\frac{1}{2n}}}+n\sqrt{1+\frac{1}{n}} = 0$

$\frac{3}{2}-\frac{9}{8}+\frac{27}{32}-\dots=\frac{a_1}{1-k}=\frac{\frac{3}{2}}{1+\frac{3}{4}}=\frac{\frac{3}{2}}{\frac{7}{4}}=\frac{12}{14}=\frac{6}{7}$
$k = -\frac{3}{4}$