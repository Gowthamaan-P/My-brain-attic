---
title: Linear Transformation
weight: 22
next: linear-transformation-intuition
math: true
cascade:
  type: docs
sidebar:
  open: true
---

<br>
<div style="text-align: justify;">

A transformation is a function. A function can be anything that takes in a bunch of inputs and produces a output. A function, $f$ is said to be linear if and only if it satisfies the following conditions,

> - $f(x+y) = f(x) + f(y)$
> - $f(ax) = af(x)$, where $a$ is a constant.

What is a function has to do with linear algebra? So, in all our discussions we were looking into one vector space. A vector space over some field. What if we want to relate two vector spaces? This is where functions come into picture. These functions are called linear tranformation or linear maps. These functions are linear because they have to preserve the properties of the underlying structure (vector space). So, a function between two vector space should preserve the properties of vector space (i.e) addition and scalar multiplication. Let's define a linear transformation,

> Let $\nu_1$ and $\nu_2$ be two vector spaces over $\mathbb{F}$. A function T:$\nu_1 \rarr \nu_2$ is called a linear map/linear transformation if it satisfies the following conditions,
>
> - T($u + v$) = T($u$) + T($v$)
> - T($\alpha u$) = $\alpha$ T($u$)

**Properties**

> - T(0) = 0
> - T($-v$) = - T($v$)

## Kernel and Image

For every transformation T between two vector spaces $\nu_1$ and $\nu_2$, we define a kernel and image.

> The kernel of the transformation T is the set of elements in $\nu_1$ that goes to zero after transformation. $$\text{Ker(T)} = \lbrace v \in \nu_1 \mid \text{T}(v) = 0\rbrace$$
> The image of the transformation T is the set of elements in $\nu_2$ which can be obtained by applying the transformation on $\nu_1$. $$\text{Im(T)} = \lbrace \text{T}(v)\mid v \in \nu_1\rbrace$$

![Kernel and Image of Transformation](/images/linear-algebra/transformation-intuition/kernel_image.png)

</div>
