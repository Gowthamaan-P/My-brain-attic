---
title: Linear Transformation - An Intuition
weight: 22
next: vector-operations-intuition
math: true
cascade:
  type: docs
sidebar:
  open: true
---

<style>
    video.center {
        display: block;
        margin-top: 20px;
        margin-left: auto;
        margin-right: auto;
    }
</style>
<br>
<div style="text-align: justify;">

We have discussed what are linear transformations. Let us take a visual look into them to understand them better. For this note, the focus will simply be on what these linear transformations look like in the case of two-dimensions. All the discussions we make to two dimensional vectors and vector spaces can be scaled to $n$-dimensional vectors also.

As we discussed, Transformation is essentially a fancy word for function; it's something that takes in inputs, and spit out some output for each one. Specifically, in the context of linear algebra, we think about transformations that take in some vector, and spit out another vector. An example is a transformation takes some input vector and move it to the output vector.

<video width="640" height="360" class="center" controls>
  <source src="/videos/linear-algebra/transformation-intuition/transformation_example.mp4" type="video/mp4">
</video>

As discussed earlier, the transformation will connect two vector spaces, which means the transformation is applied to the whole space.

<video width="640" height="360" class="center" controls>
  <source src="/videos/linear-algebra/transformation-intuition/space_transformation.mp4" type="video/mp4">
</video>

It gets very crowded to think about all vectors all at once, each as an arrow. So let's think of each vector not as an arrow, but as a single point: the point where its tip sits. That way, to think about a transformation taking every possible input vector to its corresponding output vector, we watch every point in space move to some other point.

<video width="640" height="360" class="center" controls>
  <source src="/videos/linear-algebra/transformation-intuition/point_transformation.mp4" type="video/mp4">
</video>

As we know, linear algebra talks about linear transformations which preserve the notion of vector addition and scalar multiplication. Visually speaking, a transformation is "linear" if it has two properties: all lines must remain lines, without getting curved, and the origin must remain fixed in place.

![Conditions for Linear Transformation](/images/linear-algebra/transformation-intuition/linear_transformation_condition.png)

In general you should think of linear transformations as keeping grid lines parallel and evenly spaced, although they might change the angles between perpendicular grid lines. Some linear transformations are simple to think about, like rotations about the origin. Others are a little trickier to describe with words.

## Matrix as Transformations

How think about these transformations numerically? If we are creating a function that rotates the vector by $90\degree$, how do we represent this?

> It turns out we only need to observe the change in the basis vectors. As all the remaining vectors can be obtained as a linear combination of this vectors.

For the two dimensional $xy$ plane, the basis vectors are $\hat{\text{\i}} = \begin{bmatrix} 1 \\\\ 0\end{bmatrix} \text{ and } \hat{\text{\j}} = \begin{bmatrix} 0 \\\\ 1\end{bmatrix}$.

<video width="640" height="360" class="center" controls>
  <source src="/videos/linear-algebra/transformation-intuition/basis_vectors_2d.mp4" type="video/mp4">
</video>

For example, consider a vector $v$ with the coordinates $\begin{bmatrix} -1 \\\\ 2\end{bmatrix}$, meaning it is equal to $-1\hat{i} + 2\hat{j}$.

![Linear Transformation - Example Vector](/images/linear-algebra/transformation-intuition/transformation_vector_setup.svg)

If we play some transformation, and follow where all three of these vectors go, the property that grid lines remain parallel and evenly spaced has a really important consequence: the place where $v$ lands will be (-1) times the vector where $\hat{i}$ landed, plus 2 times the vector where $\hat{j}$ landed.

<video width="640" height="360" class="center" controls>
  <source src="/videos/linear-algebra/transformation-intuition/transformation.mp4" type="video/mp4">
</video>

![Linear Transformation - Example](/images/linear-algebra/transformation-intuition/transformation.svg)

In other words, it started as a certain combination of $\hat{i}$ and $\hat{j}$, and it ended up at that same linear combination of where those two vectors landed.

![Linear Transformation - Example Coordinates](/images/linear-algebra/transformation-intuition/transformation_coordinates.svg)

We can actually deduce the coordinates of $v$ without needing to watch the transformation visually.

![Linear Transformation - Example Coordinates](/images/linear-algebra/transformation-intuition/transformation_numerical.svg)

From the above, we can infer that the transformations in two dimensional space can represented using just 4 numbers (i.e) the coordinates of $\hat{i}$ and $\hat{j}$. In practice, we pack these two vectors in a $2\times 2$ matrix to represent a linear transformation.

![Matrix as Linear Transformation](/images/linear-algebra/transformation-intuition/matrix_as_transformation.svg)

If you're given a $2\times 2$ matrix describing a linear transformation, and a specific vector, and you want to know where the linear transformation takes that vector, you take the coordinates of that vector, multiply them by the corresponding column of the matrix, then add together what you get. This corresponds with the idea of adding scaled versions of our new basis vectors. In general, a matrix vector multiplication is some kind of transformation.

![General 2D Linear Transformation](/images/linear-algebra/transformation-intuition/general_2d_transformation.svg)

## Linear Dependency

If the vectors $\hat{i}$ and $\hat{j}$ are linearly dependent meaning that one is a scaled version of other, he linear transformation squishes all of 2d space onto the line where those vectors sit, also known as the one-dimensional span of these two linearly dependent vectors.

<video width="640" height="360" class="center" controls>
  <source src="/videos/linear-algebra/transformation-intuition/linearly_dependent_transformation.mp4" type="video/mp4">
</video>

Thus, matrices are used to represent linear transformation in many fields including graphic design, modelling and image analysis. Understanding how matrices can be thought of as transformation is a powerful mental tool for understanding the various constructs in Linear algebra.

</div>
