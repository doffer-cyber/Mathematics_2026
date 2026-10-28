### Exercise 10. Inverse of a Diagonal Matrix
Given

$$
D=
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix},\qquad E=
\begin{pmatrix}
2 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}.
$$

Without using Gauss–Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

> **Why this exercise:** teaches how to recognize invertibility and the inverse without using a full procedure when the matrix structure gives the answer immediately.

---

#### Solution

**Determinants**

A diagonal matrix is triangular, so its determinant is the product of the diagonal entries.

$$
\begin{aligned}
\det D &= 2\cdot(-3)\cdot 5 \\
       &= -30.
\end{aligned}
$$

$$
\begin{aligned}
\det E &= 2\cdot 0\cdot 5 \\
       &= 0.
\end{aligned}
$$

**Which matrix is invertible**

A square matrix is invertible if and only if its determinant is nonzero. Hence $D$ is invertible, and $E$ is not invertible.

The matrix $E$ also has a zero row, so its rows are linearly dependent. For every matrix $X$, the second row of $EX$ is zero, so $EX$ can never equal $I$.

**Inverse of $D$**

The inverse of a diagonal matrix with nonzero diagonal entries is obtained by inverting each diagonal entry:

$$
D^{-1}=
\begin{pmatrix}
\dfrac{1}{2} & 0 & 0 \\
0 & -\dfrac{1}{3} & 0 \\
0 & 0 & \dfrac{1}{5} \\
\end{pmatrix}.
$$

**Check by multiplication**

$$
\begin{aligned}
DD^{-1} &=
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}
\begin{pmatrix}
\dfrac{1}{2} & 0 & 0 \\
0 & -\dfrac{1}{3} & 0 \\
0 & 0 & \dfrac{1}{5} \\
\end{pmatrix} \\
&=
\begin{pmatrix}
2\cdot\dfrac{1}{2} & 0 & 0 \\
0 & (-3)\cdot\left(-\dfrac{1}{3}\right) & 0 \\
0 & 0 & 5\cdot\dfrac{1}{5} \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}.
\end{aligned}
$$

Since the product of two diagonal matrices is computed entry by entry on the diagonal, $D^{-1}D=I$ as well.

**Answer:** $D$ is invertible and $E$ is not. The inverse of $D$ is

$$
D^{-1}=
\begin{pmatrix}
\dfrac{1}{2} & 0 & 0 \\
0 & -\dfrac{1}{3} & 0 \\
0 & 0 & \dfrac{1}{5} \\
\end{pmatrix}.
$$