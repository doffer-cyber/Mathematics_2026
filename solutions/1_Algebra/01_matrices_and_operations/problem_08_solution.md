### Exercise 8. Row Operations and Their Reversibility
For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

perform, in order:

1. $R_2\leftarrow R_2-2R_1$,
2. $R_3\leftarrow R_3+R_1$,
3. interchange $R_2$ and $R_3$.

Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

> **Why this exercise:** prepares for elimination by showing that row operations are controlled and reversible transformations of a matrix.

**Solution**

**Step 1. Operation $R_2\leftarrow R_2-2R_1$**

The new second row is

$$
R_2-2R_1 = (2,\,4,\,1)-2(1,\,2,\,-1) = (0,\,0,\,3).
$$

The matrix after this step is

$$
A_1=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

**Step 2. Operation $R_3\leftarrow R_3+R_1$**

The new third row is

$$
R_3+R_1 = (-1,\,1,\,3)+(1,\,2,\,-1) = (0,\,3,\,2).
$$

The matrix after this step is

$$
A_2=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix}
$$

**Step 3. Interchange of $R_2$ and $R_3$**

The matrix after this step is

$$
A_3=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}
$$

The matrix $A_3$ is in row echelon form.

**Step 4. Reversing the operations**

Each operation is undone by an operation of the same type. The operations must be undone in the opposite order.

1. The interchange of $R_2$ and $R_3$ is reversed by interchanging $R_2$ and $R_3$ again.
2. The operation $R_3\leftarrow R_3+R_1$ is reversed by $R_3\leftarrow R_3-R_1$.
3. The operation $R_2\leftarrow R_2-2R_1$ is reversed by $R_2\leftarrow R_2+2R_1$.

**Step 5. Check of the reversal**

Starting from $A_3$, interchange $R_2$ and $R_3$. This gives $A_2$:

$$
A_2=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix}
$$

Apply $R_3\leftarrow R_3-R_1$. The new third row is $(0,\,3,\,2)-(1,\,2,\,-1)=(-1,\,1,\,3)$, which gives $A_1$:

$$
A_1=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

Apply $R_2\leftarrow R_2+2R_1$. The new second row is $(0,\,0,\,3)+2(1,\,2,\,-1)=(2,\,4,\,1)$, which gives the original matrix:

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

Hence every row operation used here is reversible, and the original matrix is recovered exactly.