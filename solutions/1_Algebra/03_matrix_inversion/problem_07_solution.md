### Exercise 7. Inverse of a Product
For

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix}
$$

compute $(AB)^{-1}$ and $B^{-1}A^{-1}$. Check that the results are the same and explain the meaning of the reversed order.

> **Why this exercise:** reinforces the inverse-of-a-product property and requires its interpretation.

---

#### Solution

**The product $AB$**

$$
\begin{aligned}
AB &=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1\cdot 2 + 1\cdot 0 & 1\cdot 0 + 1\cdot 3 \\
0\cdot 2 + 1\cdot 0 & 0\cdot 0 + 1\cdot 3 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
2 & 3 \\
0 & 3 \\
\end{pmatrix}.
\end{aligned}
$$

**Computation of $(AB)^{-1}$**

$$
\begin{aligned}
\det(AB) &= 2\cdot 3 - 3\cdot 0 \\
         &= 6.
\end{aligned}
$$

By the formula for a $2\times2$ matrix,

$$
\begin{aligned}
(AB)^{-1} &= \frac{1}{6}
\begin{pmatrix}
3 & -3 \\
0 & 2 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
\dfrac{1}{2} & -\dfrac{1}{2} \\
0 & \dfrac{1}{3} \\
\end{pmatrix}.
\end{aligned}
$$

**Computation of $A^{-1}$ and $B^{-1}$**

Since $\det A = 1$,

$$
A^{-1}=
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}.
$$

The matrix $B$ is diagonal, so its inverse is obtained by inverting the diagonal entries:

$$
B^{-1}=
\begin{pmatrix}
\dfrac{1}{2} & 0 \\
0 & \dfrac{1}{3} \\
\end{pmatrix}.
$$

**Computation of $B^{-1}A^{-1}$**

$$
\begin{aligned}
B^{-1}A^{-1} &=
\begin{pmatrix}
\dfrac{1}{2} & 0 \\
0 & \dfrac{1}{3} \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
\dfrac{1}{2}\cdot 1 + 0\cdot 0 & \dfrac{1}{2}\cdot(-1) + 0\cdot 1 \\
0\cdot 1 + \dfrac{1}{3}\cdot 0 & 0\cdot(-1) + \dfrac{1}{3}\cdot 1 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
\dfrac{1}{2} & -\dfrac{1}{2} \\
0 & \dfrac{1}{3} \\
\end{pmatrix}.
\end{aligned}
$$

**Comparison**

The two results coincide:

$$
(AB)^{-1} = B^{-1}A^{-1}.
$$

**Meaning of the reversed order**

The product $AB$ means: first apply $B$, then apply $A$. To undo this, the steps must be undone in the opposite order: first undo $A$, then undo $B$. This is exactly the product $B^{-1}A^{-1}$.

Algebraically,

$$
\begin{aligned}
(AB)(B^{-1}A^{-1}) &= A(BB^{-1})A^{-1} \\
                   &= AIA^{-1} \\