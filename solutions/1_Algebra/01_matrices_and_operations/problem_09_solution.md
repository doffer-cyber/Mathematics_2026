### Exercise 9. Composing Transformations

Let

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad R=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}.
$$

The matrix $S$ describes nonuniform scaling, while $R$ describes a $90^\circ$ counterclockwise rotation.
For

$$
x=
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
$$

compute $RSx$ and $SRx$. Compare the results and explain geometrically why the order of these transformations matters.

### Solution

**Product matrices**

The expression $RSx$ means that $S$ is applied first and $R$ second.

$$
\begin{aligned}
RS &= \begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
0 & -1 \\
2 & 0 \\
\end{pmatrix}
\end{aligned}
$$

The expression $SRx$ means that $R$ is applied first and $S$ second.

$$
\begin{aligned}
SR &= \begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix} \\
&= \begin{pmatrix}
0 & -2 \\
1 & 0 \\
\end{pmatrix}
\end{aligned}
$$

**Computation of $RSx$**

$$
\begin{aligned}
Sx &= \begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2 \\
2 \\
\end{pmatrix}
\end{aligned}
$$

$$
\begin{aligned}
RSx &= \begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}
\end{aligned}
$$

**Computation of $SRx$**

$$
\begin{aligned}
Rx &= \begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
-2 \\
1 \\
\end{pmatrix}
\end{aligned}
$$

$$
\begin{aligned}
SRx &= \begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
-2 \\
1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}
\end{aligned}
$$

**Comparison**

The two results are different:

$$
RSx=(-2,\,2)^T \neq (-4,\,1)^T=SRx
$$

Hence $RS\neq SR$, so matrix multiplication is not commutative. The lengths of the results also differ:

$$
\|RSx\|=\sqrt{8}, \qquad \|SRx\|=\sqrt{17}
$$

**Geometric explanation**

The rotation $R$ preserves lengths and angles. The scaling $S$ stretches only in the direction of the $x$-axis and leaves the $y$-direction unchanged. Its action is tied to the fixed coordinate axes, not to the vector itself.

- In $RSx$, the vector $(1,2)^T$ is first stretched to $(2,2)^T$. The rotation then turns this vector without changing its length.
- In $SRx$, the vector is first rotated to $(-2,1)^T$. It now points mostly along the $x$-axis, so the scaling stretches it more, giving $(-4,1)^T$.

The same stretch acts on a different part of the vector depending on its orientation at that moment. Therefore the order of the transformations matters.

> **Why this exercise:** interprets matrix multiplication as composition of transformations.