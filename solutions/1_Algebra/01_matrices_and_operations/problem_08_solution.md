### Exercise 8. Row Operations and Their Reversibility

**Given matrix**

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

**Step 1.** $R_2\leftarrow R_2-2R_1$.

The new second row is $(2-2,\ 4-4,\ 1+2)=(0,\ 0,\ 3)$.

$$
A_1=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

**Step 2.** $R_3\leftarrow R_3+R_1$.

The new third row is $(-1+1,\ 1+2,\ 3-1)=(0,\ 3,\ 2)$.

$$
A_2=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix}
$$

**Step 3.** Interchange $R_2$ and $R_3$.

$$
A_3=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}
$$

The matrix $A_3$ is in row echelon form (upper triangular).

**Reversing operations**

Each operation is undone by an operation of the same type:

1. $R_2\leftarrow R_2-2R_1$ is reversed by $R_2\leftarrow R_2+2R_1$.
2. $R_3\leftarrow R_3+R_1$ is reversed by $R_3\leftarrow R_3-R_1$.
3. The interchange of $R_2$ and $R_3$ is reversed by the same interchange, since swapping twice returns the original order.

To return from $A_3$ to $A$, apply the reversing operations in the opposite order: first the interchange, then $R_3\leftarrow R_3-R_1$, then $R_2\leftarrow R_2+2R_1$.