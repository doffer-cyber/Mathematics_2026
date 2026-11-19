### Exercise 9. Cross Product as a Perpendicular Direction

For $u=(1,2,0)$ and $v=(0,1,3)$ compute $u\times v$. Use dot products to check perpendicularity to both vectors, compute $v\times u$, and compare the results.

> **Why this exercise:** teaches the geometric meaning of the cross product and the effect of changing the order of its arguments.

#### Solution

Using the determinant formula for the cross product in $\mathbb{R}^3$,

$$
\begin{aligned}
u\times v &= (2\cdot 3 - 0\cdot 1,\, 0\cdot 0 - 1\cdot 3,\, 1\cdot 1 - 2\cdot 0) \\
          &= (6,\,-3,\,1).
\end{aligned}
$$

To verify perpendicularity, compute the dot products with $u$ and $v$:

$$
(u\times v)\cdot u = 6\cdot 1 + (-3)\cdot 2 + 1\cdot 0 = 6 - 6 + 0 = 0,
$$

$$
(u\times v)\cdot v = 6\cdot 0 + (-3)\cdot 1 + 1\cdot 3 = 0 - 3 + 3 = 0.
$$

Since both dot products equal $0$, $u\times v$ is orthogonal to both $u$ and $v$.

Next, compute $v\times u$:

$$
\begin{aligned}
v\times u &= (1\cdot 0 - 3\cdot 2,\, 3\cdot 1 - 0\cdot 0,\, 0\cdot 2 - 1\cdot 1) \\
          &= (-6,\,3,\,-1).
\end{aligned}
$$

**Comparison:** Comparing the two vectors gives $v\times u = -(u\times v)$. Reversing the order of the factors preserves the magnitude and perpendicular line of action, while reversing the orientation (direction) in accordance with the anti-commutativity of the cross product and the right-hand rule.

---