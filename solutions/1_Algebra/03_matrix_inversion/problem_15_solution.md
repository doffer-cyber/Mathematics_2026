### Solution 15. Two Methods for Solving the Same System

Given:

A =

| 2  1 |
| 1  3 |

b =

| 7 |
| 8 |

We want to solve:

Ax = b


METHOD 1. Using A^(-1)b

Step 1. Calculate the inverse of A.

For a 2x2 matrix:

A^(-1) = 1/(ad-bc) x

|  d  -b |
| -c   a |

Calculate the determinant:

det(A) = (2 x 3) - (1 x 1) = 5

Therefore:

A^(-1) = 1/5 x

|  3  -1 |
| -1   2 |


Step 2. Calculate A^(-1)b.

x = A^(-1)b

x = 1/5 x

|  3  -1 |   | 7 |
| -1   2 | x | 8 |

Multiplying:

x = 1/5 x

| 3(7) + (-1)(8) |
| (-1)(7) + 2(8) |

Simplifying:

x = 1/5 x

| 13 |
|  9 |

Therefore:

x =

| 13/5 |
|  9/5 |



METHOD 2. Using Gaussian Elimination

Step 1. Write the augmented matrix.

| 2  1 | 7 |
| 1  3 | 8 |

Step 2. Eliminate the first variable from the second row.

Use the row operation:

R2 = 2R2 - R1

The new augmented matrix is:

| 2  1 |  7 |
| 0  5 |  9 |

Step 3. Solve for the variables.

From the second row:

5x2 = 9

x2 = 9/5

Substitute into the first row:

2x1 + x2 = 7

2x1 + 9/5 = 7

2x1 = 26/5

x1 = 13/5

Therefore:

x =

| 13/5 |
|  9/5 |



STEP 3. Compare both methods.

Both methods give the same solution:

x =

| 13/5 |
|  9/5 |

Method 1 requires:
- Calculating the determinant.
- Finding the inverse matrix.
- Multiplying the inverse by b.

Method 2 requires:
- Performing one row elimination.
- Solving for the variables using substitution.


Final Conclusion:

Both methods produce the same solution.

In this example, Gaussian elimination is simpler because
it requires fewer calculations and avoids finding the
inverse matrix.

For larger systems, Gaussian elimination is generally
more practical than calculating the inverse explicitly.