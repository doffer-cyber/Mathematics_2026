### Exercise 12. Formula for a Matrix Power

Let

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}.
$$

Compute $A^2$, $A^3$, and $A^4$, and use them to formulate a conjecture for $A^n$. Then do not stop after checking one more case: assume the formula is true for $n$, multiply by $A$, and explain why you obtain exactly the formula for $n+1$.

> **Why this exercise:** teaches how to recognize a pattern and formulate a generalization from several computations.

#### Solution

**Step 1. Compute $A^2$.**

$$
A^2=A\cdot A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

Multiplying row by column gives

$$
A^2=
\begin{pmatrix}
1\cdot 1+1\cdot 0 & 1\cdot 1+1\cdot 1 \\
0\cdot 1+1\cdot 0 & 0\cdot 1+1\cdot 1 \\
\end{pmatrix}
$$

$$
A^2=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}.
$$

**Step 2. Compute $A^3$.**

$$
A^3=A^2\cdot A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

$$
A^3=
\begin{pmatrix}
1\cdot 1+2\cdot 0 & 1\cdot 1+2\cdot 1 \\
0\cdot 1+1\cdot 0 & 0\cdot 1+1\cdot 1 \\
\end{pmatrix}
$$

$$
A^3=
\begin{pmatrix}
1 & 3 \\
0 & 1 \\
\end{pmatrix}.
$$

**Step 3. Compute $A^4$.**

$$
A^4=A^3\cdot A=
\begin{pmatrix}
1 & 3 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

$$
A^4=
\begin{pmatrix}
1\cdot 1+3\cdot 0 & 1\cdot 1+3\cdot 1 \\
0\cdot 1+1\cdot 0 & 0\cdot 1+1\cdot 1 \\
\end{pmatrix}
$$

$$
A^4=
\begin{pmatrix}
1 & 4 \\
0 & 1 \\
\end{pmatrix}.
$$

**Step 4. Conjecture.**

In every computed case the diagonal entries equal $1$, the lower left entry equals $0$, and the upper right entry equals the exponent. Hence we conjecture that for every integer $n\ge 1$

$$
A^n=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}.
$$

**Step 5. Proof by induction.**

*Base case.* For $n=1$ the formula gives

$$
A^1=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},
$$

which is the matrix $A$ itself.

*Inductive step.* Assume that for some $n\ge 1$

$$
A^n=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}.
$$

Since $A^{n+1}=A^n\cdot A$, we multiply:

$$
A^{n+1}=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

Computing the entries row by column:

$$
A^{n+1}=
\begin{pmatrix}
1\cdot 1+n\cdot 0 & 1\cdot 1+n\cdot 1 \\
0\cdot 1+1\cdot 0 & 0\cdot 1+1\cdot 1 \\
\end{pmatrix}
$$

$$
A^{n+1}=
\begin{pmatrix}
1 & n+1 \\
0 & 1 \\
\end{pmatrix}.
$$

This is exactly the conjectured formula with $n$ replaced by $n+1$.

**Step 6. Why the step works.**

Multiplying by $A$ leaves the first column unchanged, namely $(1,0)^T$. The second column of the product is the sum of the two columns of $A^n$, that is, $(n,1)^T+(1,0)^T=(n+1,1)^T$. So each multiplication by $A$ increases the upper right entry by exactly $1$ and changes nothing else. This argument works for every $n$, not only for the checked cases.

**Answer.** For every integer $n\ge 1$

$$
A^n=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}.
$$