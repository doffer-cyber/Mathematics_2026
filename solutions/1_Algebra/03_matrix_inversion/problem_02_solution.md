### Exercise 2. Formula for a 2×2 Matrix
Find the inverse of

$$
A=
\begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
$$

using the formula for a $2\times2$ matrix. At the end, check the result by computing one product with $A$.

> **Why this exercise:** teaches the simplest explicit formula for an inverse and requires verification using the definition.

---

#### Solution

**Formula**

For a $2\times2$ matrix with $ad-bc\neq 0$,

$$
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}^{-1}
=
\frac{1}{ad-bc}
\begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix}.
$$

**Determinant**

$$
\begin{aligned}
\det A &= 3\cdot 4 - 2\cdot 5 \\
       &= 12 - 10 \\
       &= 2.
\end{aligned}
$$

Since $\det A = 2\neq 0$, the matrix $A$ is invertible.

**Inverse**

Here $a=3$, $b=2$, $c=5$, $d=4$. Hence

$$
\begin{aligned}
A^{-1} &= \frac{1}{2}
\begin{pmatrix}
4 & -2 \\
-5 & 3 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
2 & -1 \\
-\dfrac{5}{2} & \dfrac{3}{2} \\
\end{pmatrix}.
\end{aligned}
$$

**Check**

Compute the product $AA^{-1}$, using the form with the factor $\frac12$ outside:

$$
\begin{aligned}
AA^{-1} &= \frac{1}{2}
\begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
\begin{pmatrix}
4 & -2 \\
-5 & 3 \\
\end{pmatrix} \\
&= \frac{1}{2}
\begin{pmatrix}
3\cdot 4 + 2\cdot(-5) & 3\cdot(-2) + 2\cdot 3 \\
5\cdot 4 + 4\cdot(-5) & 5\cdot(-2) + 4\cdot 3 \\
\end{pmatrix} \\
&= \frac{1}{2}
\begin{pmatrix}
2 & 0 \\
0 & 2 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}.
\end{aligned}
$$

Since $AA^{-1}=I$ for a square matrix, the computed matrix is the inverse of $A$.

**Answer:**

$$
A^{-1}=
\begin{pmatrix}
2 & -1 \\
-\dfrac{5}{2} & \dfrac{3}{2} \\
\end{pmatrix}.
$$