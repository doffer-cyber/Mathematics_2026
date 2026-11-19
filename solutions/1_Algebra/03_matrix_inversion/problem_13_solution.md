### Solution 13. Undoing a Composite Transformation

Given:

S =

| 2  0 |
| 0  1 |

H =

| 1  1 |
| 0  1 |

T = HS


Step 1. Compute T, then find its inverse.

T = HS

T =

| 1  1 |   | 2  0 |
| 0  1 | x | 0  1 |

Multiplying:

T =

| 2  1 |
| 0  1 |


Now calculate the inverse using the 2x2 inverse formula.

For a matrix:

| a  b |
| c  d |

The inverse is:

1/(ad-bc) x

|  d  -b |
| -c   a |


Substituting:

det(T) = (2 x 1) - (1 x 0) = 2

Therefore:

T^(-1) =

1/2 x | 1  -1 |
       | 0   2 |

T^(-1) =

| 1/2  -1/2 |
|  0      1 |


Step 2. Use the inverse of a product property.

The property is:

(HS)^(-1) = S^(-1)H^(-1)

First, calculate the individual inverses.

S^(-1) =

| 1/2  0 |
|  0   1 |

H^(-1) =

| 1  -1 |
| 0   1 |


Now multiply S^(-1)H^(-1).

| 1/2  0 |   | 1  -1 |
|  0   1 | x | 0   1 |

The result is:

T^(-1) =

| 1/2  -1/2 |
|  0      1 |


Step 3. Compute H^(-1)S^(-1) (incorrect order).

Now multiply in the opposite order:

| 1  -1 |   | 1/2  0 |
| 0   1 | x |  0   1 |

The result is:

H^(-1)S^(-1) =

| 1/2  -1 |
|  0    1 |


Step 4. Compare the results.

Correct order:

| 1/2  -1/2 |
|  0      1 |

Incorrect order:

| 1/2  -1 |
|  0    1 |


The two matrices are different.

This demonstrates that matrix multiplication is not
commutative and the order of inverse operations matters.


Final Answer:

T^(-1) =

| 1/2  -1/2 |
|  0      1 |


Conclusion:

When undoing a composition of operations, we undo them
from the end.

Since T = HS, the shear H is applied after the scaling S.

To undo the transformation, we must first undo H and
then undo S.

Therefore:

(HS)^(-1) = S^(-1)H^(-1)

The order of the inverse matrices is reversed.