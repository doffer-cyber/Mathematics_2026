### Exercise 4. Infinitely Many Solutions

Solve

$$
\begin{cases}
x+y+z=2, \\
2x+2y+2z=4, \\
x-y+z=0.
\end{cases}
$$

Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

> **Why this exercise:** shows the case of multiple solutions and teaches a simple parametric description.

**Solution**

**Step 1. Augmented matrix**

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
2 & 2 & 2 & \mid & 4 \\
1 & -1 & 1 & \mid & 0 \\
\end{pmatrix}
$$

**Step 2. Eliminate $x$ from rows 2 and 3**

Apply $R_2 \to R_2-2R_1$ and $R_3 \to R_3-R_1$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
0 & 0 & 0 & \mid & 0 \\
0 & -2 & 0 & \mid & -2 \\
\end{pmatrix}
$$

The second row represents $0=0$. The second equation is twice the first, so it is redundant.

**Step 3. Swap rows 2 and 3 and normalize**

Apply $R_2 \leftrightarrow R_3$ and then $R_2 \to -\tfrac{1}{2}R_2$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
0 & 1 & 0 & \mid & 1 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

The matrix has two pivots (in the columns of $x$ and $y$) and three unknowns. The system is consistent, so it has infinitely many solutions.

**Step 4. Free variable**

The column of $z$ has no pivot, so $z$ is a free variable. Set $z=t$, where $t\in\mathbb{R}$.

**Step 5. Back substitution**

From row 2:

$$
y=1
$$

From row 1:

$$
x+y+z=2 \quad\Rightarrow\quad x=2-1-t=1-t
$$

**Parametric form of the solution**

$$
x=1-t, \qquad y=1, \qquad z=t, \qquad t\in\mathbb{R}
$$

In vector form:

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}=
\begin{pmatrix}
1 \\
1 \\
0 \\
\end{pmatrix}+t
\begin{pmatrix}
-1 \\
0 \\
1 \\
\end{pmatrix}
$$

The solution set is a line in $\mathbb{R}^3$ passing through $(1,\,1,\,0)$ with direction vector $(-1,\,0,\,1)$.

**Step 6. Check for a chosen parameter value**

Choose $t=2$. Then

$$
(x,\,y,\,z)=(-1,\,1,\,2)
$$

Substituting into the original equations:

- Equation 1: $-1+1+2=2$.
- Equation 2: $2\cdot(-1)+2\cdot 1+2\cdot 2=-2+2+4=4$.
- Equation 3: $-1-1+2=0$.

All three equations are satisfied, so the point lies in the solution set.