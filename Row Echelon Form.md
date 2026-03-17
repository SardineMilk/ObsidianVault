For a matrix to be in *row echelon form (REF)*:
- If a row is not entirely zeros, the leftmost non-zero number is 1
- If a row is entirely zeros, it is at the bottom of the matrix
- The first 1 in each row is to the right of the first one in the row above

To convert a matrix to REF, use [[Gaussian Elimination]]
### Examples
#### Row Echelon Form
$$
\begin{bmatrix}
1 & 4 & 2 \\
0 & 1 & -1 \\
0 & 0 & 1
\end{bmatrix}
$$
$$
\begin{bmatrix}
1 & -1 & 0 \\
0 & 1 & 3 \\
0 & 0 & 0
\end{bmatrix}
$$
$$
\begin{bmatrix}
1 & 2 & -1 & 3 \\
0 & 1 & 4 & -2 \\
0 & 0 & 1 & 5
\end{bmatrix}
$$

#### **NOT** Row Echelon Form
##### Leftmost non-zero number is not 1
$$
\begin{bmatrix}
1 & 4 & 2 \\
0 & 3 & -1 \\
0 & 0 & 7
\end{bmatrix}
$$
$$
\begin{bmatrix}
2 & -1 & 0 \\
0 & 5 & 3 \\
0 & 0 & 0
\end{bmatrix}
$$
##### 1's in lower rows not to the right of 1's above them
$$
\begin{bmatrix}
0 & 1 & 2 \\
1 & 0 & 3 \\
0 & 0 & 0
\end{bmatrix}
$$

##### Zero row is not at bottom
$$
\begin{bmatrix}
1 & 2 & 3 \\
0 & 0 & 0 \\
0 & 1 & 5
\end{bmatrix}
$$
