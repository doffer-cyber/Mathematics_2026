### Solution 12. Finding Inverses Without Starting from Scratch

Given:

A^(-1) =

|  2  -1 |
| -3   2 |


Step 1. Compute (3A)^(-1).

Using the scalar multiplication property:

(3A)^(-1) = (1/3) A^(-1)

Substituting:

(3A)^(-1) =

(1/3) x |  2  -1 |
         | -3   2 |

Therefore:

(3A)^(-1) =

|  2/3  -1/3 |
| -1     2/3 |


Step 2. Compute (A^T)^(-1).

Using the transpose property:

(A^T)^(-1) = (A^(-1))^T

Taking the transpose means switching rows and columns.

Therefore:

(A^T)^(-1) =

|  2  -3 |
| -1   2 |


Step 3. Compute (A^2)^(-1).

Using the power property:

(A^2)^(-1) = (A^(-1))^2

Therefore:

(A^2)^(-1) = A^(-1) x A^(-1)

|  2  -1 |   |  2  -1 |
| -3   2 | x | -3   2 |

Multiplying:

| 2(2)+(-1)(-3)    2(-1)+(-1)(2) |
| (-3)(2)+2(-3)    (-3)(-1)+2(2) |

Simplifying:

(A^2)^(-1) =

|   7   -4 |
| -12    7 |


Final Answers:

1. (3A)^(-1) =

   |  2/3  -1/3 |
   | -1     2/3 |

2. (A^T)^(-1) =

   |  2  -3 |
   | -1   2 |

3. (A^2)^(-1) =

   |   7   -4 |
   | -12    7 |


Conclusion:

The inverse properties allow us to calculate the required
inverses directly without finding the original matrix A.