### Exercise 14. Contrast: Intersection and Parallelism

From the point $P=(0,0,1)$, two lines are drawn with direction vectors

$$
v_1=(2,1,-1),\qquad v_2=(2,1,0).
$$

For each line, analyze its position relative to the plane $z=0$.

For the line that intersects the plane, find the intersection point. For the other line, explain how you can recognize parallelism without solving an equation.

> **Why this exercise:** compares two very similar data sets that lead to different outcomes and forces recognition of the geometric condition before calculation.

#### Solution

The two lines are

$$
L_1: (x, y, z) = (0, 0, 1) + t(2, 1, -1) = (2t, t, 1 - t)
$$

$$
L_2: (x, y, z) = (0, 0, 1) + s(2, 1, 0) = (2s, s, 1)
$$

The plane $\Pi: z = 0$ has normal vector $n = (0, 0, 1)$.

**Analysis of $L_1$:**

Since $v_1 \cdot n = (2, 1, -1) \cdot (0, 0, 1) = -1 \neq 0$, the line $L_1$ intersects $\Pi$ at a unique point. Setting $z = 0$ in $L_1$:

$$
1 - t = 0 \implies t = 1
$$

Substituting $t = 1$ gives the intersection point:

$$
(x, y, z) = (2(1), 1, 1 - 1) = (2, 1, 0)
$$

**Analysis of $L_2$:**

The direction vector $v_2 = (2, 1, 0)$ has third component $0$, so $v_2 \cdot n = 0$ and $v_2$ lies entirely within horizontal directions parallel to the $xy$-plane ($z=0$). Because $L_2$ starts at $P=(0,0,1)$ (where $z = 1 \neq 0$) and its direction vector produces zero change in the $z$-coordinate, $L_2$ remains at constant height $z = 1$ and is strictly parallel to the plane $z = 0$.

---