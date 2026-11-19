### Solution 3. Vector Normalization

Given:

v = (3, 4)

We want to find a unit vector e with the same direction
and orientation as v.


Step 1. Calculate the length of v.

The length of a vector is:

||v|| = sqrt(x^2 + y^2)

Substitute the coordinates:

||v|| = sqrt(3^2 + 4^2)

||v|| = sqrt(9 + 16)

||v|| = sqrt(25)

Therefore:

||v|| = 5


Step 2. Find the unit vector e.

To normalize a vector, divide each component
by its length.

e = v / ||v||

e = (3/5, 4/5)

Therefore:

e = (3/5, 4/5)


Step 3. Verify that ||e|| = 1.

Calculate the length:

||e|| = sqrt((3/5)^2 + (4/5)^2)

||e|| = sqrt(9/25 + 16/25)

||e|| = sqrt(25/25)

Therefore:

||e|| = 1


Step 4. Reconstruct v.

We want to verify:

v = ||v||e

Substitute the values:

v = 5(3/5, 4/5)

v = (3, 4)

Therefore:

v = ||v||e


Final Answer:

||v|| = 5

e = (3/5, 4/5)

||e|| = 1

v = 5e = (3, 4)


Conclusion:

During normalization:
- The length of the vector changes to 1.
- The direction remains unchanged.
- The orientation remains unchanged.

Normalization separates the direction of a vector
from its magnitude.