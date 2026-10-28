### Exercise 6. Parameter and Invertibility
For

$$
A(t)=
\begin{pmatrix}
t & 1 \\
2 & t \\
\end{pmatrix}
$$

find all values of $t$ for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

> **Why this exercise:** shows how the determinant can be used to study a family of matrices depending on a parameter.

---

#### Solution

**Determinant as a function of $t$**

$$
\begin{aligned}
\det A(t) &= t\cdot t - 1\cdot 2 \\
          &= t^2 - 2.
\end{aligned}
$$

**Condition for non-invertibility**

A square matrix is not invertible if and only if its determinant equals zero. Hence $A(t)$ is not invertible exactly when

$$
t^2 - 2 = 0.
$$

Solving this equation gives

$$
t = \sqrt{2}
\qquad\text{or}\qquad
t = -\sqrt{2}.
$$

**Relation to the determinant**

For every $t$ with $t\neq\pm\sqrt{2}$ we have $\det A(t)=t^2-2\neq 0$, so $A(t)$ is invertible. For $t=\pm\sqrt{2}$ the determinant vanishes, so $A(t)$ is not invertible.

This can also be seen from the rows. For $t=\sqrt{2}$ the matrix is

$$
A(\sqrt{2})=
\begin{pmatrix}
\sqrt{2} & 1 \\
2 & \sqrt{2} \\
\end{pmatrix},
$$

and the second row equals $\sqrt{2}$ times the first row, because $\sqrt{2}\cdot\sqrt{2}=2$ and $\sqrt{2}\cdot 1=\sqrt{2}$. Hence the rows are linearly dependent. For $t=-\sqrt{2}$ the second row equals $-\sqrt{2}$ times the first row, with the same conclusion.

**Answer:** $A(t)$ is not invertible if and only if $t=\sqrt{2}$ or $t=-\sqrt{2}$, that is, exactly when $\det A(t)=t^2-2=0$.