### Exercise 9. Distances

Compute:

1. the distance from $P=(2,3)$ to the line $3x+4y-10=0$,
2. the distance from $Q=(2,-1,3)$ to the plane $2x-2y+z-4=0$.

Compare the two formulas and explain their common connection with the normal direction.

> **Why this exercise:** organizes two similar formulas through one geometric idea.

#### Solution

**1. Distance from $P=(2,3)$ to the line $3x+4y-10=0$:**

Using the point-to-line distance formula $d = \frac{|ax_0 + by_0 + c|}{\sqrt{a^2 + b^2}}$ with $a=3$, $b=4$, $c=-10$:

$$
d_1 = \frac{|3(2) + 4(3) - 10|}{\sqrt{3^2 + 4^2}} = \frac{|6 + 12 - 10|}{\sqrt{9 + 16}} = \frac{8}{5}
$$

**2. Distance from $Q=(2,-1,3)$ to the plane $2x-2y+z-4=0$:**

Using the point-to-plane distance formula $d = \frac{|ax_0 + by_0 + cz_0 + d|}{\sqrt{a^2 + b^2 + c^2}}$ with $a=2$, $b=-2$, $c=1$, $d=-4$:

$$
d_2 = \frac{|2(2) - 2(-1) + 1(3) - 4|}{\sqrt{2^2 + (-2)^2 + 1^2}} = \frac{|4 + 2 + 3 - 4|}{\sqrt{4 + 4 + 1}} = \frac{5}{3}
$$

**Comparison and geometric connection:** Both formulas are instances of the same vector projection formula:

$$
d = \frac{|n \cdot (X_0 - X_1)|}{\|n\|}
$$

where $X_1$ is any point on the hyperplane (line in $\mathbb{R}^2$ or plane in $\mathbb{R}^3$) and $n$ is its normal vector. The numerator evaluates the signed linear functional with $X_0$ plugged in, and dividing by $\|n\|$ normalizes the measurement to unit length along the orthogonal (normal) direction.

---