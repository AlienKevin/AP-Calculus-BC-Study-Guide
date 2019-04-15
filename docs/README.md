# Proof of the Sum of a Geometric Sequence

A geometric series looks like $\sum_{k=0}^{n-1}r^k$

The partial sum of a geometric series:
$$
\begin{aligned}
S_{n-1} &= r^0 + r^1 + r^2 + ... + r^{n-1}\\
rS_{n-1} &= r^1 + r^2 + r^3 + ... + r^n\\
rS_{n-1} - S_{n-1} &= r^n - r^0\\
(r-1)S_{n-1} &= r^n - 1\\
S_{n-1} &= \frac{r^n - 1}{r-1}\\
\sum_{k=0}^{n-1}r^k &= \frac{r^n - 1}{r-1} = \frac{1-r^n}{1-r}
\end{aligned}
$$
 Adding a constant $a$ to the geometric series yields:
$$
\sum_{k=0}^{n-1}ar^k = a\frac{1-r^n}{1-r}
$$
For a infinite power series in the form of $\sum_{n=0}^{\infin}ax^n$,
$$
\sum_{n=0}^{\infin}ax^n = \lim_{n\to\infin}a\frac{1-x^n}{1-x}
$$
If $|x| < 1$, then
$$
\sum_{n=0}^{\infin}ax^n = a\frac{1-\lim_{n\to\infin}x^n}{1-x} = a\frac{1}{1-x} = \frac{a}{1-x}
$$


# Derivative of Inverse Function

Let function $f(x)$'s inverse function be $g(x)$. Because $f(x)$ and $g(x)$ are inverse of each other, we know that $f(g(x)) = x$ and $g(f(x)) = x$. Suppose we know the derivative of $f(x)$ ($f'(x)$) but want to know the derivative of $g(x)$ ($g'(x)$), how can we do it? We can take advantage of the fact that $f(x)$ and $g(x)$ undo each other when combined to derive a formula that relates $f'(x)$ and $g'(x)$.
$$
\begin{aligned}
\frac{d}{dx}[g(f(x))] &= g'(f(x)) \cdot f'(x) &\text{Chain Rule}\\
\frac{d}{dx}[x] &= g'(f(x)) \cdot f'(x)\\
1 &= g'(f(x)) \cdot f'(x)\\
\frac{1}{f'(x)} &= g'(f(x))\\
g'(f(x)) &= \frac{1}{f'(x)}\\
let\space x &= g(x)\\
g'(f(g(x))) &=\frac{1}{f'(g(x))}\\
g'(x) &= \frac{1}{f'(g(x))}&f(g(x))=x
\end{aligned}
$$

<div>This website's icon is made by <a href="https://www.freepik.com/" title="Freepik">Freepik</a> from <a
      href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a> and is licensed by <a
      href="http://creativecommons.org/licenses/by/3.0/" title="Creative Commons BY 3.0" target="_blank">CC 3.0 BY</a>
  </div>