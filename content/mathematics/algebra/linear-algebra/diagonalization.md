---
title: Diagonalization
weight: 26
math: true
cascade:
  type: docs
sidebar:
  open: true
---

<br>
<div style="text-align: justify;">

A transformation T $:\nu \rarr \nu$ has many matrix representations given a basis $B$. If there exists a diagonal matrix to represent T, it would be easier for computations.Matrix computations are in general expensive. But computations on diagonal matrix are fairly easy and reduces the overall complexity of the computations. This applies to computing the determinant, inverse, powers and so on. A diagonal matrix is always computationally least expensive.

If a basis $B$ exists such that the transformation T on $B$ yields a diagonal matrix, we say T is diagonalizable.

> A matrix $A$ is called diagonalizable, if the matrix is similar to a diagonal matrix $D$ such that $$D = P^{-1}AP$$

## Eigen Vectors and Eigen Values

> If a non-zero vector from a vector space which on transformation yields a scaled version of the same vector, the vector is called the eigen vector of the transformation and the value of scaling is called the eigen value.
> $$\text{Eigen vectors} = \lbrace v \in \nu \mid v \neq 0,\text{T}(v) = \alpha v \rbrace,$$ where $\alpha$ is the eigen value

Eigen is a german word meaning belongs to the same. Here, it belongs to T in the relation $\text{T}(v) = \alpha v$ With this we can define that, **T is diagonalizable if and only if it has a basis of eigen vectors and D is a diagonal matrix with the eigen values on its main diagonal**

</div>
