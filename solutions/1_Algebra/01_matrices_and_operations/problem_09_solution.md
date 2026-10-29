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

> **Why this exercise:** interprets matrix multiplication as composition of transformations.

**Solution**

**Step 1. The vector $RSx$**

In the product $RSx$ the vector $x$ is first multiplied by $S$, and the result is then multiplied by $R$.

$$
\begin{aligned}
Sx &=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2\cdot 1 + 0\cdot 2 \\
0\cdot 1 + 1\cdot 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2 \\
2 \\
\end{pmatrix}
\end{aligned}
$$

$$
\begin{aligned}
R(Sx) &=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
0\cdot 2 + (-1)\cdot 2 \\
1\cdot 2 + 0\cdot 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}
\end{aligned}
$$

**Step 2. The vector $SRx$**

In the product $SRx$ the vector $x$ is first multiplied by $R$, and the result is then multiplied by $S$.

$$
\begin{aligned}
Rx &=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
0\cdot 1 + (-1)\cdot 2 \\
1\cdot 1 + 0\cdot 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
-2 \\
1 \\
\end{pmatrix}
\end{aligned}
$$

$$
\begin{aligned}
S(Rx) &=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
-2 \\
1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2\cdot(-2) + 0\cdot 1 \\
0\cdot(-2) + 1\cdot 1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}
\end{aligned}
$$

**Step 3. Check with the product matrices**

$$
\begin{aligned}
RS &=
\begin{pmatrix}
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

$$
\begin{aligned}
SR &=
\begin{pmatrix}
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

Applying these matrices to $x$:

$$
RSx=
\begin{pmatrix}
0 & -1 \\
2 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
=
\begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}
$$

$$
SRx=
\begin{pmatrix}
0 & -2 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
=
\begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}
$$

**Step 4. Comparison**

$$
RSx=
\begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}
\neq
\begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}
=SRx.
$$

Hence $RS\neq SR$, and the order of the transformations changes the result.

**Step 5. Geometric explanation**

For $RSx$ the vector is first stretched horizontally by the factor $2$, which moves $(1,\,2)$ to $(2,\,2)$. The rotation by $90^\circ$ then moves this vector to $(-2,\,2)$. A rotation does not change lengths, so

$$
\|RSx\|=\|Sx\|=\sqrt{8}.
$$

For $SRx$ the vector is first rotated, which moves $(1,\,2)$ to $(-2,\,1)$. The original vertical component is now horizontal, and the scaling stretches it by the factor $2$, which gives $(-4,\,1)$. Its length is

$$
\|SRx\|=\sqrt{17}.
$$

The scaling $S$ acts only along the horizontal axis. In $RSx$ it stretches the original horizontal component of $x$. In $SRx$ it stretches the component that the rotation has already moved into the horizontal direction, which is the original vertical component. Since these two components of $x$ are different, the results are different.