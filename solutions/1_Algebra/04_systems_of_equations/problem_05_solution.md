### Exercise 5. Row Echelon Form and Number of Solutions

For the augmented matrix

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 3 \\
0 & 1 & 2 & \mid & 1 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

> **Why this exercise:** teaches how to read information about solutions directly from row echelon form.

**Solution**

**Step 1. Read the matrix as a system**

The columns correspond to $x$, $y$, $z$ and the right-hand side. The rows represent the equations

$$
\begin{cases}
x+2y-z=3, \\
y+2z=1, \\
0=0.
\end{cases}
$$

**Step 2. Consistency and pivots**

The third row is $0=0$. It is always true, so it gives no contradiction and no restriction. The system is consistent.

The pivots are in column 1 ($x$) and column 2 ($y$). The matrix has 2 pivots and 3 unknowns.

**Step 3. Number of solutions**

The system is consistent and the number of pivots is smaller than the number of unknowns. Hence the system has infinitely many solutions.

**Step 4. Free variables**

The number of free variables is

$$
3-2=1
$$

The column of $z$ has no pivot, so $z$ is the free variable. Set $z=t$, where $t\in\mathbb{R}$.

**Step 5. Back substitution**

From row 2:

$$
y=1-2z=1-2t
$$

From row 1:

$$
\begin{aligned}
x &= 3-2y+z \\
  &= 3-2(1-2t)+t \\
  &= 1+5t
\end{aligned}
$$

**Parametric form of the solution**

$$
x=1+5t, \qquad y=1-2t, \qquad z=t, \qquad t\in\mathbb{R}
$$

In vector form:

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}=
\begin{pmatrix}
1 \\
1 \\
0 \\
\end{pmatrix}+t
\begin{pmatrix}
5 \\
-2 \\
1 \\
\end{pmatrix}
$$

The solution set is a line in $\mathbb{R}^3$ passing through $(1,\,1,\,0)$ with direction vector $(5,\,-2,\,1)$.

**Step 6. Check**

For $t=0$ the point is $(1,\,1,\,0)$:

- Row 1: $1+2\cdot 1-0=3$.
- Row 2: $1+2\cdot 0=1$.

For $t=1$ the point is $(6,\,-1,\,1)$:

- Row 1: $6+2\cdot(-1)-1=3$.
- Row 2: $-1+2\cdot 1=1$.

Both points satisfy the system.

**How the number of free variables is determined**

For a consistent system, the number of free variables equals the number of unknowns minus the number of pivots. Free variables correspond to the columns without a pivot:

- Pivot in every unknown column: exactly one solution.
- Fewer pivots than unknowns: infinitely many solutions, with $3-2=1$ free parameter here.
- A row of the form $0 \;\; 0 \;\; 0 \;\; \mid \;\; c$ with $c\neq 0$: no solution.