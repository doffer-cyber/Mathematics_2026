### Exercise 4. Gauss–Jordan

**Solution.**

Form the augmented matrix $[A\mid I]$:

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
3 & 5 & \mid & 0 & 1 \\
\end{pmatrix}
$$

**Step 1.** Apply $R_2 \to R_2 - 3R_1$ to eliminate the entry below the first pivot:

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & -1 & \mid & -3 & 1 \\
\end{pmatrix}
$$

**Step 2.** Apply $R_2 \to -R_2$ to normalise the second pivot:

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}
$$

**Step 3.** Apply $R_1 \to R_1 - 2R_2$ to eliminate the entry above the second pivot:

$$
\begin{pmatrix}
1 & 0 & \mid & -5 & 2 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}
$$

The left block is now $I$, hence

$$
A^{-1}=
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}.
$$

**Why this works.**

Each elementary row operation is equivalent to left multiplication by an invertible elementary matrix $E_i$. The three steps above give

$$
E_3 E_2 E_1 A = I.
$$

Multiplying both sides on the right by $A^{-1}$ gives

$$
E_3 E_2 E_1 = A^{-1}.
$$

The same operations are applied to the right block, which starts as $I$, so it becomes

$$
E_3 E_2 E_1 I = A^{-1}.
$$

Therefore, when the left block is reduced to $I$, the right block is exactly $A^{-1}$.

**Verification.**

$$
A A^{-1}=
\begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}
=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}.
$$

Also $\det A = 1\cdot 5 - 2\cdot 3 = -1 \neq 0$, so $A$ is invertible.

> **Why this exercise:** introduces the Gauss–Jordan method together with its meaning, not merely as a sequence of operations.