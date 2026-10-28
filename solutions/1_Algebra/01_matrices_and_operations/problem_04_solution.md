## Solution to Exercise 4

Let

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix},\qquad
B=
\begin{pmatrix}
2 & 0 \\
3 & 1
\end{pmatrix}.
$$

### Computing $AB$

Each entry $(AB)_{ij}$ is the dot product of row $i$ of $A$ with column $j$ of $B$:

$$
AB=
\begin{pmatrix}
1\cdot 2+2\cdot 3 & 1\cdot 0+2\cdot 1 \\
0\cdot 2+1\cdot 3 & 0\cdot 0+1\cdot 1
\end{pmatrix}
=
\begin{pmatrix}
8 & 2 \\
3 & 1
\end{pmatrix}.
$$

### Computing $BA$

Now the roles are swapped: rows of $B$ against columns of $A$:

$$
BA=
\begin{pmatrix}
2\cdot 1+0\cdot 0 & 2\cdot 2+0\cdot 1 \\
3\cdot 1+1\cdot 0 & 3\cdot 2+1\cdot 1
\end{pmatrix}
=
\begin{pmatrix}
2 & 4 \\
3 & 7
\end{pmatrix}.
$$

### Is $AB = BA$?

No:

$$
AB=
\begin{pmatrix}
8 & 2 \\
3 & 1
\end{pmatrix}
\neq
\begin{pmatrix}
2 & 4 \\
3 & 7
\end{pmatrix}
=BA.
$$

The two products differ in three of the four entries (only the $(2,1)$ entry, $3$, agrees).

### What noncommutativity means

For real numbers, $ab=ba$ always holds, so the order of the factors doesn't matter. For matrices, **the order of multiplication matters**: in general

$$
AB\neq BA.
$$

This example shows it concretely: multiplying the same two matrices in different orders gives different results.

Why this happens:

- $AB$ means "apply $B$ first, then $A$" (as linear transformations acting on column vectors), while $BA$ means "apply $A$ first, then $B$". Doing two transformations in a different order generally gives a different overall transformation.
- In $AB$, rows of $A$ are combined with columns of $B$; in $BA$, rows of $B$ are combined with columns of $A$. These are different computations.

Notes:

- Noncommutativity does not mean $AB=BA$ *never* happens. Some pairs do commute (e.g., $A$ and $A^2$, or any matrix and the identity $I$). It just isn't guaranteed.
- Matrix multiplication is still **associative**, $(AB)C=A(BC)$, and **distributive**, so only commutativity is lost.
- Practical consequence: algebra rules from numbers must be adjusted. For example,
  $$(A+B)^2 = A^2 + AB + BA + B^2 \neq A^2 + 2AB + B^2$$
  in general, since $AB$ and $BA$ can't be combined.