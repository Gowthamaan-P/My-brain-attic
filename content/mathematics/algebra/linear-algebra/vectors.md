---
title: Vectors
weight: 12
math: true
next: linear-transformation
cascade:
  type: docs
sidebar:
  open: true
---

<br>
<div style="text-align: justify;">

Vectors are the basic building block of Linear algebra. There are different definitions for a vector and intuitions about a vector. So, what is a vector?

> - In Physics, a vector is a quantity with both magnitude and direction. Eg. Displacement
> - In Computer scince, a vector is a ordered list of numbers. (Note: Order of the elements does matter here).
> - In Mathematics, a vector is a point in a n-dimensional space.

To get a better understanding physically and mathematically, we assume a vector to be an arrow whose tail is at the origin of the co-ordinate system and head at the point of the vector. Vectors are denoted as $\vec{z}$ with a arrow in the head or as an (row or column) array. For example, $z = \begin{bmatrix}-3 & 2 \end{bmatrix}$, $z = \begin{bmatrix} -3 \\\\ 2 \end{bmatrix}$.

![Visualizing a vector](/images/linear-alegbra/vectors/visualizing_a_vector.svg)

So, what all these mean is that z is a point in space (Cartesian co-ordinate system or Cartesian space), whose tail is at the origin (0,0) and the tip is at (-3,2). To distinguish vectors from points, the convention is to write this n-numbers vertically or horizontally with square brackets around them. For better visulization and understanding, we stick to two and three dimensional vectors in this notes but vectors can be of any length in general.

## Basic Operations

As stated earlier, a scalar couldn't express a complex process. So, we use a vector. Similar to scalar, there are many mathematical operations defined for a vector.

### Vector addition

What happens when we add two vectors? Let's consider two vectors $\vec{v}$ and $\vec{w}$.

![Example vectors](/images/linear-alegbra/vectors/example_vectors.svg)

To add these two vectors, move the second vector so that it's tail sits on the tip of the first one. Then if you draw a new vector from the tail of the first one to where the tip of the second now sits, that new vector is their sum.

![Vector addition](/images/linear-alegbra/vectors/vector_addition.svg)

Why is this a reasonable thing to do? Why this definition of addition and not some other? Well, one way to think about it is that each vector represents a certain movement; a step with a certain distance and direction. If you take a step along the first vector, then take a step in the direction and distance described by the second vector, the overall effect is the same as if it just moved along the sum of those two vectors.

Consider two vectors, $v = \begin{bmatrix}1 \\\\ 2\end{bmatrix}$ and $w = \begin{bmatrix}3 \\\\ -1\end{bmatrix}$. When you take their vector sum using this tip to tail method, you can think of a four step path from the tail of the first to the tip of the second:

```mermaid
flowchart LR
    A(Walk 1 to the right)
    -->B(Walk 2 up)
    -->C(Walk 3 to the right)
    -->D(Walk 1 down)
```

![Vector addition - Example](/images/linear-alegbra/vectors/vector_addition_example.svg)

Gathering all the steps, what we did effectively is that,

$v + w = \begin{bmatrix}1 \\\\ 2\end{bmatrix} + \begin{bmatrix}3 \\\\ -1\end{bmatrix} = \begin{bmatrix}1+3 \\\\ 2-1\end{bmatrix} = \begin{bmatrix}4 \\\\ 1\end{bmatrix}$

So, in general addition of two vectors of length $n$ can be defined as,

$\begin{bmatrix}x_1 \\\\ x_2 \\\\ . \\\\ . \\\\ . \\\\ x_n\end{bmatrix} + \begin{bmatrix}y_1 \\\\ y_2 \\\\ . \\\\ . \\\\ . \\\\ y_n\end{bmatrix} = \begin{bmatrix}x_1 + y_1 \\\\ x_2 + y_2 \\\\ . \\\\ . \\\\ . \\\\ x_n + y_n\end{bmatrix}$

`The length of the vectors should be equal for vector addition`.

### Vector multiplication

We will delve deep into vector multiplication after seeing Linear Transformations. Traditionally, vector multiplication is introduced very early on in a linear algebra course, but to get a full understanding of the role of vector multiplication, a strong intuition on linear transformation is really required. So, we will skip vector multiplication for now.

### Scalar-Vector addition

Scalar-Vector addition is also called as `broadcasting`.

### Scalar-Vector multiplication

Scalar-Vector multiplication is also called as `scaling`. If we multiply a vector $\vec{v}$ by a scalar $a$, the resulting vector is a scaled version of the vector $\vec{v}$. In general, the multiplication of a scalar and a vector is defined as,

$\begin{bmatrix}x_1 \\\\ x_2 \\\\ . \\\\ . \\\\ . \\\\ x_n\end{bmatrix} \times a = \begin{bmatrix}ax_1 \\\\ ax_2 \\\\ . \\\\ . \\\\ . \\\\ ax_n\end{bmatrix}$

For example, if we multiply a vector $\vec{v}$ by $2$, it will stretch out that vector so that it is two times its original length.

![Stretching a vector](/images/linear-alegbra/vectors/streching_a_vector.svg)

If we multiply by $\frac{1}{3}$, it will squish it down so that it is one-third its original length.

![Squishing a vector](/images/linear-alegbra/vectors/squishing_a_vector.svg)

If we multiply by $-1$, the vector will get flipped around. If you multiply −1.5, the vector gets flipped around and stretched out by a factor of 1.5.

![Flipping and Strectching a vector](/images/linear-alegbra/vectors/flipping_and_streching_a_vector.svg)

Here, scaling is `either streching or squishing` and a `optional flipping` of the direction of a vector.

</div>
