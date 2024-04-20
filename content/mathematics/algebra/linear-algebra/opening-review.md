---
title: Opening Review
weight: 11
next: vectors
math: true
cascade:
  type: docs
sidebar:
  open: true
---

<br>
<div style="text-align: justify;">

This opening review introduces definition, properties and examples of a scalar, a set and a algebraic structures like group and field. There are a lot more structures like ring which are not dealt here.

## Scalar

Elementary math introduces us to scalars, which are essentially useful for handling one-dimensional variables or data. **A scalar is a simple quantity with a magnitude or value**. Eg. 5 is a scalar, height and weight are scalars. A scalar has `zero dimensions`. There are three aspects of analysis which are usually familiar using scalars,

- **Elementary operations**: Addition, multiplication, etc.
- **Comparisons and strengths**: Equality, magnitude, etc.
- **Functions of scalars**: Squares, cubic roots, etc.

## Set

A set is a well-defined collection of objects. These objects can be of any kind. For example, $\mathbb{N}$ is the set of all natural numbers. Here, every number is a scalar. Similarly, there are other sets like $\mathbb{Z}, \mathbb{Q}, \mathbb{R}$ which are set of integers, rational numbers and real numbers respectively.

## Algebraic Structure

An algebraic structure consists of a `nonempty set` A (called the underlying set, carrier set or domain), a `collection of operations` on A (typically binary operations such as addition and multiplication), and a `finite set of identities`, known as axioms, that these operations must satisfy.

## Group

As discussed earlier, there are many elementary operations that can be performed over scalars like addition, multiplication, subtraction and so on. If a set includes a certain operation and satisfies certain axioms, we call that set as a group. For example, $\mathbb{Z}$ is a group over scalar addition.

> A group $G$ is a set together with an operation $\cdot$ which satisfies the following properties:
>
> - Closure: $\forall$ $a, b \in G, a \cdot b \in G$
> - Associativity: $\forall$ $a,b,c \in G, a \cdot (b \cdot c) = (a \cdot b) \cdot c$
> - Identity: $\exists$ $e \in G$ such that, $e \cdot a = a \cdot e = a, \forall$ $a \in G$
> - Inverse: $\forall$ $a \in G, \exists$ $b$ such that, $a \cdot b = b \cdot a = e$

Now, $\mathbb{Z}$ is a group over scalar addition with identity $0$ and inverse $-a$. On the other hand $\mathbb{N}$ is a not a group over scalar addition since it lacks the identity and inverse element. Here, the operation can be anything and set can be a collection of any mathematical object not limited to scalars.

> If a group satisfies the commutative property, $\forall$ $a, b \in G, a \cdot b = b \cdot a$ in addition to the above four properties, the group is called as an `Abelian group` or a Commutative group.

A set of $n \times n$ matrices is a group under matrix multiplication but not a abelian group, as matrix multiplication is not commutative.

## Field

> A field $\mathbb{F}$ is a set together with two binary operations (+, $\cdot$) which satisfies the following properties:
>
> - Closure: $\forall$ $a, b \in \mathbb{F}, a + b \in \mathbb{F}$
> - Associativity: $\forall$ $a,b,c \in \mathbb{F}, a + (b + c) = (a + b) + c$
> - Identity: $\exists$ $e_a \in \mathbb{F}$ such that, $e_a + a = a + e_a = a, \forall$ $a \in \mathbb{F}$
> - Inverse: $\forall$ $a \in \mathbb{F}, \exists$ $b$ such that, $a + b = b + a = e_a$
> - Commutativity: $\forall$ $a,b \in \mathbb{F}, a + b = b + a$

> - Closure: $\forall$ $a, b \in \mathbb{F}, a \cdot b \in \mathbb{F}$
> - Associativity: $\forall$ $a,b,c \in \mathbb{F}, a \cdot (b \cdot c) = (a \cdot b) \cdot c$
> - Identity: $\exists$ $e_m \in \mathbb{F}$ such that, $e_m \cdot a = a \cdot e_m = a, \forall$ $a \in \mathbb{F}$
> - Inverse: $\forall$ $ a\neq e_a$ and $a \in \mathbb{F}, \exists$ $b$ such that, $a \cdot b = b \cdot a = e_m$
> - Commutativity: $\forall$ $a,b \in \mathbb{F}, a \cdot b = b \cdot a$

And finally the set must satisfy the distributive property.

> - Distributivity: $\forall$ $a,b,c \in \mathbb{F}, a \cdot (b + c) = (a \cdot b) + (a \cdot c)$

If a set satisfies all the above 11 properties, it is called as a field. $\mathbb{Q}$ over $(+, \cdot)$ is a field.

## Generalization of Algebraic Structures

Groups and Fields are broad algebraic structures applicable to various mathematical objects within a set. These objects could range from scalars to vectors, polynomials, and beyond. This abstraction is a significance of mathematical concepts, offering a versatile framework with wide range of applications.

## Limitation of Scalars

Scalars effectively define quantities, yet they often fall short in various processes. In disciplines like geometry, computer vision, and data science, tasks frequently involve data with multiple dimensions, rendering scalars inadequate for fully elucidating the underlying processes.

</div>
