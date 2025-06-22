Monsuru Muadh Adekunle
FUO/22/0353


1. Define Basis, Dimension, Rank, and Nullity of a Matrix

* **Basis:**
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
	
![[Pasted image 20250621134652.png]]![[Pasted image 20250621134709.png]]