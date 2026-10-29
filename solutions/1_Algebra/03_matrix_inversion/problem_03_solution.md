### Exercise 3. When Does the Inverse Not Exist?

For

$$
A=
\begin{pmatrix}
2 & 4 \\
1 & 2 \\
\end{pmatrix}
$$

explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

> **Why this exercise:** connects two signs of noninvertibility instead of treating them as unrelated facts.

**Solution**

**Method 1: determinant**

$$
\det A = 2\cdot 2 - 4\cdot 1 = 0
$$

Suppose $A^{-1}$ existed. Then $AA^{-1}=I$, and taking determinants gives

$$
\det A \cdot \det A^{-1} = \det I = 1
$$

But $\det A=0$, so the left side is $0$, which is a contradiction. Hence $A^{-1}$ does not exist.

**Method 2: dependence between the rows**

The rows of $A$ are $R_1=(2,4)$ and $R_2=(1,2)$. They satisfy

$$
R_1 = 2R_2
$$

so the rows are linearly dependent and the rank of $A$ is $1<2$.

Suppose $AB=I$ for some matrix $B$. Each row of $AB$ is a combination of the rows of $B$ using the coefficients from the corresponding row of $A$. Since $R_1=2R_2$, the first row of $AB$ is twice the second row of $AB$. But the rows of $I$ are $(1,0)$ and $(0,1)$, and neither is a multiple of the other. This is a contradiction, so no such $B$ exists.

**Connection between the two methods**

For a general matrix

$$
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
$$

the determinant is $ad-bc$. It equals $0$ exactly when $(a,b)$ and $(c,d)$ are proportional, that is, when the rows are dependent. Here $\det A=0$ and $R_1=2R_2$ are two descriptions of the same fact.