### Exercise 10. Detecting Dependence
Without carrying out a full determinant calculation, explain why

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 5 \\
\end{pmatrix}=0.
$$

Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

> **Why this exercise:** teaches how to recognize a zero determinant from the structure of a matrix.

---

#### Solution

Denote the matrix by

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 5 \\
\end{pmatrix},
$$

and let $R_1,R_2,R_3$ be its rows.

**Dependence between the rows**

The second row is a multiple of the first row:

$$
R_2 = 2R_1,
$$

since $2\cdot(1,2,3)=(2,4,6)$. Equivalently,

$$
2R_1 - R_2 + 0\cdot R_3 = 0,
$$

which is a nontrivial linear combination of the rows equal to the zero row. Hence the rows of $A$ are linearly dependent.

**Why the determinant is zero**

Subtracting a multiple of one row from another row does not change the determinant. Replace $R_2$ by $R_2 - 2R_1$:

$$
A'=
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & 0 \\
0 & 1 & 5 \\
\end{pmatrix}.
$$

Then $\det A' = \det A$. The matrix $A'$ has a zero row, and expanding the determinant along that row gives $0$. Therefore

$$
\det A = 0.
$$

**Connection with noninvertibility**

A square matrix is invertible if and only if its determinant is nonzero. Since $\det A = 0$, the matrix $A$ is not invertible. This agrees with the linear dependence of the rows: a square matrix with linearly dependent rows has rank less than $3$, so it cannot be invertible.

**Answer:** $\det A = 0$ because $R_2 = 2R_1$, so the rows are linearly dependent and $A$ is not invertible.