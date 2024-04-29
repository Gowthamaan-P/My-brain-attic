---
title: Linear Independence
weight: 18
next: basis
math: true
cascade:
  type: docs
sidebar:
  open: true
---

<br>
<div style="text-align: justify;">
Let us consider a general vector from the $\mathbb{R}^2$ space.

**Example: 1**

$$
\begin{bmatrix} a \\\\ b \end{bmatrix} = a \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} + b \begin{bmatrix} 0 \\\\ 1 \end{bmatrix},
$$

where $\mathbb{R}^2 = \text{span}\lbrace \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} , \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}\rbrace$

**Example: 2**

$$
\begin{bmatrix} a \\\\ b \end{bmatrix} = a \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} + b \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} + 0 \begin{bmatrix} 4 \\\\ 5 \end{bmatrix},
$$

where $\mathbb{R}^2 = \text{span}\lbrace \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} , \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}, \begin{bmatrix} 4 \\\\ 5 \end{bmatrix}\rbrace$

Now, which one in the above example defines the span of $\mathbb{R}^2$? The span in Example: 1, spans the entire $\mathbb{R}^2$ space. Every vector in $\mathbb{R}^2$ belongs to the span. Now, look into Example: 2, the vector $\begin{bmatrix} 4 \\\\ 5 \end{bmatrix}$ can be expressed as a linear combination of $\lbrace \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} , \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}\rbrace$.

So, how do we identify the set of vectors with any redundant vector(vectors that can be expressed as linear combination of other vectors)? Using the concept of linear independence.

> A set of vectors is said to be `linearly dependent` if any of the vectors can be expressed as a linear combination of other vectors. A set of vectors is said to be `linearly independent` if the vectors cannot be expressed as a linear combination of each other.

## Definition

The formal definition of linear dependence is,

> The vectors $v_1, v_2, \dots, v_k$ are linearly dependent if $\exists \text{ } \alpha_1, \alpha_2, \dots, \alpha_k \in \mathbb{F}$ not all zero (i.e) not all $\alpha_i \neq 0  \forall \text{ } i$ such that, $\alpha_1v_1 + \alpha_2v_2 + \dots + \alpha_vu_k = 0$

On the contrary, the formal definition of linear independence is,

> The vectors $v_1, v_2, \dots, v_k$ are linearly independent when $\alpha_1v_1 + \alpha_2v_2 + \dots + \alpha_vu_k = 0$ if and only if $\alpha_i = 0 \forall \text{ } i$. In other words, the linear combination will be zero only for the trivial solution.

## Determing Linear Independence

**Objective**: Determine if a set of vectors are linear independent.

Let us do few examples and generalize this idea. For the detailed solution and steps of the solution refer this [video](https://youtu.be/DZH-0-9jDKw?si=y5AArCGli2xx-q3M).

> Consider $v_1 = \begin{bmatrix}1 \\\\ 1 \\\\0 \end{bmatrix}$, $v_2 = \begin{bmatrix} 1 \\\\ 0 \\\\1 \end{bmatrix}$ and $v_3 = \begin{bmatrix} 0 \\\\ 1 \\\\1 \end{bmatrix}$. Determine if they are linearly independent.

**Solution**

So, let us rewrite this question. Are there $\exists \text{ } \alpha_i$ such that,

$$\alpha_1v_1 + \alpha_2v_2 + \alpha_3v_3 = 0$$
$$\alpha_1\begin{bmatrix}1 \\\\ 1 \\\\0 \end{bmatrix} + \alpha_2\begin{bmatrix} 1 \\\\ 0 \\\\1 \end{bmatrix} + \alpha_3\begin{bmatrix} 0 \\\\ 1 \\\\1 \end{bmatrix} = \begin{bmatrix} 0 \\\\ 0 \\\\0 \end{bmatrix}$$

This again translates into a question of solving a system of linear equations. In this example, the number of unknowns is $n=3$ and after solving the r($A$) = r($A^\star$) = $n$ = 3. This means the system has a unique solution. For homogeneous system, the unique solution is always the zero vector. So, the given set of vectors are linearly independent.

> Consider $v_1 = \begin{bmatrix}1 \\\\2 \\\\3 \end{bmatrix}$, $v_2 = \begin{bmatrix} 1 \\\\0 \\\\6 \end{bmatrix}$ and $v_3 = \begin{bmatrix} 3\\\\2 \\\\15 \end{bmatrix}$. Determine if they are linearly independent.

In this example, the number of unknowns is $n=3$ and after solving the r($A$) = r($A^\star$) = 2 < $n$ = 3. This means the system has infinitely many solutions. So, the given set of vectors are linearly dependent.

**Remarks**

- Any set of vectors that includes a zero vector is linearly dependent
- Two vectors are linearly dependent if one of the vector can be expressed as a scalar multiple of other
- A homogeneous system $Ax=0$ has a non-trivial solution if and only if the columns of $A$ are linearly dependent

So, generalizing the above observations,

> To determine if a set of vectors are linearly independent,
>
> 1.  Rewrite the set of vectors as a homogeneous system $Ax=0$, where the given vectors are the columns of $A$
> 2.  Determine the rank of the matrix $A$.
> 3.  For a homogeneous system,
>     > - If r($A$) = n, the vectors are linearly independent
>     > - If r($A$) < n, the vectors are linearly dependent

</div>
