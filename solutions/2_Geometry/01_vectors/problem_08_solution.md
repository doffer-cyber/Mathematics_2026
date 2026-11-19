### Exercise 8. Linear Combination and Checking the Result

Check whether $w=(5,1)$ can be written as

$$
w=au+bv,
$$

where $u=(1,1)$ and $v=(2,-1)$. If so, find $a,b$, reconstruct $w$ from them, and explain the geometric meaning of the existence of such coefficients.

> **Why this exercise:** connects linear combinations with the geometry of directions.

#### Solution

Substitute the given vectors into $w=au+bv$:

$$
(5,1)=a(1,1)+b(2,-1)=(a+2b,\,a-b).
$$

Equating components yields the linear system

$$
\begin{cases}
a+2b=5, \\
a-b=1.
\end{cases}
$$

Subtracting the second equation from the first gives

$$
3b=4 \implies b=\frac{4}{3}.
$$

Substituting $b=\frac{4}{3}$ into $a-b=1$ gives

$$
a=1+\frac{4}{3}=\frac{7}{3}.
$$

Reconstructing $w$ from $a=\frac{7}{3}$ and $b=\frac{4}{3}$ confirms the result:

$$
\begin{aligned}
\frac{7}{3}(1,1)+\frac{4}{3}(2,-1) &= \left(\frac{7}{3}+\frac{8}{3},\,\frac{7}{3}-\frac{4}{3}\right) \\
                                    &= \left(\frac{15}{3},\,\frac{3}{3}\right) \\
                                    &= (5,1).
\end{aligned}
$$

**Geometric meaning:** Because $u$ and $v$ are not scalar multiples of one another, they point along two non-collinear directions in $\mathbb{R}^2$ and therefore span the entire plane. The existence of unique scalars $a=\frac{7}{3}$ and $b=\frac{4}{3}$ means that the target point $(5,1)$ can be reached from the origin by scaling $u$ by $\frac{7}{3}$, scaling $v$ by $\frac{4}{3}$, and adding the resulting vectors via the parallelogram rule.

---