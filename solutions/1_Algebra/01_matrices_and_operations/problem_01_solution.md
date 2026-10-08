### Exercise 1. Matrix Size and Entries

Given

$$
A=
\begin{pmatrix}
2 & -1 & 3 \\
0 & 4 & 5 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
-2 & 3 \\
4 & 1 \\
\end{pmatrix}.
$$

1. State the sizes of matrices $A$ and $B$.
2. Read off the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

> **Why this exercise:** builds basic fluency with matrix notation, indices, rows, and columns.

#### Solution

**Part 1. Sizes**

The size of a matrix is written as (number of rows) $\times$ (number of columns).

Matrix $A$ has 2 rows and 3 columns, so

$$
A \in \mathbb{R}^{2\times 3}.
$$

Matrix $B$ has 3 rows and 2 columns, so

$$
B \in \mathbb{R}^{3\times 2}.
$$

**Part 2. Entries**

The entry $a_{ij}$ lies in row $i$ and column $j$.

- $a_{12}$ is in row 1, column 2 of $A$, so $a_{12}=-1$.
- $a_{23}$ is in row 2, column 3 of $A$, so $a_{23}=5$.
- $b_{21}$ is in row 2, column 1 of $B$, so $b_{21}=-2$.
- $b_{32}$ is in row 3, column 2 of $B$, so $b_{32}=1$.

**Part 3. Row and column vectors**

The second row of $A$ is the row vector

$$
\begin{pmatrix}
0 & 4 & 5 \\
\end{pmatrix}.
$$

The first column of $B$ is the column vector

$$
\begin{pmatrix}
1 \\
-2 \\
4 \\
\end{pmatrix}.
$$

**Answer.** $A$ is $2\times 3$ and $B$ is $3\times 2$; $a_{12}=-1$, $a_{23}=5$, $b_{21}=-2$, $b_{32}=1$; the second row of $A$ is $(0,\,4,\,5)$ and the first column of $B$ is $(1,\,-2,\,4)^{T}$.