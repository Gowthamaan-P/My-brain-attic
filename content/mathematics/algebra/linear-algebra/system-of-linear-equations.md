---
title: System of Linear Equations
weight: 14
math: true
cascade:
  type: docs
sidebar:
  open: true
---

<br>
<div style="text-align: justify;">

One of the major applications of matrices is solving a system of linear equations. Majority of the linear algebra problem lie around solving a system of linear equations. The major questions answered by linear algebra are,

- Does this system of linear equations have a solution?
- If yes, how many solution?

## Linear equation

What is a linear equation? A linear equation is of the form,

$$
a_1x_1 + a_2x_2 + \dots + a_nx_n = b\\\\
\sum_{i=1}^n a_ix_i = b,
$$

where $a_i$ are called the coefficients, $x_i$ are called the unknowns. Geometrically, this defines a line in 2D and plane in 3D where n=2 and n=3 respectively. That's why the above equation is called linear equation. Consider, $x^2 + y =5$, is not linear and depicts a curve.

## System of linear equations

A system of linear equations is a collection of equations with $m$ equations and $n$ unknowns and all of them lie in the same $n$ dimensional space.

$$
\begin{cases}
a_{11}x_1 + a_{12}x_2 + \dots + a_{1n}x_n = b_1 \\\\
a_{21}x_1 + a_{22}x_2 + \dots + a_{2n}x_n = b_2 \\\\
\vdots\\\\
a_{m1}x_1 + a_{m2}x_2 + \dots + a_{mn}x_n = b_m
\end{cases}
$$

If we use matrices to rewrite the above equation,

$$
\begin{bmatrix}a_{11}&a_{12}&a_{13}&\dots&a_{1n} \\\\ a_{21}&a_{22}&a_{23}&\dots&a_{2n} \\\\ \vdots&\vdots&\vdots&\ddots&\vdots \\\\ a_{m1}&a_{m2}&a_{m3}&\dots&a_{mn}\end{bmatrix} \begin{bmatrix}x_1 \\\\ x_2 \\\\ \vdots \\\\ x_n\end{bmatrix} = \begin{bmatrix}b_1 \\\\ b_2 \\\\ \vdots \\\\ b_n\end{bmatrix}
$$

By generalizing the above,
$$Ax = b,$$ where $A$ is the matrix of co-efficients, $x$ is the vector of unknows and $b$ is the vector of contants or output.

## Number of Solutions

Any system of linear equations will follow under one of the following category,

- Has only one solution
- Has infinitely many solution (more than one)
- No solution

A system is said to be consistent if it has only one solution or has infinitely many solution. The system is said to be inconsistent if it has no solution.

## Solving a System of linear equations

The system of linear equations can be solved in many different methods. I haven't included the solving procedure as the part of the notes. Maybe in future if I will extend the scope of this notes to include it. The most commonly used (or taught) methods are,

- Gaussion elimination or Row-reduction method
- Cramer's Rule

Let's us consider a system of linear equations,

$$
\begin{cases}
x_1 + 2x_2 + 3x_3 + 4_x4 = 13\\\\
2x_1 - x_2 + x_3 = 8\\\\
3x_1 - 2x_2 + x_3 + 2_x4 = 13
\end{cases}
$$

The matrix form of the above system is,

$$
\begin{bmatrix}1&2&3&4 \\\\ 2&-1&1&0 \\\\ 3&-1&1&2\end{bmatrix}\begin{bmatrix}x_1 \\\\ x_2 \\\\ x_3 \\\\ x_4\end{bmatrix}=\begin{bmatrix}13 \\\\ 8 \\\\ 13\end{bmatrix}
$$

### Row-reduction

Row-reduction method is based on the following idea,

> The solution of a system remain the same if we carry out the following **elementary operations**,
>
> - Swap two equations
> - Multiply an equation by any scalar $c$, where $c\neq 0$
> - Add a scalar multiple of one equation to another equation

For a run through example, watch this [example video](https://youtu.be/_Dvi4UllI-Y?si=LlBS1JoumrgQiyPA) from the references.

### Cramer's Rule

## Terminology

- **Augmented Matrix**: The augmented matrix is the joined matrix of $A$ and $b$, usually denoted as $A|b$ or $A^\star$. The augmented matrix of the above example is,
  $$A^\star =A|b = \begin{bmatrix}1&2&3&4&13 \\\\ 2&-1&1&0&8 \\\\ 3&-1&1&2&13\end{bmatrix}$$

Once we carryout row reduction, we will be left out with the following matrix,
$$E = \begin{bmatrix}1&2&3&4&13 \\\\ 0&1&1&\frac{8}{5}&\frac{18}{5} \\\\ 0&0&0&1&1\end{bmatrix}$$
$$C = \begin{bmatrix}1&0&1&0&5 \\\\ 0&1&1&0&2 \\\\ 0&0&0&1&1\end{bmatrix}$$

- **Pivot Element**: Observer the above matrix, every row starts with either 0 or 1 (sometimes a non-zero element). This first non-zero co-efficient in each row is called the leading elements or the pivot elements.
  $$E = \begin{bmatrix}\colorbox{yellow}{1}&2&3&4&13 \\\\ 0&\colorbox{yellow}{1}&1&\frac{8}{5}&\frac{18}{5} \\\\ 0&0&0&\colorbox{yellow}{1}&1\end{bmatrix}$$

- **Echelon Form**: Observe the matrix $E$. The number of zeros preceeding each pivot element increases as go down the rows.
  $$E = \begin{bmatrix}1&2&3&4&13 \\\\ \colorbox{yellow}{0}&1&1&\frac{8}{5}&\frac{18}{5} \\\\ \colorbox{yellow}{0}&\colorbox{yellow}{0}&\colorbox{yellow}{0}&1&1\end{bmatrix}$$
  A matrix in which the number of zeros preceeding each pivot element grows or strictly increases from one row to the other is called the row-echelon form.

- **Canonical Form**: The matrix $C$ is called the reduced row echelon form or the canonical form. This form directly provides the solution for the system of linear equation. The canonical form of a system of linear equation is always unique.

The solution to the above system is the $(x, x-3, 5-x, 1)$.

- **Degree of Freedom**: In the above solution $x_1$ can any value and act as a solution to the system. Here, the degree of freedom is 1. Only one variable of the solution gives us the freedom to pick any value from the field. Having a non-zero degree of freedom implies that the system has infinitely many solutions.

## Homogeneous and Non-Homogeneous Systems

If $b$ in $Ax=b$ is a zero vector (i.e) $b_i = 0, \forall \text{ } i$, the system is said to be homogeneous. If $b$ is a non-zero vector, the system is said to be non-homogeneous.

As defined above, $Ax = 0$ is called a homogeneous system. **A homogeneous system always has a solution**.

- If a homogeneous system has zero solution, the solution is called the trivial solution of a homogeneous system and is defined as $x=0$ so that, $Ax = 0$
- If a homogeneous system has a non-zero solution, it has infinitely manay solutions. This means if $x\neq 0$ and $Ax=0$, the system has infinitely many solutions or infinitely many combination of $x$ such that $Ax=0$.

Thus, for a homogeneous system, the solution should be either trivial or infinitely many solution (i.e) a non-trivial solution.

## Determining Number of Solutions

Let us assume a system is consistent, (i.e) the system has solution. Now, the question arises that how many solutions? One or Infinitely many solutions. To determine this, we need to understand the rank of a matrix.

> Let $A$ be a matrix of size $m\times n$. The number of non-zero rows in a row-echelon form obtained from $A$ using elementary row operations is called the rank of $A$, denoted by rank($A$) or r($A$).

**Remarks**

- The rank of a matrix doesnot depend on the way we carry out row-reduction or on the row-echelon form
- Matrices that correspond to equivalent system have the same rank
- All the operations mentioned above can be carried in columns also. Column reduction and rank by columns can be also computed. The rank by rows and rank by columns is always the same.

So, how the rank helps in determining the number of solutions of a system of linear equations?

> Let $Ax=b$ be a system of $m$ equations with $n$ unknowns.
>
> - The system has a unique solution or only one solution if and only if r($A$) = r($A^\star$) = $n$
> - If r($A$) $\neq$ r($A^\star$), the system has no solution
> - If r($A$) = r($A^\star$) < $n$, the system has infinitely many solutions with $n-$ r($A$) degrees of freedom

</div>
