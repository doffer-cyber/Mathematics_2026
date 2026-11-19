### Exercise 6. Angle Between Planes

Given

$$
\Pi_1:x+y+z=1,\qquad \Pi_2:x-y=2.
$$

First use the normal vectors to decide whether the planes are parallel. If not, compute the angle between them and explain why the normal vectors alone are enough for this calculation.

> **Why this exercise:** focuses attention on one mechanism—using normals to analyze position and angle—without also introducing the construction of the intersection line.

#### Solution

The normal vectors of the planes are $n_1 = (1, 1, 1)$ and $n_2 = (1, -1, 0)$. Since $n_1$ is not a scalar multiple of $n_2$ (the third component of $n_2$ is $0$ while that of $n_1$ is $1$), the planes are not parallel.

Compute the dot product and magnitudes of the normal vectors:

$$
n_1 \cdot n_2 = (1)(1) + (1)(-1) + (1)(0) = 0
$$

$$
\|n_1\| = \sqrt{1^2 + 1^2 + 1^2} = \sqrt{3}, \qquad \|n_2\| = \sqrt{1^2 + (-1)^2 + 0^2} = \sqrt{2}
$$

The acute angle $\theta \in [0, \frac{\pi}{2}]$ between the planes satisfies

$$
\cos\theta = \frac{|n_1 \cdot n_2|}{\|n_1\|\,\|n_2\|} = \frac{0}{\sqrt{3}\sqrt{2}} = 0
$$

Thus, $\theta = \frac{\pi}{2}$ (or $90^\circ$); the planes are perpendicular.

**Geometric justification:** Rotating a plane in space rotates its normal vector by the exact same angle. Consequently, the dihedral angle between two intersecting planes equals the angle between their normal vectors (taken as the acute or right angle $\theta \le \frac{\pi}{2}$).

---
