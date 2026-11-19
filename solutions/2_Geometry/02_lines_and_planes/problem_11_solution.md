### Exercise 11. Plane Containing a Line and a Point

Find the equation of the plane containing

$$
(x,y,z)=(1,0,2)+t(1,1,-1)
$$

and the point $P=(0,2,1)$. Check that both the entire line and the point lie in the plane you obtain.

> **Why this exercise:** requires independently constructing two linearly independent directions in the plane.

#### Solution

The line passes through $Q=(1,0,2)$ and has direction vector $v=(1,1,-1)$. Since both $Q$ and $P=(0,2,1)$ lie in the plane, the vector $\overrightarrow{QP}$ also lies in the plane:

$$
u = \overrightarrow{QP} = (0 - 1, 2 - 0, 1 - 2) = (-1, 2, -1)
$$

Compute a normal vector $n = v \times u$:

$$
n = (1, 1, -1) \times (-1, 2, -1) = (1(-1) - (-1)(2),\; (-1)(-1) - 1(-1),\; 1(2) - 1(-1)) = (1, 2, 3)
$$

Using point $Q=(1,0,2)$ and normal vector $n=(1,2,3)$:

$$
1(x - 1) + 2(y - 0) + 3(z - 2) = 0
$$

Simplifying gives the plane equation:

$$
x + 2y + 3z = 7
$$

**Verification:**

* **Point $P=(0,2,1)$:** $0 + 2(2) + 3(1) = 4 + 3 = 7$. The point lies in the plane.
* **Entire line $(1+t, t, 2-t)$:** Substituting into the plane equation for arbitrary $t \in \mathbb{R}$ gives

$$
(1 + t) + 2(t) + 3(2 - t) = 1 + t + 2t + 6 - 3t = 7
$$

Because the identity holds for all $t \in \mathbb{R}$, the entire line lies in the plane.

---