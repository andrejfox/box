Definicija odvoda:
Odvod funkcije $f$ v točki $x_1$ je enak limiti diferenčnega kličnika, ko gre h proti 0.
Če limita obstaja je funkcija odvedljiva.

[[Šola/Mat/Odvodi/Enačbe|Enačbe]]

[[Odvodi]]
[[Pravila za odvajanje funkcij]]
[[Odvodi kotnih funkcij]]
[[Odvod eksponentne in logaritemske funkcije]]
[[Odvod implicitno podane funkcije]]
[[Odvod sestavljene funkcije]]
[[Višji odvodi]]
[[Stacionarne točke]]
[[Kot med grafom funkcije f(x) in k. osema]]

naklonski kot premice:
$y=kx+n$
$k = \tan \phi$
$k=\frac{\Delta y}{\Delta x}$ - diferenčni količnik

diferenčni količnik:
$\frac{f(x_1 + h) - f(x_1)}{h}$

Odvod $f$ v točki $x_1$
$f'(x_1)=\lim_{h \to 0} \frac{f(x_1 + h) - f(x_1)}{h}$
![[Pasted image 20241125135018.png]]

Geometriski pomen odvoda:
Odvod funkcije $f$ v točki $x_1$ je enak smernemu koeficientu tangente na krivuljo $f(x)$ v točki $x_1$.

1. $f(x)=n$
$f'(x)=\lim_{h \to 0} \frac{f(x + h) - f(x)}{h} = \lim_{h \to 0} \frac{n - n}{h} = 0$
2. $f(x)=kx+n$
$f'(x)=\lim_{h \to 0} \frac{k(x+h)+n-kx-h}{h} = \lim_{h \to 0} \frac{kx + kh -kx}{h} = \lim_{h \to 0} \frac{kh}{h} = k$
3. $f(x) = x^2$
$f'(x) = \lim_{h \to 0} \frac{(x+ h)^2 - x^2}{h} =\lim_{h \to 0} \frac{x^2 + 2xh + h^2 - x^2}{h} = \lim_{h \to 0} \frac{h(2x+h)}{h} = 2x$
$x=0$, $k=0$
![[Pasted image 20241125140154.png]]

$x = 1$, $k=2$
$x = -1$, $k = -2$
![[Pasted image 20241125140432.png]]

$x = 2$, $k = 4$
![[Pasted image 20241125140615.png]]

$x = \frac{1}{2}$, $k = 1$
![[Pasted image 20241125140722.png]]

4. $f(x) = x^{-1} = \frac{1}{x}$
$f'(x)= \lim_{h \to 0} \frac{(x + h)^{-1} - x^{-1}}{h} = \lim_{h \to 0} \frac{\frac{1}{x+h} - \frac{1}{x}}{h} = \lim_{h \to 0} \frac{\frac{x}{x^2+xh} - \frac{x+h}{x^2 + xh}} {h} = \lim_{h \to 0} \frac{\frac{-h}{x^2 + xh}}{h} = \lim_{h \to 0} \frac{-h}{h(x(x+h))}= \frac{-1}{x^2}$
$(x^{-1})'=-x^2=-\frac{1}{x^2}$

$x = 1$, $k=-1$
![[Pasted image 20241125141642.png]]

$x= -1$, $k = -1$
![[Pasted image 20241125141811.png]]

$f(x)=ax^3$
$f'(x)=\lim_{h \to 0} \frac{f(x+h) - f(x)}{h} = \lim_{h \to 0} \frac{a(x+4)^2-ax^3}{h} = \lim_{h \to 0} \frac{a(x^3+h^3+3x^2h+3xh^2)}{h} = \lim_{h \to 0} \frac{a(h^3+3x^2+3xh^2)}{h} = \lim_{h \to 0} \frac{ah(h^2+3xh+3x^2)}{h} = 3x^2a$