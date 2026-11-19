### Solution 11. A Parameter in a System of Three Equations

Given:

x + y + z = 1
x + ty + z = 2
x + y + tz = 3

We want to analyze the number of solutions depending on t.


Step 1. Eliminate x.

Subtract the first equation from the second equation:

(x + ty + z) - (x + y + z) = 2 - 1

ty - y = 1

(t - 1)y = 1


Now subtract the first equation from the third equation:

(x + y + tz) - (x + y + z) = 3 - 1

tz - z = 2

(t - 1)z = 2


Step 2. Analyze the parameter t.

We obtain:

(t - 1)y = 1
(t - 1)z = 2

There are two possible cases.

CASE 1. When t = 1

Substituting t = 1:

0y = 1
0z = 2

Both equations are impossible.

Therefore, the system has no solution when:

t = 1


CASE 2. When t is not equal to 1

We can divide both equations by (t - 1).

Therefore:

y = 1/(t - 1)

z = 2/(t - 1)


Step 3. Find x.

Using the first original equation:

x + y + z = 1

Substitute the values of y and z:

x + 1/(t - 1) + 2/(t - 1) = 1

x + 3/(t - 1) = 1

x = 1 - 3/(t - 1)

Simplifying:

x = (t - 4)/(t - 1)


Step 4. Write the general solution.

For t not equal to 1:

x = (t - 4)/(t - 1)
y = 1/(t - 1)
z = 2/(t - 1)


Final Answer:

CASE 1:
When t = 1, the system has no solution.

CASE 2:
When t is not equal to 1, the system has exactly one solution:

x = (t - 4)/(t - 1)
y = 1/(t - 1)
z = 2/(t - 1)


Conclusion:

- If t = 1, there is no solution.
- If t is not equal to 1, there is exactly one solution.
- There is no value of t for which the system has infinitely many solutions.

The important point is that division by (t - 1) is valid
only when t is not equal to 1.

Therefore, t = 1 must be analyzed separately before
continuing with the elimination process.