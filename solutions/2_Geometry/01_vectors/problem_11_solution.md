### Exercise 11. Decomposition into Parallel and Perpendicular Components

Decompose $u=(3,4)$ into components parallel and perpendicular to $v=(1,2)$. Check

$$
u=u_{\parallel}+u_{\perp},\qquad u_{\perp}\cdot v=0.
$$

Explain why these are two independent checks of correctness.

> **Why this exercise:** deepens the idea of projection through construction and verification.

#### Solution

Compute the dot products $u\cdot v$ and $v\cdot v$:

$$
u\cdot v = 3\cdot 1 + 4\cdot 2 = 3 + 8 = 11,
$$

$$
v\cdot v = 1^2 + 2^2 = 1 + 4 = 5.
$$

The component of $u$ parallel to $v$ is the orthogonal projection of $u$ onto $v$:

$$
u_{\parallel} = \frac{u\cdot v}{v\cdot v}\,v = \frac{11}{5}(1,2) = \left(\frac{11}{5},\,\frac{22}{5}\right).
$$

Subtracting $u_{\parallel}$ from $u$ gives the perpendicular component:

$$
u_{\perp} = u - u_{\parallel} = (3,4) - \left(\frac{11}{5},\,\frac{22}{5}\right) = \left(\frac{15}{5}-\frac{11}{5},\,\frac{20}{5}-\frac{22}{5}\right) = \left(\frac{4}{5},\,-\frac{2}{5}\right).
$$

Verify both conditions:

1. **Reconstruction ($u = u_{\parallel} + u_{\perp}$):**

$$
u_{\parallel} + u_{\perp} = \left(\frac{11}{5},\,\frac{22}{5}\right) + \left(\frac{4}{5},\,-\frac{2}{5}\right) = \left(\frac{15}{5},\,\frac{20}{5}\right) = (3,4) = u.
$$

2. **Orthogonality ($u_{\perp}\cdot v = 0$):**

$$
u_{\perp}\cdot v = \frac{4}{5}\cdot 1 + \left(-\frac{2}{5}\right)\cdot 2 = \frac{4}{5} - \frac{4}{5} = 0.
$$

**Why these are two independent checks:** An arbitrary decomposition $u = w_1 + w_2$ satisfies the first check without ensuring that $w_1$ and $w_2$ have the required directions; for instance, taking $w_1 = (2,2)$ and $w_2 = (1,2)$ sums to $(3,4)$ but neither lies along $v$ nor is perpendicular to $v$. Conversely, an arbitrary vector $w_2$ orthogonal to $v$, such as $(2,-1)$, satisfies $w_2\cdot v = 0$ without matching the orthogonal residual $u - u_{\parallel}$. Together with $u_{\parallel}$ being a scalar multiple of $v$, these two conditions uniquely characterize the orthogonal decomposition.

---