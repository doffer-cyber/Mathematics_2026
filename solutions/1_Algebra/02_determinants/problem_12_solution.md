### Exercise 12. A Parameter Revealed by a Row Operation

For

$$
A(t)=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & t \\
0 & 1 & 1 \\
\end{pmatrix}
$$

find the values of $t$ for which the matrix is not invertible.

Before computing the determinant, perform the operation

$$
R_2\leftarrow R_2-2R_1
$$

and use the resulting structure. At the end, explain what special thing happens to the rows for the value of the parameter you found.

> **Why this exercise:** combines a parameter, row operations, and recognition of dependence in one short argument.

#### Solution

**Step 1. Apply the row operation.**

Adding a multiple of one row to another row does not change the determinant. Hence $R_2\leftarrow R_2-2R_1$ leaves $\det A(t)$ unchanged. The new second row is

$$
(2-2\cdot 1,\ 4-2\cdot 2,\ t-2\cdot 3)=(0,\ 0,\ t-6).
$$

Therefore

$$
\det A(t)=
\det
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & t-6 \\
0 & 1 & 1 \\
\end{pmatrix}.
$$

**Step 2. Expand along the first column.**

The first column contains only one nonzero entry, namely $1$ in the first row. Hence

$$
\det A(t)=1\cdot
\det
\begin{pmatrix}
0 & t-6 \\
1 & 1 \\
\end{pmatrix}.
$$

$$
\det A(t)=0\cdot 1-(t-6)\cdot 1 = 6-t.
$$

**Step 3. Condition for non-invertibility.**

A square matrix is not invertible if and only if its determinant equals $0$.

$$
6-t=0 \iff t=6.
$$

**Step 4. Verification by direct expansion.**

Expanding the original matrix along the first row:

$$
\det A(t)=1\cdot(4\cdot 1-t\cdot 1)-2\cdot(2\cdot 1-t\cdot 0)+3\cdot(2\cdot 1-4\cdot 0)
$$

$$
\det A(t)=(4-t)-4+6=6-t.
$$

Both methods give the same result.

**Step 5. What happens to the rows for $t=6$.**

For $t=6$ the operation $R_2\leftarrow R_2-2R_1$ produces the zero row $(0,0,0)$. This means

$$
R_2=2R_1,
$$

that is, $(2,4,6)=2\cdot(1,2,3)$. The second row is a multiple of the first row, so the rows are linearly dependent. The rows $R_1$ and $R_3$ remain independent, hence the matrix $A(6)$ has rank $2$ and is not invertible.

**Answer.** The matrix $A(t)$ is not invertible exactly for $t=6$, where $\det A(t)=6-t=0$. For this value the second row equals twice the first row.