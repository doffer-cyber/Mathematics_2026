### Exercise 5. Row Operations
For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

find $\det A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

> **Why this exercise:** connects determinants with row operations and requires conscious tracking of every step.

---

#### Solution

**Effect of row operations on the determinant**

- Swapping two rows multiplies the determinant by $-1$.
- Multiplying a row by a scalar $c$ multiplies the determinant by $c$.
- Adding a multiple of one row to another row does not change the determinant.

**Step 1.** Replace $R_2$ by $R_2 - 2R_1$ and $R_3$ by $R_3 + R_1$. Both operations add a multiple of one row to another row, so the determinant does not change.

$$
A_1=
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 6 & 5 \\
\end{pmatrix}.
$$

Here $\det A_1 = \det A$.

**Step 2.** Replace $R_3$ by $R_3 + 2R_2$. This again adds a multiple of one row to another row, so the determinant does not change.

$$
A_2=
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 0 & -7 \\
\end{pmatrix}.
$$

Here $\det A_2 = \det A_1 = \det A$.

**Step 3.** The matrix $A_2$ is upper triangular, so its determinant is the product of the diagonal entries:

$$
\begin{aligned}
\det A_2 &= 1\cdot(-3)\cdot(-7) \\
         &= 21.
\end{aligned}
$$

Since no step changed the determinant,

$$
\det A = \det A_2 = 21.
$$

**Check using Sarrus' rule**

$$
\begin{aligned}
P &= 1\cdot 1\cdot 2 + 2\cdot 0\cdot(-1) + 3\cdot 2\cdot 4 \\
  &= 2 + 0 + 24 \\
  &= 26,
\end{aligned}
$$

$$
\begin{aligned}
N &= 3\cdot 1\cdot(-1) + 1\cdot 0\cdot 4 + 2\cdot 2\cdot 2 \\
  &= -3 + 0 + 8 \\
  &= 5.
\end{aligned}
$$

$$
\begin{aligned}
\det A &= P - N \\
       &= 26 - 5 \\
       &= 21.
\end{aligned}
$$

The result agrees with the row-operation computation.

**Answer:** $\det A = 21$.