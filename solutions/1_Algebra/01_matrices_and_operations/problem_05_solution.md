### Exercise 5. Matrix Times Vector
Let

$$
A=
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix},\qquad x=
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix}.
$$

Compute $Ax$. Then express $Ax$ as a linear combination of the columns of $A$, with coefficients coming from the vector $x$.

> **Why this exercise:** shows that multiplying a matrix by a vector can be understood as a linear combination of the matrix columns.

**Solution**

**Step 1. The product $Ax$ (row by column)**

Each entry of $Ax$ is the dot product of a row of $A$ with $x$:

$$
\begin{aligned}
Ax &=
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2\cdot 4 + (-1)\cdot 2 \\
1\cdot 4 + 3\cdot 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
\end{aligned}
$$

**Step 2. The columns of $A$**

$$
a_1=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
$$

$$
a_2=
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}
$$

**Step 3. Linear combination of the columns**

The coefficients are the entries of $x$, that is $x_1=4$ and $x_2=2$:

$$
Ax = x_1 a_1 + x_2 a_2 = 4a_1 + 2a_2.
$$

Substituting the columns:

$$
\begin{aligned}
Ax &= 4
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
+ 2
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix} \\
&= \begin{pmatrix}
8 \\
4 \\
\end{pmatrix}
+
\begin{pmatrix}
-2 \\
6 \\
\end{pmatrix} \\
&= \begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
\end{aligned}
$$

**Step 4. Comparison**

Both methods give the same vector:

$$
Ax=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}.
$$

Hence multiplying $A$ by $x$ produces a linear combination of the columns of $A$, where the first column is scaled by $4$ and the second column is scaled by $2$.