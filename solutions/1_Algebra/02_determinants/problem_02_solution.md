### Exercise 2. Determinant of a 3×3 Matrix
For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5 \\
\end{pmatrix}
$$

compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

> **Why this exercise:** teaches a basic method for $3\times3$ matrices and builds the habit of checking the result without adding a second full solution.

---

#### Solution

**Sarrus' rule**

For a $3\times3$ matrix with entries $a_{ij}$, the determinant is $\det A = P - N$, where $P$ is the sum of the products along the three diagonals going down to the right, and $N$ is the sum of the products along the three diagonals going down to the left.

**Products along the main diagonals**

$$
\begin{aligned}
P &= 1\cdot 3\cdot 5 + 2\cdot 4\cdot 2 + (-1)\cdot 0\cdot 1 \\
  &= 15 + 16 + 0 \\
  &= 31.
\end{aligned}
$$

**Products along the anti-diagonals**

$$
\begin{aligned}
N &= (-1)\cdot 3\cdot 2 + 1\cdot 4\cdot 1 + 2\cdot 0\cdot 5 \\
  &= -6 + 4 + 0 \\
  &= -2.
\end{aligned}
$$

**Determinant**

$$
\begin{aligned}
\det A &= P - N \\
       &= 31 - (-2) \\
       &= 33.
\end{aligned}
$$

**Check using a property of the determinant**

Adding a multiple of one row to another row does not change the determinant. Replace the third row $R_3$ by $R_3 - 2R_1$:

$$
A