---
title: Inverse and Determinants - Revisited
weight: 21
math: true
next: next
cascade:
  type: docs
sidebar:
  open: true
---

<br>
<div style="text-align: justify;">

As mentioned in earlier notes, a matrix $A$ is invertible if there exists a another matrix $A^{-1}$ such that $AA^{-1}=I$. Observe the words here, there is always a if around $A^{-1}$. So, what does that mean?

> **Not every square matrix is invertible**

**Examples**

> $A = \begin{bmatrix}2&1 \\\\ 4&5\end{bmatrix}$ is invertible and the inverse matrix is $A^{-1} = \begin{bmatrix}\frac{5}{6}&-\frac{1}{6} \\\\ -\frac{2}{3}&\frac{1}{3}\end{bmatrix}$. You can verify this by $AA^{-1} = I$.

> $A = \begin{bmatrix}1&1 \\\\ 2&2\end{bmatrix}$ is not invertible.

Let us verify this.

$$AA^{-1} = I$$

$$\begin{bmatrix}1&1 \\\\ 2&2\end{bmatrix} \begin{bmatrix}a&b \\\\ c&d\end{bmatrix} = \begin{bmatrix}1&0 \\\\ 0&1\end{bmatrix}$$

If we multiply the above we will get a system of equations.

$$\begin{bmatrix}a+c&b+d \\\\ 2a+2c&2b+2d\end{bmatrix} = \begin{bmatrix}1&0 \\\\ 0&1\end{bmatrix}$$

$$\begin{cases} a+c=1 \\\\ b+d=0 \\\\ 2a+2c=0 \\\\ 2b+2d=1\end{cases}$$

The above system is inconsistent (i.e) no solution exists as $a+c=0$ and $2a+2c=0$ can't be true. So, $A^{-1}$ doesn't exist.

## Determine if $A$ is invertible

So, how do we determine if $A$ is invertible? In the above example, we looked into the system of equations to determine if $A^{-1}$ exists. So, the simple answer if the system has a solution, the matrix is invertible. Remember that the inverse of a matrix is unique. So, the solution needs to be unique. How do we determine if a system has a unique solution? If the number of unknowns $n$ is equal to the rank of the matrix, the system has unique solution. So, the straight forward answer is,

> A matrix $A$ is invertible if and only if it has full rank.

For any invertible matrix $A$, the system $Ax=b$ where $b \in \mathbb{F}^n$ has a unique solution.

## Computing $A^{-1}$

## Determinant and Invertibility

There is a another way determining whether a matrix invertible.

> **The determinant of a invertible matrix is always non-zero**. If a matrix $A_{n\times n}$ is invertible, $|A| \neq 0$

If $A$ is invertible (i.e) $|A| \neq 0$, $|A^{-1}| = \frac{1}{|A|}$

### Adjoint/Adjugate

An Adjoint/Adjugate of a matrix $A$ is a matrix denoted as adj($A$) whose entries are given by,

$$a_{ij} = (-1)^{i+j} M_{ji} $$

**Properties**

> - adj($I$) = $I$
> - adj($AB$) = adj($A$)adj($B$)

There is important theorem, based on the adjugate matrix. The theorem states that, $A$ adj($A$) = $\mid A\mid$ $I$. When looking at it, the theorem doesn't make much sense. The theorem is used to find the inverse of $A$.

$$A^{-1} = \frac{1}{|A|} \text{adj}(A)$$

Instead of using row operations and reduce $(A \mid I)$, we use adjugate matrix to find the inverse.

</div>
