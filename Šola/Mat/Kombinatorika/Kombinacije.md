Permutacije: vsi elementi v vrsto
Variacijo: nekateri elementi v vrsto

[[Lastnosti binomskih simbolov]]

Kombinacije: Imamo $n$ elementov, od tega izberemo $r$ elementov in jih ne razporedimo.
Vrstni red ni pomemben!

$$C_n^r = \frac{V_n^r}{r!} = \frac{n}{(n - r)! * r!)} = \frac{n * (n - 1) * \dots * (n - r + 1)}{r * (r - 1) * \dots * 1}$$

Kombinacije reda $r$ iz $n$ elementov
Binomski simbol:
$$C_n^r = \binom{n}{r}$$ 
Število kombinacij reda $r$ iz $n$ elementov je enako številu podmnožic z $r$ elementi v množici z $n$ elementi.

---
V ravnini so dane točke $a, b, c, d, e, f$ od katerih nobena trojica ne leži na isti premici.
Koliko različnih premic določajo te točke?
$\binom{6}{2} = 15$
Koliko različnih trikotnikov določajo te točke?
$\binom{6}{3} = \frac{6 * 5 * 4}{6} = 20$
Koliko med temi trikotnikih je takih, ki imajo oglišče a?
$\binom{5}{2} = 10$
Koliko je med trikotnikih takih ki imajo stranico $(ab)$?
$\binom{4}{1} = 4$

V seriji 100 izdelkov je 8 pokvarjenih, iz serije sočasno izberemo 5 izdelkov.
Koliko je med vsemi vzorci takšnih, da so v vzorcu sami pokvarjeni izdelki?
$\binom{8}{5} = 56$
Koliko je vzorcev v katerih so sami nepokvarjeni izdelki?
$\binom{92}{5} = 49177128$
Koliko je vzorcev v katerih je natanko en pokvarjen izdelek?
$8 * \binom{92}{4} = 22353240$
Dva pokvarjena + trije dobri?
$\binom{8}{2} * \binom{92}{3} = 3516240$

$\Omega / 99 / c)$
$C_{n + 1}^3 = 3C_n^3 - n$
$\frac{(n+1)*n(n-1)}{3!} = 3 * \frac{n(n - 1)}{2} - n$
$(n + 1)(n-1)n = 9n(n-1)-6n$
$(n + 1)(n - 1) = 9(n -1)-6$
$n^2 - 9n+14 = 0$
$(n-7)(n-2) = 0$
$n_1 = 7$
$n_2 = 2$

$C_{n + 1}^3 = \frac{5}{3}*C_n^5$
$\frac{(n+1)*n*(n-1))}{3!} = \frac{5}{3}\frac{n(n-1)(n-2)(n-3)(n-4)}{5!}$
$n+1 = \frac{(n-2)(n-3)(n-4)}{12}$
$12n + 12 = (n^2 - 5n+6)(n-4)$
$12n + 12 = n^3 - 4n^2-5n^2+20n+6n-24$
$n^3-9n^2+14n-36 = 0$

Množica 80 el.
Koliko podmnožic z 78 el.?
$\binom{80}{78} = \binom{80}{2} = \frac{80 * 79}{2} = 3160$

$\Omega/111$
5 - svetlolask
6 - črnolask
4 - rjavolask
kombinacije = 5
a) ni dodatnih pogojev
$\binom{15}{5} = 3003$
b) vsaj ena črnolaska
$\binom{15}{5} - \binom{9}{5} = 3003 - 126 = 2877$
c) morata v drugi krog priti natanko 2 svetlolaski
$\binom{5}{2} + \binom{10}{3} = 1200$
d) v drugem krogu ne smejo biti same svetlolaske
$3003 - \binom{5}{5} = 3002$
e) bosta v drugem krogu največ dve, ki nista črnolasi
$\binom{6}{5} + \binom{6}{4} * \binom{9}{1} + \binom{6}{3} * \binom{9}{2} = 861$

Izmed 5 kandidatov iz 1., 6 iz 2., 8 iz 3. ter 6 iz 4. razreda bi radi sestavili 6 člansko delegacijo.
Koloko je možnih kombinacij če ni drugih omejitev
$\binom{6}{25} = \binom{25}{6} = 177100$
b) Če morata biti v delegaciji iz 2 * 3., 4. in 1 * 1., 2.
$\binom{2}{6} * \binom{2}{8} * \binom{6}{1} * \binom{5}{1} = 12600$
c) je lahko iz 1. letnika v delegaciji največ 1 dijak
$\binom{6}{20} + \binom{5}{20} * \binom{1}{5} = 116280$
d) je iz vsakega letnika vsaj eden in 4. pa vsaj 2
$\binom{2}{6}(\binom{2}{5} * \binom{1}{6} * \binom{1}{8} + \binom{1}{5} * \binom{2}{6} * \binom{1}{8} + \binom{1}{5} * \binom{1}{6} * \binom{2}{8}) = \binom{2}{6} * 1290 = 28800$

5 - čevljev
4 - hlače
3 - srajce
6 - kravat
a) Na koliko načinov se lahko obleče?
$5 * 4 * 3 * 6 = 360$
b) ni omejitev
$6! = 720$
d) pari sedijo skupaj
$3! * 2 * 2 * 2= 48$
e) ženske skupaj na skrajni levi
$3! * 3! = 36$
f) Bojan in Aloj ne smeta biti skupaj
$6! - 2! * 5! = 720 - 240 = 480$
g) dva gresta
$\binom{6}{4} = 360$
h) 3 čaji, 2 vodi, 4 piva, 5 sokov (Alojz pivo, Alojzi sok, Bojan voda, Branka čaj) (vsak samo 1)
$4*5*2*3 = 120$
i) pin: 4 mesta, x > 8000, x%5 = 0 (konča se z 0), samo sode števke
$0, 2, 4, 6, 8$
$8 \dots 0$
$1 * 5 * 5 * 1 - 1 = 24$
j) palindrom, 4 števke, lihe ($1, 3, 5, 7, 9$)
$5 * 5 * 1 = 25$

DN: $C_n^3 = \frac{5}{3}*C_n^5$ (n = 7)
