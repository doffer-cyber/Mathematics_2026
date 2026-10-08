### Exercise 1. Dominant Terms in a Sequence
Compute

$$
\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7}.
$$

Explain why the highest-degree terms determine the result.

## Solution

### 1. Identify the dominant terms

The numerator has the terms

$$
4n^2,
\quad -3n,
\quad 1,
$$

and the denominator has

$$
2n^2,
\quad 5n,
\quad -7.
$$

For very large $n$, the terms containing $n^2$ are much larger than the terms containing $n$ or a constant. For example, when $n=1000$,

$$
4n^2=4{,}000{,}000,
\qquad
-3n=-3000,
\qquad
1=1.
$$

Therefore, $4n^2$ dominates the numerator, and $2n^2$ dominates the denominator.

### 2. Divide by the highest power of $n$

We divide both the numerator and denominator by $n^2$:

$$
\frac{4n^2-3n+1}{2n^2+5n-7}
=
\frac{4-\frac{3}{n}+\frac{1}{n^2}}{2+\frac{5}{n}-\frac{7}{n^2}}.
$$

### 3. Evaluate the limit

As $n\to\infty$,

$$
\frac{1}{n}\to0,
\qquad
\frac{1}{n^2}\to0.
$$

So,

$$
\lim_{n\to\infty}
\frac{4-\frac{3}{n}+\frac{1}{n^2}}{2+\frac{5}{n}-\frac{7}{n^2}}
=
\frac{4-0+0}{2+0-0}
=
\frac{4}{2}=2.
$$

### Final answer

$$
\boxed{\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7}=2}
$$

### Why the highest-degree terms determine the result

Both numerator and denominator are quadratic polynomials. Their leading terms are $4n^2$ and $2n^2$, and they grow much faster than the lower-degree terms. After dividing by $n^2$, the remaining lower-degree terms become zero in the limit. The limit is therefore the ratio of the leading coefficients:

$$
\frac{4}{2}=2.
$$

> **Why this exercise:** introduces the idea of dominant terms and explains how to simplify expressions whose behavior is determined by their highest powers.
