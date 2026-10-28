### Exercise 8. Determinant of a Product
Let $A,B$ be square matrices such that $\det A=3$ and $\det B=-5$. Compute $\det(AB)$, $\det(BA)$ and, if it exists, $\det(A^{-1}B)$. Explain why the first two results are equal even though usually $AB\neq BA$.

> **Why this exercise:** organizes how determinants behave with respect to products and inverses.

---

#### Solution

**Properties used**

For square matrices $A,B$ of the same size:

- $\det(AB)=\det A\cdot\det B$.
- If $\det A\neq 0$, then $A$ is invertible and $\det(A^{-1})=\dfrac{1}{\det A}$.

**Computation of $\det(AB)$**

$$
\begin{aligned}
\det(AB) &= \det A\cdot\det B \\
         &= 3\cdot(-5) \\
         &= -15.
\end{aligned}
$$

**Computation of $\det(BA)$**

$$
\begin{aligned}
\det(BA) &= \det B\cdot\det A \\
         &= (-5)\cdot 3 \\
         &= -15.
\end{aligned}
$$

**Computation of $\det(A^{-1}B)$**

Since $\det A=3\neq 0$, the matrix $A$ is invertible, so $A^{-1}$ exists. Then

$$
\begin{aligned}
\det(A^{-1}B) &= \det(A^{-1})\cdot\det B \\
              &= \frac{1}{3}\cdot(-5) \\
              &= -\frac{5}{3}.
\end{aligned}
$$

**Why $\det(AB)=\det(BA)$ although usually $AB\neq BA$**

The matrices $AB$ and $BA$ are in general different. However, the determinant of each of them is the product of the two real numbers $\det A$ and $\det B$. Multiplication of real numbers is commutative, so

$$
\det A\cdot\det B = \det B\cdot\det A.
$$

Hence the determinant does not detect the difference between $AB$ and $BA$, even though the matrices themselves may differ.

**Answer:**

$$
\det(AB)=-15,\qquad \det(BA)=-15,\qquad \det(A^{-1}B)=-\frac{5}{3}.
$$