### Exercise 3. Swapping Two Rows
For

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$.

First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

> **Why this exercise:** gives a second classical calculation with a $3\times3$ determinant while teaching the precise effect of a row swap on the sign of the determinant.

---

#### Solution

**Determinant of $A$**

Using Sarrus' rule, $\det A = P - N$, where $P$ is the sum of the products along the diagonals going down to the right, and $N$ is the sum of the products along the diagonals going down to the left.

$$
\begin{aligned}
P &= 1\cdot 3\cdot 1 + 2\cdot 1\cdot 2 + 0\cdot 0\cdot 1 \\
  &= 3 + 4 + 0 \\
  &= 7,
\end{aligned}
$$

$$
\begin{aligned}
N &= 0\cdot 3\cdot 2 + 1\cdot 1\cdot 1 + 2\cdot 0\cdot 1 \\
  &= 0 + 1 + 0 \\
  &= 1.
\end{aligned}
$$

Therefore

$$
\begin{aligned}
\det A &= P - N \\
       &= 7 - 1 \\
       &= 6.
\end{aligned}
$$

**The matrix $B$**

Swapping the first and second rows of $A$ gives

$$
B=
\begin{pmatrix}
0 & 3 & 1 \\
1 & 2 & 0 \\
2 & 1 & 1 \\
\end{pmatrix}.
$$

**Prediction**

Swapping two rows of a square matrix changes the sign of its determinant. Hence

$$
\begin{aligned}
\det B &= -\det A \\
       &= -6.
\end{aligned}
$$

**Verification by calculation**

Using Sarrus' rule for $B$:

$$
\begin{aligned}
P &= 0\cdot 2\cdot 1 + 3\cdot 0\cdot 2 + 1\cdot 1\cdot 1 \\
  &= 0 + 0 + 1 \\
  &= 1,
\end{aligned}
$$

$$
\begin{aligned}
N &= 1\cdot 2\cdot 2 + 0\cdot 0\cdot 1 + 3\cdot 1\cdot 1 \\
  &= 4 + 0 + 3 \\
  &= 7.
\end{aligned}
$$

Therefore

$$
\begin{aligned}
\det B &= P - N \\
       &= 1 - 7 \\
       &= -6.
\end{aligned}
$$

The calculation agrees with the prediction.

**Answer:** $\det A = 6$ and $\det B = -6$.