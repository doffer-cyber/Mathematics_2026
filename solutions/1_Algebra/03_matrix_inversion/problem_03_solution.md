### Exercise 3. When Does the Inverse Not Exist?
For

$$
A=
\begin{pmatrix}
2 & 4 \\
1 & 2 \\
\end{pmatrix}
$$

explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

> **Why this exercise:** connects two signs of noninvertibility instead of treating them as unrelated facts.

---

#### Solution

**Method 1: the determinant**

A square matrix is invertible if and only if its determinant is nonzero. For $A$,

$$
\begin{aligned}
\det A &= 2\cdot 2 - 4\cdot 1 \\
       &= 4 - 4 \\
       &= 0.
\end{aligned}
$$

The $2\times2$ inverse formula contains the factor $\dfrac{1}{\det A}$, which is undefined for $\det A = 0$. Hence $A^{-1}$ does not exist.

**Method 2: dependence between the rows**

Let $R_1=(2,4)$ and $R_2=(1,2)$ be the rows of $A$. The first row is a multiple of the second row:

$$
R_1 = 2R_2.
$$

Equivalently,

$$
R_1 - 2R_2 = (0,0),
$$

which is a nontrivial linear combination of the rows equal to the zero row. Hence the rows are linearly dependent.

Suppose that $A^{-1}$ existed. Then the equation $A\mathbf{x}=\mathbf{0}$ would have only the zero solution, since multiplying by $A^{-1}$ gives $\mathbf{x}=A^{-1}\mathbf{0}=\mathbf{0}$. However, the vector $\mathbf{x}=(2,-1)^T$ is nonzero and satisfies

$$
A\mathbf{x}=
\begin{pmatrix}
2\cdot 2 + 4\cdot(-1) \\
1\cdot 2 + 2\cdot(-1) \\
\end{pmatrix}
=
\begin{pmatrix}
0 \\
0 \\
\end{pmatrix}.
$$

This is a contradiction, so $A^{-1}$ does not exist.

**Connection between the two methods**

Linearly dependent rows make the determinant vanish: subtracting $2R_2$ from $R_1$ does not change the determinant and produces a zero row, so $\det A = 0$. Conversely, $\det A=0$ means that the rows are linearly dependent. Both statements describe the same property of $A$.

**Answer:** $A^{-1}$ does not exist because $\det A = 0$, equivalently because $R_1 = 2R_2$, so the rows of $A$ are linearly dependent.