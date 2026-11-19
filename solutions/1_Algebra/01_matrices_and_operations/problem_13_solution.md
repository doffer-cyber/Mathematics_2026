### Exercise 13. A Recurrence Written in Matrix Form

Let

$$
F=
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}.
$$

Compute $F^2$, $F^3$, $F^4$, and $F^5$. Compare the numbers obtained with the sequence

$$
0,1,1,2,3,5,8,\ldots
$$

and describe the relationship you observe. Then compute

$$
F
\begin{pmatrix}
a \\
b \\
\end{pmatrix}
$$

and explain how this multiplication performs one recurrence step: it creates the sum of two consecutive terms and keeps one of them for the next step.

> **Why this exercise:** shows the connection between matrix powers and a simple numerical recurrence.

#### Solution

**Step 1. Compute $F^2$.**

$$
F^2=F\cdot F=
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}
$$

Multiplying row by column gives

$$
F^2=
\begin{pmatrix}
1\cdot 1+1\cdot 1 & 1\cdot 1+1\cdot 0 \\
1\cdot 1+0\cdot 1 & 1\cdot 1+0\cdot 0 \\
\end{pmatrix}
$$

$$
F^2=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}.
$$

**Step 2. Compute $F^3$.**

$$
F^3=F^2\cdot F=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}
$$

$$
F^3=
\begin{pmatrix}
2\cdot 1+1\cdot 1 & 2\cdot 1+1\cdot 0 \\
1\cdot 1+1\cdot 1 & 1\cdot 1+1\cdot 0 \\
\end{pmatrix}
$$

$$
F^3=
\begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix}.
$$

**Step 3. Compute $F^4$.**

$$
F^4=F^3\cdot F=
\begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}
$$

$$
F^4=
\begin{pmatrix}
3\cdot 1+2\cdot 1 & 3\cdot 1+2\cdot 0 \\
2\cdot 1+1\cdot 1 & 2\cdot 1+1\cdot 0 \\
\end{pmatrix}
$$

$$
F^4=
\begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix}.
$$

**Step 4. Compute $F^5$.**

$$
F^5=F^4\cdot F=
\begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}
$$

$$
F^5=
\begin{pmatrix}
5\cdot 1+3\cdot 1 & 5\cdot 1+3\cdot 0 \\
3\cdot 1+2\cdot 1 & 3\cdot 1+2\cdot 0 \\
\end{pmatrix}
$$

$$
F^5=
\begin{pmatrix}
8 & 5 \\
5 & 3 \\
\end{pmatrix}.
$$

**Step 5. Relationship with the Fibonacci sequence.**

Denote the sequence $0,1,1,2,3,5,8,\ldots$ by $F_0,F_1,F_2,\ldots$, so that

$$
F_0=0, \qquad F_1=1, \qquad F_{k+1}=F_k+F_{k-1}.
$$

The computed powers have the form

$$
F^n=
\begin{pmatrix}
F_{n+1} & F_n \\
F_n & F_{n-1} \\
\end{pmatrix},
\qquad n\ge 1.
$$

Check for $n=5$: $F_6=8$, $F_5=5$, $F_4=3$, which agrees with $F^5$. The same check works for $n=1,2,3,4$.

*Proof by induction.* For $n=1$ the formula gives

$$
F^1=
\begin{pmatrix}
F_2 & F_1 \\
F_1 & F_0 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix},
$$

which is the matrix $F$. Assume the formula holds for some $n\ge 1$. Then

$$
F^{n+1}=F^n\cdot F=
\begin{pmatrix}
F_{n+1} & F_n \\
F_n & F_{n-1} \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}
$$

$$
F^{n+1}=
\begin{pmatrix}
F_{n+1}+F_n & F_{n+1} \\
F_n+F_{n-1} & F_n \\
\end{pmatrix}.
$$

By the recurrence, $F_{n+1}+F_n=F_{n+2}$ and $F_n+F_{n-1}=F_{n+1}$, hence

$$
F^{n+1}=
\begin{pmatrix}
F_{n+2} & F_{n+1} \\
F_{n+1} & F_n \\
\end{pmatrix},
$$

which is the formula for $n+1$.

**Step 6. One recurrence step as a matrix multiplication.**

$$
F
\begin{pmatrix}
a \\
b \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot a+1\cdot b \\
1\cdot a+0\cdot b \\
\end{pmatrix}
$$

$$
F
\begin{pmatrix}
a \\
b \\
\end{pmatrix}=
\begin{pmatrix}
a+b \\
a \\
\end{pmatrix}.
$$

The first component is the sum of the two consecutive terms $a$ and $b$. The second component is $a$, the larger of the two old terms, which is kept for the next step.

For $a=F_{n+1}$ and $b=F_n$ this gives

$$
F
\begin{pmatrix}
F_{n+1} \\
F_n \\
\end{pmatrix}=
\begin{pmatrix}
F_{n+2} \\
F_{n+1} \\
\end{pmatrix},
$$

so one multiplication by $F$ moves the pair of consecutive terms one position forward. Starting from the vector $(F_1,F_0)^T=(1,0)^T$ and applying $F$ exactly $n$ times gives

$$
F^n
\begin{pmatrix}
1 \\
0 \\
\end{pmatrix}=
\begin{pmatrix}
F_{n+1} \\
F_n \\
\end{pmatrix},
$$

which is the first column of $F^n$.

**Answer.**

$$
F^2=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix},
\qquad
F^3=
\begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix},
$$

$$
F^4=
\begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix},
\qquad
F^5=
\begin{pmatrix}
8 & 5 \\
5 & 3 \\
\end{pmatrix}.
$$

In general $F^n$ has the entries $F_{n+1}$, $F_n$, $F_n$, $F_{n-1}$, and multiplication by $F$ maps $(a,b)^T$ to $(a+b,a)^T$.