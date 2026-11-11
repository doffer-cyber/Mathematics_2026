### Exercise 7. Choosing a Method Deliberately

Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:

1. one system with a triangular coefficient matrix

$$
\begin{cases}
2x-y=3, \\
4y=8;
\end{cases}
$$

2. three systems $A\mathbf{x}=\mathbf{b}_i$ with the same invertible matrix $A$, when $A^{-1}$ is already known;
3. one $3\times 3$ system for which the inverse matrix is not given and the goal is only to find one solution vector.

For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone — refer to the number of right-hand sides and the structure of the matrix.

> **Why this exercise:** practices choosing a method based on the structure of the problem instead of solving another small system by two methods.

**Solution**

**Case 1. Triangular system**

**Choice of method:** back substitution.

The coefficient matrix is upper triangular:

$$
\begin{pmatrix}
2 & -1 & \mid & 3 \\
0 & 4 & \mid & 8 \\
\end{pmatrix}
$$

The elimination is already finished. The last equation contains only $y$, so each unknown can be found one at a time, starting from the bottom. Gaussian elimination or computing an inverse would only repeat work that the triangular structure has already done.

From row 2:

$$
4y=8 \quad\Rightarrow\quad y=2
$$

From row 1:

$$
2x-y=3 \quad\Rightarrow\quad 2x=3+2=5 \quad\Rightarrow\quad x=\frac{5}{2}
$$

The solution is

$$
(x,\,y)=\left(\frac{5}{2},\,2\right)
$$

Check:

- Equation 1: $2\cdot\frac{5}{2}-2=5-2=3$.
- Equation 2: $4\cdot 2=8$.

Both equations are satisfied. The pivots $2$ and $4$ are nonzero, so the solution is unique.

**Case 2. Three right-hand sides, $A^{-1}$ known**

**Choice of method:** multiplication by the known inverse.

The three systems share the same matrix $A$, and $A^{-1}$ is already available. The solutions are

$$
\mathbf{x}_i=A^{-1}\mathbf{b}_i, \qquad i=1,\,2,\,3
$$

**Plan:**

1. Use the given $A^{-1}$ without any further elimination.
2. Compute the three products $A^{-1}\mathbf{b}_1$, $A^{-1}\mathbf{b}_2$, $A^{-1}\mathbf{b}_3$. Equivalently, collect the right-hand sides as columns of one matrix

$$
B=
\begin{pmatrix}
\mathbf{b}_1 & \mathbf{b}_2 & \mathbf{b}_3 \\
\end{pmatrix}
$$

and compute $X=A^{-1}B$. The columns of $X$ are the three solutions.

**Reusable:** the matrix $A^{-1}$. It is computed once and serves every right-hand side, including any further ones added later.

**Unnecessary:** repeating Gaussian elimination on $(A \mid \mathbf{b}_i)$ for each $i$. That would redo the same row operations three times.

The deciding factors are that there are several right-hand sides and that the expensive part, the inverse, is already paid for.

**Case 3. One $3\times 3$ system, no inverse given, one solution vector wanted**

**Choice of method:** Gaussian elimination on the augmented matrix $(A \mid \mathbf{b})$, followed by back substitution.

**Plan:**

1. Write the augmented matrix $(A \mid \mathbf{b})$.
2. Use row operations to reach row echelon form (a triangular form if $A$ is invertible).
3. Solve by back substitution, starting from the last row.
4. Substitute the result into all original equations as a check.

**Reusable:** the elimination itself. If another right-hand side appears later, the same row operations can be applied to it, which is the idea behind an LU factorization.

**Unnecessary:** computing $A^{-1}$. Finding the inverse means reducing $(A \mid I)$, which is equivalent to solving three systems with the columns of $I$ as right-hand sides. For a single right-hand side this is several times more work than needed, and the inverse would then be used for only one product.

Elimination has an additional advantage. It also reveals whether the system is inconsistent or has infinitely many solutions, whereas an inverse exists only when $A$ is invertible.

**Summary**

| Case | Structure | Number of right-hand sides | Method |
|---|---|---|---|
| 1 | triangular matrix | 1 | back substitution |
| 2 | invertible $A$, $A^{-1}$ known | 3 | multiplication $A^{-1}\mathbf{b}_i$ |
| 3 | general $3\times 3$ matrix, no inverse | 1 | Gaussian elimination on $(A \mid \mathbf{b})$ |