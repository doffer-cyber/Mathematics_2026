### Exercise 11. Parameter and Invertibility

For

$$
A(t)=
\begin{pmatrix}
1 & t \\
t & 1 \\
\end{pmatrix}
$$

find all $t$ for which the matrix is invertible, and then give a formula for $A(t)^{-1}$. Explain what happens to this formula at the excluded values.

> **Why this exercise:** combines a parameter, determinant, and an explicit inverse formula in one problem.

#### Solution

**Step 1. Compute the determinant.**

$$
\det A(t)=1\cdot 1-t\cdot t=1-t^2.
$$

**Step 2. Condition for invertibility.**

A square matrix is invertible if and only if its determinant is nonzero.

$$
1-t^2=0 \iff (1-t)(1+t)=0 \iff t=1 \ \ \mathrm{or} \ \ t=-1.
$$

Hence $A(t)$ is invertible if and only if $t\neq 1$ and $t\neq -1$.

**Step 3. Inverse formula.**

For a $2\times 2$ matrix with entries $a,b,c,d$ and $ad-bc\neq 0$, the inverse is

$$
\frac{1}{ad-bc}
\begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix}.
$$

Here $a=1$, $b=t$, $c=t$, $d=1$, so for $t\neq \pm 1$

$$
A(t)^{-1}=\frac{1}{1-t^2}
\begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix}.
$$

**Step 4. Verification.**

$$
A(t)\cdot
\begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1-t^2 & -t+t \\
t-t & -t^2+1 \\
\end{pmatrix}
$$

$$
A(t)\cdot
\begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1-t^2 & 0 \\
0 & 1-t^2 \\
\end{pmatrix}.
$$

Dividing by $1-t^2$ gives the identity matrix, so the formula is correct.

**Step 5. What happens at the excluded values.**

For $t=1$ and $t=-1$ the denominator $1-t^2$ equals $0$, so the formula is undefined. The matrices are

$$
A(1)=
\begin{pmatrix}
1 & 1 \\
1 & 1 \\
\end{pmatrix},
\qquad
A(-1)=
\begin{pmatrix}
1 & -1 \\
-1 & 1 \\
\end{pmatrix}.
$$

In both cases the two rows are proportional: they are equal for $t=1$ and opposite for $t=-1$. The rows are linearly dependent, the rank equals $1$, and the matrix has no inverse. Moreover, as $t\to\pm 1$ the entries of the formula grow without bound, which reflects the loss of invertibility.

**Answer.** $A(t)$ is invertible if and only if $t\neq \pm 1$, and then

$$
A(t)^{-1}=\frac{1}{1-t^2}
\begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix}.
$$

For $t=\pm 1$ the determinant is $0$, the rows are dependent, and the inverse does not exist.