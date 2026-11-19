### Exercise 15. Combining Determinant Properties

Let $A$ and $B$ be invertible $2\times2$ matrices with

$$
\det A=-2,\qquad \det B=3.
$$

Without finding the entries of the matrices, compute

$$
\det\left(B^{-1}A^TB\right).
$$

State the determinant properties you use in order and explain why the factors involving $B$ eventually cancel.

> **Why this exercise:** tests the transfer of several known properties into one short problem instead of checking a single property again with numbers.

#### Solution

**Step 1. Properties used.**

- Multiplicativity: $\det(XY)=\det X\cdot\det Y$ for square matrices of the same size.
- Transpose: $\det(X^T)=\det X$.
- Inverse: $\det(X^{-1})=\dfrac{1}{\det X}$ for an invertible matrix $X$.

**Step 2. Split the product.**

By multiplicativity applied to the three factors $B^{-1}$, $A^T$ and $B$:

$$
\det\left(B^{-1}A^TB\right)=\det\left(B^{-1}\right)\cdot\det\left(A^T\right)\cdot\det B.
$$

**Step 3. Replace each factor.**

By the inverse property,

$$
\det\left(B^{-1}\right)=\frac{1}{\det B}=\frac{1}{3}.
$$

By the transpose property,

$$
\det\left(A^T\right)=\det A=-2.
$$

**Step 4. Substitute and compute.**

$$
\det\left(B^{-1}A^TB\right)=\frac{1}{3}\cdot(-2)\cdot 3=-2.
$$

**Step 5. Why the factors involving $B$ cancel.**

Determinants of matrices are ordinary numbers, and multiplication of numbers is commutative. Therefore the numbers $\det\left(B^{-1}\right)=\dfrac{1}{\det B}$ and $\det B$ can be moved next to each other and cancel:

$$
\frac{1}{\det B}\cdot\det B=1.
$$

This happens even though the matrices $B^{-1}$ and $B$ are not next to each other in the matrix product, and $A^T$ does not commute with $B$ in general. Taking determinants replaces the matrices by scalars, for which the order of the factors does not matter.

In general, for every invertible $B$ and every square $X$ of the same size,

$$
\det\left(B^{-1}XB\right)=\det X.
$$

So the determinant is unchanged by a similarity transformation, and the value depends only on $\det A$.

**Answer.**

$$
\det\left(B^{-1}A^TB\right)=-2.
$$