### Solution 11. When Do Matrices Commute?

Step 1. Compute both products.

AB =

| a + c | b + d |
|-------|-------|
| c     | d     |


BA =

| a | a + b |
|---|-------|
| c | c + d |


Step 2. Set AB = BA.

Comparing corresponding entries:

a + c = a
b + d = a + b
c = c
d = c + d

Simplifying:

c = 0
d = a

Step 3. Determine the general form of B.

There are no restrictions on a and b.

Therefore:

B =

| a | b |
|---|---|
| 0 | a |


Final Answer:

The matrices commute if and only if:

c = 0 and d = a.

The general form is:

B = | a  b |
    | 0  a |

where a and b are arbitrary real numbers.

Conclusion:

Although matrix multiplication is generally noncommutative,
certain matrices commute. In this case, B must have equal
diagonal entries and a zero lower-left entry.