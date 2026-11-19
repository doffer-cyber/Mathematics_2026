### Exercise 15. Complete Classification of a Line Relative to a Plane

Let

$$
L:p+tv,\qquad \Pi:n\cdot x=d.
$$

State the conditions distinguishing the three cases: one intersection point, parallel with no common points, and the line contained in the plane. Then illustrate each case with your own simple numerical example.

> **Why this exercise:** requires formulating a general mathematical criterion instead of carrying out one isolated calculation.

#### Solution

Substituting $x = p + tv$ into $n \cdot x = d$ yields the linear equation in $t$:

$$
(n \cdot v)t = d - n \cdot p
$$

Assuming $v \neq 0$ and $n \neq 0$, the three geometric cases are completely classified by the scalars $n \cdot v$ and $d - n \cdot p$:

1. **One intersection point:** $n \cdot v \neq 0$. The direction vector is not orthogonal to the plane's normal, yielding the unique parameter $t = \frac{d - n \cdot p}{n \cdot v}$.
2. **Parallel with no common points:** $n \cdot v = 0$ and $n \cdot p \neq d$. The line is orthogonal to the normal vector, but its base point $p$ does not satisfy the plane equation ($0 \cdot t = d - n \cdot p \neq 0$, no solution).
3. **Line contained in the plane:** $n \cdot v = 0$ and $n \cdot p = d$. The line is orthogonal to the normal vector and passes through a point $p$ on the plane ($0 \cdot t = 0$, satisfied for all $t \in \mathbb{R}$).

**Numerical Examples**

Let the plane be $\Pi: z = 0$, where $n = (0, 0, 1)$ and $d = 0$.

* **Case 1 (One intersection point):** Let $L_1: (0, 0, 1) + t(0, 0, 1)$. Here $n \cdot v = 1 \neq 0$, and $L_1$ intersects $\Pi$ at $(0, 0, 0)$ for $t = -1$.
* **Case 2 (Strictly parallel):** Let $L_2: (0, 0, 1) + t(1, 0, 0)$. Here $n \cdot v = 0$ while $n \cdot p = 1 \neq 0$, so $L_2$ is parallel to $\Pi$ with no intersection.
* **Case 3 (Contained in the plane):** Let $L_3: (0, 0, 0) + t(1, 0, 0)$. Here $n \cdot v = 0$ and $n \cdot p = 0 = d$, so $L_3$ lies entirely inside $\Pi$