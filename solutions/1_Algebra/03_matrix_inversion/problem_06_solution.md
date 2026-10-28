### Exercise 5. A 3×3 Matrix
Use Gauss–Jordan elimination to find the inverse of

$$
A=
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix}.
$$

Check the result by multiplication.

> **Why this exercise:** provides necessary practice with the full method in a situation where the $2\times2$ formula no longer applies.

---

#### Solution

**Initial augmented matrix**

$$
[A\mid I]=
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
1 & 0 & 1 & \mid & 0 & 0 & 1 \\
\end{pmatrix}.
$$

**Step 1.** Replace $R_3$ by $R_3 - R_1$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & -1 & 1 & \mid & -1 & 0 & 1 \\
\end{pmatrix}.
$$

**Step 2.** Replace $R_3$ by $R_3 + R_2$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & 0 & 2 & \mid & -1 & 1 & 1 \\
\end{pmatrix}.
$$

**Step 3.** Replace $R_3$ by $\frac{1}{2}R_3$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & 0 & 1 & \mid & -\dfrac{1}{2} & \dfrac{1}{2} & \dfrac{1}{2} \\
\end{pmatrix}.
$$

**Step 4.** Replace $R_2$ by $R_2 - R_3$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 0 & \mid & \dfrac{1}{2} & \dfrac{1}{2} & -\dfrac{1}{2} \\
0 & 0 & 1 & \mid & -\dfrac{1}{2} & \dfrac{1}{2} & \dfrac{1}{2} \\
\end{pmatrix}.
$$

**Step 5.** Replace $R_1$ by $R_1 - R_2$:

$$
\begin{pmatrix}
1 & 0 & 0 & \mid & \dfrac{1}{2} & -\dfrac{1}{2} & \dfrac{1}{2} \\
0 & 1 & 0 & \mid & \dfrac{1}{2} & \dfrac{1}{2} & -\dfrac{1}{2} \\
0 & 0 & 1 & \mid & -\dfrac{1}{2} & \dfrac{1}{2} & \dfrac{1}{2} \\
\end{pmatrix}.
$$

The left block is now $I$, so the right block is the inverse:

$$
A^{-1}=\frac{1}{2}
\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix}.
$$

**Check by multiplication**

$$
\begin{aligned}
AA^{-1} &= \frac{1}{2}
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix} \\
&= \frac{1}{2}
\begin{pmatrix}
1+1+0 & -1+1+0 & 1-1+0 \\
0+1-1 & 0+1+1 & 0-1+1 \\
1+0-1 & -1+0+1 & 1+0+1 \\
\end{pmatrix} \\
&= \frac{1}{2}
\begin{pmatrix}
2 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 2 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}.
\end{aligned}
$$

Since $AA^{-1}=I$ for a square matrix, the computed matrix is the inverse of $A$.

**Answer:**

$$
A^{-1}=\frac{1}{2}
\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix}.
$$