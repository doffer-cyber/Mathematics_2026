### Solution 14. A Matrix That Is Its Own Inverse

Given:

A^2 = I

We want to show that:

A^(-1) = A


Step 1. Use the definition of the inverse.

By definition, a matrix A^(-1) is the inverse of A if:

A x A^(-1) = I

and

A^(-1) x A = I

Since A^2 = I, we can write:

A x A = I

Therefore, A satisfies the definition of its own inverse.

Hence:

A^(-1) = A


Step 2. Construct an example.

Choose a matrix different from I and -I:

A =

| 1   0 |
| 0  -1 |


Step 3. Verify the condition by multiplication.

Calculate A^2:

A^2 =

| 1   0 |   | 1   0 |
| 0  -1 | x | 0  -1 |

Multiplying:

A^2 =

| 1(1)+0(0)       1(0)+0(-1) |
| 0(1)+(-1)(0)    0(0)+(-1)(-1) |

Simplifying:

A^2 =

| 1   0 |
| 0   1 |


Therefore:

A^2 = I


Final Answer:

A^(-1) = A

An example of such a matrix is:

A =

| 1   0 |
| 0  -1 |


Conclusion:

A matrix satisfying A^2 = I is its own inverse.
Such a matrix is called an involutory matrix.

The example above confirms that a matrix different
from both I and -I can also be its own inverse.