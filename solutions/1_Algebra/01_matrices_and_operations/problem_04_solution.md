### Exercise 1. Determinant of a 2×2 Matrix
Compute

$$
\det
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix},
\qquad
\det
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}.
$$

Which matrix is invertible? Justify your answer.

> **Why this exercise:** introduces the simplest determinant calculation and immediately connects it with invertibility.

---

#### Solution

For a general 2×2 matrix, the determinant is given by

$$
M=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
\quad\Longrightarrow\quad
\det M = ad-bc.
$$

Denote the two given matrices by

$$
A=
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix},
\qquad
B=
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}.
$$

**First matrix**

$$
\begin{aligned}
\det A &= 3\cdot 4 - (-2)\cdot 5 \\
       &= 12 + 10 \\
       &= 22.
\end{aligned}
$$

**Second matrix**

$$
\begin{aligned}
\det B &= 1\cdot 14 - 7\cdot 2 \\
       &= 14 - 14 \\
       &= 0.
\end{aligned}
$$

**Invertibility**

A square matrix is invertible if and only if its determinant is nonzero.

- Since $\det A = 22 \neq 0$, the matrix $A$ is invertible.
- Since $\det B = 0$, the matrix $B$ is not invertible. Indeed, the second row of $B$ equals $2$ times its first row, so the rows are linearly dependent.

**Answer:** the determinants are $22$ and $0$, and only the first matrix is invertible.