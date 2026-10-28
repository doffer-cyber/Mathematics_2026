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

---

#### Solution

**Initial augmented matrix**

$$
[A\mid I]=
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
3 & 5 & \mid & 0 & 1 \\
\end{pmatrix}.
$$

**Step 1.** Replace $R_2$ by $R_2 - 3R_1$:

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & -1 & \mid & -3 & 1 \\
\end{pmatrix}.
$$

**Step 2.** Replace $R_2$ by $-R_2$:

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}.
$$

**Step 3.** Replace $R_1$ by $R_1 - 2R_2$:

$$
\begin{pmatrix}
1 & 0 & \mid & -5 & 2 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}.
$$

The left block is now $I$, so the right block is $A^{-1}$:

$$
A^{-1}=
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}.
$$

**Why this works**

Each elementary row operation is multiplication from the left by an invertible elementary matrix $E_k$. After all the steps, the augmented matrix is

$$
E_3E_2E_1\,[A\mid I]=[E_3E_2E_1A\mid E_3E_2E_1].
$$

Denote $E=E_3E_2E_1$. The operations were chosen so that the left block becomes the identity:

$$
EA=I.
$$

Hence $E$ is a left inverse of the square matrix $A$, so $E=A^{-1}$. The right block started as $I$ and was multiplied by the same matrices, so it equals $EI=E=A^{-1}$.

**Check**

$$
\begin{aligned}
AA^{-1} &=
\begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}