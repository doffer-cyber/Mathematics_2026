### Exercise 8. Two Systems with the Same Coefficient Matrix

Solve by elimination the two systems

$$
\begin{cases}
2x+y=5, \\
x-y=1,
\end{cases}
$$

$$
\begin{cases}
2x+y=1, \\
x-y=4.
\end{cases}
$$

Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?

> **Why this exercise:** shows the role of the coefficient matrix independently of the right-hand side.

**Solution**

Both systems have the same coefficient matrix

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & -1 \\
\end{pmatrix}
$$

and differ only in the right-hand side vector.

**System 1**

**Step 1. Augmented matrix**

$$
\begin{pmatrix}
2 & 1 & \mid & 5 \\
1 & -1 & \mid & 1 \\
\end{pmatrix}
$$

**Step 2. Swap rows 1 and 2**

Apply $R_1 \leftrightarrow R_2$ to obtain a pivot equal to $1$:

$$
\begin{pmatrix}
1 & -1 & \mid & 1 \\
2 & 1 & \mid & 5 \\
\end{pmatrix}
$$

**Step 3. Eliminate $x$ from row 2**

Apply $R_2 \to R_2-2R_1$:

$$
\begin{pmatrix}
1 & -1 & \mid & 1 \\
0 & 3 & \mid & 3 \\
\end{pmatrix}
$$

**Step 4. Back substitution**

From row 2:

$$
3y=3 \quad\Rightarrow\quad y=1
$$

From row 1:

$$
x-y=1 \quad\Rightarrow\quad x=1+1=2
$$

The solution is

$$
(x,\,y)=(2,\,1)
$$

**System 2**

**Step 1. Augmented matrix**

$$
\begin{pmatrix}
2 & 1 & \mid & 1 \\
1 & -1 & \mid & 4 \\
\end{pmatrix}
$$

**Step 2. Swap rows 1 and 2**

Apply $R_1 \leftrightarrow R_2$:

$$
\begin{pmatrix}
1 & -1 & \mid & 4 \\
2 & 1 & \mid & 1 \\
\end{pmatrix}
$$

**Step 3. Eliminate $x$ from row 2**

Apply $R_2 \to R_2-2R_1$:

$$
\begin{pmatrix}
1 & -1 & \mid & 4 \\
0 & 3 & \mid & -7 \\
\end{pmatrix}
$$

**Step 4. Back substitution**

From row 2:

$$
3y=-7 \quad\Rightarrow\quad y=-\frac{7}{3}
$$

From row 1:

$$
x=4+y=4-\frac{7}{3}=\frac{5}{3}
$$

The solution is

$$
(x,\,y)=\left(\frac{5}{3},\,-\frac{7}{3}\right)
$$

**Check**

System 1, $(2,\,1)$:

- Equation 1: $2\cdot 2+1=5$.
- Equation 2: $2-1=1$.

System 2, $\left(\frac{5}{3},\,-\frac{7}{3}\right)$:

- Equation 1: $2\cdot\frac{5}{3}-\frac{7}{3}=\frac{10}{3}-\frac{7}{3}=1$.
- Equation 2: $\frac{5}{3}+\frac{7}{3}=\frac{12}{3}=4$.

**Comparison of the elimination steps**

The sequence of row operations is identical in both systems:

$$
R_1 \leftrightarrow R_2, \qquad R_2 \to R_2-2R_1
$$

The coefficient part of the matrix is also identical after every step:

$$
\begin{pmatrix}
2 & 1 \\
1 & -1 \\
\end{pmatrix}
\quad\to\quad
\begin{pmatrix}
1 & -1 \\
2 & 1 \\
\end{pmatrix}
\quad\to\quad
\begin{pmatrix}
1 & -1 \\
0 & 3 \\
\end{pmatrix}
$$

Only the last column differs:

- System 1: $(5,\,1) \to (1,\,5) \to (1,\,3)$.
- System 2: $(1,\,4) \to (4,\,1) \to (4,\,-7)$.

**Why the elimination is the same**

The choice of row operations depends only on the entries of the coefficient matrix $A$: where the pivots are and which multiples must be subtracted. The right-hand side is only carried along and transformed by the same operations. It never influences which operation is chosen.

This allows both systems to be solved in one computation, by writing both right-hand sides as columns of one augmented matrix:

$$
\begin{pmatrix}
2 & 1 & \mid & 5 & 1 \\
1 & -1 & \mid & 1 & 4 \\
\end{pmatrix}
$$

After $R_1 \leftrightarrow R_2$ and $R_2 \to R_2-2R_1$ it becomes

$$
\begin{pmatrix}
1 & -1 & \mid & 1 & 4 \\
0 & 3 & \mid & 3 & -7 \\
\end{pmatrix}
$$

Back substitution is then performed once for each of the two right-hand side columns.

Since $\det A=2\cdot(-1)-1\cdot 1=-3\neq 0$, the matrix $A$ is invertible. Therefore both systems have exactly one solution, whatever the right-hand side is.