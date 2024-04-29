---
title: Basis
weight: 19
next: next
math: true
cascade:
  type: docs
sidebar:
  open: true
---

<br>
<div style="text-align: justify;">

Consider a set vectors $v_1,v_2,\dots,v_k$ from the vector space $\nu$.

> A set of vectors $v_1,v_2,\dots,v_k$ is said to be the **basis** for a vector space $\nu$ if
>
> - The vectors are linearly independent (not too many vectors)
> - They span all of $\nu$ (not too few vectors)

## Basis vectors

The vectors in the basis set are called as basis vectors. These are very special vectors as any vector in the vector space can be expressed as the linear combination of these vectors.

For example, consider the vector space $\mathbb{R^2}$ which is the $xy$-coordinate system. The basis vectors of this vector space are $\hat{\text{\i}} = \begin{bmatrix} 1 \\\\ 0\end{bmatrix} \text{ and } \hat{\text{\j}} = \begin{bmatrix} 0 \\\\ 1\end{bmatrix}$

![xy-coordinate system - Basis vectors](/images/linear-algebra/basis/r2_basis.svg)

## Determine a set v is a basis

For example, consider the following vectors from the vector space $\mathbb{R^3}$,

$$v_1 = \begin{bmatrix} 1 \\\\ 0 \\\\0 \end{bmatrix}, v_2 = \begin{bmatrix} 0 \\\\ 1 \\\\0 \end{bmatrix}, v_3 = \begin{bmatrix} 0 \\\\ 0 \\\\1 \end{bmatrix}$$

The above three vectors are linearly independent and they span the whole $\mathbb{R}^3$ space. Any vector in $\mathbb{R}^3$ can be expressed as a linear combination of these three vectors. So, the above vectors form the basis for $\mathbb{R}^3$.

> In general, the set of vectors of form $\lbrace \begin{bmatrix} 1 \\\\ 0 \\\\ \vdots \\\\0 \end{bmatrix}, \begin{bmatrix} 0 \\\\ 1 \\\\ \vdots \\\\0 \end{bmatrix}, \dots, \begin{bmatrix} 0 \\\\ 0 \\\\ \vdots \\\\1 \end{bmatrix} \rbrace$ is a basis for $\mathbb{F}^n$ and is called the `standard basis`.

Similarly, consider the following vectors from $\mathbb{R^3}$,

$$v_1 = \begin{bmatrix} 1 \\\\ 1 \\\\0 \end{bmatrix}, v_2 = \begin{bmatrix} 1 \\\\ 0 \\\\1 \end{bmatrix}, v_3 = \begin{bmatrix} 0 \\\\ 1 \\\\1 \end{bmatrix}$$

To verify whether they form a basis, we need to solve the following system of equations,

$$X\begin{bmatrix} 1 \\\\ 1 \\\\0 \end{bmatrix} + Y\begin{bmatrix} 1 \\\\ 0 \\\\1 \end{bmatrix}+Z\begin{bmatrix} 0 \\\\ 1 \\\\1 \end{bmatrix} = \begin{bmatrix} a \\\\ b \\\\ c \end{bmatrix}$$

Solving the above yields, the following result,

$$\frac{a-c+b}{2}\begin{bmatrix} 1 \\\\ 1 \\\\0 \end{bmatrix} + \frac{c-b+a}{2}\begin{bmatrix} 1 \\\\ 0 \\\\1 \end{bmatrix}+\frac{b-a+c}{2}\begin{bmatrix} 0 \\\\ 1 \\\\1 \end{bmatrix} = \begin{bmatrix} a \\\\ b \\\\ c \end{bmatrix}$$

This implies that given vectors are linearly independent and span the whole $\mathbb{R}^3$ space. Thus, this given set forms a basis.

> **Remark**: From the above examples, we can observe that a basis is not unique for a given vector space. A vector space can have multiple basis (bases).

A basis is called finite basis if the number of elements in the basis is finite.

## Dimension of a Vector space

> The number of basis vectors or elements in a basis set for a vector space $\nu$ is called the dimension of the vector space $\nu$ denoted by dim($\nu$)

If all the bases of a vector space have same finite number of vectors, the vector space is called **finite dimensional vector space**. In other words, $\nu$ be a finite dimensional vector space, if amy bases of $\nu$ have the same number of vectors.

Examples,

- dim($\mathbb{R}^3$) = 3
- dim($\mathbb{F}^4$) = 4
- dim($\mathbb{R}_n[x]$) = $n+1$ (a vector space of polynomials of degree $\leq n$)
- dim($\mathbb{M}_{m\times n}(\mathbb{F})$) = $mn$

Now, consider the vector space $\mathbb{R}n[x]$, a vector space of polynomials. The number of basis vector for this vector space is infinite. So, $\mathbb{R}[x]$ is not a finite dimensional vector space.

## Properties of bases

Let $\mathbb{B}$ be a basis for a finite dimensional vector space $\nu$, the following are equivalent,

- $\mathbb{B}$ is a maximal linearly independent set
- $\mathbb{B}$ is a minimal spanning set

The following properties are trivial and based on the above explanation for a vector space $\nu$ of dimension $n$,

- Any spanning set with $n$ elements is a basis
- Any set with $n$ linearly dependent vectors from $\nu$ is a basis
- Any spanning set should have atleast $n$ elements
- Any linearly independent set can have atmost $n$ elements
- Any linearly independent set can be completed to form a basis

## Bases and Dimension of Subspace

All the properties mentioned above are also applicable to subspaces, since every subspace is itself a vector space. For more theorems and examples, go through this [video](https://youtu.be/ZizWun0RlP0?si=H2KQqvEwVrQ1M_Uz)

## Change of basis

As stated above, a vector space can have multiple basis. Consider a vector space $\nu$ with basis $B = \lbrace v_1,v_2,\dots,v_k\rbrace$.

> Any vector $u \in \nu$ can be expressed **uniquely** as a linear combination of $v_1,v_2,\dots,v_k$

The statement implies that any vector $u \in \nu$ can be expressed as $u = \alpha_1v_1 + \alpha_2v_2 + \dots + \alpha_kv_k$ such that this relation is valid only a unique set of $\alpha_i$ (i.e) $u$ can be expressed as a linear combination in only one way. The uniqueness here lies in the $\alpha_i$. If the basis changes, the values of $\alpha_i$ also changes. Here, $\alpha_1, \alpha_2, \dots, \alpha_k$ are called the coordinates of the vector $u$ with respect to $B$.

</div>
