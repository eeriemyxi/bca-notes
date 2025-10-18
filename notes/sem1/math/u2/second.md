# Matrix Operations

Matrix operations are the algebraic procedures performed on matrices. These include addition, subtraction, scalar multiplication, and matrix multiplication.

---

## Addition and Subtraction of Matrices

Two matrices can be added or subtracted only if they have the **same order** (i.e., the same number of rows and the same number of columns). The operation is performed by adding or subtracting the corresponding elements.

If \(A = [a_{ij}]\) and \(B = [b_{ij}]\) are two matrices of order \(m \times n\), then their sum \(A+B\) is a matrix \(C = [c_{ij}]\) of the same order, where \(c_{ij} = a_{ij} + b_{ij}\) for all \(i\) and \(j\).

-   **Example**:
    Let \(A = \begin{bmatrix} 8 & 3 \\ 4 & 5 \end{bmatrix}\) and \(B = \begin{bmatrix} 1 & -2 \\ -4 & 6 \end{bmatrix}\).
    -   **Addition**:

        \[
        A+B = \begin{bmatrix} 8+1 & 3+(-2) \\ 4+(-4) & 5+6 \end{bmatrix} = \begin{bmatrix} 9 & 1 \\ 0 & 11 \end{bmatrix}
        \]

    -   **Subtraction**:

        \[
        A-B = \begin{bmatrix} 8-1 & 3-(-2) \\ 4-(-4) & 5-6 \end{bmatrix} = \begin{bmatrix} 7 & 5 \\ 8 & -1 \end{bmatrix}
        \]

### Properties of Matrix Addition

-   **Commutative Law**: \(A + B = B + A\)
-   **Associative Law**: \((A + B) + C = A + (B + C)\)
-   **Existence of Additive Identity**: The zero matrix \(O\) is the additive identity. \(A + O = O + A = A\).
-   **Existence of Additive Inverse**: For any matrix \(A\), there is a matrix \(-A\) such that \(A + (-A) = (-A) + A = O\).

---

## Scalar Multiplication

Multiplying a matrix by a scalar (a single number) involves multiplying **every element** of the matrix by that scalar.

If \(A = [a_{ij}]\) is a matrix of order \(m \times n\) and \(k\) is a scalar, then \(kA\) is another matrix of the same order, obtained by multiplying each element of \(A\) by \(k\). So, \(kA = [ka_{ij}]\).

-   **Example**:
    Let \(A = \begin{bmatrix} 3 & 1 \\ -2 & 0 \\ 5 & 4 \end{bmatrix}\) and \(k = -2\).

    \[
    -2A = -2 \begin{bmatrix} 3 & 1 \\ -2 & 0 \\ 5 & 4 \end{bmatrix} = \begin{bmatrix} -2(3) & -2(1) \\ -2(-2) & -2(0) \\ -2(5) & -2(4) \end{bmatrix} = \begin{bmatrix} -6 & -2 \\ 4 & 0 \\ -10 & -8 \end{bmatrix}
    \]

### Properties of Scalar Multiplication
If \(k\) and \(l\) are scalars and \(A\) and \(B\) are matrices of the same order:

-   \(k(A + B) = kA + kB\)
-   \((k + l)A = kA + lA\)

---

## Matrix Multiplication

The product of two matrices \(A\) and \(B\), denoted \(AB\), is defined only if the **number of columns in \(A\) is equal to the number of rows in \(B\) L**.

If \(A\) is an \(m \times n\) matrix and \(B\) is an \(n \times p\) matrix, then their product \(AB\) is an \(m \times p\) matrix.

[insert image on matrix multiplication rule columns equal rows here]

To find the element in the \(i\)-th row and \(j\)-th column of the product matrix \(AB\), you take the dot product of the \(i\)-th row of \(A\) with the \(j\)-th column of \(B\).

-   **Example**:
    Let \(A = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}\) (\(2 \times 3\)) and \(B = \begin{bmatrix} 7 & 8 \\ 9 & 1 \\ 2 & 3 \end{bmatrix}\) (\(3 \times 2\)). The product \(AB\) will be a \(2 \times 2\) matrix.

    \[
    AB = \begin{bmatrix}
    (1\cdot7 + 2\cdot9 + 3\cdot2) & (1\cdot8 + 2\cdot1 + 3\cdot3) \\
    (4\cdot7 + 5\cdot9 + 6\cdot2) & (4\cdot8 + 5\cdot1 + 6\cdot3)
    \end{bmatrix}
    \]

    \[
    AB = \begin{bmatrix}
    (7 + 18 + 6) & (8 + 2 + 9) \\
    (28 + 45 + 12) & (32 + 5 + 18)
    \end{bmatrix} = \begin{bmatrix}
    31 & 19 \\
    85 & 55
    \end{bmatrix}
    \]

### Properties of Matrix Multiplication

-   **Not Commutative (Generally)**: In most cases, \(AB \neq BA\). In the example above, \(BA\) would be a \(3 \times 3\) matrix, which is clearly not equal to the \(2 \times 2\) matrix \(AB\).
-   **Associative Law**: \((AB)C = A(BC)\), provided the products are defined.
-   **Distributive Law**:
    -   \(A(B+C) = AB + AC\)
    -   \((A+B)C = AC + BC\)
-   **Existence of Multiplicative Identity**: For every square matrix \(A\), there is an identity matrix \(I\) of the same order such that \(AI = IA = A\).

---

## Elementary Row and Column Operations

These are fundamental operations used to manipulate matrices, often for solving systems of linear equations or finding a matrix inverse. There are three types of elementary operations.

### 1. Interchange (Swapping)
Any two rows (or columns) of a matrix can be interchanged.

-   **Notation**: \(R_i \leftrightarrow R_j\) denotes the interchange of the \(i\)-th and \(j\)-th rows.

### 2. Multiplication (Scaling)
The elements of any row (or column) can be multiplied by a **non-zero** scalar.

-   **Notation**: \(R_i \to kR_i\) denotes multiplying the \(i\)-th row by the scalar \(k\).

### 3. Addition (Combination)
You can add a scalar multiple of one row (or column) to another row (or column).

-   **Notation**: \(R_i \to R_i + kR_j\) denotes adding \(k\) times the \(j\)-th row to the \(i\)-th row.

-   **Example of Row Operations**:

    Let \(A = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{bmatrix}\).

    - Applying \(R_2 \leftrightarrow R_3\):

    \[
    \begin{bmatrix} 1 & 2 & 3 \\ 7 & 8 & 9 \\ 4 & 5 & 6 \end{bmatrix}
    \]

    -   Applying \(R_2 \to R_2 - 4R_1\) to the original matrix \(A\):

        \[
        R_2: \begin{bmatrix} 4 & 5 & 6 \end{bmatrix} - 4 \begin{bmatrix} 1 & 2 & 3 \end{bmatrix} = \begin{bmatrix} 4-4 & 5-8 & 6-12 \end{bmatrix} = \begin{bmatrix} 0 & -3 & -6 \end{bmatrix}
        \]

        Resulting matrix:

        \[
        \begin{bmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 7 & 8 & 9 \end{bmatrix}
        \]

!!! info "Vector Operations"
    Vectors can be represented as single-row (row vectors) or single-column (column vectors) matrices. Therefore, vector addition, subtraction, and scalar multiplication are simply special cases of the matrix operations defined above.

## Problem-set

**Section A: Matrix Addition, Subtraction & Scalar Multiplication**

1.  Given matrices \(A = \begin{pmatrix} 2 & 4 \\ 3 & 1 \end{pmatrix}\) and \(B = \begin{pmatrix} 1 & 0 \\ -1 & 5 \end{pmatrix}\), find \(A + B\).
2.  Given matrices \(P = \begin{pmatrix} 7 & -2 \\ 4 & 5 \end{pmatrix}\) and \(Q = \begin{pmatrix} 3 & 3 \\ 1 & 0 \end{pmatrix}\), find \(P - Q\).
3.  If \(C = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & -1 \end{pmatrix}\), find \(3C\).
4.  Using matrices \(A = \begin{pmatrix} 2 & 4 \\ 3 & 1 \end{pmatrix}\) and \(B = \begin{pmatrix} 1 & 0 \\ -1 & 5 \end{pmatrix}\), compute \(2A - B\).
5.  Verify the commutative property of addition (\(A+B = B+A\)) for \(A = \begin{pmatrix} 1 & 5 \\ 2 & 3 \end{pmatrix}\) and \(B = \begin{pmatrix} 0 & -2 \\ 3 & -1 \end{pmatrix}\).
6.  Find matrix \(X\) such that \(2X + A = B\), where \(A = \begin{pmatrix} 4 & 0 \\ -2 & 2 \end{pmatrix}\) and \(B = \begin{pmatrix} 2 & -2 \\ 4 & 6 \end{pmatrix}\).
7.  If \(k=4\), \(A = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}\), and \(B = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}\), show that \(k(A+B) = kA + kB\).
8.  Given \(A = \begin{pmatrix} 8 & 0 \\ 4 & -2 \\ 3 & 6 \end{pmatrix}\) and \(B = \begin{pmatrix} 2 & -2 \\ 4 & 2 \\ -5 & 1 \end{pmatrix}\), find the matrix \(X\) such that \(2A + 3X = 5B\).

***

**Section B: Matrix Multiplication**

9.  Let \(A = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}\) and \(B = \begin{pmatrix} 5 & 6 \\ 7 & 8 \end{pmatrix}\). Calculate \(AB\).
10. Using the matrices from Q9, calculate \(BA\) and show that \(AB \neq BA\).
11. Let \(C = \begin{pmatrix} 1 & 0 & 2 \\ -1 & 3 & 1 \end{pmatrix}\) and \(D = \begin{pmatrix} 3 & 1 \\ 2 & 1 \\ 1 & 0 \end{pmatrix}\). Compute \(CD\).
12. Is the product \(DC\) defined for the matrices in Q11? If yes, compute it.
13. Given \(A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}\), \(B = \begin{pmatrix} 2 & 0 \\ 3 & 4 \end{pmatrix}\), and \(C = \begin{pmatrix} 1 & 0 \\ 2 & 3 \end{pmatrix}\), verify the associative property \((AB)C = A(BC)\).
14. Using the matrices from Q13, verify the distributive property \(A(B+C) = AB + AC\).
15. If \(A = \begin{pmatrix} 3 & -2 \\ 4 & -2 \end{pmatrix}\), find a scalar \(k\) such that \(A^2 = kA - 2I\), where \(I\) is the \(2 \times 2\) identity matrix.
16. If \(A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}\), find \(A^2\) and \(A^3\).
17. Find two non-zero \(2 \times 2\) matrices \(A\) and \(B\) such that their product \(AB\) is the zero matrix \(O\).
18. If \(f(x) = x^2 - 5x + 6\), find \(f(A)\) where \(A = \begin{pmatrix} 2 & 0 & 1 \\ 2 & 1 & 3 \\ 1 & -1 & 0 \end{pmatrix}\).

***

**Section C: Elementary Row and Column Operations**

*For questions 19-24, use the matrix \(M = \begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{pmatrix}\).*

19. Apply the row operation \(R_1 \leftrightarrow R_3\) to matrix \(M\).
20. Apply the column operation \(C_2 \leftrightarrow C_3\) to matrix \(M\).
21. Apply the row operation \(R_2 \to 3R_2\) to matrix \(M\).
22. Apply the column operation \(C_1 \to \frac{1}{2}C_1\) to matrix \(M\).
23. Apply the row operation \(R_2 \to R_2 - 4R_1\) to matrix \(M\).
24. Apply the column operation \(C_3 \to C_3 - 2C_2\) to matrix \(M\).
25. On matrix \(A = \begin{pmatrix} 1 & 1 & 1 \\ 2 & 1 & -1 \\ 3 & 2 & 0 \end{pmatrix}\), perform the operations \(R_2 \to R_2 - 2R_1\) and then \(R_3 \to R_3 - 3R_1\).
26. Transform the matrix \(B = \begin{pmatrix} 2 & 4 & 6 \\ 1 & 3 & 5 \\ 3 & 7 & 11 \end{pmatrix}\) by making the element in the first row, first column a '1' using a scaling operation.
27. Using the result from Q26, perform row operations to create zeros below the leading '1' in the first column.
28. A matrix \(A = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}\) is transformed into \(B = \begin{pmatrix} 1 & 2 \\ 0 & -2 \end{pmatrix}\). What elementary row operation was applied?
29. What single elementary row operation will transform the matrix \(C = \begin{pmatrix} 1 & 5 & 2 \\ 0 & 1 & 7 \\ 0 & 0 & 3 \end{pmatrix}\) into an upper triangular matrix with only 1s on the diagonal?
30. Given \(A = \begin{pmatrix} 1 & 0 \\ -1 & 3 \end{pmatrix}\), find the matrix obtained by applying \(R_2 \to R_2 + R_1\) followed by \(C_1 \to C_1 - C_2\).
