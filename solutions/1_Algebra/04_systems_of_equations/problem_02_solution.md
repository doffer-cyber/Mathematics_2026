### Exercise 2. Gaussian Elimination — One Solution

Solve using Gaussian elimination:

$$
\begin{cases}
x+y+z=6, \\
2x-y+z=3, \\
x+2y-z=2.
\end{cases}
$$

After solving, substitute the result into all equations and check consistency.

> **Why this exercise:** introduces the basic method for solving a system and builds the habit of checking the result.

**Solution**

**Step 1. Augmented matrix**

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
2 & -1 & 1 & \mid & 3 \\
1 & 2 & -1 & \mid & 2 \\
\end{pmatrix}
$$

**Step 2. Eliminate $x$ from rows 2 and 3**

Apply $R_2 \to R_2-2R_1$ and $R_3 \to R_3-R_1$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & -3 & -1 & \mid & -9 \\
0 & 1 & -2 & \mid & -4 \\
\end{pmatrix}
$$

**Step 3. Swap rows 2 and 3**

Apply $R_2 \leftrightarrow R_3$ to obtain a simpler pivot:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & 1 & -2 & \mid & -4 \\
0 & -3 & -1 & \mid & -9 \\
\end{pmatrix}
$$

**Step 4. Eliminate $y$ from row 3**

Apply $R_3 \to R_3+3R_2$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & 1 & -2 & \mid & -4 \\
0 & 0 & -7 & \mid & -21 \\
\end{pmatrix}
$$

The matrix is now in row echelon form. It has three pivots, so the system has exactly one solution.

**Step 5. Back substitution**

From row 3:

$$
-7z=-21 \quad\Rightarrow\quad z=3
$$

From row 2:

$$
y-2z=-4 \quad\Rightarrow\quad y=-4+6=2
$$

From row 1:

$$
x+y+z=6 \quad\Rightarrow\quad x=6-2-3=1
$$

Hence the solution is

$$
(x,\,y,\,z)=(1,\,2,\,3)
$$

**Step 6. Check in all original equations**

- Equation 1: $1+2+3=6$.
- Equation 2: $2\cdot 1-2+3=3$.
- Equation 3: $1+2\cdot 2-3=2$.

All three equations are satisfied, so the system is consistent and $(1,\,2,\,3)$ is its unique solution.