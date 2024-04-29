---
title: Rank-Revisited
weight: 20
next: inverse-determinants
math: true
cascade:
  type: docs
sidebar:
  open: true
---

<br>
<div style="text-align: justify;">

For every matrix we can define spaces based on the rows and columns. Consider a matrix $A$,

> - Row($A$) is the row subspace of the matrix A. This is all possible linear combinations of the rows of $A$. This implies the subspace spanned by the rows of $A$.
> - Column($A$) is the column subspace of the matrix A.

In the previous notes, we defined rank as:

> Let $A$ be a matrix of size $m\times n$. The number of non-zero rows in a row-echelon form obtained from $A$ using elementary row operations is called the rank of $A$, denoted by rank($A$) or r($A$).

The core idea here is that, `the non-zero rows of a matrix in the row-echelon are linearly independent` and the rank is the number of non-zero rows in the row-echelon form. This means that rank indicates the number of linearly independent rows in a matrix. If we call Row($A$) as the row-subspace of $A$, the dim(Row($A$)) = r($A$). The rank of the matrix is the dimension of the row-subspace.

Let us rewrite the definition of the rank of a matrix,

> The column / row rank of a matrix $A$ is the maximum number of linearly independent columns/rows in $A$.

## Properties

- Row and column ranks of a matrix are identical.
- If the matrix $A \in \mathbb{R}_{m\times n}$, the rank of $A$ is r($A$)$\leq min(m, n)$
- If the rank of the matrix is equal to the number of unknowns, the matrix is called full rank
- If the rank is less than the number of unknowns, the matrix is called rank deficient

## Basis of Row($A$) and Column($A$)

As defined above, dim(Row($A$)) = r($A$). This means the number of vectors in the basis of Row($A$) is r($A$) which is the number of non-zero rows in the row echelon form of the matrix. So, the rows of the row-echelon form are the basis vectors forming the basis for the row subspace of $A$.

To find the basis of the row space of a matrix $A$, we will carryout the row operations and reduce the matrix to its row-echelon form.

> Example: Determine the row subspace of matrix $A = \begin{bmatrix}1&2&3&4 \\\\ 2&-1&1&0 \\\\ 3&-2&1&2\end{bmatrix}$

**Solution:**

If we carry out row reduction, we will get $A = \begin{bmatrix}1&0&1&0 \\\\ 0&1&1&0 \\\\ 0&0&0&1\end{bmatrix}$. This implies that the basis of the Row($A$) is $B = \{(1010), (0110), (0001) \}$

The above notion applies for the column subspace of the matrix also. As the rank by rows and rank by columns is also the same, the number of linearly independent columns and rows is the same.

## Null Space

Consider a homogeneous system, $Ax=0$. The solutions to $Ax=0$ form a subspace over $\mathbb{R}^n$ or $\mathbb{C}^n$, where $n$ is the number of unknowns.

> The null space of $A$ is the set of solutions of $Ax=0$

The dimension of the null space is $n-$ r($A$). The dimension of the null space correspond to the degrees of freedom.

## Rank Nullity Theorem

Consider a matrix $A$ which forms a homogeneous system $Ax=0$. All the vectors that satisfy $Ax=0$ forms the null space of dimension $k$.

The rank nullity theorem states that,

> For a homogeneous system $Ax=0$, the number of unknowns $n$ is given by $n = $ r($A$) + $k$.

### Corollary

Let $A \in M_{m\times n}(\mathbb{F})$,

- If $Av=0$ for every $v \in \mathbb{F}^n$, $A=0$
- If $Av=Bv$ for every $v$, $A=B$

</div>
