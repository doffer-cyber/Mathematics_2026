# Exercise 1. Dominant Terms in a Sequence[cite: 1]

Compute[cite: 1]

$$
\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7}
$$[cite: 1]

Explain why the highest-degree terms determine the result[cite: 1].

## Solution[cite: 1]

### 1. Identify the dominant terms[cite: 1]

The numerator has the terms[cite: 1]

$$
4n^2, \quad -3n, \quad 1
$$[cite: 1]

and the denominator has[cite: 1]

$$
2n^2, \quad 5n, \quad -7
$$[cite: 1]

For very large $n$, the terms containing $n^2$ are much larger than the terms containing $n$ or a constant[cite: 1]. For example, when $n=1000$[cite: 1],

$$
4n^2=4{,}000{,}000, \qquad -3n=-3000, \qquad 1=1
$$[cite: 1]

Therefore, $4n^2$ dominates the numerator, and $2n^2$ dominates the denominator[cite: 1].

### 2. Divide by the highest power of $n$[cite: 1]

We divide both the numerator and denominator by $n^2$[cite: 1]:

$$
\frac{4n^2-3n+1}{2n^2+5n-7} = \frac{4-\frac{3}{n}+\frac{1}{n^2}}{2+\frac{5}{n}-\frac{7}{n^2}}
$$[cite: 1]

### 3. Evaluate the limit[cite: 1]

As $n\to\infty$[cite: 1],

$$
\frac{1}{n}\to0, \qquad \frac{1}{n^2}\to0
$$[cite: 1]

So[cite: 1],

$$
\lim_{n\to\infty} \frac{4-\frac{3}{n}+\frac{1}{n^2}}{2+\frac{5}{n}-\frac{7}{n^2}} = \frac{4-0+0}{2+0-0} = \frac{4}{2} = 2
$$[cite: 1]

### Final answer[cite: 1]

$$
\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7}=2
$$[cite: 1]

### Why the highest-degree terms determine the result[cite: 1]

Both numerator and denominator are quadratic polynomials[cite: 1]. Their leading terms are $4n^2$ and $2n^2$, and they grow much faster than the lower-degree terms[cite: 1]. After dividing by $n^2$, the remaining lower-degree terms become zero in the limit[cite: 1]. The limit is therefore the ratio of the leading coefficients[cite: 1]:

$$
\frac{4}{2}=2
$$[cite: 1]

> **Why this exercise:** introduces the idea of dominant terms and explains how to simplify expressions whose behavior is determined by their highest powers[cite: 1].