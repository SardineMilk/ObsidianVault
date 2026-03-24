Transform a [[Vector Spaces|vector space]]
Do any vectors remain on the same span
These are **eigenvectors**
The value they are linearly scaled by is their **eigenvalue**

**Eigenvectors**
Vectors, which when multiplied by the matrix, are linearly scaled

**Eigenvalue**
The value by which the corresponding eigenvector is scaled
### $Av = \lambda v$
$A$: transformation matrix
$v$: eigenvector
$\lambda$: corresponding eigenvalue

To find the eigenvalues of $A$, solve for $\lambda$


$$Av = \lambda v$$
$$Av = \begin{bmatrix}
\lambda & 0 \\
0 & \lambda
\end{bmatrix} v$$



**Example**
Find the eigenvalues of 
$$
A =\begin{bmatrix}
1 & 2 \\
1 & 0
\end{bmatrix}
$$
The values of $\lambda$ that satisfy 
$$Av = \lambda v$$
Left is matrix-vector, right is scalar-vector. lets rearrange
$$\begin{bmatrix}
1 & 2 \\
1 & 0
\end{bmatrix}v = \begin{bmatrix}
\lambda & 0 \\
0 & \lambda
\end{bmatrix} v$$
$$\begin{bmatrix}
1 & 2 \\
1 & 0
\end{bmatrix}v = \lambda \begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix} v$$
$$\begin{bmatrix}
1 & 2 \\
1 & 0
\end{bmatrix}v = \lambda \begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}v$$
$$Av = \lambda Iv$$
$$(A - \lambda I)v = 0$$

$$
(A - \lambda I)v  =\begin{bmatrix}
1-\lambda & 2 \\
1 & 0-\lambda
\end{bmatrix}v
$$
[[Determinant]]

[[Gaussian Elimination|Downsweep]] the first column
$$
A - \lambda I  =\begin{bmatrix}
1-\lambda & 2 \\
0 & -\lambda - \frac{2}{1-\lambda}
\end{bmatrix}
$$
Solve for bottom-right equal to zero
$-\lambda - \frac{2}{1-\lambda} = \lambda^2 - \lambda - 2 = (\lambda - 2)(\lambda + 1) = 0$
$\lambda =  2, -1$
