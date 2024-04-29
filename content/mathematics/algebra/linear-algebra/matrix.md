---
title: Matrix
weight: 13
next: vector-space
math: true
cascade:
  type: docs
sidebar:
  open: true
---

<br>
<div style="text-align: justify;">

A matrix is a table or chart or array of elements arranged in rows and columns. Every element of a matrix is called an entry. A matrix is usually defined over a field $\mathbb{F}$, which means that the elements of the matrix are from $\mathbb{F}$.

> To provide a simple idea, a matrix is a collection of vectors. A matrix with a single row is called a row vector and a matrix with a single column is called as column vector.

In general, a matrix is denoted using a upper case letter and defined as,

$A = \begin{bmatrix}a_{11}&a_{12}&a_{13}&\dots &a_{1n} \\\\ a_{21}&a_{22}&a_{23}&\dots&a_{2n} \\\\ \vdots&\vdots&\vdots&\ddots&\vdots \\\\ a_{m1}&a_{m2}&a_{m3}&\dots&a_{mn}\end{bmatrix} = \begin{pmatrix}a_{11}&a_{12}&a_{13}&\dots &a_{1n} \\\\ a_{21}&a_{22}&a_{23}&\dots&a_{2n} \\\\ \vdots&\vdots&\vdots&\ddots&\vdots \\\\ a_{m1}&a_{m2}&a_{m3}&\dots&a_{mn}\end{pmatrix}$

**Size of the matrix**: The size of a matrix is defined by the number of rows and columns and denoted by $m \times n$, where $m$ is number of rows and $n$ is the number of columns. There is no limit to the numbers of rows and columns.

> $a_{ij}$ or $a_{i,j}$ or $a_{(i,j)}$ is the entry at $i^{th}$ row and $j^{th}$ column of the matrix

The following are some of the notation used for matrix,

> - $A_{m\times n}$
> - $A \in M_{m \times n} (\mathbb{C})$, This means A is a matrix of size $m \times n$ whose entries are from the field $\mathbb{C}$
> - If $m=n$, $A \in M_n (\mathbb{C})$

## Terminology

Let us see a few terminologies and different types of matrices that we will come across in this notes,

- **Zero Matrix** - A matrix whose entries are all zero. $a_{ij} = 0$, $\forall$ $i, j$
- **Square Matrix** - A matrix whose number of rows is equal to the number of columns
- **Main Diagonal** - Main diagonal is all the elements whose index is denoted by $a_{ii}$. This term is mostly associated with a square matrix but also valid for a rectangular matrix where the diagonal will not end with the last entry of the matrix
- **Diagonal Matrix** - A Diagonal matrix is a square matrix whose main diagonal has non-zero entries and off-diagonal entries are zero. $a_{ii} \neq 0$, $\forall$ $i$ and $a_{ij} = 0$, $\forall$ $i\neq j$
- **Identity Matrix** - An Identity matrix is a special case of diagonal matrix whose main diagonal entires are 1. $a_{ii} = 1$, $\forall$ $i$ and $a_{ij} = 0$, $\forall$ $i\neq j$
- **Scalar Matrix** - A Scalar matrix is a special case of diagonal matrix whose main diagonal entires are a constant $c$. $a_{ii} = c$, $\forall$ $i$ and $a_{ij} = 0$, $\forall$ $i\neq j$
- **Transposed Matrix** - The transposed of a matrix $A$ is denoted by $A^T$ and defined as $A^T_{ij} = A_{ji}$. A transpose operation will convert the rows into columns and columns into rows.
- **Symmetric Matrix** - A symmetric matrix is a matrix which is equal to its transpose. $A = A^T$ (i.e) $a_{ij} = a_{ji}$
- **Negation** - A negation of a matrix will add negation (multiply by -1) to all the entries of the matrix. $-A$ converts $a_{ij}$ into $-a_{ij}$, $\forall$ $i, j$
- **Skew-Symmetric Matrix** - A skew-symmetric matrix is a matrix which is equal to the negation of its transpose. $A = -A^T$. Consider here, the only possibility of having a skew-symmetric matrix, is to have zero as a entry in its main diagonal.
- **Upper Triangular Matrix** - A matrix with zero entries below the diagonal and non-zero entries above the diagonal. $a_{ij} = 0$, $\forall$ $i > j$
- **Lower Triangular Matrix** - A matrix with zero entries above the diagonal and non-zero entries below the diagonal. $a_{ij} = 0$, $\forall$ $j > i$

## Basic Operations

### Equality

Two matrices $A$ and $B$ are said to be equal if they have exactly same size and exactly the same entries. $A_{ij} = B_{ij}$, $\forall$ $i\leq m$ and $j\leq n$.

Consider two matrices $V = \begin{bmatrix}3&2&6 \\\\ 2&1&2\end{bmatrix}$ and $W = \begin{bmatrix}0&1&2 \\\\ -1&4&6\end{bmatrix}$. Though $V$ and $W$ are of same size, their entries are different. So, $V \neq W$.

### Matrix addition and subtraction

Similar to vector, Matrix addition and subtraction is an element-wise operation. Addition of two matrices $A$ and $B$ of length $m \times n$ results in a new matrix $C$ of size $m \times n$ and defined as,

$$C_{ij} = A_{ij} + B_{ij}, \forall \text{ } i\leq m \text{ and } j\leq n $$

`Matrix addition and subtraction is defined only if both tha matrices are of same size` (i.e) the number of rows and columns in both the matrices should be equal. For example $V+W$ is,

$V+W = \begin{bmatrix}3&2&6 \\\\ 2&1&2\end{bmatrix} + \begin{bmatrix}0&1&2 \\\\ -1&4&6\end{bmatrix} = \begin{bmatrix}3+0&2+1&6+2 \\\\ 2-1&1+4&2+6\end{bmatrix} = \begin{bmatrix}3&3&8 \\\\ 1&5&8\end{bmatrix}$

Similarly, subtraction of two matrices $A$ and $B$ of length $m \times n$ results in a new matrix $C$ of size $m \times n$ and defined as,

$$C_{ij} = A_{ij} - B_{ij}, \forall \text{ } i\leq m \text{ and } j\leq n $$

For example $V-W$ is,

$V-W = \begin{bmatrix}3&2&6 \\\\ 2&1&2\end{bmatrix} - \begin{bmatrix}0&1&2 \\\\ -1&4&6\end{bmatrix} = \begin{bmatrix}3-0&2-1&6-2 \\\\ 2+1&1-4&2-6\end{bmatrix} = \begin{bmatrix}3&1&4 \\\\ 3&-3&-4\end{bmatrix}$

**Properties**

> - Addition of matrices is commutative, $A + B = B + A$
> - Addition of matrices is associative, $(A+B)+C = A+(B+C)$
> - $A + O = A$, where $O$ is the zero matrix
> - $A + (-A) = O$
> - Subtraction of matrices is not always commutative, $A - B \neq B - A$, unless $A=B$
> - Subtraction of matrices is associative, $(A-B)-C = A-(B-C)$
> - $A - O = A$, where $O$ is the zero matrix

### Matrix Multiplication

Matrix multiplication between two matrices $A$ and $B$ of size $m\times n$ and $p\times q$ respectively is defined if and only if,

> $n=p$ (i.e) number of columns in the first matrix is equal to the number of rows in the second matrix

The result of the matrix multiplication is a matrix $C$ of size $m\times q$.

Matrix multiplication will result in another matrix $C$ and is computed by,

$$
C = AB\\\\
C_{ij} = \sum_{k=1}^{n} A_{ik}B_{kj},
$$

where n is the number of columns in the first matrix or the number of rows in the second matrix.

For example, if we consider $V$ and $W$, matrix multiplication is not defined since the size of the matrices are $2\times 3$. Now, consider $V$ and $W^T$, the size of matrix $V$ is $2\times 3$ and the size of matrix $W^T$ is $3\times 2$. So, matrix multiplication is defined for $V$ and $W^T$ and the resultant matrix will be of size $2\times 2$.

$VW^T = \begin{bmatrix}3&2&6 \\\\ 2&1&2\end{bmatrix} \begin{bmatrix}0&-1 \\\\ 1&4 \\\\ 2&6\end{bmatrix}$

$VW^T = \begin{bmatrix}(3\times 0) + (2\times 1) + (6\times 2)&(2\times 0) + (1\times 1) + (2\times 2) \\\\ (3\times -1) + (2\times 4) + (6\times 6)&(2\times -1) + (1\times 4) + (2\times 6)\end{bmatrix}$

$VW^T = \begin{bmatrix}(0+2+12)&(0+1+4) \\\\ (-3+8+36)&(-2+4+12)\end{bmatrix}$

$VW^T = \begin{bmatrix}14&5 \\\\ 41&14\end{bmatrix}$

**Remarks**

- $AB \neq BA$. In fact, sometimes the product is not even defined. Consider $A$ and $B$ of size $2\times 3$ and $3\times 4$ respectively. Here, $AB$ is defined whereas, $BA$ is not defined as the number of columns in $B$ is 4 and number of rows in $A$ is 2.
- For any two numbers $X$ and $Y$ from $\mathbb{R}$ or $\mathbb{C}$, $XY \neq 0$ if $X\neq 0, Y \neq 0$. But in matrix multiplication, $AB=0$ even if $A\neq O, B\neq O$, where $O$ is the zero matrix.
- No cancellation allowed. Consider $X$, $Y$ and $Z$ from $\mathbb{R}$ or $\mathbb{C}$, $XY = XZ => Y = Z$. But in matrices, $AB = AC => B \neq C$

**Properties**

> - Matrix multiplication is not commutative. $AB \neq BA$
> - Matrix multiplication is associative, $(AB)C = A(BC)$
> - Matrix multiplication is distributive with addition or subtraction. $A(B+C) = AB + AD$ and $(A+B)C = AC + BC$
> - $\alpha(AB) = (\alpha A)B = A(\alpha B)$, where $\alpha$ is a scalar
> - $AI = IA = A$, where $I$ is the identity matrix of size $n$
> - $AO = OA = O$, where $O$ is the zero matrix
> - $(AB)^T = B^TA^T$
> - $A^0 = I$
> - Powers of the matrix is defined only for square matrix, as $A^2 = AA$. For a rectangular matrix, the sizes would satisfy the definition.

Multiplication of matrix and vector is also allowed. Consider a matrix $A$ of size $2\times 3$ and a vector of dimension 3. Here, we consider the vector to be a column vector (i.e) a matrix with one column. Now, the size of the column vector is $3\times 1$. So, matrix multiplication is defined and the resultant matrix is of size $2\times 1$.

Hadamard product is also defined for matrices of same size. Hadamard product of two matrices $A$ and $B$ of size $m\times n$ is a elementwise multiplication and defined as,

$$C_{ij} =  A_{ij}B_{ij} \forall \text{ } i\leq m \text{ and } j\leq n$$

### Scalar-Matrix addition and subtraction

Addition or subtraction of a scalar to a matrix simply involves adding or subtracting the scalar to each element.

$$A_{ij} = A_{ij} \pm C$$

The above definition doesn't hold in a polynomial of the matrix. Consider a polynomial $P(A) = 3A^2-4A+5$, where $A$ is a matrix. By definition, 5 is actually $5A^0$. So, the polynomial will be, $P(A) = 3A^2-4A+5A^0$ and $A^0 = I$.

So, $P(A) = 3A^2-4A+5I$

### Scalar-Matrix multiplication

Mutlipliying a scalar $C$ to with a matrix $A$ will result in a matrix whose entries are defined as,

$$A_{ij} = CA_{ij}, \forall \text{ } i, j $$

For example, if we multiply $V$ by 2,

$2V = 2\begin{bmatrix}3&2&6 \\\\ 2&1&2\end{bmatrix} = \begin{bmatrix}6&4&12 \\\\ 4&2&4\end{bmatrix}$

**Properties**

> - $\alpha (A+B) = \alpha A + \alpha B$
> - $(\alpha + \beta)A = \alpha A + \beta A$
> - $(\alpha \beta)A = \alpha(\beta A)$

where $\alpha$ and $\beta$ are scalars.

### Transpose

As stated above, the transpose operation will convert the rows into columns and columns into rows and is defined as, $$A^T_{ij} = A_{ji}$$

For example, the transpose of the matrix $V$ is $V^T = \begin{bmatrix}3&2 \\\\ 2&1 \\\\ 6&2\end{bmatrix}$

**Properties**

> - $(A^T)^T = A$
> - $(A+B)^T = A^T + B^T$
> - $(A-B)^T = A^T - B^T$
> - $(\alpha A)^T = \alpha A^T$, where $\alpha$ is a scalar

### Vector-Matrix addition and subtraction

## Determinant

We going to see the qualitative aspect of determinant of a matrix. For how to compute the determinant, please watch this [video](https://youtu.be/_Se_ZiFNVzU?si=n063fxtnngnNPTgE). Determinant is only defined for a square matrix. The determinant of a matrix is obtained by eliminating the $i^{th}$ row and the $j^{th}$ column of $A$ called the $ij^{th}$ minor of $A$ denoted by $M_{ij}$.

> The determinant of a matrix $A_{n\times n}$ denoted by $|A|$ is defined as,
> $$ |A| = (-1)^{n+1} a\_{1n} M\_{1n}$$

**Properties**

> - |A^T| = A
> - If one the rows/columns of a matrix $A$ is zero, $|A| = 0$
> - Determinant of a triangular matrix is the product of the main-diagonal entries
> - If we exchange or swap two rows/columns, the sign of the determinant changes
> - If two rows/columns of a matrix $A$ is equal, $|A| = 0$
> - A common factor of a row/column can be taken out of the determinant. $|\alpha A| = \alpha^n |A|$
> - If one row or column is a multiple of another, the determinant is zero
> - If we add a scalar multiple of a row/column to another row/column, the determinant doesn't change
> - Determinant of the identity matrix is 1
> - $|AB| = |A||B|$

## Inverse

The following discussion will hold only for a square matrix. So, how do we define the inverse of a matrix or determine if a matrix is invertible?

> A square matrix $A$ is invertible if there exists a matrix $A^{-1}$ such that $AA^{-1} = I$

**Properties**

> - If $A^{-1}$ exists, $AA^{-1} = A^{-1}A = I$. Matrix multiplication is not commutative except in this case.
> - If $A$ is invertible, $A^{-1}$ is unique to $A$
> - If two matrices $A$ and $B$ are invertible, $(AB)^{-1} = B^{-1}A^{-1}$
> - If $A$ is invertible, $(A^T)^{-1} = (A^{-1})^T$

We will see how to find the inverse of a matrix in the later notes.

</div>
