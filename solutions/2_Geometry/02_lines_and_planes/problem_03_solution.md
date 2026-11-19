### Exercise 3. Plane Through a Point with a Given Normal Vector

Find the equation of the plane through $P=(1,-2,3)$ and perpendicular to $n=(2,1,-1)$. Check the result by substituting the point $P$ and explain the role of the normal vector.

> **Why this exercise:** shows the basic construction of a plane from a point and a normal vector.

#### Solution

A point $X=(x,y,z)$ lies on the plane if and only if the vector $\overrightarrow{PX} = (x-1, y+2, z-3)$ is orthogonal to the normal vector $n=(2,1,-1)$, meaning $n \cdot \overrightarrow{PX} = 0$:

$$
2(x - 1) + 1(y + 2) - 1(z - 3) = 0
$$

Expanding and simplifying gives

$$
\begin{aligned}
2x - 2 + y + 2 - z + 3 &= 0 \\
2x + y - z + 3 &= 0
\end{aligned}
$$

**Verification:** Substituting $P=(1,-2,3)$ into the left-hand side gives

$$
2(1) + (-2) - 3 + 3 = 2 - 2 - 3 + 3 = 0
$$

**Role of the normal vector:** The normal vector $n=(2,1,-1)$ uniquely determines the spatial orientation (tilt) of the plane by defining the direction perpendicular to every vector lying within the plane. Its components appear directly as the coefficients of $x$, $y$, and $z$ in the general linear equation.

---
