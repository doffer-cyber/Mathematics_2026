### Exercise 1. Line Through Two Points

Find the equation of the line through $A=(1,2)$ and $B=(4,-1)$ in parametric and general form. Identify a direction vector and an example of a normal vector. Check that both points satisfy the equation you obtain.

> **Why this exercise:** teaches how to move between equivalent descriptions of a line and connect them with the appropriate vectors.

#### Solution

A direction vector of the line is given by

$$
v = \overrightarrow{AB} = (4 - 1, -1 - 2) = (3, -3)
$$

Taking $A=(1,2)$ as the reference point and $v=(3,-3)$ as the direction vector, the parametric equation of the line is

$$
(x, y) = (1, 2) + t(3, -3), \qquad t \in \mathbb{R}
$$

Equivalently, in coordinate form:

$$
\begin{cases}
x = 1 + 3t, \\
y = 2 - 3t,
\end{cases}
\qquad t \in \mathbb{R}
$$

A vector perpendicular to $v=(3,-3)$ is $n=(3,3)$, or simplified by dividing by $3$, $n=(1,1)$. Using the point-normal form $n \cdot ((x,y) - A) = 0$:

$$
1(x - 1) + 1(y - 2) = 0
$$

Simplifying yields the general equation of the line:

$$
x + y - 3 = 0
$$

**Verification:**

* For $A=(1,2)$: $1 + 2 - 3 = 0$. The equation is satisfied.
* For $B=(4,-1)$: $4 + (-1) - 3 = 0$. The equation is satisfied.

---