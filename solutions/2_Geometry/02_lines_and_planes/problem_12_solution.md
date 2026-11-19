### Exercise 12. Intersection Line of Two Planes

Find a parametric equation of the line that is the intersection of

$$
x+y+z=3,\qquad x-y+z=1.
$$

Find its direction vector in two ways: from the system of equations and from the cross product of the normal vectors. Compare the results.

> **Why this exercise:** shows the equivalence of the algebraic and geometric approaches to constructing an intersection line.

#### Solution

**Method 1: Solving the system of equations**

Consider the system

$$
\begin{cases}
x + y + z = 3, \\
x - y + z = 1.
\end{cases}
$$

Subtracting the second equation from the first yields $2y = 2 \implies y = 1$. Substituting $y = 1$ into the first equation gives $x + 1 + z = 3 \implies x = 2 - z$. Letting $z = t \in \mathbb{R}$ be the free parameter:

$$
\begin{cases}
x = 2 - t, \\
y = 1, \\
z = t,
\end{cases}
\qquad t \in \mathbb{R}
$$

In vector parametric form:

$$
(x, y, z) = (2, 1, 0) + t(-1, 0, 1), \qquad t \in \mathbb{R}
$$

From this parameterization, a direction vector is $v_{\mathrm{alg}} = (-1, 0, 1)$.

**Method 2: Cross product of normal vectors**

The normal vectors of the two planes are $n_1 = (1, 1, 1)$ and $n_2 = (1, -1, 1)$. Since the intersection line lies in both planes, its direction is orthogonal to both $n_1$ and $n_2$:

$$
v_{\mathrm{geom}} = n_1 \times n_2 = (1, 1, 1) \times (1, -1, 1) = (1(1) - 1(-1),\; 1(1) - 1(1),\; 1(-1) - 1(1)) = (2, 0, -2)
$$

**Comparison:** Notice that $v_{\mathrm{geom}} = (2, 0, -2) = -2(-1, 0, 1) = -2v_{\mathrm{alg}}$. The two direction vectors are non-zero scalar multiples of one another, confirming they define the exact same direction in space.

---
