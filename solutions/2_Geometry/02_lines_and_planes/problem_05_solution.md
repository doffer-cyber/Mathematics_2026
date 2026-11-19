### Exercise 5. Relative Position of Two Lines

Analyze the position of

$$
L_1:(x,y,z)=(1,1,0)+t(1,2,1),
$$

$$
L_2:(x,y,z)=(2,0,1)+s(0,1,-1).
$$

If they intersect, give the intersection point. If not, determine whether they are parallel or skew. Justify the classification.

> **Why this exercise:** teaches how to distinguish qualitatively different relationships between lines in space.

#### Solution

The direction vectors of the lines are $v_1 = (1, 2, 1)$ and $v_2 = (0, 1, -1)$. Because the first component of $v_2$ is $0$ while that of $v_1$ is $1$, there is no scalar $\lambda$ such that $v_1 = \lambda v_2$. Therefore, $L_1$ and $L_2$ are not parallel.

To test for intersection, equate the coordinates of $L_1$ and $L_2$:

$$
\begin{cases}
1 + t = 2, \\
1 + 2t = s, \\
t = 1 - s.
\end{cases}
$$

From the first equation, $t = 1$. Substituting $t = 1$ into the second equation gives

$$
s = 1 + 2(1) = 3
$$

Check the third equation with $t = 1$ and $s = 3$:

$$
1 = 1 - 3 \implies 1 = -2
$$

This is a contradiction, so the system has no solution and the lines do not intersect.

**Classification:** Because $L_1$ and $L_2$ are neither parallel nor intersecting, they are **skew lines**.

---