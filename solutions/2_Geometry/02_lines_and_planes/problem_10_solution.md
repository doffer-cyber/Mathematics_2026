### Exercise 10. Projection of a Point onto a Plane

Find the orthogonal projection of $P=(2,1,3)$ onto the plane $x+y+z=3$, and then find the reflection of $P$ across this plane. Check that the midpoint of the segment joining the point and its reflection lies on the plane.

> **Why this exercise:** combines the normal, intersection, and distance into the construction of a projection and reflection.

#### Solution

The normal vector to the plane $\Pi: x + y + z = 3$ is $n = (1, 1, 1)$. The line passing through $P=(2,1,3)$ in the direction of $n$ is

$$
L: (x, y, z) = (2, 1, 3) + t(1, 1, 1) = (2 + t, 1 + t, 3 + t)
$$

To find the orthogonal projection $P'$, intersect $L$ with $\Pi$:

$$
\begin{aligned}
(2 + t) + (1 + t) + (3 + t) &= 3 \\
6 + 3t &= 3 \\
3t &= -3 \\
t &= -1
\end{aligned}
$$

Substituting $t = -1$ into $L$ gives the orthogonal projection:

$$
P' = (2 - 1, 1 - 1, 3 - 1) = (1, 0, 2)
$$

Since $P'$ is the midpoint of $P$ and its reflection $P''$, we have $P'' = 2P' - P$ (corresponding to $t = -2$ along $L$):

$$
P'' = 2(1, 0, 2) - (2, 1, 3) = (2 - 2, 0 - 1, 4 - 3) = (0, -1, 1)
$$

**Verification:** The midpoint $M$ of segment $PP''$ is

$$
M = \frac{P + P''}{2} = \left(\frac{2 + 0}{2}, \frac{1 + (-1)}{2}, \frac{3 + 1}{2}\right) = (1, 0, 2)
$$

Substituting $M=(1,0,2)$ into the plane equation gives $1 + 0 + 2 = 3$, confirming that $M$ lies on the plane.

---
