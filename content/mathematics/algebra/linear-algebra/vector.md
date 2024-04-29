---
title: Vector
weight: 12
math: true
next: matrix
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

We will discuss about the mathematics definition in detail in further notes. At the moment, to get a better understanding geometrically and mathematically, throughout this notes we assume a vector to be an arrow whose tail is at the origin of the co-ordinate system and head at the point of the vector. Vectors are denoted as $\vec{z}$ with a arrow in the head or as an (row or column) array. For example, $z = \begin{bmatrix}-3 & 2 \end{bmatrix}$, $z = \begin{bmatrix} -3 \\\\ 2 \end{bmatrix}$.

![Visualizing a vector](/images/linear-alegbra/vectors/visualizing_a_vector.svg)

So, what all these mean is that z is a point in space (Cartesian co-ordinate system or Cartesian space), whose tail is at the origin (0,0) and the tip is at (-3,2). To distinguish vectors from points, the convention is to write this n-numbers vertically or horizontally with square brackets around them. For better visulization and understanding, we stick to two and three dimensional vectors in this notes but vectors can be of any length in general.

## Basic Operations

As stated earlier, a scalar couldn't express a complex process. So, we use a vector. Similar to scalar, there are many mathematical operations defined for a vector.

### Vector addition and subtraction

Vector addition and subtraction is an element-wise operation. Addition of two vectors of length $n$ can be defined as,

$$\begin{bmatrix}x_1 \\\\ x_2 \\\\ \vdots \\\\ x_n\end{bmatrix} + \begin{bmatrix}y_1 \\\\ y_2 \\\\ \vdots \\\\ y_n\end{bmatrix} = \begin{bmatrix}x_1 + y_1 \\\\ x_2 + y_2 \\\\ \vdots \\\\ x_n + y_n\end{bmatrix}$$

Consider two vectors, $v = \begin{bmatrix}1 \\\\ 2\end{bmatrix}$ and $w = \begin{bmatrix}3 \\\\ -1\end{bmatrix}$,

$v + w = \begin{bmatrix}1 \\\\ 2\end{bmatrix} + \begin{bmatrix}3 \\\\ -1\end{bmatrix} = \begin{bmatrix}1+3 \\\\ 2-1\end{bmatrix} = \begin{bmatrix}4 \\\\ 1\end{bmatrix}$

`The length of the vectors should be equal for vector addition and subtraction`. Vector subtraction also follows the same principles. Subtraction of two vectors of length $n$ can be defined as,

$$\begin{bmatrix}x_1 \\\\ x_2 \\\\ \vdots \\\\ x_n\end{bmatrix} - \begin{bmatrix}y_1 \\\\ y_2 \\\\ \vdots \\\\ y_n\end{bmatrix} = \begin{bmatrix}x_1 - y_1 \\\\ x_2 - y_2 \\\\ \vdots \\\\ x_n - y_n\end{bmatrix}$$

### Vector multiplication

There are three different most commonly used vector products. Every product serves a different purpose. They are,

- Dot product
- Cross product
- Hadamard product

#### Dot product

Dot product between two vectors $\vec{x}$ and $\vec{y}$ is denoted by $\cdot$ and defined as,
$$\vec{x} \cdot \vec{y} = \sum_{i=1}^{n} x_iy_i$$

A vector dot product is basically summation of element wise multiplication. `So, dot product of two vector will always result in a scalar`. For example, the dot product of $\vec{v}$ and $\vec{w}$ is,

$\vec{v} \cdot \vec{w} = \begin{bmatrix}1 \\\\ 2\end{bmatrix} \cdot \begin{bmatrix}3 \\\\ -1\end{bmatrix} = (1\times 3) + (2\times -1) = 3-2 = 1$

`The length of the vectors should be equal for dot product`. So, if the entries are missing in one of the vectors, they are assumed to be zero.

#### Cross product

`Cross product between two vectors will always result in a new vector`. For simplicity, we will see cross product definition for 3 dimensional vectors here. The cross product between two 3 dimensional vectors is denoted by $\times$ and defined as,

$$ \vec{x} \times \vec{y} = \begin{bmatrix}x_2y_3-y_2x_3 \\\\ x_3y_1-y_3x_1 \\\\ x_1y_2-y_1x_2\end{bmatrix}$$

For example, the cross product between $v = \begin{bmatrix}1 \\\\ 2 \\\\ 3\end{bmatrix}$ and $w = \begin{bmatrix}3 \\\\ -1 \\\\ 4\end{bmatrix}$ is,

$\vec{v} \times \vec{w} = \begin{bmatrix}1 \\\\ 2 \\\\ 3\end{bmatrix} \times \begin{bmatrix}3 \\\\ -1 \\\\ 4\end{bmatrix} = \begin{bmatrix}8+3 \\\\ 9-4 \\\\ -1-6\end{bmatrix} = \begin{bmatrix}11 \\\\ 5 \\\\ -7\end{bmatrix}$

Cross product is defined for vectors with dimension $n\geq 3$. In the further notes, we will generalize this idea for $n$ dimensional vectors.

#### Hadamard product

Hadamard product between two vectors $\vec{x}$ and $\vec{y}$ is denoted by $$ and defined as,

$$\begin{bmatrix}x_1 \\\\ x_2 \\\\ \vdots \\\\ x_n\end{bmatrix} \odot \begin{bmatrix}y_1 \\\\ y_2 \\\\ \vdots \\\\ y_n\end{bmatrix} = \begin{bmatrix}x_1y_1 \\\\ x_2y_2 \\\\ \vdots \\\\ x_ny_n\end{bmatrix}$$

A vector hadamrd product is basically element wise multiplication. For example, the hadamard product of $\vec{v}$ and $\vec{w}$ is,

$\vec{v} \odot \vec{w} = \begin{bmatrix}1 \\\\ 2\end{bmatrix} \odot \begin{bmatrix}3 \\\\ -1\end{bmatrix} = \begin{bmatrix}1\times 3 \\\\ 2\times -1\end{bmatrix} = \begin{bmatrix}3 \\\\ -2\end{bmatrix}$

`The length of the vectors should be equal for hadamard product`. So, if the entries are missing in one of the vectors, they are assumed to be zero.

### Scalar-Vector addition

Addition of a scalar and a vector is defined as,

$$\begin{bmatrix}x_1 \\\\ x_2 \\\\ \vdots \\\\ x_n\end{bmatrix} + a = \begin{bmatrix}a+x_1 \\\\ a+x_2 \\\\ \vdots \\\\ a+x_n\end{bmatrix}$$

For example, if we add a scalar $2$ to the vector $\vec{v}$,

$\vec{v} + 2 = \begin{bmatrix} 1+2 \\\\ 2+2 \end{bmatrix} = \begin{bmatrix} 3 \\\\ 4 \end{bmatrix}$

### Scalar-Vector multiplication

Multiplication of a scalar and a vector is defined as,

$$\begin{bmatrix}x_1 \\\\ x_2 \\\\ \vdots \\\\ x_n\end{bmatrix} \times a = \begin{bmatrix}ax_1 \\\\ ax_2 \\\\ \vdots \\\\ ax_n\end{bmatrix}$$

For example, if we multiply a vector $\vec{v}$ by $2$,

$\vec{v} \times 2 = \begin{bmatrix}1 \\\\ 2\end{bmatrix} \times 2 = \begin{bmatrix}1\times 2 \\\\ 2\times 2\end{bmatrix} = \begin{bmatrix}2 \\\\ 4\end{bmatrix}$

</div>
