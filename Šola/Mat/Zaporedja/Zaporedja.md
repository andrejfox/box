 Zaporedje je preslikava iz množice naravnih števil v množico realnih števil.

**[[Lastnosti zaporedij]]**

[[Aritmetična Zaporedja AZ]]
[[Geometrijsko Zaporedje GZ]]

[[Limita zaporedja]]
 
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
$a_{n + 2} = a_n + a_{n + 1}$ <- Fibonaccijevo zaporedje


Graf zaporedja je množica urejenih parov (1, $a_1$), (2, $a_2$),...
![[zaporedja_graf.png]]

---
[[Šola/Mat/Zaporedja/Vaje|Vaje]]

$a_n = 3q^n$
$a_1 = 1$
$a_{10} = ?$
$a_1 = 3q^1$
$q=\frac{1}{3}$
$a_n = 3(\frac{1}{3})^2$
$a_n = (\frac{1}{3})^{n-1}$
$a_{10} = (\frac{1}{3})^9 = \frac{1}{19683}$
$\lim_{n \to \infty} a_n=0$
$a_n < 10^{-8}$
$( \frac{1}{3})^{n-1}<10^{-8}$
$\log_{\frac{1}{3}} 10^{-8} > n -1$
od 18 člena

$|(3x-1)| \leq 1$
$3x-1 < 1$
$-(3x-1) < 1$
$-3x + 1 < 1$
$-3x<0$
$x>0$
$3x<2$
$x<\frac{2}{3}$
$x=(0,\frac{2}{3})$

$1,2,3$
a) $3! = 6$
b) $3^3 = 9$
c) 6 mest, 1 1x, 2 3x-5x, 3 0x-3x
122222
132222
133222
$\frac{6!}{5!}+\frac{6!}{4!}+\frac{6!}{2!*3!} = 96$

---
![[Pasted image 20241017140329.png]]72.3
GZ: $a, b, c$
$a_1 = a$
$b = a * k$
$c = a * k^2$
$ax^2+2bx+c=0$
$ax^2+2akx+ak^2 = 0$
$D = 4a^2k^2x^2 - 4* a^2k^2x^2$
$D = 0$
^ ena realna rešitev 

72.4
$a_1, a_2, a_3, a_4$
GZ: $a_1, a_2, a_3$
AZ: $a_2, a_3, a_4$
$a_1 + a_4 = 14$
$a_2 + a_3 = 12$
GZ: $a_1, a_2, 12 - a_2$
AZ: $a_2, 12 - a_2, 14 - a_1$
$(\sqrt{2}-a_2)*2=a_2+14-a_1$
$24-2a_2=a_2+14-a_1$
$a_1=3a_2-10$
$a_2^2 =(3a_2-10)(12-a_2)$
$a_2^2 = 36a_2 - 3a_2^2-120+10a_2$
$4a_2^2-46a_2+120=6$
$2a_2^2-23a_2+60=0$
$a_2 = \frac{23 \pm 7}{4}$
$a_{2_1}=\frac{15}{2}$
$a_{2_2}=4$
