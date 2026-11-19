### Exercise 14. Rotation Matrices

The matrix for a rotation through an angle $\theta$ is

$$
R(\theta)=
\begin{pmatrix}
\cos\theta & -\sin\theta \\
\sin\theta & \cos\theta \\
\end{pmatrix}.
$$

Compute $R(\alpha)R(\beta)$ and, using the angle-sum formulas for sine and cosine, show that

$$
R(\alpha)R(\beta)=R(\alpha+\beta).
$$

Explain the result geometrically.

> **Why this exercise:** shows the consistency between matrix algebra and the geometry of composing rotations.

#### Solution

**Step 1. Write the product.**

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos\alpha & -\sin\alpha \\
\sin\alpha & \cos\alpha \\
\end{pmatrix}
\begin{pmatrix}
\cos\beta & -\sin\beta \\
\sin\beta & \cos\beta \\
\end{pmatrix}
$$

**Step 2. Multiply row by column.**

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos\alpha\cos\beta-\sin\alpha\sin\beta & -\cos\alpha\sin\beta-\sin\alpha\cos\beta \\
\sin\alpha\cos\beta+\cos\alpha\sin\beta & -\sin\alpha\sin\beta+\cos\alpha\cos\beta \\
\end{pmatrix}
$$

**Step 3. Apply the angle-sum formulas.**

The angle-sum formulas are

$$
\cos(\alpha+\beta)=\cos\alpha\cos\beta-\sin\alpha\sin\beta,
$$

$$
\sin(\alpha+\beta)=\sin\alpha\cos\beta+\cos\alpha\sin\beta.
$$

The entries of the product are identified as follows.

- Entry $(1,1)$: $\cos\alpha\cos\beta-\sin\alpha\sin\beta=\cos(\alpha+\beta)$.
- Entry $(1,2)$: $-\cos\alpha\sin\beta-\sin\alpha\cos\beta=-\sin(\alpha+\beta)$.
- Entry $(2,1)$: $\sin\alpha\cos\beta+\cos\alpha\sin\beta=\sin(\alpha+\beta)$.
- Entry $(2,2)$: $\cos\alpha\cos\beta-\sin\alpha\sin\beta=\cos(\alpha+\beta)$.

**Step 4. Conclusion.**

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos(\alpha+\beta) & -\sin(\alpha+\beta) \\
\sin(\alpha+\beta) & \cos(\alpha+\beta) \\
\end{pmatrix}
$$

$$
R(\alpha)R(\beta)=R(\alpha+\beta).
$$

**Step 5. Geometric explanation.**

The matrix $R(\theta)$ rotates every vector of the plane counterclockwise about the origin through the angle $\theta$. For a vector $v$, the product $R(\alpha)R(\beta)v$ means that $v$ is first rotated through $\beta$ and the result is then rotated through $\alpha$. The total effect is a rotation through the angle $\alpha+\beta$, which is exactly the action of $R(\alpha+\beta)$. Hence composing two rotations about the origin corresponds to adding their angles, and the matrix product encodes this composition.

**Step 6. Consequence.**

Since $\alpha+\beta=\beta+\alpha$, we also have

$$
R(\alpha)R(\beta)=R(\beta)R(\alpha).
$$

Thus rotations in the plane about the origin commute with each other, in contrast to general matrices.

**Answer.** $R(\alpha)R(\beta)=R(\alpha+\beta)$, because the entries of the product are the angle-sum formulas for cosine and sine. Geometrically, rotating through $\beta$ and then through $\alpha$ is the same as rotating once through $\alpha+\beta$.