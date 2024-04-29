---
title: Vectors Operations - An Intuition
weight: 24
math: true
next: matrix-operations-intuition
cascade:
  type: docs
sidebar:
  open: true
---

<br>
<div style="text-align: justify;">

We have seen different vector operations earlier. As we assumed earlier that a vector to be an arrow whose tail is at the origin of the co-ordinate system and head at the point of the vector. Vectors are denoted as $\vec{z}$ with a arrow in the head or as an (row or column) array. So, every operation that we studied earlier has a geometric representation. This note will give intuition behind what happens geometrically during these operations.

## Vector addition

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

## Scalar-Vector multiplication

Scalar-Vector multiplication is also called as `scaling`. If we multiply a vector $\vec{v}$ by a scalar $a$, the resulting vector is a scaled version of the vector $\vec{v}$. In general, the multiplication of a scalar and a vector is defined as,

$\begin{bmatrix}x_1 \\\\ x_2 \\\\ \vdots \\\\ x_n\end{bmatrix} \times a = \begin{bmatrix}ax_1 \\\\ ax_2 \\\\ \vdots \\\\ ax_n\end{bmatrix}$

For example, if we multiply a vector $\vec{v}$ by $2$, it will stretch out that vector so that it is two times its original length.

![Stretching a vector](/images/linear-alegbra/vectors/streching_a_vector.svg)

If we multiply by $\frac{1}{3}$, it will squish it down so that it is one-third its original length.

![Squishing a vector](/images/linear-alegbra/vectors/squishing_a_vector.svg)

If we multiply by $-1$, the vector will get flipped around. If you multiply −1.5, the vector gets flipped around and stretched out by a factor of 1.5.

![Flipping and Strectching a vector](/images/linear-alegbra/vectors/flipping_and_streching_a_vector.svg)

Here, scaling is `either streching or squishing` and a `optional flipping` of the direction of a vector.

## Scalar-Vector addition

Scalar-Vector addition is also called as `broadcasting`. If we add a scalar $a$ to a vector $\vec{v}$, the resulting vector is a translated and scaled version of the vector $\vec{v}$. In general, the addition of a scalar and a vector is defined as,

$\begin{bmatrix}x_1 \\\\ x_2 \\\\ \vdots \\\\ x_n\end{bmatrix} + a = \begin{bmatrix}a+x_1 \\\\ a+x_2 \\\\ \vdots \\\\ a+x_n\end{bmatrix}$

For example, if we add a scalar $2$ to the vector $v = \begin{bmatrix} 1 \\\\ 2 \end{bmatrix}$, the resultant vector will be,
$v = \begin{bmatrix} 1+2 \\\\ 2+2 \end{bmatrix} = \begin{bmatrix} 3 \\\\ 4 \end{bmatrix}$

## Linear Combination and Span

Any time when we scale and add two vectors it's called a "linear combination" of those two vectors.

![Linear Combination](/images/linear-algebra/vector-operations/linear_combination.svg)

Where does the word "linear" come from here? What does this have to do with lines? Well, when you multiply a scalar by a vector, it changes the magnitude of that vector. Multiplying every real number by the vector produces an infinite line that passes through the origin and the point defined by the vector.

![Linear Combination and Lines](/images/linear-algebra/vector-operations/linear_combination_and_lines.svg)

So a linear combination of two vectors is a method of combining these two lines. For most pairs of vectors, if you let both scalars range freely and consider every possible vector you could get, you will be able to reach every possible point on the plane. Every two-dimensional vector is within your grasp. Basis vectors tend to span the whole space.

<style>
    video.center {
        display: block;
        margin-top: 20px;
        margin-left: auto;
        margin-right: auto;
    }
</style>
<video width="640" height="360" class="center" controls>
  <source src="/videos/linear-algebra/vector-operations/vectors_r2_span.mp4" type="video/mp4">
</video>

However, if the two vectors happen to line up, the lines produced by the scalar multiplication will be the same line, so adding them together can't yield a vector outside of that line.

<video width="640" height="360" class="center" controls>
  <source src="/videos/linear-algebra/vector-operations/span_lineup.mp4" type="video/mp4">
</video>

There's a third possibility too: Both vectors could be the zero vector, in which case there will be no lines and the linear combination just be stuck at the origin.

### Vector multiplication

There are three different most commonly used vector products. Every product serves a different purpose. They are,

- Dot product
- Cross product
- Hadamard product

### Dot Product

Dot product between two vectors $\vec{v}$ and $\vec{w}$ is denoted by $\cdot$ and defined as,
$$\vec{v} \cdot \vec{w} = \sum_{i=1}^{n} v_iw_i$$

But the above operation has a very good geometric representation. To think about the dot products of two vectors, imagine projecting $w$ onto the line that passes through the origin and the tip of $v$. Multiply the length of this projection by the length of $v$ and you have the dot product of $v$ and $w$.

![Dot Product - Case One](/images/linear-algebra/vector-operations/dot_product.svg)

When the projection of $w$ is pointing in the opposite direction from $v$, the dot product will actually be negative. When they are perpendicular to each other, the projection of one onto the other is the zero vector.

![Dot Product - Case Two](/images/linear-algebra/vector-operations/dot_product_opposite.svg)

Notice that the sign of the dot product will tells you how much two vectors $v$ and $w$ align or the angle between them.

> - $v \dot w > 0$ - When they point in similar directions (i.e) the angle between them is less than $90\degree$
> - $v \dot w = 0$ - When they are perpendicular (i.e) the angle between them is $90\degree$
> - $v \dot w < 0$ - When they point in opposite directions (i.e) the angle between them is greater than $90\degree$

![Dot Product - Sign](/images/linear-algebra/vector-operations/dot_product_sign.svg)

If the tip of $w$ lies in the green region the dot product is positive, if it lies in the red region the dot product is negative, and if it lies on the blue line perpendicular $v$ the dot product is zero.

This geometric interpretation of dot product is very asymmetric, in that it treats the two vectors very differently.

</div>
