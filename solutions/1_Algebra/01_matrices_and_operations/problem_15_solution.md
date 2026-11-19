### Exercise 15. Associativity of Multiplication and Different Calculation Paths

Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\quad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix},\quad C=
\begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix}.
$$

Compute $(AB)C$ and $A(BC)$. Compare the results and the number of intermediate operations. Explain what associativity of matrix multiplication means in this example.

> **Why this exercise:** reinforces associativity by comparing two mathematically equivalent calculation path

#### Solution

The matrix $A$ has size $2\times 3$, $B$ has size $3\times 2$, and $C$ has size $2\times 2$. Both products $(AB)C$ and $A(BC)$ are defined and have size $2\times 2$.

**Path 1. Compute $(AB)C$.**

*Step 1. Compute $AB$.*

$$
AB=
\begin{pmatrix}
1\cdot 1+2\cdot 2+0\cdot(-1) & 1\cdot 0+2\cdot 1+0\cdot 3 \\
0\cdot 1+1\cdot 2+1\cdot(-1) & 0\cdot 0+1\cdot 1+1\cdot 3 \\
\end{pmatrix}
$$

$$
AB=
\begin{pmatrix}
5 & 2 \\
1 & 4 \\
\end{pmatrix}.
$$

*Step 2. Multiply by $C$.*

$$
(AB)C=
\begin{pmatrix}
5\cdot 2+2\cdot 0 & 5\cdot 1+2\cdot(-1) \\
1\cdot 2+4\cdot 0 & 1\cdot 1+4\cdot(-1) \\
\end{pmatrix}
$$

$$
(AB)C=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}.
$$

**Path 2. Compute $A(BC)$.**

*Step 3. Compute $BC$.*

$$
BC=
\begin{pmatrix}
1\cdot 2+0\cdot 0 & 1\cdot 1+0\cdot(-1) \\
2\cdot 2+1\cdot 0 & 2\cdot 1+1\cdot(-1) \\
(-1)\cdot 2+3\cdot 0 & (-1)\cdot 1+3\cdot(-1) \\
\end{pmatrix}
$$

$$
BC=
\begin{pmatrix}
2 & 1 \\
4 & 1 \\
-2 & -4 \\
\end{pmatrix}.
$$

*Step 4. Multiply $A$ by $BC$.*

$$
A(BC)=
\begin{pmatrix}
1\cdot 2+2\cdot 4+0\cdot(-2) & 1\cdot 1+2\cdot 1+0\cdot(-4) \\
0\cdot 2+1\cdot 4+1\cdot(-2) & 0\cdot 1+1\cdot 1+1\cdot(-4) \\
\end{pmatrix}
$$

$$
A(BC)=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}.
$$

**Step 5. Comparison of the results.**

$$
(AB)C=A(BC)=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}.
$$

The two calculation paths give the same matrix.

**Step 6. Comparison of the number of operations.**

A product of a $p\times q$ matrix by a $q\times r$ matrix requires $pqr$ multiplications and $pr(q-1)$ additions.

- Path 1, product $AB$ ($2\times 3$ by $3\times 2$): $12$ multiplications and $8$ additions.
- Path 1, product $(AB)C$ ($2\times 2$ by $2\times 2$): $8$ multiplications and $4$ additions.
- Path 1 in total: $20$ multiplications and $12$ additions.
- Path 2, product $BC$ ($3\times 2$ by $2\times 2$): $12$ multiplications and $6$ additions.
- Path 2, product $A(BC)$ ($2\times 3$ by $3\times 2$): $12$ multiplications and $8$ additions.
- Path 2 in total: $24$ multiplications and $14$ additions.

The first path is cheaper here, because it produces the small intermediate matrix $AB$ of size $2\times 2$, while the second path produces the larger intermediate matrix $BC$ of size $3\times 2$. The final results are identical, only the amount of work differs.

**Step 7. Meaning of associativity.**

Associativity of matrix multiplication means that for matrices of compatible sizes

$$
(AB)C=A(BC).
$$

The grouping of the factors does not change the result, so the product $ABC$ is well defined without parentheses. In this example the grouping affects only the intermediate matrices ($AB$ of size $2\times 2$ versus $BC$ of size $3\times 2$) and the number of operations. The order of the factors $A$, $B$, $C$ must not be changed, since matrix multiplication is not commutative in general.

**Answer.**

$$
(AB)C=A(BC)=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}.
$$

The first path needs $20$ multiplications and the second needs $24$, while the result is the same.