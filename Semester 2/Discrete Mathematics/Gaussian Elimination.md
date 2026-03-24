A sequence of row operations to transform a matrix into its [[Row Echelon Form|row echelon form]]

Three operations can be used to transform the matrix:

$R_j \rightarrow R_j + kR_i$ 
Add $k$ times row $i$ to row $j$ of the matrix

$R_i \rightarrow kR_i$ 
Multiply row $i$ by $k \neq 0$

$P_i \leftrightarrow P_j$
Swap rows $i$ and $j$

### Examples
#### 5.2
Solve the system of linear equations
$x + 2y − 3z = 4$
$x + 3y + z = 11$
$2x + 5y − 4z = 13$

##### Solution
*Translate into a matrix*

$$
A=\begin{bmatrix}
1 & 2 & -3 & |4 \\
1 & 3 & 1  & |11 \\
2 & 5 & -4 & |13
\end{bmatrix}
$$
*1: Move any all-zero rows to the bottom*
*2: Multiply row $A_1$ until first entry is 1*
*3: Add $a_1$ to lower rows until the first column under $a_1$ is all zeros - called a downsweep*
$A_2 \rightarrow A_2 - A_1$
$$
A=\begin{bmatrix}
1 & 2 & -3 & |4 \\
0 & 1 & 4  & |7 \\
2 & 5 & -4 & |13
\end{bmatrix}
$$

$A_4 \rightarrow A_2 - 2A_1$

$$
A=\begin{bmatrix}
1 & 2 & -3 & |4 \\
0 & 1 & 4  & |7 \\
0 & 1 & 2 & |5
\end{bmatrix}
$$
*Repeat 2/3 for second row, ignoring first row*
$A_3 \rightarrow A_3 - A_2$
$$
A=\begin{bmatrix}
1 & 2 & -3 & |4 \\
0 & 1 & 4  & |7 \\
0 & 0 & -2 & |-2
\end{bmatrix}
$$
 *Repeat 2/3 for third row, ignoring second row*
 $A_3 \rightarrow -1/2 A_3$

$$
A=\begin{bmatrix}
1 & 2 & -3 & |4 \\
0 & 1 & 4  & |7 \\
0 & 0 & 1 & |1
\end{bmatrix}
$$
*Solve equations*
$x + 2y - 3z = 4$
$y + 4z = 7$
$z = 1$

$y = 7 - 4 = 3$
$x = 4 - 2(3) + 3(1) = 1$

$(1, 3, 1)$