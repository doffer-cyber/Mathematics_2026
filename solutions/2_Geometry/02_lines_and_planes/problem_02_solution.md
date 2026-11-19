### Exercise 2. A Line in Space

Given

$$
L:(x,y,z)=(2,-1,3)+t(1,2,-2).
$$

State a point on the line and its direction vector, check whether $P=(4,3,-1)$ lies on $L$, and find the point corresponding to $t=-1$.

> **Why this exercise:** reinforces the interpretation of parametric form as “point + direction.”

#### Solution

From the parametric representation $(x,y,z) = p + tv$:

* **Point on the line:** $P_0 = (2, -1, 3)$ (corresponding to $t=0$).
* **Direction vector:** $v = (1, 2, -2)$.

To check whether $P=(4,3,-1)$ lies on $L$, substitute its coordinates into the parametric equation:

$$
\begin{cases}
4 = 2 + t, \\
3 = -1 + 2t, \\
-1 = 3 - 2t.
\end{cases}
$$

Solving each equation for $t$:

* From the first equation: $t = 4 - 2 = 2$.
* From the second equation: $2t = 4 \implies t = 2$.
* From the third equation: $-2t = -4 \implies t = 2$.

Since all three equations yield the consistent parameter value $t = 2$, the point $P=(4,3,-1)$ lies on $L$.

For $t = -1$, the corresponding point is

$$
(x, y, z) = (2, -1, 3) + (-1)(1, 2, -2) = (2 - 1, -1 - 2, 3 + 2) = (1, -3, 5)
$$

---