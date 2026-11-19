### Exercise 11. When Do Matrices Commute?

Given

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}.
$$

Find the conditions on $a,b,c,d$ under which $AB=BA$. Describe the general form of all such matrices $B$.

> **Why this exercise:** deepens the idea of noncommutativity by finding the conditions under which commutativity does hold

#### Solution

**Step 1. Compute both products.**

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
=
\begin{pmatrix}
a+c & b+d \\
c & d \\
\end{pmatrix}
$$

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
=
\begin{pmatrix}
a & a+b \\
c & c+d \\
\end{pmatrix}
$$

**Step 2. Compare the entries.**

The equality $AB=BA$ holds if and only if all four corresponding entries are equal:

$$
\begin{cases}
a+c = a, \\
b+d = a+b, \\
c = c, \\
d = c+d.
\end{cases}
$$

**Step 3. Simplify the system.**

The first equation gives $c=0$.

The second equation gives $d=a$.

The third equation is always true.

The fourth equation gives $c=0$, which is already known.

Therefore

$$
AB=BA \iff c=0 \ \text{and} \ d=a,
$$

while $a$ and $b$ are arbitrary real numbers.

**Step 4. General form of $B$.**

$$
B=
\begin{pmatrix}
a & b \\
0 & a \\
\end{pmatrix},
\qquad a,b\in\mathbb{R}.
$$

Equivalently,

$$
B=aI+bN,
\qquad
I=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix},
\quad
N=
\begin{pmatrix}
0 & 1 \\
0 & 0 \\
\end{pmatrix}.
$$

Since $A=I+N$, the matrices commuting with $A$ are exactly the polynomials in $A$ of degree at most $1$. They form a two-parameter family.

**Step 5. Verification.**

For $c=0$ and $d=a$:

$$
AB=
\begin{pmatrix}
a & a+b \\
0 & a \\
\end{pmatrix}
=BA.
$$

**Answer.** $AB=BA$ if and only if $c=0$ and $d=a$, that is, $B$ is upper triangular with equal diagonal entries, and $b$ is arbitrary.