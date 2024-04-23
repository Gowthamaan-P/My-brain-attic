---
title: Vector Space
weight: 15
next: vector-subspace
math: true
cascade:
  type: docs
sidebar:
  open: true
---

<br>
<div style="text-align: justify;">

In mathematics, the term "space" is a set of objects with a structure (relationship among the elements of the set). The structure can be algebraic structure like field, ring or any mathematical structure. A space consists of selected mathematical objects that are called as points, and selected relationships between these points. The nature of the points can vary widely: for example, the points can represent numbers, functions on another space, or subspaces of another space. It is the structure that define the nature of the space. There are many different types of spaces like geometric space, vector space, measure space and so on. The prime concept in Linear algebra is the Vector space.

## Vector Space

Consider the vectors $\vec{u}, \vec{v}, \vec{w} \in \nu$.

> $\nu$ is called a vector space over a field $\mathbb{F}$ if $\nu$ with two operations namely addition and multiplication by a scalar $c \in \mathbb{F}$ if and only if it satisfies,
>
> - **Additive closure**: $\vec{u} + \vec{v} \in \nu$ (result of operation stays in $\nu$)
> - **Additive commutativity**: $\vec{u} + \vec{v} = \vec{v} + \vec{u}$ (order invariant)
> - **Additive associativity**: $(\vec{u} + \vec{v}) + \vec{w} = \vec{u}+(\vec{v} +\vec{w})$ (order invariance with respect to addition)
> - **Zero vector existence**: $0$ such that $\vec{u} +0 = \vec{u}, \forall \text{ }\vec{u} \in \nu$ (additive identity)
> - **Additive inverse**: For every $\vec{u} \in \nu$, there exists $\vec{w} \in \nu$ such that $\vec{u} + \vec{w} = 0$.
> - **Multiplicative closure**: $c.\vec{u} \in \nu,\forall \text{ } c \in \mathbb{F}$ (result of operation stays in $\nu$)
> - **Distributivity I**: $(c + d).\vec{u} = c.\vec{u} + d.\vec{u},\forall \text{ } c,d \in \mathbb{F}$ (scalar multiplication distributes over addition of scalars)
> - **Distributivity II**: $c.(\vec{u} + \vec{v}) = c.\vec{u} + c.\vec{v},\forall \text{ } c \in \mathbb{F}$ (scalar multiplication distributes over addition of vectors)
> - **Multiplicative Associativity**: $(cd).\vec{u} = c.(d.\vec{u}),\forall \text{ } c,d \in \mathbb{F}$ (order invariance with respect to multiplication)
> - **Unity**: There exists $1 \in \mathbb{F}$ such that $1.\vec{u} = \vec{u}$ (multiplicative identify)

A vector space is also called a Linear space.

## The Space $\mathbb{R}^n$

The most common vector space that we come across throughout this notes is the space $\mathbb{R}^n$. The space $\mathbb{R}^n$ is a collection of $n$ dimensional vectors whose elements belong to the field $\mathbb{R}$.

$$
\mathbb{R}^n = \Bigg\lbrace \begin{pmatrix}a_1 \\\\ a_2 \\\\ . \\\\ . \\\\ a_n\end{pmatrix} \mid  a_i \in \mathbb{R} \Bigg\rbrace
$$

Interestingly, $\mathbb{R}^2$ and $\mathbb{R}^3$ have a very good geometric realization. Remember that, we consider a vector to be an arrow whose tail is at the origin of the co-ordinate system and head at the point of the vector.

For example, $z = \begin{bmatrix}-3 \\\\ 2 \end{bmatrix} \in \mathbb{R}^2$ is a point in the 2D space.

![Visualizing a vector](/images/linear-alegbra/vectors/visualizing_a_vector.svg)

Similarly, $z = \begin{bmatrix}-3 \\\\ 2 \\\\ 1\end{bmatrix} \in \mathbb{R}^3$ is a point in the 3D space. So, the whole $\mathbb{R}^n$ vector space contains vectors which are present in a $n$ dimensional space. But, it gets really hard to visualize a vector beyond 3 dimensions.

</div>
