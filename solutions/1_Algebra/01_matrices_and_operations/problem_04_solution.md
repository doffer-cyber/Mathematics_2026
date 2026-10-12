## Exercise 4. Matrix Multiplication and Noncommutativity

### Solution

Let

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
$$

and

$$
B=
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

### Computation of $AB$

The entry $(AB)_{ij}$ is the dot product of row $i$ of $A$ with column $j$ of $B$.

$$
AB=
\begin{pmatrix}
1\cdot 2+2\cdot 3 & 1\cdot 0+2\cdot 1 \\
0\cdot 2+1\cdot 3 & 0\cdot 0+1\cdot 1 \\
\end{pmatrix}
$$

Therefore

$$
AB=
\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix}
$$

### Computation of $BA$

The entry $(BA)_{ij}$ is the dot product of row $i$ of $B$ with column $j$ of $A$.

$$
BA=
\begin{pmatrix}
2\cdot 1+0\cdot 0 & 2\cdot 2+0\cdot 1 \\
3\cdot 1+1\cdot 0 & 3\cdot 2+1\cdot 1 \\
\end{pmatrix}
$$

Therefore

$$
BA=
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}
$$

### Comparison

The two products are

$$
AB=
\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix}
$$

and

$$
BA=
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}
$$

These matrices are different, so $AB\neq BA$. Only the $(2,1)$ entry, equal to $3$, coincides.

### Meaning of noncommutativity

For real numbers, $ab=ba$ always holds, so the order of the factors is irrelevant. For matrices, the order of multiplication matters. In general

$$
AB\neq BA
$$

and this example confirms it.

The reason is that $AB$ and $BA$ describe different operations:

- $AB$ means "apply $B$ first, then $A$" (as linear maps acting on column vectors).
- $BA$ means "apply $A$ first, then $B$".
- Performing two transformations in a different order generally gives a different overall transformation.
- In $AB$, rows of $A$ are paired with columns of $B$. In $BA$, rows of $B$ are paired with columns of $A$.

### Remarks

- Noncommutativity does not mean that $AB=BA$ never occurs. Some pairs commute, for example any matrix $A$ with the identity matrix $I$, or $A$ with $A^2$. Commutativity is simply not guaranteed.
- Matrix multiplication remains associative, $(AB)C=A(BC)$, and distributive. Only commutativity is lost.
- Familiar algebraic identities must be adjusted. For example,

$$
(A+B)^2 = A^2 + AB + BA + B^2
$$

which in general differs from

$$
A^2 + 2AB + B^2
$$

because $AB$ and $BA$ cannot be combined.
