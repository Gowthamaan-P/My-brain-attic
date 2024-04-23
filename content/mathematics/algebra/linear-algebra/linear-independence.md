---
title: Linear Independence
weight: 18
next: next
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

So, how do we identify the set of vectors with any redundant vector(vectors that can be expressed as linear combination of other vectors)?

> A set of vectors is said to be `linearly dependent` if any of the vectors can be expressed as a linear combination of other vectors. A set of vectors is said to be `linearly independent` if the vectors cannot be expressed as a linear combination of each other.

## Definition

The formal definition of linear dependence is,

> The vectors $v_1, v_2, \dots, v_k$ are linearly dependent if $\exists \text{ } \alpha_1, \alpha_2, \dots, \alpha_k \in \mathbb{F}$ not all zero such that, $\alpha_1v_1 + \alpha_2v_2 + \dots + \alpha_vu_k = 0$

On the contrary, the formal definition of linear independence is,

> The vectors $v_1, v_2, \dots, v_k$ are linearly independent when $\alpha_1v_1 + \alpha_2v_2 + \dots + \alpha_vu_k = 0$ if and only if $\forall \text{ } \alpha_i = 0$. In other words, the linear combination will be zero only for the trivial solution.

</div>
