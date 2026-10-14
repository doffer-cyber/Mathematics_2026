### Exercise 9. Composing Transformations

**Matrix products**

The product $RSx$ means: first apply $S$, then $R$.

$$
RS=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
=
\begin{pmatrix}
0 & -1 \\
2 & 0 \\
\end{pmatrix}
$$

The product $SRx$ means: first apply $R$, then $S$.

$$
SR=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
=
\begin{pmatrix}
0 & -2 \\
1 & 0 \\
\end{pmatrix}
$$

**Computation of $RSx$**

$$
Sx=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
=
\begin{pmatrix}
2 \\
2 \\
\end{pmatrix}
$$

$$
RSx=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
2 \\
\end{pmatrix}
=
\begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}
$$

**Computation of $SRx$**

$$
Rx=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
=
\begin{pmatrix}
-2 \\
1 \\
\end{pmatrix}
$$

$$
SRx=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
-2 \\
1 \\
\end{pmatrix}
=
\begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}
$$

**Comparison**

The results differ:

$$
RSx=(-2,\,2)^T \neq (-4,\,1)^T=SRx
$$

Hence $RS\neq SR$, and the matrix product is not commutative. The lengths also differ:

$$
\|RSx\|=\sqrt{8}, \qquad \|SRx\|=\sqrt{17}
$$

**Geometric explanation**

The rotation $R$ preserves lengths and angles, while the scaling $S$ stretches only in the direction of the $x$-axis and leaves the $y$-direction unchanged. The scaling is tied to the fixed coordinate axes, not to the vector itself.

- In $RSx$, the vector $(1,2)^T$ is stretched first, giving $(2,2)^T$, and this stretched vector is then rotated. The rotation does not change its length.
- In $SRx$, the vector is rotated first, giving $(-2,1)^T$. It now points mostly along the $x$-axis, so the scaling stretches it much more, giving $(-4,1)^T$.

The same stretch acts on a different part of the vector depending on its orientation at that moment. Therefore the order of the transformations matters.