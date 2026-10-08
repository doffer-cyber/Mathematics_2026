### Exercise 1. Dominant Terms in a Sequence

Compute

$$
\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7}.
$$

Explain why the highest-degree terms determine the result.

> **Why this exercise:** introduces the idea of a dominant term and teaches how to simplify the behavior of expressions for large arguments.

#### Solution

Both the numerator and the denominator are polynomials of degree $2$. Divide each of them by $n^2$, the highest power of $n$ that occurs:

$$
\frac{4n^2-3n+1}{2n^2+5n-7} = \frac{4-\dfrac{3}{n}+\dfrac{1}{n^2}}{2+\dfrac{5}{n}-\dfrac{7}{n^2}}.
$$

For $n\to\infty$ the following limits hold:

$$
\frac{3}{n}\to 0, \qquad \frac{1}{n^2}\to 0, \qquad \frac{5}{n}\to 0, \qquad \frac{7}{n^2}\to 0.
$$

The limit of the denominator is $2\neq 0$, so the quotient rule for limits applies:

$$
\begin{aligned}
\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7} &= \frac{4-0+0}{2+0-0} \\
&= 2.
\end{aligned}
$$

#### Why the highest-degree terms decide

For large $n$, the terms of lower degree are negligible compared with $n^2$, because

$$
\frac{n}{n^2}=\frac{1}{n}\to 0, \qquad \frac{1}{n^2}\to 0.
$$

Hence for large $n$ the numerator behaves like $4n^2$ and the denominator like $2n^2$:

$$
\frac{4n^2-3n+1}{2n^2+5n-7}\approx\frac{4n^2}{2n^2}=2.
$$

The ratio of the leading coefficients is therefore the limit.

**Answer**

$$
\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7}=2.
$$