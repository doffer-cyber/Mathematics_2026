### Exercise 6. Transpose
For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
$$

compute $A^T$, $B^T$, and $AB$. Then verify in this example that

$$
(AB)^T=B^TA^T.
$$

> **Why this exercise:** teaches transposition and an important property that reverses the order of factors.

**Solution**

**Step 1. The transposes $A^T$ and $B^T$**

The transpose turns the rows of a matrix into columns.

$$
A^T=
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix}
$$

$$
B^T=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}
$$

**Step 2. The product $AB$**

The matrix $A$ is of size $2\times 3$ and $B$ is of size $3\times 2$, so $AB$ is of size $2\times 2$.

$$
\begin{aligned}
AB &=
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1\cdot 1 + 2\cdot 2 + 3\cdot(-1) & 1\cdot 0 + 2\cdot 1 + 3\cdot 3 \\
4\cdot 1 + 5\cdot 2 + 6\cdot(-1) & 4\cdot 0 + 5\cdot 1 + 6\cdot 3 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2 & 11 \\
8 & 23 \\
\end{pmatrix}
\end{aligned}
$$

**Step 3. The transpose $(AB)^T$**

$$
(AB)^T=
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}
$$

**Step 4. The product $B^TA^T$**

The matrix $B^T$ is of size $2\times 3$ and $A^T$ is of size $3\times 2$, so $B^TA^T$ is of size $2\times 2$.

$$
\begin{aligned}
B^TA^T &=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1\cdot 1 + 2\cdot 2 + (-1)\cdot 3 & 1\cdot 4 + 2\cdot 5 + (-1)\cdot 6 \\
0\cdot 1 + 1\cdot 2 + 3\cdot 3 & 0\cdot 4 + 1\cdot 5 + 3\cdot 6 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}
\end{aligned}
$$

**Step 5. Comparison**

Steps 3 and 4 give the same matrix, so

$$
(AB)^T=B^TA^T=
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}.
$$

**Step 6. Remark on the order of factors**

The product $A^TB^T$ is not even defined here, because $A^T$ is of size $3\times 2$ and $B^T$ is of size $2\times 3$ give a $3\times 3$ product, which has a different size from $(AB)^T$. Hence the reversed order $B^TA^T$ is the only order that gives a matrix of the correct size $2\times 2$.