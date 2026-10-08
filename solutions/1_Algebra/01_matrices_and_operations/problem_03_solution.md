### Exercise 3. When Can Matrices Be Multiplied?

The matrix sizes are

$$
A_{2\times3},\qquad B_{3\times4},\qquad C_{4\times2},\qquad D_{2\times2}.
$$

For the products

$$
AB,\ BA,\ BC,\ CB,\ AC,\ CA,\ AD,\ DA
$$

determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

> **Why this exercise:** forces an understanding of dimension compatibility before carrying out any calculation.

#### Solution

**Compatibility condition.** If $X$ has size $m\times n$ and $Y$ has size $p\times q$, then the product $XY$ is defined if and only if $n=p$, that is, the number of columns of $X$ equals the number of rows of $Y$. In this case $XY$ has size $m\times q$.

**Product $AB$**

Here $A$ is $2\times3$ and $B$ is $3\times4$. The inner dimensions are $3$ and $3$, which are equal. The product is defined, and $AB$ has size $2\times4$.

**Product $BA$**

Here $B$ is $3\times4$ and $A$ is $2\times3$. The inner dimensions are $4$ and $2$, which are not equal. The product is not defined.

**Product $BC$**

Here $B$ is $3\times4$ and $C$ is $4\times2$. The inner