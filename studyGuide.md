# Series and Sequences

## Proof of the Sum of a Geometric Sequence

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

# Derivatives

## Derivative of Inverse Function

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

# Integration Techniques

## Proof of Integration by Parts

$$
\begin{aligned} \frac{d}{dx}[uv]&=\frac{d}{dx}[u]v+u\frac{d}{dx}[v]\\
\int\frac{d}{dx}[uv]dx&=\int\frac{d}{dx}[u]vdx+\int u\frac{d}{dx}[v]dx\\

uv&=\int\frac{du}{dx}vdx+\int u\frac{dv}{dx}dx\\

uv&=\int vdu+\int udv\\ \int udv &= uv - \int vdu\\
\end{aligned}
$$

## Proof of Tabular Integration[^1]

$$
\begin{array}{c|c}
u & dv\\
u^{(1)} & v\\
u^{(2)} & v^{(-1)}\\ 
u^{(3)} & v^{(-2)}\\
\vdots & \vdots \\
u^{(n)} & v^{(-(n-1))}\\
0 & v^{(-n)} 
\end{array}
$$

$$
\begin{array}{lllll}
\int udv = uv - &\hspace{-1em}\underbrace {\int vu^{(1)}dx}\\
&\hspace{-1em}(u^{(1)}v^{(-1)} - &\hspace{-1em}\underbrace{\int v^{(-1)}u^{(2)}dx})\\
&&\hspace{-1em}(u^{(2)}v^{(-2)} - &\hspace{-2.1em}\underbrace{\int v^{(-2)}u^{(3)}dx})\\
&&& \hspace{.5em}{\vdots}\\
&&& \hspace{-2em}(u^{(n-1)}v^{(-(n-1))}+ (-1)^{(n-1)} & \hspace{-1em}\underbrace{\int v^{(-(n-1))}u^{(n)}dx})\\
&&&&\hspace{-1em}(u^{(n)}v^{(-n)} - \cancelto{0}{\int v^{(-n)}u^{(n+)}dx})
\end{array}
$$



# Application of Integrals

## Arc Length[^2]

For any continuous and differentiable function $f(x)$, we want to find its arc length from $x=a$ to $x=b$.

![This is a graph of an unknown function on the domain a<x<b that is completely in the 1st quadrant.  The domain is split into 9 equal subintervals and the corresponding points on the graph are labeled $P_{0}$, $P_{1}$, $P_{2}$, $P_{3}$, $P_{4}$, $P_{5}$, $P_{6}$, $P_{7}$, $P_{8}$ and $P_{9}$.  A line then connects each of these points approximating the graph of the curve in each subinterval.](../images/Arc Length Curve Demo.png)

Just like how we calculate the Riemann Sum, we can divide the arc/curve into many segments where $P_{i-1}$ to $P_{i}$ is a straight line approximating the arc. The arc length $L$ from $a$ to $b$ then becomes
$$
L \approx \sum_{i=1}^{n}|P_{i-1}P_{i}|
$$
where $|P_{i-1}P_{i}|$ represents the line segment connecting point $P_{i-1}$ to $P_{i}$

Again, like how we increase the number of rectangles when evaluating the Riemann Sum and get the exact area under the curve called *Integral*, we can increase the number of segments to get the accurate arc length.
$$
L = \lim_{n\to \infin}\sum_{i=1}^{n}|P_{i-1}P_{i}|
$$
To calculate each segment's length $|P_{i-1}P_{i}|$, we need to apply the Pythagorean's Theorem. Let's make all segments have the same horizontal length $Δx$ so the arc is evenly divided into $n$ numbers of segments. Then, the height of each segment $Δy$ is just $Δx \times \text{slope of segment}$, or $Δx \times \frac{Δy}{Δx}$. 

![Arc Length Segment Triangle Demo](../images/Arc Length Segment Triangle Demo.png)

So the segment length $|P_{i-1}P_{i}| = \sqrt{(Δx)^2 + (Δy)^2}$

Let's substitute this into our arc length equation above:
$$
\begin{aligned}
L &= \lim_{n\to \infin}\sum_{i=1}^{n}|P_{i-1}P_{i}|\\
&=\lim_{n\to \infin}\sum_{i=1}^{n}\sqrt{(Δx)^2 + (Δy)^2}\\
\because \space Δy &= y_{i} - y_{i-1}, Δx = x_{i} - x_{i-1}\\
\therefore L&=\lim_{n\to \infin}\sum_{i=1}^{n}\sqrt{(x_{i} - x_{i-1})^2 + (y_{i} - y_{i-1})^2}\\
\because f(x)\text{is } &\text{continuous and differentiable,}\\
\text{we can} &\text{ apply the Mean Value Theorem }\\
\therefore f'(x_i^*)&=\frac{y_{i} - y_{i-1}}{x_{i} - x_{i-1}} \space \text{($x_i^*$ means a point between}\\
&\text{ $x_{i}$ and $x_{i-1}$ that satisfy the mean value theorem)}\\
y_{i} - y_{i-1}&=f'(x_i^*)\times (x_{i} - x_{i-1})\\
\therefore L&=\lim_{n\to \infin}\sum_{i=1}^{n}\sqrt{(x_{i} - x_{i-1})^2 + (f'(x_i^*)\times (x_{i} - x_{i-1}))^2}\\
&=\lim_{n\to \infin}\sum_{i=1}^{n}(x_{i} - x_{i-1})\sqrt{1 + (f'(x_i^*))^2}\space (x_{i} > x_{i-1}, x_{i} - x_{i-1} > 0)\\
&=\lim_{n\to \infin}\sum_{i=1}^{n}(Δx)\sqrt{1 + (f'(x_i^*))^2}\space (x_{i} > x_{i-1}, x_{i} - x_{i-1} > 0)\\
\because \int_{{\,a}}^{{\,b}}{{g\left( x \right)\,dx}} &= \mathop {\lim }\limits_{n \to \infty } \sum\limits_{i = 1}^n (\Delta x){g\left({x_i^*} \right)} \text{ (definition of definite integral)}\\
\therefore L&=\int_{a}^{b}\sqrt{1 + (f'(x))^2}dx\\
&=\boxed{\int_{a}^{b}\sqrt{1 + \left(\frac{dy}{dx}\right)^2}dx}\\
\end{aligned}
$$

# Citations

[^1]: http://ramanujan.math.trinity.edu/rdaileda/teach/s18/m3357/parts.pdf
[^2]: http://tutorial.math.lamar.edu/Classes/CalcII/ArcLength.aspx