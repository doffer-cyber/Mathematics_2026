### Exercise 4. Gauss–Jordan

Find $A^{-1}$ using the Gauss–Jordan method for

$$
A=
\begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}.
$$

Show the augmented matrix $[A\mid I]$ after successive operations and explain why obtaining $I$ on the left gives the inverse on the right.

> **Why this exercise:** introduces the Gauss–Jordan method together with its meaning, not merely as a sequence of operations.

**Solution**

**Initial augmented matrix**

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
3 & 5 & \mid & 0 & 1 \\
\end{pmatrix}
$$

**Step 1.** Eliminate the entry below the first pivot with $R_2 \to R_2 - 3R_1$.

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & -1 & \mid & -3 & 1 \\
\end{pmatrix}
$$

**Step 2.** Normalize the second pivot with $R_2 \to -R_2$.

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}
$$

**Step 3.** Eliminate the entry above the second pivot with $R_1 \to R_1 - 2R_2$.

$$
\begin{pmatrix}
1 & 0 & \mid & -5 & 2 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}
$$

The left block is $I$, therefore

$$
A^{-1}=
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}.
$$

**Verification**

$$
AA^{-1}=
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
\end{pmatrix}
$$

**Why the right block becomes $A^{-1}$**

Each row operation is multiplication on the left by an elementary matrix $E_i$. Applying all steps to the augmented matrix $[A\mid I]$ gives

$$
\begin{aligned}
E_3E_2E_1\,[A\mid I] &= [E_3E_2E_1A \mid E_3E_2E_1I] \\
                     &= [I \mid E_3E_2E_1].
\end{aligned}
$$

The left block shows $E_3E_2E_1A=I$, so the matrix $E_3E_2E_1$ is a left inverse of $A$. For square matrices a left inverse is the inverse, so $E_3E_2E_1=A^{-1}$. The right block started as $I$ and received exactly the same operations, so it equals $E_3E_2E_1I=A^{-1}$.

The same operations that reduce $A$ to $I$ therefore build $A^{-1}$ on the right.