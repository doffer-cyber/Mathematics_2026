### Exercise 4. Triangular Matrix
Without expanding the determinant, compute

$$
\det
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}.
$$

State the rule for an arbitrary triangular matrix and explain it using this example.

> **Why this exercise:** reinforces an important property of triangular matrices.

---

#### Solution

**Rule**

If $A=(a_{ij})$ is an $n\times n$ upper triangular matrix (all entries below the main diagonal are zero) or a lower triangular matrix (all entries above the main diagonal are zero), then its determinant is the product of the diagonal entries:

$$
\det A = a_{11}\,a_{22}\cdots a_{nn}.
$$

**Application to the given matrix**

Denote

$$
A=
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}.
$$

The matrix $A$ is upper triangular, with diagonal entries $2$, $-3$, $7$. Hence

$$
\begin{aligned}
\det A &= 2\cdot(-3)\cdot 7 \\
       &= -42.
\end{aligned}
$$

**Explanation using this example**

Expand along the first column. Its only nonzero entry is $2$ in the position $(1,1)$, so

$$
\det A = 2\cdot\det
\begin{pmatrix}
-3 & 5 \\
0 & 7 \\
\end{pmatrix}.
$$

The remaining $2\times2$ matrix is again upper triangular. Expanding along its first column in the same way gives

$$
\begin{aligned}
\det
\begin{pmatrix}
-3 & 5 \\
0 & 7 \\
\end{pmatrix}
&= (-3)\cdot 7 - 5\cdot 0 \\
&= -21.
\end{aligned}
$$

Therefore

$$
\begin{aligned}
\det A &= 2\cdot(-21) \\
       &= -42.
\end{aligned}
$$

At every step the first column contains only one nonzero entry, namely the diagonal one, so the expansion produces exactly the product of the diagonal entries. The same argument works for any triangular matrix by induction on $n$. For a lower triangular matrix, expand along the first row instead.

**Answer:** $\det A = -42$.