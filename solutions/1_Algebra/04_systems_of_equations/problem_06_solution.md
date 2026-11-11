### Exercise 6. A System with a Parameter — Which Cases Actually Occur?

Analyze, depending on the parameter $a$, the system

$$
\begin{cases}
x+y=2, \\
ax+ay=4.
\end{cases}
$$

Among the three possibilities — exactly one solution, infinitely many solutions, no solution — determine which actually occur and for which values of $a$. If one type cannot occur, explain why.

> **Why this exercise:** teaches how to analyze a parameter without assuming in advance that all theoretically possible cases must occur in a specific system.

**Solution**

**Step 1. Augmented matrix**

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
a & a & \mid & 4 \\
\end{pmatrix}
$$

**Step 2. Eliminate $x$ from row 2**

Apply $R_2 \to R_2-aR_1$:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 4-2a \\
\end{pmatrix}
$$

The second row represents the equation

$$
0=4-2a
$$

Its truth depends only on the value of $a$. No division by $a$ was needed, so the elimination is valid for every real $a$, including $a=0$.

**Step 3. Case $a\neq 2$**

Then $4-2a\neq 0$, so the second row reads $0=c$ with $c\neq 0$. This is a contradiction.

The system has **no solution**.

Direct explanation: if $x+y=2$, then

$$
ax+ay=a(x+y)=2a
$$

and the second equation requires $2a=4$, which holds only for $a=2$.

**Step 4. Case $a=2$**

Then $4-2a=0$ and the second row becomes $0=0$:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

The second equation is $2(x+y)=4$, a multiple of the first equation, so it is redundant. The system is consistent, has 1 pivot and 2 unknowns, so there is $2-1=1$ free variable.

The column of $y$ has no pivot, so set $y=t$, where $t\in\mathbb{R}$. From row 1:

$$
x=2-t
$$

The solution set is

$$
x=2-t, \qquad y=t, \qquad t\in\mathbb{R}
$$

In vector form:

$$
\begin{pmatrix}
x \\
y \\
\end{pmatrix}=
\begin{pmatrix}
2 \\
0 \\
\end{pmatrix}+t
\begin{pmatrix}
-1 \\
1 \\
\end{pmatrix}
$$

The system has **infinitely many solutions**.

**Step 5. Check for $a=2$**

Choose $t=1$. Then $(x,\,y)=(1,\,1)$:

- Equation 1: $1+1=2$.
- Equation 2: $2\cdot 1+2\cdot 1=4$.

The point satisfies both equations.

**Step 6. Why exactly one solution cannot occur**

The coefficient matrix

$$
\begin{pmatrix}
1 & 1 \\
a & a \\
\end{pmatrix}
$$

has two identical columns for every value of $a$. After elimination its second row is always zero, so it has at most 1 pivot, while there are 2 unknowns. Hence at least one free variable always exists, or the system is inconsistent.

A unique solution would require 2 pivots, which is impossible for this matrix for every $a$.

**Summary**

| Value of $a$ | Number of solutions |
|---|---|
| $a\neq 2$ | none |
| $a=2$ | infinitely many (one free parameter) |
| no value of $a$ | exactly one |

Only two of the three theoretically possible cases occur. The case of exactly one solution never occurs, because the structure of the coefficient matrix excludes it independently of $a$.