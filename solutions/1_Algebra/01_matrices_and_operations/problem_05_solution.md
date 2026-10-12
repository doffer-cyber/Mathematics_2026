### Exercise 5. Matrix Times Vector

#### Solution

Let

$$
A=
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix}
$$

and

$$
x=
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix}
$$

#### Computation of $Ax$

The $i$-th entry of $Ax$ is the dot product of row $i$ of $A$ with the vector $x$.

$$
Ax=
\begin{pmatrix}
2\cdot 4+(-1)\cdot 2 \\
1\cdot 4+3\cdot 2 \\
\end{pmatrix}
$$

Therefore

$$
Ax=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
$$

#### Linear combination of the columns of $A$

Denote the columns of $A$ by

$$
a_1=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
$$

and

$$
a_2=
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}
$$

The coefficients are the entries of $x$, namely $x_1=4$ and $x_2=2$. Then

$$
Ax = x_1 a_1 + x_2 a_2 = 4a_1 + 2a_2
$$

Substituting the columns gives

$$
Ax=
4
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
+
2
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}
$$

Scaling each column:

$$
Ax=
\begin{pmatrix}
8 \\
4 \\
\end{pmatrix}
+
\begin{pmatrix}
-2 \\
6 \\
\end{pmatrix}
$$

Adding the two vectors:

$$
Ax=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
$$

This agrees with the row-by-row computation above.

#### Conclusion

For any matrix $A$ with columns $a_1,\dots,a_n$ and any vector $x$ with entries $x_1,\dots,x_n$,

$$
Ax = x_1 a_1 + x_2 a_2 + \dots + x_n a_n
$$

So $Ax$ is a linear combination of the columns of $A$, and the entries of $x$ are the coefficients. In this exercise, the vector $Ax$ is obtained by taking $4$ copies of the first column and $2$ copies of the second column.