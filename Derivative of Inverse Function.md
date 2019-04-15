# Derivative of Inverse Function
Let function $f(x)$'s inverse function be $g(x)$. Because $f(x)$ and $g(x)$ are inverse of each other, we know that $f(g(x)) = x$ and $g(f(x)) = x$. Suppose we know the derivative of $f(x)$ ($f'(x))$ but want to know the derivative of $g(x)$ ($g'(x)$), how can we do it? We can take advantage of the fact that $f(x)$ and $g(x)$ undo each other when combined to derive a formula that relates $f'(x)$ and $g'(x)$.
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
