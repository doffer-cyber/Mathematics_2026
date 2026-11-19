### Exercise 12. A Normal Vector to a Plane

Given $A=(1,0,2)$, $B=(2,1,0)$, and $C=(0,3,1)$. Construct two vectors lying in the plane, find a vector perpendicular to both, and check the perpendicularity using dot products.

> **Why this exercise:** creates a direct bridge from vectors to the description of a plane.

#### Solution

Construct two direction vectors lying in the plane passing through $A$, $B$, and $C$:

$$
\overrightarrow{AB} = B - A = (2-1,\,1-0,\,0-2) = (1,1,-2),
$$

$$
\overrightarrow{AC} = C - A = (0-1,\,3-0,\,1-2) = (-1,3,-1).
$$

Compute a normal vector $n$ perpendicular to both in-plane vectors using the cross product:

$$
\begin{aligned}
n &= \overrightarrow{AB}\times\overrightarrow{AC} \\
  &= \bigl(1\cdot(-1) - (-2)\cdot 3,\, (-2)\cdot(-1) - 1\cdot(-1),\, 1\cdot 3 - 1\cdot(-1)\bigr) \\
  &= (-1 + 6,\, 2 + 1,\, 3 + 1) \\
  &= (5,3,4).
\end{aligned}
$$

Check perpendicularity to both vectors via the dot product:

$$
n\cdot\overrightarrow{AB} = 5\cdot 1 + 3\cdot 1 + 4\cdot(-2) = 5 + 3 - 8 = 0,
$$

$$
n\cdot\overrightarrow{AC} = 5\cdot(-1) + 3\cdot 3 + 4\cdot(-1) = -5 + 9 - 4 = 0.
$$

Since both dot products vanish, $n=(5,3,4)$ is orthogonal to both $\overrightarrow{AB}$ and $\overrightarrow{AC}$ and hence normal to the plane.

---