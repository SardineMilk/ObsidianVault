1.
$2x + 8y + 6z = 20$
$4x + 2y - 2z = -2$
$3x - y + z = 11$

$$
A=\begin{bmatrix}
2 & 8 & 6 & |20 \\
4 & 2 & -2  & |-2 \\
3 & -1 & 1 & |11
\end{bmatrix}
$$
*first row start with 1*
$A_1 \rightarrow A_1 * 1/2$
$$
A=\begin{bmatrix}
1 & 4 & 3 & |10 \\
4 & 2 & -2  & |-2 \\
3 & -1 & 1 & |11
\end{bmatrix}
$$
*downsweep*
$A_2 \rightarrow A_2 - 4A_1$
$$
A=\begin{bmatrix}
1 & 4 & 3 & |10 \\
0 & -14 & -14  & |-42 \\
3 & -1 & 1 & |11
\end{bmatrix}
$$
$A_3 \rightarrow A_3 - 3A_1$
$$
A=\begin{bmatrix}
1 & 4 & 3 & |10 \\
0 & -14 & -14  & |-42 \\
0 & -13 & -8 & |-19
\end{bmatrix}
$$
*second row start with 1*
$A_2 \rightarrow -1/14 A_2$
$$
A=\begin{bmatrix}
1 & 4 & 3 & |10 \\
0 & 1 & 1  & |3 \\
0 & -13 & -8 & |-19
\end{bmatrix}
$$
*downsweep*
$A_3 \rightarrow A_3 + 13 A_2$
$$
A=\begin{bmatrix}
1 & 4 & 3 & |10 \\
0 & 1 & 1  & |3 \\
0 & 0 & 5 & |20
\end{bmatrix}
$$
*third row start with 1*
$$
A=\begin{bmatrix}
1 & 4 & 3 & |10 \\
0 & 1 & 1  & |3 \\
0 & 0 & 1 & |4
\end{bmatrix}
$$

*Solve for variables*
$z = 4$

$y + z = 3$
$y = -1$

$x + 4y + 3z = 10$
$x = 10 - 4(-1) - 3(4)$
$x = 10 + 4 - 12$
$x = 2$

$x = 2, y = -1, z = 4$


