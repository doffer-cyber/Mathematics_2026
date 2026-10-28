### Exercise 9. Area and the Determinant
The vectors

$$
u=
\begin{pmatrix}
3 \\
1 \\
\end{pmatrix},\qquad v=
\begin{pmatrix}
1 \\
4 \\
\end{pmatrix}
$$

span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

> **Why this exercise:** gives the determinant a geometric interpretation and distinguishes its sign from the value of the area.

---

#### Solution

**Geometric interpretation**

The area of the parallelogram spanned by $u$ and $v$ equals the absolute value of the determinant of the matrix whose columns are $u$ and $v$.

**Computation with the order $u,v$**

$$
M_1=
\begin{pmatrix}
3 & 1 \\
1 & 4 \\
\end{pmatrix}.
$$

$$
\begin{aligned}
\det M_1 &= 3\cdot 4 - 1\cdot 1 \\
         &= 12 - 1 \\
         &= 11.
\end{aligned}
$$

Hence

$$
\begin{aligned}
\mathrm{Area} &= |\det M_1| \\
              &= 11.
\end{aligned}
$$

**Computation with the order $v,u$**

Reversing the order of the vectors swaps the two columns:

$$
M_2=
\begin{pmatrix}
1 & 3 \\
4 & 1 \\
\end{pmatrix}.
$$

$$
\begin{aligned}
\det M_2 &= 1\cdot 1 - 3\cdot 4 \\
         &= 1 - 12 \\
         &= -11.
\end{aligned}
$$

Hence

$$
\begin{aligned}
\mathrm{Area} &= |\det M_2| \\
              &= 11.
\end{aligned}
$$

**What changes and what does not**

Swapping two columns of a matrix changes the sign of its determinant, so $\det M_2=-\det M_1$. The sign encodes the orientation of the ordered pair of vectors: $u,v$ is positively oriented (counterclockwise from $u$ to $v$), while $v,u$ is negatively oriented.

The parallelogram itself is the same set of points in both cases, so its area does not change. Since the area is the absolute value of the determinant, the sign is discarded and both orders give the same area.

**Answer:** the area is $11$. The determinant changes from $11$ to $-11$ when the order of the vectors is reversed, while the area remains $11$.