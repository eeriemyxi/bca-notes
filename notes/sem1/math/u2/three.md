# Matrix Identities and Inverses

In matrix algebra, identity and inverse elements are crucial concepts, similar to their roles in regular arithmetic. They provide a baseline for operations and a way to "undo" them.

---

## Additive Identity and Inverse

These concepts are related to matrix addition and subtraction.

### Additive Identity (Zero Matrix)
The **additive identity** for matrices is the **zero matrix** (or null matrix), denoted by \(O\). This is a matrix of any order where all the elements are zero.

Its key property is that when it's added to any matrix \(A\) of the same order, it leaves \(A\) unchanged.

-   **Property**: For any \(m \times n\) matrix \(A\), there exists an \(m \times n\) zero matrix \(O\) such that:

    \[
    A + O = O + A = A
    \]

-   **Example**:

    Let \(A = \begin{bmatrix} 2 & -1 \\ 5 & 0 \end{bmatrix}\) and \(O = \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix}\).

    \[
    A + O = \begin{bmatrix} 2+0 & -1+0 \\ 5+0 & 0+0 \end{bmatrix} = \begin{bmatrix} 2 & -1 \\ 5 & 0 \end{bmatrix} = A
    \]

### Additive Inverse
For any matrix \(A\), its **additive inverse** is the matrix \(-A\), which is obtained by negating every element of \(A\).

When a matrix is added to its additive inverse, the result is the zero matrix \(O\).

-   **Property**: For any matrix \(A\), there exists an additive inverse \(-A\) such that:

    \[
    A + (-A) = (-A) + A = O
    \]

-   **Example**:

    Let \(A = \begin{bmatrix} 3 & -7 \\ -1 & 4 \end{bmatrix}\). Its additive inverse is \(-A = \begin{bmatrix} -3 & 7 \\ 1 & -4 \end{bmatrix}\).

    \[
    A + (-A) = \begin{bmatrix} 3+(-3) & -7+7 \\ -1+1 & 4+(-4) \end{bmatrix} = \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix} = O
    \]

---

## Multiplicative Identity and Inverse

These concepts are related to matrix multiplication and are defined only for **square matrices**.

### Multiplicative Identity (Identity Matrix)
The **multiplicative identity** for square matrices of order \(n\) is the **identity matrix** \(I_n\) (or simply \(I\)). This is a square matrix with 1s on the main diagonal and 0s everywhere else.

When any square matrix \(A\) is multiplied by the identity matrix \(I\) of the same order, it leaves \(A\) unchanged.

-   **Property**: For any square matrix \(A\) of order \(n\),

    \[
    A \cdot I = I \cdot A = A
    \]

-   **Example**:
    Let \(A = \begin{bmatrix} 3 & 5 \\ 1 & 2 \end{bmatrix}\) and \(I = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}\).

    \[
    A \cdot I = \begin{bmatrix} 3 & 5 \\ 1 & 2 \end{bmatrix} \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} = \begin{bmatrix} (3\cdot1+5\cdot0) & (3\cdot0+5\cdot1) \\ (1\cdot1+2\cdot0) & (1\cdot0+2\cdot1) \end{bmatrix} = \begin{bmatrix} 3 & 5 \\ 1 & 2 \end{bmatrix} = A
    \]

### Multiplicative Inverse
The **multiplicative inverse** of a square matrix \(A\), denoted by \(A^{-1}\), is a matrix such that when multiplied by \(A\), the result is the identity matrix \(I\).

-   **Property**: For a square matrix \(A\), its inverse \(A^{-1}\) satisfies:

    \[
    A \cdot A^{-1} = A^{-1} \cdot A = I
    \]

!!! warning "Existence of an Inverse"
    Not every square matrix has a multiplicative inverse. An inverse exists **if and only if** the matrix is **non-singular**, which means its determinant is non-zero (\(\det(A) \neq 0\)).
    
    -   If \(\det(A) \neq 0\), the matrix is **invertible** or **non-singular**.
    -   If \(\det(A) = 0\), the matrix is **non-invertible** or **singular**.

-   **Example**:
    Let \(A = \begin{bmatrix} 2 & 5 \\ 1 & 3 \end{bmatrix}\). Its determinant is \(\det(A) = (2)(3) - (5)(1) = 6 - 5 = 1 \neq 0\), so it has an inverse.
    The inverse is \(A^{-1} = \begin{bmatrix} 3 & -5 \\ -1 & 2 \end{bmatrix}\).

    Let's verify:

    \[
    A \cdot A^{-1} = \begin{bmatrix} 2 & 5 \\ 1 & 3 \end{bmatrix} \begin{bmatrix} 3 & -5 \\ -1 & 2 \end{bmatrix} = \begin{bmatrix} (6-5) & (-10+10) \\ (3-3) & (-5+6) \end{bmatrix} = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} = I
    \]

## Problem Set

#### Section 1: Additive Identity and Inverse

1.  Find the additive inverse of the matrix \( A = \begin{pmatrix} 2 & -5 \\ 1 & 0 \end{pmatrix} \).
2.  What is the additive inverse of \( B = \begin{pmatrix} 1 & -3 & 2 \\ 4 & 0 & -5 \end{pmatrix} \)?
3.  Let \( C = \begin{pmatrix} \sqrt{3} & 1 & -1 \\ 2 & 3 & 0 \end{pmatrix} \). Find a matrix \(X\) such that \(C + X\) is a zero matrix.
4.  What is the additive identity for the set of all matrices of order \(3 \times 4\)?
5.  If \( A + B = O \), where \(A\) and \(B\) are \(2 \times 2\) matrices and \(O\) is the zero matrix, what is the relationship between \(A\) and \(B\)?
6.  Given \( A = \begin{pmatrix} 8 & 3 \\ -1 & 5 \end{pmatrix} \). Verify that \( A + (-A) = O \).
7.  Find the matrix \(P\) if \( -P \) is the matrix \( \begin{pmatrix} -9 & 2 \\ 6 & -1 \end{pmatrix} \).
8.  If \(A\) is a matrix of order \(m \times n\), what is the order of its additive inverse?
9.  Simplify the expression: \( (A + B) + (-A) \) assuming matrices are of the same order.
10. Does every matrix have a unique additive inverse? Explain in one sentence.

---

#### Section 2: Multiplicative Identity and Inverse

11. What is the multiplicative identity for the set of all square matrices of order 3? Write the matrix.
12. Given the matrix \( A = \begin{pmatrix} 3 & 1 \\ -1 & 2 \end{pmatrix} \). Show that \( AI = IA = A \), where \(I\) is the identity matrix of order 2.
13. If \( B = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 3 & 4 \\ 3 & 4 & 5 \end{pmatrix} \), verify that \(BI = B\).
14. A matrix \(A\) has a multiplicative inverse. What can you say about the determinant of \(A\)?
15. If \(A\) is an invertible matrix, prove that \( (A^T)^{-1} = (A^{-1})^T \).
16. Find the inverse of the matrix \( A = \begin{pmatrix} 2 & -3 \\ -1 & 2 \end{pmatrix} \).
17. Find the inverse of \( B = \begin{pmatrix} 4 & 5 \\ 2 & 3 \end{pmatrix} \).
18. For what value of \(x\) is the matrix \( C = \begin{pmatrix} 6 & x \\ 4 & 2 \end{pmatrix} \) singular (i.e., does not have an inverse)?
19. Find the inverse of the matrix \( D = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 2 & 4 \\ 0 & 0 & 5 \end{pmatrix} \).
20. Find the inverse of \( E = \begin{pmatrix} 2 & 1 & 3 \\ 4 & -1 & 0 \\ -7 & 2 & 1 \end{pmatrix} \).
21. Given \( A = \begin{pmatrix} 3 & 7 \\ 2 & 5 \end{pmatrix} \). Find \(A^{-1}\) and verify that \( AA^{-1} = I \).
22. Given \( A = \begin{pmatrix} 2 & 3 \\ 1 & 2 \end{pmatrix} \) and \( B = \begin{pmatrix} 1 & -2 \\ -1 & 3 \end{pmatrix} \). Compute \((AB)^{-1}\).
23. Using the matrices from the previous question, compute \(B^{-1}A^{-1}\) and show that \( (AB)^{-1} = B^{-1}A^{-1} \).
24. If \( A = \begin{pmatrix} 3 & 1 \\ -1 & 2 \end{pmatrix} \), show that \( A^2 - 5A + 7I = O \). Hence, find \( A^{-1} \).
25. True or False: The inverse of a diagonal matrix (with non-zero diagonal elements) is a diagonal matrix.
26. Find the inverse of the matrix \( F = \begin{pmatrix} \cos\theta & \sin\theta \\ -\sin\theta & \cos\theta \end{pmatrix} \).
27. If \(A\) is an invertible matrix of order 3 and \(|A| = 4\), find \(|\text{adj}(A)|\).
28. Solve the matrix equation for \(X\): \( \begin{pmatrix} 5 & 4 \\ 1 & 1 \end{pmatrix} X = \begin{pmatrix} 1 & -2 \\ 3 & -1 \end{pmatrix} \).
29. If \(A\) is a non-singular square matrix, prove that \( |\text{adj}(A)| = |A|^{n-1} \), where \(n\) is the order of the matrix.
30. If \(A\), \(B\), and \(C\) are invertible matrices of the same order, what is \( (ABC)^{-1} \)?
