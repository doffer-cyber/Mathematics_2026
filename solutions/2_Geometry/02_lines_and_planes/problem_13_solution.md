### Exercise 13. Closest Point on a Plane

Find the point on the plane $x+2y+2z=4$ closest to $P=(3,0,0)$. Give the distance and check that the segment joining the two points is perpendicular to the plane.

> **Why this exercise:** combines projection, distance, and the normal direction in one problem.

#### Solution

The closest point $P^*$ on the plane $\Pi: x + 2y + 2z = 4$ to $P=(3,0,0)$ is the orthogonal projection of $P$ onto $\Pi$. Using the normal vector $n = (1, 2, 2)$, construct the normal line through $P$:

$$
(x, y, z) = (3, 0, 0) + t(1, 2, 2) = (3 + t, 2t, 2t)
$$

Substitute into the plane equation:

$$
\begin{aligned}
(3 + t) + 2(2t) + 2(2t) &= 4 \\
3 + 9t &= 4 \\
t &= \frac{1}{9}
\end{aligned}
$$

Thus, the closest point is

$$
P^* = \left(3 + \frac{1}{9},\; 2\left(\frac{1}{9}\right),\; 2\left(\frac{1}{9}\right)\right) = \left(\frac{28}{9}, \frac{2}{9}, \frac{2}{9}\right)
$$

The distance between $P$ and $\Pi$ is

$$
d = \frac{|1(3) + 2(0) + 2(0) - 4|}{\sqrt{1^2 + 2^2 + 2^2}} = \frac{|-1|}{\sqrt{9}} = \frac{1}{3}
$$

**Perpendicularity check:** The displacement vector from $P$ to $P^*$ is

$$
\overrightarrow{PP^*} = \left(\frac{28}{9} - 3,\; \frac{2}{9} - 0,\; \frac{2}{9} - 0\right) = \left(\frac{1}{9}, \frac{2}{9}, \frac{2}{9}\right) = \frac{1}{9}(1, 2, 2) = \frac{1}{9}n
$$

Since $\overrightarrow{PP^*}$ is a scalar multiple of the normal vector $n$, the segment $PP^*$ is perpendicular to the plane.

---
