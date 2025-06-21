Monsuru Muadh Adekunle
FUO/22/0353


1. Define Basis, Dimension, Rank, and Nullity of a Matrix
 2. **Basis:**
  A set of linearly independent vectors that span a vector space.
  * A set $S = \{v_1, v_2, ..., v_k\}$ is a basis if:

    1. Vectors are linearly independent.
    2. They span the space.

  * **Example:**
    $A = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \Rightarrow \text{Basis of } \mathbb{R}^2 = \left\{ \begin{pmatrix} 1 \\ 0 \end{pmatrix}, \begin{pmatrix} 0 \\ 1 \end{pmatrix} \right\}$

* **Dimension:**
  Number of vectors in any basis.
  $\dim(V) = \text{number of vectors in basis}$
  For $\mathbb{R}^2$, $\dim(\mathbb{R}^2) = 2$

* **Rank:**
  Dimension of the column space (or row space) of a matrix.
  $\text{rank}(A) = \text{number of pivot columns}$

  * **Example:**
    $A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \end{pmatrix} \Rightarrow \text{rank}(A) = 1$

* **Nullity:**
  Dimension of the null space of the matrix.
  $\text{nullity}(A) = \text{number of free variables in } Ax = 0$

  * **Example:**
    Solve

    $$
    \begin{pmatrix}
    1 & 2 & 3 \\
    2 & 4 & 6
    \end{pmatrix}
    x = 0
    \Rightarrow \text{nullity} = 2
    $$

    Null space basis:

    $$
    \left\{
    \begin{pmatrix} -2 \\ 1 \\ 0 \end{pmatrix},
    \begin{pmatrix} -3 \\ 0 \\ 1 \end{pmatrix}
    \right\}
    $$

* **Rank-Nullity Theorem:**

  $$
  \text{rank}(A) + \text{nullity}(A) = n
  $$

---

### 2. Characteristic Polynomial, Eigenvalues, and Eigenvectors

Given:

$$
A = \begin{pmatrix} -1 & 2 & 2 \\ 2 & 2 & -1 \\ 2 & -1 & 2 \end{pmatrix}
$$

* **Characteristic Polynomial:**

  $$
  P(\lambda) = \det(A - \lambda I)
  = -(\lambda - 3)^2(\lambda + 3)
  $$

* **Eigenvalues:**
  From the polynomial roots:

  $$
  \lambda_1 = 3 \quad (\text{multiplicity 2}), \quad \lambda_2 = -3 \quad (\text{multiplicity 1})
  $$

* **Eigenvectors:**

  * For $\lambda = 3$:
    Solve:

    $$
    (A - 3I)v = 0
    \Rightarrow v = s \begin{pmatrix} \frac{1}{2} \\ 1 \\ 0 \end{pmatrix} + t \begin{pmatrix} \frac{1}{2} \\ 0 \\ 1 \end{pmatrix}
    $$

    Choose \$s=2, t=0\$ and \$s=0, t=2\$:

    $$
    v^{(1)} = \begin{pmatrix} 1 \\ 2 \\ 0 \end{pmatrix}, \quad
    v^{(2)} = \begin{pmatrix} 1 \\ 0 \\ 2 \end{pmatrix}
    $$

  * For $\lambda = -3$:
    Solve:

    $$
    (A + 3I)v = 0 \Rightarrow
    v = k \begin{pmatrix} -2 \\ 1 \\ 1 \end{pmatrix}
    $$

    Choose \$k = 1\$:

    $$
    v^{(3)} = \begin{pmatrix} -2 \\ 1 \\ 1 \end{pmatrix}
    $$

---

### ✅ Final Summary

* **Characteristic Polynomial:**
  $P(\lambda) = -(\lambda - 3)^2(\lambda + 3)$

* **Eigenvalues:**
  $\lambda = 3 \text{ (multiplicity 2)}, \quad \lambda = -3 \text{ (multiplicity 1)}$

* **Eigenvectors:**

  * For $\lambda = 3$:

    $$
    \begin{pmatrix} 1 \\ 2 \\ 0 \end{pmatrix}, \quad
    \begin{pmatrix} 1 \\ 0 \\ 2 \end{pmatrix}
    $$
  * For $\lambda = -3$:

    $$
    \begin{pmatrix} -2 \\ 1 \\ 1 \end{pmatrix}
    $$

Let me know if you'd like this turned into a printable PDF or formatted for slides.
