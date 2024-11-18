$n(x)=f(g(x))$
$n(x)=f(\sqrt{x-1})$
$n(x) = \sqrt[4]{x-1}$
$s(x)=g(\sqrt{x})$
$s(x)=\sqrt{\sqrt{x}-1}$

$f(x)=2^x$
$g(x)=\log_2 (x+1)$
$h(x) = f(g(x))=f(\log_2 (x+1))=2^{\log_2 (x+1)} = x + 1$
$s(x)=g(f(x))=g(2^2)=\log_2(2^x+1)$

$f(x)=\frac{x-1}{x+1}$
$h(x)=f(x) \circ f(x) = \frac{\frac{x-1}{x+1}-1}{\frac{x-1}{x+1}+1}=\frac{\frac{x-1-x-1}{x+1}}{\frac{x-1+x+1}{x+1}}=\frac{-2}{2x}=-\frac{1}{x}$

$h(x)=(2x+1)^5$
$h(x) = f(g(x))$
$f(x)=x^5$
$g(x)=2x+1$

$h(x)=e^{\sin x}$
$f(x)=e^x$
$g(x)=\sin x$

$h(x)=\tan^3x$
$f(x)=x^3$
$g(x)=\tan x$
$f(g(x))=(\tan x)^3=\tan^3 x$

$f(x)=10^x$
$g(x)=\log_{10} x$
$f(g(x))=10^{\log_{10} x} = x$
$g(f(x))=\log_{10} 10^x=x$
