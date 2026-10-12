### Exercise 7. Identity Matrix, Zero Matrix, and Powers

#### Solution

Let

$$
A=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

The matrices $I$ and $0$ are the $2\times 2$ identity matrix and zero matrix:

$$
I=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
$$

and

$$
0=
\begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix}
$$

#### Computation of $AI$

$$
AI=
\begin{pmatrix}
2\cdot 1+1\cdot 0 & 2\cdot 0+1\cdot 1 \\
0\cdot 1+2\cdot 0 & 0\cdot 0+2\cdot 1 \\
\end{pmatrix}
$$

Therefore

$$
AI=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
=A
$$

#### Computation of $IA$

$$
IA=
\begin{pmatrix}
1\cdot 2+0\cdot 0 & 1\cdot 1+0\cdot 2 \\
0\cdot 2+1\cdot 0 & 0\cdot 1+1\cdot 2 \\
\end{pmatrix}
$$

Therefore

$$
IA=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
=A
$$

#### Computation of $A+0$

Matrices are added entry by entry:

$$
A+0=
\begin{pmatrix}
2+0 & 1+0 \\
0+0 & 2+0 \\
\end{pmatrix}
$$

Therefore

$$
A+0=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
=A
$$

#### Computation of $A^2$

$$
A^2=
\begin{pmatrix}
2\cdot 2+1\cdot 0 & 2\cdot 1+1\cdot 2 \\
0\cdot 2+2\cdot 0 & 0\cdot 1+2\cdot 2 \\
\end{pmatrix}
$$

Therefore

$$
A^2=
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}
$$

#### Computation of $A^3$

Using $A^3=A^2A$:

$$
A^3=
\begin{pmatrix}
4\cdot 2+4\cdot 0 & 4\cdot 1+4\cdot 2 \\
0\cdot 2+4\cdot 0 & 0\cdot 1+4\cdot 2 \\
\end{pmatrix}
$$

Therefore

$$
A^3=
\begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}
$$

#### Roles of $I$ and $0$

The results above show

$$
AI=IA=A
$$

and

$$
A+0=A
$$

- The identity matrix $I$ is the neutral element for matrix multiplication: multiplying by $I$ from either side leaves a matrix unchanged. It plays the role of the number $1$.
- The zero matrix $0$ is the neutral element for matrix addition: adding $0$ leaves a matrix unchanged. It plays the role of the number $0$.

#### Pattern in the powers of $A$

The computed powers are

$$
A^1=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

$$
A^2=
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}
$$

$$
A^3=
\begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}
$$

Observations:

- The diagonal entries are $2,\,4,\,8$, that is $2^n$.
- The lower left entry stays $0$.
- The upper right entries are $1,\,4,\,12$, that is $n\cdot 2^{n-1}$.

This suggests

$$
A^n=
\begin{pmatrix}
2^n & n\cdot 2^{n-1} \\
0 & 2^n \\
\end{pmatrix}
$$

#### Explanation of the pattern

Write $A=2I+N$, where

$$
N=
\begin{pmatrix}
0 & 1 \\
0 & 0 \\
\end{pmatrix}
$$

Then

$$
N^2=
\begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix}
$$

Since $2I$ commutes with $N$, the binomial theorem applies, and all terms containing $N^2$ or higher powers vanish:

$$
A^n=(2I+N)^n=2^nI+n\cdot 2^{n-1}N
$$

This gives exactly the matrix above. Check for $n=3$: the diagonal entries are $2^3=8$ and the upper right entry is $3\cdot 2^2=12$, in agreement with the direct computation.