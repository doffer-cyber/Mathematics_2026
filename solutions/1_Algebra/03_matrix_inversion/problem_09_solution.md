### Exercise 9. Matrix Equation
Given

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}.
$$

Solve the equation $AX=B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be used. Then check the result by computing $AX$.

> **Why this exercise:** teaches that order matters in matrix equations and must guide the solution.

---

#### Solution

**Choice of side**

In the equation $AX=B$, the matrix $A$ stands to the left of $X$. To cancel it, $A^{-1}$ must be multiplied from the left on both sides:

$$
\begin{aligned}
A^{-1}(AX) &= A^{-1}B \\
(A^{-1}A)X &= A^{-1}B \\
IX &= A^{-1}B \\
X &= A^{-1}B.
\end{aligned}
$$

Multiplying from the right would give $AXA^{-1}=BA^{-1}$, in which $A$ and $A^{-1}$ are separated by $X$ and do not cancel. In general $A^{-1}B\neq BA^{-1}$, so the side matters.

**Inverse of $A$**

$$
\begin{aligned}
\det A &= 1\cdot 1 - 2\cdot 0 \\
       &= 1.
\end{aligned}
$$

Hence $A$ is invertible, and by the formula for a $2\times2$ matrix,

$$
A^{-1}=
\begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}.
$$

**Computation of $X$**

$$
\begin{aligned}
X &= A^{-1}B \\
  &=
\begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix} \\
  &=
\begin{pmatrix}
1\cdot 3 + (-2)\cdot 2 & 1\cdot 1 + (-2)\cdot 4 \\
0\cdot 3 + 1\cdot 2 & 0\cdot 1 + 1\cdot 4 \\
\end{pmatrix} \\
  &=
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}.
\end{aligned}
$$

**Check**

$$
\begin{aligned}
AX &=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1\cdot(-1) + 2\cdot 2 & 1\cdot(-7) + 2\cdot 4 \\
0\cdot(-1) + 1\cdot 2 & 0\cdot(-7) + 1\cdot 4 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix} \\
&= B.
\end{aligned}
$$

The equation is satisfied.

**Answer:**

$$
X=
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}.
$$