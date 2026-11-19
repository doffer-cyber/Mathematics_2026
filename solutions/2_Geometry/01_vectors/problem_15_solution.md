### Exercise 15. Comparing Directions Using the Cosine of the Angle

Given

$$
a=(1,2,1),\qquad b=(2,4,2),\qquad c=(2,0,3).
$$

For each pair, compute

$$
\frac{u\cdot v}{\|u\|\,\|v\|}.
$$

Order the pairs by increasing angle between the vectors. Explain why for $a$ and $b$ the value is $1$ even though the vectors have different lengths.

> **Why this exercise:** reinforces the connection between the dot product and angle, and the distinction between direction and length.

#### Solution

First compute the Euclidean norms of the three vectors:

$$
\|a\| = \sqrt{1^2 + 2^2 + 1^2} = \sqrt{6},
$$

$$
\|b\| = \sqrt{2^2 + 4^2 + 2^2} = \sqrt{24} = 2\sqrt{6},
$$

$$
\|c\| = \sqrt{2^2 + 0^2 + 3^2} = \sqrt{13}.
$$

Compute the cosine of the angle $\theta_{uv}$ for each pair:

1. **Pair $(a,b)$:**

$$
a\cdot b = 1\cdot 2 + 2\cdot 4 + 1\cdot 2 = 12,
$$

$$
\cos\theta_{ab} = \frac{a\cdot b}{\|a\|\,\|b\|} = \frac{12}{\sqrt{6}\cdot 2\sqrt{6}} = \frac{12}{12} = 1.
$$

2. **Pair $(a,c)$:**

$$
a\cdot c = 1\cdot 2 + 2\cdot 0 + 1\cdot 3 = 5,
$$

$$
\cos\theta_{ac} = \frac{a\cdot c}{\|a\|\,\|c\|} = \frac{5}{\sqrt{6}\cdot\sqrt{13}} = \frac{5}{\sqrt{78}}.
$$

3. **Pair $(b,c)$:**

$$
b\cdot c = 2\cdot 2 + 4\cdot 0 + 2\cdot 3 = 10,
$$

$$
\cos\theta_{bc} = \frac{b\cdot c}{\|b\|\,\|c\|} = \frac{10}{2\sqrt{6}\cdot\sqrt{13}} = \frac{5}{\sqrt{78}}.
$$

**Ordering by increasing angle:** On the interval $[0,\pi]$, $\cos\theta$ is strictly decreasing, so larger cosine values correspond to smaller angles. Since

$$
1 > \frac{5}{\sqrt{78}} = \frac{5}{\sqrt{78}},
$$

the ordering by increasing angle is

$$
\theta_{ab} < \theta_{ac} = \theta_{bc}.
$$

Specifically, $\theta_{ab} = 0$, while $(a,c)$ and $(b,c)$ share the exact same acute angle $\arccos\!\left(\frac{5}{\sqrt{78}}\right)$.

**Why $\cos\theta_{ab}=1$ despite different lengths:** Dividing by $\|a\|\,\|b\|$ normalizes each vector to unit length, removing all scale information and leaving only unit directions $\frac{a}{\|a\|}$ and $\frac{b}{\|b\|}$. Because $b = 2a$ is a positive scalar multiple of $a$, both vectors point in the exact same direction ($\theta_{ab} = 0$), so $\cos 0 = 1$ regardless of their magnitudes.