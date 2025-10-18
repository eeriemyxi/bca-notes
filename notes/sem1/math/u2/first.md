# Types of Matrices

A **matrix** (plural: matrices) is a rectangular array or table of numbers, symbols, or expressions, arranged in rows and columns. It's a fundamental concept in linear algebra. An \(m \times n\) matrix has \(m\) rows and \(n\) columns.

---

## Based on Dimensions

### Row Matrix
A matrix that has only **one row** is called a row matrix. Its order is \(1 \times n\), where \(n\) is the number of columns.

-   **Example**: The matrix \(A = \begin{bmatrix} 5 & -1 & 0 & 9 \end{bmatrix}\) is a \(1 \times 4\) row matrix.

### Column Matrix
A matrix that has only **one column** is called a column matrix. Its order is \(m \times 1\), where \(m\) is the number of rows.

-   **Example**: The matrix \(B = \begin{bmatrix} 7 \\ -2 \\ 4 \end{bmatrix}\) is a \(3 \times 1\) column matrix.

### Square Matrix
A matrix in which the **number of rows is equal to the number of columns** (\(m=n\)) is called a square matrix of order \(n\).

-   **Example**: \(C = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{bmatrix}\) is a square matrix of order 3.

!!! info "Principal Diagonal"
    In a square matrix, the elements \(a_{11}, a_{22}, a_{33}, ..., a_{nn}\) form the **main diagonal** or **principal diagonal** of the matrix. For matrix \(C\) above, the principal diagonal consists of the elements 1, 5, and 9.

[insert image on main diagonal of a square matrix here]

### Rectangular Matrix
A matrix where the number of rows is not equal to the number of columns (\(m \neq n\)) is a rectangular matrix. Row and column matrices are special cases of rectangular matrices.

---

## Based on Element Values

### Null or Zero Matrix
A matrix in which **all the elements are zero** is called a null or zero matrix. It is denoted by \(O\). A zero matrix can be of any order, square or rectangular.

-   **Example**: \(O_{2 \times 3} = \begin{bmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix}\) is a \(2 \times 3\) zero matrix.

!!! note
    The zero matrix is the additive identity for matrix addition, meaning \(A + O = A\).

### Diagonal Matrix
A **square matrix** where all the non-diagonal elements are zero is called a diagonal matrix. The diagonal elements themselves can be zero or non-zero.
A square matrix \(A = [a_{ij}]\) is a diagonal matrix if \(a_{ij} = 0\) whenever \(i \neq j\).

-   **Example**:

    \[
    D = \begin{bmatrix}
    -3 & 0 & 0 \\
    0 & 8 & 0 \\
    0 & 0 & 0
    \end{bmatrix}
    \]

### Scalar Matrix
A **diagonal matrix** in which all the principal diagonal elements are **equal** is called a scalar matrix.
A square matrix \(A = [a_{ij}]\) is a scalar matrix if \(a_{ij} = 0\) whenever \(i \neq j\) and \(a_{ij} = k\) (a constant) whenever \(i=j\).

-   **Example**:

    \[
    S = \begin{bmatrix}
    5 & 0 & 0 \\
    0 & 5 & 0 \\
    0 & 0 & 5
    \end{bmatrix}
    \]

    Here, \(S\) is a scalar matrix with \(k=5\). This can also be written as \(5I\), where \(I\) is the identity matrix.

### Identity Matrix (or Unit Matrix)
A **scalar matrix** where all the principal diagonal elements are **1** is called an identity matrix or unit matrix. It is denoted by \(I_n\) or simply \(I\), where \(n\) is the order of the matrix.

A square matrix \(A = [a_{ij}]\) is an identity matrix if \(a_{ij} = 1\) whenever \(i = j\) and \(a_{ij} = 0\) whenever \(i \neq j\).

-   **Example of a \(3 \times 3\) Identity Matrix**:

    \[
    I_3 = \begin{bmatrix}
    1 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & 1
    \end{bmatrix}
    \]

!!! success "Multiplicative Identity"
    The identity matrix \(I\) is the multiplicative identity for matrices, meaning for any compatible matrix \(A\), the product \(A \cdot I = I \cdot A = A\).

---

## Special Types of Square Matrices

### Triangular Matrix
A square matrix is called triangular if all its elements above or below the main diagonal are zero. There are two types:

-   **Upper Triangular Matrix**: A square matrix where all elements **below** the main diagonal are zero. That is, \(a_{ij} = 0\) for all \(i > j\).
    -   **Example**:

        \[
        U = \begin{bmatrix}
        1 & 9 & -2 \\
        0 & 5 & 3 \\
        0 & 0 & 4
        \end{bmatrix}
        \]

-   **Lower Triangular Matrix**: A square matrix where all elements **above** the main diagonal are zero. That is, \(a_{ij} = 0\) for all \(i < j\).
    -   **Example**:

        \[
        L = \begin{bmatrix}
        1 & 0 & 0 \\
        -4 & 8 & 0 \\
        7 & 0 & 2
        \end{bmatrix}
        \]

[insert image on upper and lower triangular matrices here]

### Symmetric Matrix
A square matrix \(A\) is called symmetric if it is equal to its transpose (\(A = A^T\)). This means \(a_{ij} = a_{ji}\) for all values of \(i\) and \(j\). The elements are mirrored across the main diagonal.

-   **Example**:

    \[
    A = \begin{bmatrix}
    1 & \mathbf{7} & \mathbf{-3} \\
    \mathbf{7} & 4 & \mathbf{5} \\
    \mathbf{-3} & \mathbf{5} & 6
    \end{bmatrix} \quad \text{and} \quad A^T = \begin{bmatrix}
    1 & \mathbf{7} & \mathbf{-3} \\
    \mathbf{7} & 4 & \mathbf{5} \\
    \mathbf{-3} & \mathbf{5} & 6
    \end{bmatrix}
    \]

### Skew-Symmetric Matrix
A square matrix \(A\) is called skew-symmetric if it is equal to the negative of its transpose (\(A = -A^T\)). This requires two conditions:

1.  \(a_{ij} = -a_{ji}\) for all \(i \neq j\).
2.  All principal diagonal elements must be zero (\(a_{ii} = 0\)).

-   **Example**:

    \[
    B = \begin{bmatrix}
    0 & 1 & -2 \\
    -1 & 0 & 3 \\
    2 & -3 & 0
    \end{bmatrix} \quad \text{and} \quad -B^T = -\begin{bmatrix}
    0 & -1 & 2 \\
    1 & 0 & -3 \\
    -2 & 3 & 0
    \end{bmatrix} = \begin{bmatrix}
    0 & 1 & -2 \\
    -1 & 0 & 3 \\
    2 & -3 & 0
    \end{bmatrix}
    \]


## Problem Set

---

#### **(1) Based on Dimensions**

1.  Identify the type of matrix \( A = \begin{bmatrix} 5 & -2 & 1 \end{bmatrix} \) based on its dimensions.
2.  What is the order of a column matrix containing \( n \) elements?
3.  Construct a \( 3 \times 2 \) rectangular matrix \( A \) where its elements are given by \( a_{ij} = 2i - j \).
4.  Is the matrix \( B = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix} \) a square matrix? Justify your answer.
5.  If a matrix has 13 elements, can it be a square matrix? Explain.
6.  Give an example of a matrix which is both a row matrix and a column matrix.

---

#### **(2) Based on Element Values**

7.  Define a Null Matrix. Give an example of a \( 2 \times 2 \) null matrix.
8.  Identify if the matrix \( A = \begin{bmatrix} 7 & 0 & 0 \\ 0 & 7 & 0 \\ 0 & 0 & 7 \end{bmatrix} \) is a diagonal, scalar, or identity matrix. Explain your reasoning.
9.  What is the fundamental difference between a diagonal matrix and a scalar matrix?
10. If \( I \) is an identity matrix of order 3, what are the values of \( I_{11}, I_{23}, \) and \( I_{32} \)?
11. Find the values of \( x \) and \( y \) if the matrix \( \begin{bmatrix} x-2 & 0 \\ 0 & y+5 \end{bmatrix} \) is an identity matrix.
12. Is every scalar matrix a diagonal matrix? Is the converse true?
13. Construct a \( 3 \times 3 \) diagonal matrix \( D \) such that \( D_{11}=5, D_{22}=-1, D_{33}=0 \).
14. If \( A = \begin{bmatrix} k^2-1 & 0 \\ 0 & k^2-1 \end{bmatrix} \) is a null matrix, find all possible values of \( k \).

---

#### **(3) Special Types of Square Matrices**

15. Define a Lower Triangular Matrix. Construct a \( 3 \times 3 \) lower triangular matrix \( L \) where \( L_{ij} = i+j \).
16. Identify the matrix \( B = \begin{bmatrix} 1 & 2 & 3 \\ 0 & 8 & 5 \\ 0 & 0 & 4 \end{bmatrix} \). For this matrix to be triangular, what is the condition on its elements \( b_{ij} \)?
17. Can a non-square matrix be a triangular matrix? Explain.
18. Construct a \( 3 \times 3 \) upper triangular matrix \( U \) where \( U_{ij} = i \cdot j \).
19. What type of matrix is both an upper triangular and a lower triangular matrix? Give an example.

---

#### **(4) Symmetric & Skew-Symmetric Matrices**

20. What is the necessary condition for a square matrix \( A \) to be symmetric? Express this using its transpose, \( A^T \).
21. What is the property of the diagonal elements of a skew-symmetric matrix? Prove it.
22. Find the values of \( a, b, \) and \( c \) if the matrix \( A = \begin{bmatrix} 2 & a & 3 \\ 5 & -1 & c \\ b & 1 & 7 \end{bmatrix} \) is symmetric.
23. Find the transpose of \( F = \begin{bmatrix} 0 & 5 & -2 \\ -5 & 0 & 1 \\ 2 & -1 & 0 \end{bmatrix} \). Hence, show that \( F \) is a skew-symmetric matrix.
24. If \( A \) is a square matrix, prove that the matrix \( B = A + A^T \) is always a symmetric matrix.
25. If \( A \) is a square matrix, prove that the matrix \( C = A - A^T \) is always a skew-symmetric matrix.
26. If \( A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} \), find \( \frac{1}{2}(A + A^T) \).
27. If \( B = \begin{bmatrix} 3 & -1 \\ 5 & 2 \end{bmatrix} \), find \( \frac{1}{2}(B - B^T) \).
28. Express the matrix \( A = \begin{bmatrix} 6 & 1 \\ -2 & 3 \end{bmatrix} \) as the sum of a symmetric and a skew-symmetric matrix.
29. Given \( A = \begin{bmatrix} \cos\alpha & -\sin\alpha \\ \sin\alpha & \cos\alpha \end{bmatrix} \), show that \( A^T A = I \).
30. Prove that any square matrix can be uniquely expressed as the sum of a symmetric and a skew-symmetric matrix.
