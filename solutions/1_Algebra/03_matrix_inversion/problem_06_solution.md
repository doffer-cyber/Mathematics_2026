### Exercise 6. Solving a System Using the Inverse
Solve

$$
Ax=b,
$$

where

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix},
$$

using $x=A^{-1}b$. Then substitute the resulting vector back into the equation and check the result.

> **Why this exercise:** shows the connection between inverse matrices and solving a linear system.

---

#### Solution

**Determinant**

$$
\begin{aligned}
\det A &= 2\cdot 3 - 1\cdot 1 \\
       &= 6 - 1 \\
       &= 5.
\end{aligned}
$$

Since $\det A = 5\neq 0$, the matrix $A$ is invertible.

**Inverse**

By the formula for a $2\times2$ matrix,

$$
A^{-1}=\frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}.
$$

**Solution of the system**

Multiplying $Ax=b$ from the left by $A^{-1}$ gives $x=A^{-1}b$. Hence

$$
\begin{aligned}
x &= \frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix} \\
&= \frac{1}{5}
\begin{pmatrix}
3\cdot 5 + (-1)\cdot 7 \\
(-1)\cdot 5 + 2\cdot 7 \\
\end{pmatrix} \\
&= \frac{1}{5}
\begin{pmatrix}
8 \\
9 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
\dfrac{8}{5} \\
\dfrac{9}{5} \\
\end{pmatrix}.
\end{aligned}
$$

**Check**

Substitute $x$ into $Ax$:

$$
\begin{aligned}
Ax &=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
\dfrac{8}{5} \\
\dfrac{9}{5} \\
\end{pmatrix} \\
&=
\begin{pmatrix}
\dfrac{16}{5} + \dfrac{9}{5} \\
\dfrac{8}{5} + \dfrac{27}{5} \\
\end{pmatrix} \\
&=
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix} \\
&= b.
\end{aligned}
$$

The equation is satisfied.

**Answer:**

$$
x=
\begin{pmatrix}
\dfrac{8}{5} \\
\dfrac{9}{5} \\
\end{pmatrix}.
$$