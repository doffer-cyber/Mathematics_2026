### Exercise 6. Transpose

#### Solution

Let

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix}
$$

and

$$
B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
$$

The matrix $A$ has size $2\times 3$ and $B$ has size $3\times 2$, so $AB$ is defined and has size $2\times 2$.

#### Computation of $A^T$ and $B^T$

The transpose is obtained by writing the rows as columns.

$$
A^T=
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix}
$$

and

$$
B^T=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}
$$

#### Computation of $AB$

The entry $(AB)_{ij}$ is the dot product of row $i$ of $A$ with column $j$ of $B$.

$$
AB=
\begin{pmatrix}
1\cdot 1+2\cdot 2+3\cdot(-1) & 1\cdot 0+2\cdot 1+3\cdot 3 \\
4\cdot 1+5\cdot 2+6\cdot(-1) & 4\cdot 0+5\cdot 1+6\cdot 3 \\
\end{pmatrix}
$$

Therefore

$$
AB=
\begin{pmatrix}
2 & 11 \\
8 & 23 \\
\end{pmatrix}
$$

#### Computation of $(AB)^T$

Transposing $AB$ gives

$$
(AB)^T=
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}
$$

#### Computation of $B^TA^T$

The matrix $B^T$ has size $2\times 3$ and $A^T$ has size $3\times 2$, so the product has size $2\times 2$.

$$
B^TA^T=
\begin{pmatrix}
1\cdot 1+2\cdot 2+(-1)\cdot 3 & 1\cdot 4+2\cdot 5+(-1)\cdot 6 \\
0\cdot 1+1\cdot 2+3\cdot 3 & 0\cdot 4+1\cdot 5+3\cdot 6 \\
\end{pmatrix}
$$

Therefore

$$
B^TA^T=
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}
$$

#### Verification

Both computations give the same matrix:

$$
(AB)^T=
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}
=B^TA^T
$$

Hence $(AB)^T=B^TA^T$ holds in this example.

#### Remarks

- The order of the factors is reversed under transposition. In this example $A^TB^T$ is not even defined, because $A^T$ has size $3\times 2$ and $B^T$ has size $2\times 3$ would give a $3\times 3$ product, which differs in size from $(AB)^T$.
- In general, for matrices $A$ and $B$ for which $AB$ is defined,

$$
(AB)^T=B^TA^T
$$

- The entry $(i,j)$ of $(AB)^T$ is the dot product of row $j$ of $A$ with column $i$ of $B$. This is the same as the dot product of row $i$ of $B^T$ with column $j$ of $A^T$, which is the entry $(i,j)$ of $B^TA^T$.