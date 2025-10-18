# Applications and Properties of Matrices

This section covers how matrices are used to represent discrete structures like relations and explores fundamental properties related to the transpose, symmetry, and invertibility of matrices.

---

## Representing Relations using Matrices

A binary relation \(R\) from a finite set \(A\) to a finite set \(B\) can be represented by a **relation matrix** (or adjacency matrix).

Let \(A = \{a_1, a_2, ..., a_m\}\) and \(B = \{b_1, b_2, ..., b_n\}\). The relation matrix \(M_R\) is an \(m \times n\) matrix where the entry \(m_{ij}\) in the \(i\)-th row and \(j\)-th column is defined as:

\[
m_{ij} = \begin{cases}
1 & \text{if } (a_i, b_j) \in R \\
0 & \text{if } (a_i, b_j) \notin R
\end{cases}
\]

Essentially, a **1** indicates that the relation exists between the elements, and a **0** indicates it does not.

-   **Example**:

    Let \(A = \{1, 2, 3\}\) and \(B = \{x, y\}\).

    Let the relation be \(R = \{(1, y), (2, x), (2, y), (3, x)\}\).

    The relation matrix \(M_R\) will be a \(3 \times 2\) matrix.

    -   Row 1 corresponds to element '1' from set A.
    -   Row 2 corresponds to element '2' from set A.
    -   Row 3 corresponds to element '3' from set A.
    -   Column 1 corresponds to element 'x' from set B.
    -   Column 2 corresponds to element 'y' from set B.

    \[
    M_R =
    \begin{array}{c|cc}
    & \mathbf{x} & \mathbf{y} \\
    \hline
    \mathbf{1} & 0 & 1 \\
    \mathbf{2} & 1 & 1 \\
    \mathbf{3} & 1 & 0
    \end{array}
    =
    \begin{bmatrix}
    0 & 1 \\
    1 & 1 \\
    1 & 0
    \end{bmatrix}
    \]

---

## Transpose of a Matrix

The **transpose** of a matrix \(A\), denoted as \(A^T\) or \(A'\), is the matrix obtained by **interchanging its rows and columns**. If \(A\) is an \(m \times n\) matrix, then \(A^T\) will be an \(n \times m\) matrix.

If \(A = [a_{ij}]\), then \(A^T = [a_{ji}]\).

-   **Example**:

    If \(A = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}\), then its transpose is \(A^T = \begin{bmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{bmatrix}\).

### Properties of Transpose

-   **Double Transpose**: \((A^T)^T = A\)
-   **Addition**: \((A+B)^T = A^T + B^T\)
-   **Scalar Multiplication**: \((kA)^T = kA^T\), where \(k\) is a scalar.
-   **Reversal Law for Multiplication**: \((AB)^T = B^T A^T\)

---

## Symmetric and Skew-Symmetric Matrices

These are special types of square matrices defined by their relationship with their transpose.

-   **Symmetric Matrix**: A square matrix \(A\) is symmetric if **\(A = A^T\)**. This means \(a_{ij} = a_{ji}\) for all \(i\) and \(j\).
-   **Skew-Symmetric Matrix**: A square matrix \(A\) is skew-symmetric if **\(A = -A^T\)**. This implies \(a_{ij} = -a_{ji}\), and all main diagonal elements must be zero (\(a_{ii} = 0\)).

### Key Property
Any square matrix \(A\) can be uniquely expressed as the sum of a symmetric matrix (\(P\)) and a skew-symmetric matrix (\(Q\)).

-   Where \(A = P + Q\), the components are calculated as:
    -   Symmetric part: \(P = \frac{1}{2}(A + A^T)\)
    -   Skew-symmetric part: \(Q = \frac{1}{2}(A - A^T)\)

---

## Elementary Transformations of a Matrix

These are fundamental operations used to simplify or transform a matrix into a desired form (like row-echelon form) without changing its core properties. They are the basis for methods like Gaussian elimination and finding a matrix inverse.

There are three types of elementary transformations, which can be applied to rows or columns:

1.  **Interchange**: Swapping any two rows (or columns). Notation: \(R_i \leftrightarrow R_j\).
2.  **Scaling**: Multiplying all elements of a row (or column) by a non-zero constant. Notation: \(R_i \to kR_i\).
3.  **Combination**: Adding a non-zero multiple of one row (or column) to another row (or column). Notation: \(R_i \to R_i + kR_j\).

---

## Invertible Matrices

A square matrix \(A\) is **invertible** (or **non-singular**) if there exists another square matrix \(A^{-1}\) of the same order, called its **inverse**, such that:

\[
A \cdot A^{-1} = A^{-1} \cdot A = I
\]

where \(I\) is the identity matrix.

!!! success "Condition for Invertibility"
    A square matrix \(A\) has an inverse **if and only if its determinant is non-zero** (\(\det(A) \neq 0\)). If \(\det(A) = 0\), the matrix is called **singular** or non-invertible.

### Properties of Invertible Matrices

-   **Uniqueness**: If a matrix is invertible, its inverse is unique.
-   **Inverse of Inverse**: \((A^{-1})^{-1} = A\)
-   **Reversal Law for Inverses**: \((AB)^{-1} = B^{-1}A^{-1}\)
-   **Inverse of Transpose**: \((A^T)^{-1} = (A^{-1})^T\)

### Finding the Inverse using Elementary Operations
One common method is the **Gauss-Jordan method**:

1.  Create an **augmented matrix** by placing the identity matrix \(I\) to the right of matrix \(A\): \([A | I]\).
2.  Apply a sequence of **elementary row operations** to this augmented matrix.
3.  The goal is to transform the left side (\(A\)) into the identity matrix (\(I\)).
4.  If successful, the right side will be transformed into the inverse matrix \(A^{-1}\). The final form will be \([I | A^{-1}]\).
