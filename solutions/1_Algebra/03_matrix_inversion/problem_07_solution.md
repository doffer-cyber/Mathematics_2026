### Exercise 7. Inverse of a Product
For

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix}
$$

compute $(AB)^{-1}$ and $B^{-1}A^{-1}$. Check that the results are the same and explain the meaning of the reversed order.

> **Why this exercise:** reinforces the inverse-of-a-product property and requires its interpretation.

**Solution**

**Step 1. The product $AB$**

$$
AB=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix}
=
\begin{pmatrix}
2 & 3 \\
0 & 3 \\
\end{pmatrix}
$$

**Step 2. The inverse $(AB)^{-1}$**

The determinant is

$$
\det(AB) = 2\cdot 3 - 3\cdot 0 = 6 \neq 0,
$$

so $AB$ is invertible. For a $2\times 2$ matrix, swap the diagonal entries, change the signs of the off-diagonal entries, and divide by the determinant:

$$
(AB)^{-1}=\frac{1}{6}
\begin{pmatrix}
3 & -3 \\
0 & 2 \\
\end{pmatrix}
=
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3} \\
\end{pmatrix}
$$

**Step 3. The inverses $A^{-1}$ and $B^{-1}$**

Since $\det A = 1$, and $B$ is diagonal:

$$
A^{-1}=
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix},\qquad
B^{-1}=
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & \frac{1}{3} \\
\end{pmatrix}
$$

**Step 4. The product $B^{-1}A^{-1}$**

$$
B^{-1}A^{-1}=
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & \frac{1}{3} \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
=
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3} \\
\end{pmatrix}
$$

**Step 5. Comparison**

Steps 2 and 4 give the same matrix, so

$$
(AB)^{-1}=B^{-1}A^{-1}.
$$

As a direct check:

$$
(AB)(B^{-1}A^{-1})=
\begin{pmatrix}
2 & 3 \\
0 & 3 \\
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3} \\
\end{pmatrix}
=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
$$

**Step 6. Meaning of the reversed order**

The matrix $AB$ applies $B$ first and then $A$. To undo this, the last operation must be undone first, so $A^{-1}$ is applied first and then $B^{-1}$. In algebraic form:

$$
(AB)(B^{-1}A^{-1}) = A(BB^{-1})A^{-1} = AA^{-1} = I.
$$

The factors $B$ and $B^{-1}$ meet in the middle and cancel, which only works in the reversed order. The product in the original order is different:

$$
A^{-1}B^{-1}=
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & \frac{1}{3} \\
\end{pmatrix}
=
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{3} \\
0 & \frac{1}{3} \\
\end{pmatrix}
\neq (AB)^{-1}.
$$

This shows that matrix multiplication is not commutative, so the order of the inverses matters.