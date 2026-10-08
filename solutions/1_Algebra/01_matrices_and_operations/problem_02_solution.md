### Exercise 2. Addition and Scalar Multiplication

For

$$
A=
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix}
$$

compute

$$
A+B,\qquad A-B,\qquad 3A-2B.
$$

Explain why matrix addition is possible only for matrices of the same size.

> **Why this exercise:** reinforces entry-by-entry operations and the importance of compatible dimensions.

#### Solution

Addition, subtraction, and scalar multiplication are performed entry by entry.

**Computation of $A+B$**

$$
A+B=
\begin{pmatrix}
1+4 & 2+(-2) \\
-1+0 & 3+5 \\
\end{pmatrix}
$$

$$
A+B=
\begin{pmatrix}
5 & 0 \\
-1 & 8 \\
\end{pmatrix}
$$

**Computation of $A-B$**

$$
A-B=
\begin{pmatrix}
1-4 & 2-(-2) \\
-1-0 & 3-5 \\
\end{pmatrix}
$$

$$
A-B=
\begin{pmatrix}
-3 & 4 \\
-1 & -2 \\
\end{pmatrix}
$$

**Computation of $3A-2B$**

First compute the scalar multiples:

$$
3A=
\begin{pmatrix}
3 & 6 \\
-3 & 9 \\
\end{pmatrix},\qquad 2B=
\begin{pmatrix}
8 & -4 \\
0 & 10 \\
\end{pmatrix}.
$$

Then subtract entry by entry:

$$
3A-2B=
\begin{pmatrix}
3-8 & 6-(-4) \\
-3-0 & 9-10 \\
\end{pmatrix}
$$

$$
3A-2B=
\begin{pmatrix}
-5 & 10 \\
-3 & -1 \\
\end{pmatrix}
$$

**Why the sizes must agree**

By definition, the sum of two matrices is formed by adding corresponding entries:

$$
(A+B)_{ij}=a_{ij}+b_{ij}.
$$

This requires that for every position $(i,j)$ in $A$ there is an entry $b_{ij}$ in the same position of $B$. If $A$ and $B$ have different sizes, some entries have no partner. For example, if $A$ is $2\times 2$ and $B$ is $2\times 3$, then the entry $b_{23}$ has no corresponding entry $a_{23}$ in $A$, so the sum is not defined. Hence $A+B$ and $A-B$ exist only when $A$ and $B$ have the same number of rows and the same number of columns.

**Answer.**

$$
A+B=
\begin{pmatrix}
5 & 0 \\
-1 & 8 \\
\end{pmatrix},\qquad A-B=
\begin{pmatrix}
-3 & 4 \\
-1 & -2 \\
\end{pmatrix},\qquad 3A-2B=
\begin{pmatrix}
-5 & 10 \\
-3 & -1 \\
\end{pmatrix}.
$$