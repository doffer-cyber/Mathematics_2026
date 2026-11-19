### Exercise 13. Do Four Points Lie in One Plane?

Given

$$
A=(0,0,0),\qquad B=(1,2,0),\qquad C=(0,1,1),\qquad D=(2,5,1).
$$

1. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$.
2. Find $n=\overrightarrow{AB}\times\overrightarrow{AC}$.
3. Construct $\overrightarrow{AD}$ and check whether $\overrightarrow{AD}\cdot n=0$.
4. Based on this, decide whether $D$ lies in the plane determined by $A,B,C$, and justify the criterion.

> **Why this exercise:** combines the known cross and dot products into a geometric criterion needed for planes, without introducing a separate concept used only once.

#### Solution

1. **In-plane direction vectors:**

$$
\overrightarrow{AB} = B - A = (1,2,0),
$$

$$
\overrightarrow{AC} = C - A = (0,1,1).
$$

2. **Normal vector:**

$$
\begin{aligned}
n &= \overrightarrow{AB}\times\overrightarrow{AC} \\
  &= (2\cdot 1 - 0\cdot 1,\, 0\cdot 0 - 1\cdot 1,\, 1\cdot 1 - 2\cdot 0) \\
  &= (2,-1,1).
\end{aligned}
$$

3. **Displacement to $D$ and dot product with $n$:**

$$
\overrightarrow{AD} = D - A = (2,5,1).
$$

Computing the dot product gives

$$
\overrightarrow{AD}\cdot n = 2\cdot 2 + 5\cdot(-1) + 1\cdot 1 = 4 - 5 + 1 = 0.
$$

4. **Coplanarity conclusion and justification:** Because $\overrightarrow{AD}\cdot n = 0$, the point $D$ lies in the plane determined by $A$, $B$, and $C$. Geometrically, $n = \overrightarrow{AB}\times\overrightarrow{AC}$ is non-zero and orthogonal to the plane spanned by $\overrightarrow{AB}$ and $\overrightarrow{AC}$ anchored at $A$. Every vector $\overrightarrow{AD}$ starting at $A$ lies inside that plane if and only if it is perpendicular to the plane's normal direction $n$, which is equivalent to $\overrightarrow{AD}\cdot n = 0$.

---