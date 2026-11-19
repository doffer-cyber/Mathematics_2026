### Exercise 11. Shortening the Calculation with Row Operations

Compute

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}
$$

by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

> **Why this exercise:** develops planning instead of mechanically repeating the same procedure.

#### Solution

Denote the matrix by $A$.

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}.
$$

**Step 1. Plan.**

The first column already has the entry $1$ in the first row. Subtracting the first row from the other two rows creates zeros below it.

**Step 2. Create zeros in the first column.**

Apply $R_2\to R_2-R_1$ and $R_3\to R_3-R_1$.

$$
\det A=
\det
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 2 & 3 \\
\end{pmatrix}.
$$

**Step 3. Create a zero in the second column.**

Apply $R_3\to R_3-2R_2$.

$$
\det A=
\det
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{pmatrix}.
$$

**Step 4. Evaluate the triangular determinant.**

The determinant of an upper triangular matrix is the product of its diagonal entries.

$$
\det A = 1\cdot 1\cdot 1 = 1.
$$

**Step 5. Which operations do not change the determinant.**

Adding a multiple of one row to a different row does not change the determinant. All three operations used above, $R_2\to R_2-R_1$, $R_3\to R_3-R_1$ and $R_3\to R_3-2R_2$, are of this type, so no correction factor is needed.

For comparison, the other elementary row operations behave as follows.

- Swapping two rows multiplies the determinant by $-1$.
- Multiplying one row by a number $k$ multiplies the determinant by $k$.

**Step 6. Verification by cofactor expansion along the first row.**

$$
\det A =
1\cdot
\det
\begin{pmatrix}
3 & 4 \\
4 & 6 \\
\end{pmatrix}
-2\cdot
\det
\begin{pmatrix}
1 & 4 \\
1 & 6 \\
\end{pmatrix}
+3\cdot
\det
\begin{pmatrix}
1 & 3 \\
1 & 4 \\
\end{pmatrix}
$$

$$
\det A = 1\cdot(18-16)-2\cdot(6-4)+3\cdot(4-3)
$$

$$
\det A = 2-4+3 = 1.
$$

Both methods give the same value.

**Answer.**

$$
\det A = 1.
$$

The row operations used (adding a multiple of one row to another) leave the determinant unchanged.