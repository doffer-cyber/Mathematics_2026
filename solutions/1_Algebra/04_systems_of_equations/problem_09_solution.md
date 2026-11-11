### Exercise 9. A System from a Sum Condition

Find numbers $x,y$ satisfying

$$
x+y=10,\qquad 2x+5y=32.
$$

Solve the system and explain geometrically why the solution is unique.

> **Why this exercise:** reinforces the transition from two linear conditions to the intersection point of two lines.

**Solution**

**Step 1. System and augmented matrix**

The conditions form the system

$$
\begin{cases}
x+y=10, \\
2x+5y=32.
\end{cases}
$$

Its augmented matrix is

$$
\begin{pmatrix}
1 & 1 & \mid & 10 \\
2 & 5 & \mid & 32 \\
\end{pmatrix}
$$

**Step 2. Eliminate $x$ from row 2**

Apply $R_2 \to R_2-2R_1$:

$$
\begin{pmatrix}
1 & 1 & \mid & 10 \\
0 & 3 & \mid & 12 \\
\end{pmatrix}
$$

**Step 3. Back substitution**

From row 2:

$$
3y=12 \quad\Rightarrow\quad y=4
$$

From row 1:

$$
x+y=10 \quad\Rightarrow\quad x=10-4=6
$$

The solution is

$$
(x,\,y)=(6,\,4)
$$

**Step 4. Check**

- Equation 1: $6+4=10$.
- Equation 2: $2\cdot 6+5\cdot 4=12+20=32$.

Both equations are satisfied.

**Geometric interpretation**

Each equation describes a line in the plane. Solving for $y$ gives

$$
y=10-x \qquad\mbox{and}\qquad y=\frac{32-2x}{5}
$$

The first line has slope $-1$ and the second has slope $-\frac{2}{5}$. The slopes are different, so the lines are not parallel and not identical. Two lines in the plane with different slopes intersect in exactly one point. That point is $(6,\,4)$, so the solution is unique.

The same conclusion follows from the coefficient matrix

$$
A=
\begin{pmatrix}
1 & 1 \\
2 & 5 \\
\end{pmatrix}
$$

whose determinant is

$$
\det A = 1\cdot 5-1\cdot 2 = 3
$$

Since $\det A\neq 0$, the rows of $A$ are not proportional. The two lines have different directions, and the system has exactly one solution for any right-hand side.