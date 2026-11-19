### Exercise 7. A Line Relative to a Plane

For

$$
L:(x,y,z)=(1,1,0)+t(1,-1,0),\qquad \Pi:x+y+z=2,
$$

determine whether the line intersects the plane at one point, is parallel to it, or lies in it. Explain the role of the dot product of the direction vector and the normal vector.

> **Why this exercise:** builds a universal test for the relative position of a line and a plane.

#### Solution

The direction vector of $L$ is $v = (1, -1, 0)$, and the normal vector of $\Pi$ is $n = (1, 1, 1)$. Compute their dot product:

$$
v \cdot n = (1)(1) + (-1)(1) + (0)(1) = 1 - 1 + 0 = 0
$$

Because $v \cdot n = 0$, the direction vector $v$ is orthogonal to the normal vector $n$, which means $L$ is parallel to $\Pi$ (either strictly parallel or contained in $\Pi$).

To distinguish between these two cases, test whether the base point $P_0 = (1, 1, 0)$ of $L$ lies in $\Pi$:

$$
1 + 1 + 0 = 2
$$

Since $P_0$ satisfies the plane equation $x + y + z = 2$, the entire line $L$ lies in the plane $\Pi$.

**Role of the dot product:** The dot product $v \cdot n$ measures whether the line moves toward/away from the plane ($v \cdot n \neq 0$, guaranteeing a unique intersection) or moves purely perpendicular to the normal ($v \cdot n = 0$, meaning constant signed distance from the plane).

---
