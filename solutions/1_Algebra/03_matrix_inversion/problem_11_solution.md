### Solution 11. When Do Matrices Commute?

Given

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},
\qquad
B=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}.
$$

We want to find the conditions under which

$$
AB=BA.
$$

**Step 1. Calculate $AB$.**

$$
AB=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
$$

$$
AB=
\begin{pmatrix}
a+c & b+d \\
c & d \\
\end{pmatrix}.
$$

**Step 2. Calculate $BA$.**

$$
BA=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

$$
BA=
\begin{pmatrix}
a & a+b \\
c & c+d \\
\end{pmatrix}.
$$

**Step 3. Set $AB=BA$.**

Equating the corresponding entries gives

$$
\begin{cases}
a+c=a, \\
b+d=a+b, \\
c=c, \\
d=c+d.
\end{cases}
$$

Simplifying:

$$
\begin{cases}
c=0, \\
d=a, \\
0=0, \\
c=0.
\end{cases}
$$

**Step 4. Determine the general form of $B$.**

The conditions are

$$
c=0,\qquad d=a.
$$

There are no restrictions on $a$ and $b$.

Therefore, the general form of all matrices $B$ satisfying $AB=BA$ is

$$
B=
\begin{pmatrix}
a & b \\
0 & a \\
\end{pmatrix},
\qquad a,b\in\mathbb{R}.
$$

**Final Answer:**

$$
\boxed{
B=
\begin{pmatrix}
a & b \\
0 & a \\
\end{pmatrix}
}
$$

Thus, matrices $A$ and $B$ commute if and only if $c=0$ and $d=a$.

**Conclusion:** Matrix multiplication is generally noncommutative, but certain matrices do commute. In this case, every matrix $B$ with equal diagonal entries and a zero lower-left entry commutes with $A$.