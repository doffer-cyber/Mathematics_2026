### Exercise 4. Plane Through Three Points

Find the equation of the plane through

$$
A=(1,0,0),\quad B=(0,1,0),\quad C=(0,0,1).
$$

First construct two vectors lying in the plane, and then use the cross product. Check the resulting equation on all three points.

> **Why this exercise:** connects earlier vector tools with constructing the equation of a plane.

#### Solution

Construct two non-collinear vectors lying in the plane using point $A$:

$$
u = \overrightarrow{AB} = (0 - 1, 1 - 0, 0 - 0) = (-1, 1, 0)
$$

$$
w = \overrightarrow{AC} = (0 - 1, 0 - 0, 1 - 0) = (-1, 0, 1)
$$

Compute a normal vector $n$ via the cross product $n = u \times w$:

$$
n = (-1, 1, 0) \times (-1, 0, 1) = (1 \cdot 1 - 0 \cdot 0,\; 0 \cdot (-1) - (-1) \cdot 1,\; (-1) \cdot 0 - 1 \cdot (-1)) = (1, 1, 1)
$$

Using point $A=(1,0,0)$ and normal vector $n=(1,1,1)$:

$$
1(x - 1) + 1(y - 0) + 1(z - 0) = 0
$$

Simplifying yields

$$
x + y + z = 1
$$

**Verification:**

* For $A=(1,0,0)$: $1 + 0 + 0 = 1$.
* For $B=(0,1,0)$: $0 + 1 + 0 = 1$.
* For $C=(0,0,1)$: $0 + 0 + 1 = 1$.

All three points satisfy the equation.

---