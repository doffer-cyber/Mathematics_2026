### Exercise 7. Using Properties Instead of Recomputing
Suppose that for a $3\times3$ matrix, $\det A=-4$. Compute

$$
\det(2A),\qquad \det(A^T),\qquad \det(A^2),\qquad \det(-A).
$$

Justify each answer using the appropriate property.

> **Why this exercise:** teaches how to use determinant properties instead of repeating a full calculation.

---

#### Solution

**Properties used**

For an $n\times n$ matrix $A$ and a scalar $c$:

- $\det(cA)=c^n\det A$, because each of the $n$ rows is multiplied by $c$.
- $\det(A^T)=\det A$.
- $\det(AB)=\det A\cdot\det B$.

Here $n=3$ and $\det A=-4$.

**Computation of $\det(2A)$**

Multiplying all three rows by $2$ multiplies the determinant by $2^3$:

$$
\begin{aligned}
\det(2A) &= 2^3\det A \\
         &= 8\cdot(-4) \\
         &= -32.
\end{aligned}
$$

**Computation of $\det(A^T)$**

A matrix and its transpose have the same determinant:

$$
\begin{aligned}
\det(A^T) &= \det A \\
          &= -4.
\end{aligned}
$$

**Computation of $\det(A^2)$**

By multiplicativity of the determinant:

$$
\begin{aligned}
\det(A^2) &= \det(A\cdot A) \\
          &= \det A\cdot\det A \\
          &= (-4)^2 \\
          &= 16.
\end{aligned}
$$

**Computation of $\det(-A)$**

This is the case $c=-1$ with $n=3$:

$$
\begin{aligned}
\det(-A) &= (-1)^3\det A \\
         &= -(-4) \\
         &= 4.
\end{aligned}
$$

**Answer:**

$$
\det(2A)=-32,\qquad \det(A^T)=-4,\qquad \det(A^2)=16,\qquad \det(-A)=4.
$$