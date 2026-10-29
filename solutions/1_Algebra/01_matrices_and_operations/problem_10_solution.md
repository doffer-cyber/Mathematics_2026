### Exercise 10. Columns of a Matrix Product
Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}.
$$

Denote the columns of $B$ by $b_1,b_2$.

1. Compute $Ab_1$ and $Ab_2$.
2. Compute the matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

> **Why this exercise:** extends the interpretation of matrix-vector multiplication to a full product of two matrices instead of simply repeating another $Ax$ exercise.

**Solution**

**Step 1. The columns of $B$**

$$
b_1=
\begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix}
$$

$$
b_2=
\begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix}
$$

**Step 2. The vector $Ab_1$**

$$
\begin{aligned}
Ab_1 &=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1\cdot 1 + 2\cdot(-1) + 0\cdot 3 \\
0\cdot 1 + 1\cdot(-1) + 1\cdot 3 \\
\end{pmatrix} \\
&= \begin{pmatrix}
-1 \\
2 \\
\end{pmatrix}
\end{aligned}
$$

**Step 3. The vector $Ab_2$**

$$
\begin{aligned}
Ab_2 &=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1\cdot 2 + 2\cdot 0 + 0\cdot 1 \\
0\cdot 2 + 1\cdot 0 + 1\cdot 1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
\end{aligned}
$$

**Step 4. The product $AB$ (row by column)**

The matrix $A$ is of size $2\times 3$ and $B$ is of size $3\times 2$, so $AB$ is of size $2\times 2$.

$$
\begin{aligned}
AB &=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1\cdot 1 + 2\cdot(-1) + 0\cdot 3 & 1\cdot 2 + 2\cdot 0 + 0\cdot 1 \\
0\cdot 1 + 1\cdot(-1) + 1\cdot 3 & 0\cdot 2 + 1\cdot 0 + 1\cdot 1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}
\end{aligned}
$$

**Step 5. Comparison**

The first column of $AB$ is $(-1,\,2)$, which is $Ab_1$. The second column of $AB$ is $(2,\,1)$, which is $Ab_2$. Hence

$$
AB=
\begin{pmatrix}
Ab_1 & Ab_2 \\
\end{pmatrix}.
$$

**Step 6. Why the columns of $AB$ are $Ab_1$ and $Ab_2$**

The entry of $AB$ in row $i$ and column $j$ is the dot product of row $i$ of $A$ with column $j$ of $B$:

$$
(AB)_{ij} = a_{i1}b_{1j} + a_{i2}b_{2j} + a_{i3}b_{3j}.
$$

For a fixed $j$, the column $b_j$ of $B$ has entries $b_{1j},b_{2j},b_{3j}$. The same sums, collected for $i=1,2$, form exactly the vector $Ab_j$. Therefore the $j$-th column of $AB$ equals $Ab_j$.

In block form, writing $B$ as a row of its columns:

$$
AB = A
\begin{pmatrix}
b_1 & b_2 \\
\end{pmatrix}
=
\begin{pmatrix}
Ab_1 & Ab_2 \\
\end{pmatrix}.
$$

So the product $AB$ is obtained by applying $A$ separately to each column of $B$. Each column of $AB$ is a linear combination of the columns of $A$, with the entries of the corresponding column of $B$ as coefficients.