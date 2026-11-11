### Exercise 10. A Polynomial Through Three Points

Find a polynomial $p(x)=ax^2+bx+c$ whose graph passes through $(0,1)$, $(1,3)$, and $(2,9)$. Reduce the problem to a system of equations and check the result by substituting all three points.

> **Why this exercise:** shows that finding unknown coefficients can be reduced to solving a linear system.

**Solution**

**Step 1. Conditions on the coefficients**

The graph passes through a point $(x_0,\,y_0)$ exactly when $p(x_0)=y_0$. The unknowns are $a$, $b$, $c$.

For $(0,1)$:

$$
p(0)=c=1
$$

For $(1,3)$:

$$
p(1)=a+b+c=3
$$

For $(2,9)$:

$$
p(2)=4a+2b+c=9
$$

**Step 2. System of equations**

$$
\begin{cases}
a+b+c=3, \\
4a+2b+c=9, \\
c=1.
\end{cases}
$$

**Step 3. Augmented matrix**

The columns correspond to $a$, $b$, $c$ and the right-hand side:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 3 \\
4 & 2 & 1 & \mid & 9 \\
0 & 0 & 1 & \mid & 1 \\
\end{pmatrix}
$$

**Step 4. Eliminate $a$ from row 2**

Apply $R_2 \to R_2-4R_1$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 3 \\
0 & -2 & -3 & \mid & -3 \\
0 & 0 & 1 & \mid & 1 \\
\end{pmatrix}
$$

**Step 5. Normalize row 2**

Apply $R_2 \to -\tfrac{1}{2}R_2$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 3 \\
0 & 1 & \frac{3}{2} & \mid & \frac{3}{2} \\
0 & 0 & 1 & \mid & 1 \\
\end{pmatrix}
$$

The matrix is in row echelon form with three pivots, so the system has exactly one solution.

**Step 6. Back substitution**

From row 3:

$$
c=1
$$

From row 2:

$$
b=\frac{3}{2}-\frac{3}{2}c=\frac{3}{2}-\frac{3}{2}=0
$$

From row 1:

$$
a=3-b-c=3-0-1=2
$$

Hence

$$
p(x)=2x^2+1
$$

**Step 7. Check**

- $p(0)=2\cdot 0^2+1=1$.
- $p(1)=2\cdot 1^2+1=3$.
- $p(2)=2\cdot 2^2+1=8+1=9$.

All three points lie on the graph of $p$.

**Uniqueness**

The system has a unique solution, so $p(x)=2x^2+1$ is the only polynomial of the form $ax^2+bx+c$ passing through these three points.