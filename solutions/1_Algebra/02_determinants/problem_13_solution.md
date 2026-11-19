### Exercise 13. Determinant by Elimination

Compute the determinant

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 5 & 7 \\
1 & 0 & 2 \\
\end{pmatrix}
$$

using elimination. Record the effect of every row operation used on the value of the determinant.

> **Why this exercise:** reinforces organizing a determinant calculation through row operations without introducing an unnecessary second procedure.

#### Solution

**Step 1. Create zeros in the first column.**

Apply $R_2\leftarrow R_2-2R_1$ and $R_3\leftarrow R_3-R_1$. Both operations add a multiple of one row to another row, so the determinant does not change.

$$
\det A=
\det
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & -2 & -1 \\
\end{pmatrix}.
$$

The new rows were computed as

$$
R_2:\ (2-2,\ 5-4,\ 7-6)=(0,\ 1,\ 1),
$$

$$
R_3:\ (1-1,\ 0-2,\ 2-3)=(0,\ -2,\ -1).
$$

**Step 2. Create a zero in the second column.**

Apply $R_3\leftarrow R_3+2R_2$. This again adds a multiple of one row to another row, so the determinant does not change.

$$
\det A=
\det
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{pmatrix}.
$$

The new third row is $(0,\ -2+2\cdot 1,\ -1+2\cdot 1)=(0,\ 0,\ 1)$.

**Step 3. Evaluate the triangular determinant.**

The determinant of an upper triangular matrix is the product of its diagonal entries.

$$
\det A = 1\cdot 1\cdot 1 = 1.
$$

**Step 4. Summary of the effect of the row operations.**

| Operation | Effect on the determinant |
|---|---|
| $R_2\leftarrow R_2-2R_1$ | unchanged |
| $R_3\leftarrow R_3-R_1$ | unchanged |
| $R_3\leftarrow R_3+2R_2$ | unchanged |

No row swap and no row scaling was used, so no correction factor appears and the determinant of the triangular matrix equals $\det A$.

**Step 5. Verification by cofactor expansion along the first row.**

$$
\det A =
1\cdot
\det
\begin{pmatrix}
5 & 7 \\
0 & 2 \\
\end{pmatrix}
- 2\cdot
\det
\begin{pmatrix}
2 & 7 \\
1 & 2 \\
\end{pmatrix}
+ 3\cdot
\det
\begin{pmatrix}
2 & 5 \\
1 & 0 \\
\end{pmatrix}
$$

$$
\det A = 1\cdot(10-0)-2\cdot(4-7)+3\cdot(0-5)
$$

$$
\det A = 10+6-15 = 1.
$$

Both methods give the same value.

**Answer.** $\det A = 1$. All three row operations used are of the type "add a multiple of one row to another row", so none of them changes the determinant.