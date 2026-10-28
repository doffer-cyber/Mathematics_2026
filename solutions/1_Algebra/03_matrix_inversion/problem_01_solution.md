### Exercise 1. Definition of the Inverse
For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
$$

check, without using a formula, whether $B=A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

> **Why this exercise:** starts from the definition of the inverse through multiplication before any formulas or computational methods are introduced

---

#### Solution

**Definition**

A square matrix $B$ is the inverse of $A$ if

$$
AB = BA = I,
$$

where $I$ is the identity matrix of the same size. Here

$$
I=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}.
$$

**Computation of $AB$**

$$
\begin{aligned}
AB &=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
2\cdot 1 + 1\cdot(-1) & 2\cdot(-1) + 1\cdot 2 \\
1\cdot 1 + 1\cdot(-1) & 1\cdot(-1) + 1\cdot 2 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}.
\end{aligned}
$$

**Computation of $BA$**

$$
\begin{aligned}
BA &=
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1\cdot 2 + (-1)\cdot 1 & 1\cdot 1 + (-1)\cdot 1 \\
(-1)\cdot 2 + 2\cdot 1 & (-1)\cdot 1 + 2\cdot 1 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}.
\end{aligned}
$$

**Conclusion**

Since $AB = I$ and $BA = I$, the matrix $B$ satisfies the definition of the inverse of $A$. Therefore

$$
B = A^{-1}.
$$

**Answer:** yes, $B=A^{-1}$, because $AB=BA=I$.