### Exercise 14. A System of Equations and the Determinant

Consider the system $Ax=b$, where

$$
A=
\begin{pmatrix}
1 & 2 \\
k & 4 \\
\end{pmatrix}.
$$

For which values of $k$ does the system have exactly one solution for every $b$? For the remaining value, give an example of a right-hand side $b$ for which the system has infinitely many solutions, and an example for which it has no solution.

> **Why this exercise:** connects the determinant with uniqueness of solutions and requires distinguishing the exceptional cases.

#### Solution

**Step 1. Compute the determinant.**

$$
\det A = 1\cdot 4-2\cdot k = 4-2k.
$$

**Step 2. Condition for a unique solution.**

The system $Ax=b$ has exactly one solution for every $b$ if and only if $A$ is invertible, that is, if and only if $\det A\neq 0$.

$$
4-2k=0 \iff k=2.
$$

Hence the system has exactly one solution for every $b$ if and only if $k\neq 2$.

**Step 3. The exceptional value $k=2$.**

For $k=2$ the matrix is

$$
A=
\begin{pmatrix}
1 & 2 \\
2 & 4 \\
\end{pmatrix}.
$$

The second row is twice the first row. Write $b=(b_1,b_2)^T$. The system is

$$
\begin{cases}
x_1+2x_2=b_1, \\
2x_1+4x_2=b_2.
\end{cases}
$$

Subtracting twice the first equation from the second equation gives

$$
0=b_2-2b_1.
$$

Therefore the system is consistent if and only if $b_2=2b_1$.

**Step 4. Example with infinitely many solutions.**

Take $b=(1,2)^T$, so that $b_2=2b_1$.

$$
\begin{cases}
x_1+2x_2=1, \\
2x_1+4x_2=2.
\end{cases}
$$

The second equation is twice the first one, so only one independent equation remains. Choose $x_2=s$ as a free parameter. Then $x_1=1-2s$, and

$$
\begin{pmatrix}
x_1 \\
x_2 \\
\end{pmatrix}=
\begin{pmatrix}
1-2s \\
s \\
\end{pmatrix},
\qquad s\in\mathbb{R}.
$$

This is a line of solutions, so there are infinitely many.

**Step 5. Example with no solution.**

Take $b=(1,3)^T$, so that $b_2\neq 2b_1$.

$$
\begin{cases}
x_1+2x_2=1, \\
2x_1+4x_2=3.
\end{cases}
$$

Subtracting twice the first equation from the second equation gives $0=1$, which is impossible. Hence the system has no solution.

**Step 6. Verification of the generic case.**

For $k\neq 2$ the inverse exists:

$$
A^{-1}=\frac{1}{4-2k}
\begin{pmatrix}
4 & -2 \\
-k & 1 \\
\end{pmatrix},
$$

so $x=A^{-1}b$ is the unique solution for every $b$.

**Answer.** The system has exactly one solution for every $b$ if and only if $k\neq 2$. For $k=2$ the system is consistent if and only if $b_2=2b_1$. For example, $b=(1,2)^T$ gives infinitely many solutions $(1-2s,\ s)^T$, and $b=(1,3)^T$ gives no solution.