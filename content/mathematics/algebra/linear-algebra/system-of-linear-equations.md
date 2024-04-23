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

One of the major applications of matrices is solving a system of linear equations.

## Linear equation

What is a linear equation? A linear equation is of the form,

$$
a_1x_1 + a_2x_2 + . . . + a_nx_n = b\\\\
\sum_{i=1}^n a_ix_i = b,
$$

where $a_i$ are called the coefficients, $x_i$ are called the unknowns. Geometrically, this defines a line in 2D and plane in 3D where n=2 and n=3 respectively. That's why the above equation is called linear equation. Consider, $x^2 + y =5$, is not linear and depicts a curve.

## System of linear equations

A system of linear equations is a collection of equations with $m$ equations and $n$ unknowns and all of them lie in the same $n$ dimensional space.

$$
\begin{cases}
a_{11}x_1 + a_{12}x_2 + . . . + a_{1n}x_n = b_1 \\\\
a_{21}x_1 + a_{22}x_2 + . . . + a_{2n}x_n = b_2 \\\\
    .\\\\
    . \\\\
a_{m1}x_1 + a_{m2}x_2 + . . . + a_{mn}x_n = b_m
\end{cases}
$$

If we use matrices to rewrite the above equation,

$$
\begin{bmatrix}a_{11}&a_{12}&a_{13}&.&.&.&a_{1n} \\\\ a_{21}&a_{22}&a_{23}&.&.&.&a_{2n} \\\\ .&.&.&.& & &. \\\\ .&.&.&&.&&.  \\\\ .&.&.&&&.&. \\\\ a_{m1}&a_{m2}&a_{m3}&.&.&.&a_{mn}\end{bmatrix} \begin{bmatrix}x_1 \\\\ x_2 \\\\ . \\\\ . \\\\ . \\\\ x_n\end{bmatrix} = \begin{bmatrix}b_1 \\\\ b_2 \\\\ . \\\\ . \\\\ . \\\\ b_n\end{bmatrix}
$$

By generalizing the above,
$$Ax = b,$$ where $A$ is the matrix of co-efficients, $x$ is the vector of unknows and $b$ is the vector of contants or output. If $b$ is a zero vector (i.e) $b_i = 0, \forall \text{ } i$, the system is said to be homogeneous. If $b$ is a non-zero vector, the system is said to be non-homogeneous.

### Solution

The solution for any system of linear equations will follow under the any of the following category,

- Has only one solution
- Has infinitely many solution (more than one)
- No solution

A system is said to be consistent if it has only one solution or has infinitely many solution. The system is said to be inconsistent if it has no solution.

## Solving a System of linear equations

The system of linear equations can be solved in many different methods. I haven't included the solving procedure as the part of the notes. Maybe in future if I will extend the scope of this notes to include it. The most commonly used (or taught) methods are,

- Gaussion elimination or Row-reduction method
- Cramer's Rule

### Row-reduction

Row-reduction method is based on the following idea,

> The solution of a system remain the same if we carry out the following **elementary operations**,
>
> - Swap two equations
> - Multiply an equation by any scalar $c$, where $c\neq 0$
> - Add a scalar multiple of one equation to another equation

For a run through example, watch this [example video](https://youtu.be/_Dvi4UllI-Y?si=LlBS1JoumrgQiyPA) from the references.

### Cramer's Rule

## Number of Solution

## Homogeneous and Non-Homogeneous Systems

As defined above, $Ax = 0$ is called a homogeneous system. **A homogeneous system always has a solution**.

- If a homogeneous system has zero solution, the solution is called the trivial solution of a homogeneous system and is defined as $x=0$ so that, $Ax = 0$
- If a homogeneous system has a non-zero solution, it has infinitely manay solutions. This means if $x\neq 0$ and $Ax=0$, the system has infinitely many solutions or infinitely many combination of $x$ such that $Ax=0$.

Thus, for a homogeneous system, the solution should be either trivial or infinitely many solution.

</div>
