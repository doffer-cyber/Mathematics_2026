### Exercise 1. From a System to a Matrix

Write the system

$$
\begin{cases}
2x-y+z=4, \\
x+3y-2z=1, \\
3x+y+z=7.
\end{cases}
$$

in the form $A\mathbf{x}=\mathbf{b}$.
Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

> **Why this exercise:** teaches how to move between a system of equations and matrix notation.

**Solution**

The coefficients of $x$, $y$, $z$ in each equation form one row of the coefficient matrix:

$$
A=
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1 \\
\end{pmatrix}
$$

The vector of unknowns is

$$
\mathbf{x}=
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
$$

and the right-hand side vector is

$$
\mathbf{b}=
\begin{pmatrix}
4 \\
1 \\
7 \\
\end{pmatrix}
$$

Hence the system is written as

$$
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
=
\begin{pmatrix}
4 \\
1 \\
7 \\
\end{pmatrix}
$$

**Row–equation correspondence**

Multiplying $A$ by $\mathbf{x}$ gives

$$
A\mathbf{x}=
\begin{pmatrix}
2x-y+z \\
x+3y-2z \\
3x+y+z \\
\end{pmatrix}
$$

so each entry of $A\mathbf{x}$ is the product of one row of $A$ with the vector $\mathbf{x}$.
The condition $A\mathbf{x}=\mathbf{b}$ means that these entries equal the corresponding entries of $\mathbf{b}$:

- Row 1, $(2,\,-1,\,1)$, gives the first equation $2x-y+z=4$.
- Row 2, $(1,\,3,\,-2)$, gives the second equation $x+3y-2z=1$.
- Row 3, $(3,\,1,\,1)$, gives the third equation $3x+y+z=7$.

In general, row $i$ of $A$ contains the coefficients of the $i$-th equation, and the $i$-th entry of $\mathbf{b}$ is its right-hand side.