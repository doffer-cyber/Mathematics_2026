### Exercise 3. Inconsistent System

Solve or show that the system is inconsistent:

$$
\begin{cases}
x+2y=3, \\
2x+4y=7.
\end{cases}
$$

Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

> **Why this exercise:** teaches how to recognize that a system has no solution without guessing.

**Solution**

**Step 1. Augmented matrix**

$$
\begin{pmatrix}
1 & 2 & \mid & 3 \\
2 & 4 & \mid & 7 \\
\end{pmatrix}
$$

**Step 2. Eliminate $x$ from row 2**

Apply $R_2 \to R_2-2R_1$:

$$
\begin{pmatrix}
1 & 2 & \mid & 3 \\
0 & 0 & \mid & 1 \\
\end{pmatrix}
$$

**Step 3. Interpret the last row**

The second row of the matrix represents the equation

$$
0\cdot x+0\cdot y=1
$$

that is,

$$
0=1
$$

This is impossible for any values of $x$ and $y$.

**Conclusion**

The system is inconsistent and has no solution.

**Interpretation in terms of equations**

The left side of the second equation is twice the left side of the first equation:

$$
2x+4y=2(x+2y)
$$

If the first equation holds, then $x+2y=3$, so

$$
2x+4y=2\cdot 3=6
$$

The second equation requires $2x+4y=7$, and $6\neq 7$. Hence the two equations contradict each other.

**Geometric interpretation**

Both equations describe lines in the plane. They have the same slope, so the lines are parallel. Their right-hand sides are not in the same ratio as the coefficients, so the lines are distinct and never intersect.