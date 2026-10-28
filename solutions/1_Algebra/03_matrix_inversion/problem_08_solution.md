### Exercise 8. Inverse of a Transformation
The matrix

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & \frac12 \\
\end{pmatrix}
$$

describes a scaling of the plane. Find $S^{-1}$ and explain geometrically what the inverse transformation does. Check the action of the pair $S,S^{-1}$ on one simple vector.

> **Why this exercise:** gives the inverse the interpretation of undoing a transformation.

---

#### Solution

**Determinant**

$$
\begin{aligned}
\det S &= 2\cdot\frac{1}{2} - 0\cdot 0 \\
       &= 1.
\end{aligned}
$$

Since $\det S = 1\neq 0$, the matrix $S$ is invertible.

**Inverse**

By the formula for a $2\times2$ matrix,

$$
\begin{aligned}
S^{-1} &= \frac{1}{1}
\begin{pmatrix}
\dfrac{1}{2} & 0 \\
0 & 2 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
\dfrac{1}{2} & 0 \\
0 & 2 \\
\end{pmatrix}.
\end{aligned}
$$

The same result follows from the fact that the inverse of a diagonal matrix is obtained by inverting each diagonal entry.

**Geometric meaning**

The transformation $S$ stretches the plane by the factor $2$ in the $x$-direction and compresses it by the factor $\frac12$ in the $y$-direction. To undo this, the $x$-direction must be compressed by the factor $\frac12$ and the $y$-direction must be stretched by the factor $2$. This is exactly the action of $S^{-1}$. Note that $\det S = 1$, so $S$ preserves areas, and so does $S^{-1}$: the stretching and compression compensate each other.

**Check on a simple vector**

Take

$$
v=
\begin{pmatrix}
1 \\
1 \\
\end{pmatrix}.
$$

Applying $S$:

$$
\begin{aligned}
Sv &=
\begin{pmatrix}
2 & 0 \\
0 & \frac12 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
1 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
2 \\
\dfrac{1}{2} \\
\end{pmatrix}.
\end{aligned}
$$

Applying $S^{-1}$ to the result:

$$
\begin{aligned}
S^{-1}(Sv) &=
\begin{pmatrix}
\dfrac{1}{2} & 0 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
\dfrac{1}{2} \\
\end{pmatrix} \\
&=
\begin{pmatrix}
\dfrac{1}{2}\cdot 2 \\
2\cdot\dfrac{1}{2} \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1 \\
1 \\
\end{pmatrix} \\
&= v.
\end{aligned}
$$

The vector $v$ is returned to its original position, so $S^{-1}$ undoes $S$.

**Answer:**

$$
S^{-1}=
\begin{pmatrix}
\dfrac{1}{2} & 0 \\
0 & 2 \\
\end{pmatrix}.
$$