### Exercise 14. Closest Point on a Line

Given a point $P=(4,1)$ and a line through the origin with direction $v=(1,2)$. Using projection, find the closest point on the line, the distance from $P$ to the line, and verify that the appropriate vector is perpendicular to the direction of the line.

> **Why this exercise:** shows projection as a complete solution to a minimum-distance problem.

#### Solution

Let $p = \overrightarrow{OP} = (4,1)$ be the position vector of $P$. The closest point $Q$ on the line through the origin with direction $v=(1,2)$ has position vector $q = \mathrm{proj}_v\,p$:

$$
p\cdot v = 4\cdot 1 + 1\cdot 2 = 6,
$$

$$
v\cdot v = 1^2 + 2^2 = 5.
$$

Hence

$$
q = \frac{p\cdot v}{v\cdot v}\,v = \frac{6}{5}(1,2) = \left(\frac{6}{5},\,\frac{12}{5}\right),
$$

so the closest point on the line is $Q=\left(\frac{6}{5},\,\frac{12}{5}\right)$.

The residual vector from $Q$ to $P$ is

$$
\overrightarrow{QP} = p - q = (4,1) - \left(\frac{6}{5},\,\frac{12}{5}\right) = \left(\frac{14}{5},\,-\frac{7}{5}\right).
$$

The shortest distance from $P$ to the line is the Euclidean length of $\overrightarrow{QP}$:

$$
d = \|\overrightarrow{QP}\| = \sqrt{\left(\frac{14}{5}\right)^2 + \left(-\frac{7}{5}\right)^2} = \sqrt{\frac{196 + 49}{25}} = \sqrt{\frac{245}{25}} = \frac{7\sqrt{5}}{5}.
$$

Verify that $\overrightarrow{QP}$ is perpendicular to the line direction $v$:

$$
\overrightarrow{QP}\cdot v = \frac{14}{5}\cdot 1 + \left(-\frac{7}{5}\right)\cdot 2 = \frac{14}{5} - \frac{14}{5} = 0.
$$

Because $\overrightarrow{QP}\cdot v = 0$, the segment connecting $Q$ to $P$ meets the line at a right angle, confirming that $Q$ minimizes the distance.

---