# Sucesiones

## *definición*:

$$\displaystyle \lim_{n\to\infin} a_n = L
\qquad\text{o}\qquad
a_n \to L$$

Si podemos hacer que los terminos $a_n$ se aproximen a $L$ tanto como se quiera tomando $n$ lo suficientemente grande. si $\lim_{n\to\infin} a_n$ existe, se dice que la sucesión es *convergente*. De lo contrario, se dice que la sucesión es *divergente*.

## *definición*:
Una sucesión $\{a_n\}$ tiene el límite $L$ y lo expresamos como

$$ \displaystyle\lim_{n\to\infin}
\qquad\text{o bien}\qquad
a_n\to L\text{ cuando } n\to\infin$$

Si para todo $\varepsilon>0$ hay un correspondiente entero $N$ tal que

$$\text{Si}\quad
n>N\qquad\text{entonces}\qquad
|a_n-L|<\varepsilon$$

No importa qué tan pequeño se elija un intervalo ($L-\varepsilon,L+\varepsilon$), existe una $N$ tal que todos los términos de la sucesión desde $a_{N+1}$ en adelante deben estar en ese intervalo.

## *teorema*:

$$\text{Si}
\lim f(x)_{n\to\infin}=L\quad\text{y}\quad
f(n)=a_n\quad\text{cuando }n\text{ es un entero, entonces}\quad
\lim_{n\to\infin} a_n=L
$$

$$\lim_{n\to\infin}
\left( \dfrac{1}{n^r} \right) = 0
\quad\text{si}\quad r>0$$

Si $a_n$ es muy grande cuando $n$ es muy grande, usamos la notación $\lim_{n\to\infin}a_n=\infin$

## *definición*:

$\lim f(x)_{n\to\infin}=L\text{ y }f(n)$ significa que para todo número positivo $M$ existe un entero $N$ tal que

$$\text{Si}\quad n>N\quad\text{entonces}\quad a_n>M$$

Si $\lim_{a\to\infin}a_n=\infin$, entonces la sucesion $\{a_n\}$ es divergente, pero de una manera especial. Se dice que $\{a_n\}$ diverge a $\infin$.

Si $\{a_n\}$ y $\{b_n\}$ son sucesiones convergentes y $c$ es una constante, entonces

$\displaystyle\lim_{n\to\infin}(a_n)\pm(b_n)=\displaystyle\lim_{n\to\infin}(a_n)\pm\displaystyle\lim_{n\to\infin}(b_n)$

$\displaystyle\lim_{n\to\infin}(ca_n)=c\displaystyle\lim_{n\to\infin}(a_n)\qquad\displaystyle\lim_{n\to\infin}c=c$

$\displaystyle\lim_{n\to\infin}(a_nb_n)=\displaystyle\lim_{n\to\infin}a_n*\displaystyle\lim_{n\to\infin}b_n$

$\displaystyle\lim_{n\to\infin}\frac{a_n}{b_n}=\frac{\displaystyle\lim_{n\to\infin}(a_n)}{\displaystyle\lim_{n\to\infin}(b_n)}\quad\text{si}\quad\displaystyle\lim_{n\to\infin}(b_n)\not ={0}$

$\displaystyle\lim_{n\to\infin}(a_n^p)=[\displaystyle\lim_{n\to\infin}(a_n)]^p\quad\text{si}\quad p>0,a_n>0$

El teorema de la compresión se puede adaptar a las suseciones como sigue

$$\text{Si }a_n\leq b_n\leq c_n\text{ para }n\geq n_0\text{ y }\displaystyle\lim_{n\to\infin}a_n=\displaystyle\lim_{n\to\infin}c_n=L,\text{ entonces }\displaystyle\lim_{n\to\infin}b_n=L$$

## *teorema*:

$$\text{Si }\displaystyle\lim_{n\to\infin}|a_n|=0,\text{ entonces }\displaystyle\lim_{n\to\infin}a_n=0$$

Es una aplicación directa del teoremade compresión ya que $|a_n|\leq$