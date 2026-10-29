### Exercise 7. Identity Matrix, Zero Matrix, and Powers
For

$$
A=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

compute

$$
AI,\qquad IA,\qquad A+0,\qquad A^2,\qquad A^3.
$$

Explain the roles of the matrices $I$ and $0$, and describe the pattern you observe in successive powers of $A$.

> **Why this exercise:** organizes the roles of neutral elements and reveals regularity in successive powers of a matrix.

**Solution**

**Step 1. The matrices $I$ and $0$**

Since $A$ is of size $2\times 2$, the matrices $I$ and $0$ are also of size $2\times 2$.

$$
I=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
$$

$$
0=
\begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix}
$$

**Step 2. The product $AI$**

$$
\begin{aligned}
AI &=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2\cdot 1 + 1\cdot 0 & 2\cdot 0 + 1\cdot 1 \\
0\cdot 1 + 2\cdot 0 & 0\cdot 0 + 2\cdot 1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\end{aligned}
$$

**Step 3. The product $IA$**

$$
\begin{aligned}
IA &=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1\cdot 2 + 0\cdot 0 & 1\cdot 1 + 0\cdot 2 \\
0\cdot 2 + 1\cdot 0 & 0\cdot 1 + 1\cdot 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\end{aligned}
$$

**Step 4. The sum $A+0$**

$$
\begin{aligned}
A+0 &=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
+
\begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\end{aligned}
$$

**Step 5. The power $A^2$**

$$
\begin{aligned}
A^2 &= AA \\
&= \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2\cdot 2 + 1\cdot 0 & 2\cdot 1 + 1\cdot 2 \\
0\cdot 2 + 2\cdot 0 & 0\cdot 1 + 2\cdot 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}
\end{aligned}
$$

**Step 6. The power $A^3$**

$$
\begin{aligned}
A^3 &= A^2A \\
&= \begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
4\cdot 2 + 4\cdot 0 & 4\cdot 1 + 4\cdot 2 \\
0\cdot 2 + 4\cdot 0 & 0\cdot 1 + 4\cdot 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}
\end{aligned}
$$

**Step 7. Roles of $I$ and $0$**

The results of Steps 2, 3, and 4 show that

$$
AI = IA = A,\qquad A+0=A.
$$

The identity matrix $I$ is the neutral element of matrix multiplication: multiplying by $I$ from either side leaves a matrix unchanged. The zero matrix $0$ is the neutral element of matrix addition: adding $0$ leaves a matrix unchanged.

**Step 8. Pattern in the powers of $A$**

Collecting the results:

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

The diagonal entries are $2$, $4$, $8$, that is $2^n$. The entry in the upper right corner is $1$, $4$, $12$, that is $n\cdot 2^{n-1}$. The lower left entry stays $0$. This suggests

$$
A^n=
\begin{pmatrix}
2^n & n\cdot 2^{n-1} \\
0 & 2^n \\
\end{pmatrix}.
$$

**Step 9. Check of the pattern**

Assume the formula holds for $n$. Then

$$
\begin{aligned}
A^{n+1} &= A^nA \\
&= \begin{pmatrix}
2^n & n\cdot 2^{n-1} \\
0 & 2^n \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2^{n+1} & 2^n + n\cdot 2^n \\
0 & 2^{n+1} \\
\end{pmatrix} \\
&= \begin{pmatrix}
2^{n+1} & (n+1)\cdot 2^n \\
0 & 2^{n+1} \\
\end{pmatrix}
\end{aligned}
$$

This is the same formula with $n$ replaced by $n+1$. Since the formula holds for $n=1$, it holds for every positive integer $n$.