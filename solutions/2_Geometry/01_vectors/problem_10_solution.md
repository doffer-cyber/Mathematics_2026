### Exercise 10. Triangle Area from Vectors

The points $A=(0,0,0)$, $B=(2,1,0)$, and $C=(1,3,2)$ form a triangle. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$, compute the area of the parallelogram using the cross product, and then find the area of the triangle. Explain the factor $\frac12$.

> **Why this exercise:** shows the interpretation of the length of the cross product as area.

#### Solution

Construct the displacement vectors from $A$:

$$
\overrightarrow{AB} = B - A = (2-0,\,1-0,\,0-0) = (2,1,0),
$$

$$
\overrightarrow{AC} = C - A = (1-0,\,3-0,\,2-0) = (1,3,2).
$$

Compute their cross product:

$$
\begin{aligned}
\overrightarrow{AB}\times\overrightarrow{AC} &= (1\cdot 2 - 0\cdot 3,\, 0\cdot 1 - 2\cdot 2,\, 2\cdot 3 - 1\cdot 1) \\
                                               &= (2,\,-4,\,5).
\end{aligned}
$$

The area of the parallelogram spanned by $\overrightarrow{AB}$ and $\overrightarrow{AC}$ is the Euclidean norm of their cross product:

$$
A_{\mathrm{parallelogram}} = \|\overrightarrow{AB}\times\overrightarrow{AC}\| = \sqrt{2^2 + (-4)^2 + 5^2} = \sqrt{4 + 16 + 25} = \sqrt{45} = 3\sqrt{5}.
$$

The area of $\triangle ABC$ is half the area of this parallelogram:

$$
A_{\mathrm{triangle}} = \frac{1}{2}\|\overrightarrow{AB}\times\overrightarrow{AC}\| = \frac{3\sqrt{5}}{2}.
$$

**Explanation of the factor $\frac{1}{2}$:** Two adjacent sides $\overrightarrow{AB}$ and $\overrightarrow{AC}$ span a parallelogram whose area is $\|\overrightarrow{AB}\times\overrightarrow{AC}\|$. The diagonal segment $BC$ divides this parallelogram into two congruent triangles, one of which is $\triangle ABC$. Consequently, the triangle occupies exactly half of the parallelogram's area.