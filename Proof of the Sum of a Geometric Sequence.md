# Proof of the Sum of a Geometric Sequence

A geometric series looks like $\sum_{k=0}^{n-1}r^k​$

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
 Adding a constant $$a$$ to the geometric series yields:

$$
\sum_{k=0}^{n-1}ar^k = a\frac{1-r^n}{1-r}
$$
For a infinite power series in the form of $\sum_{n=0}^{\infin}ax^n​$,
$$
\sum_{n=0}^{\infin}ax^n = \lim_{n\to\infin}a\frac{1-x^n}{1-x}
$$
If $|x| < 1$, then
$$
\sum_{n=0}^{\infin}ax^n = a\frac{1-\lim_{n\to\infin}x^n}{1-x} = a\frac{1}{1-x} = \frac{a}{1-x}
$$






