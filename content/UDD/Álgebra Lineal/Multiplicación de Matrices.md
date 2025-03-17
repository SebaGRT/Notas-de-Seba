	Para multiplicar una matriz con otra matriz es necesario realizar el 
	producto punto entre las filas y las columnas de la matriz.

	Diremos que el producto punto es cuando multiplicamos cifras relacionadas
	y posteriormente las sumamos.

<img src="https://www.mathsisfun.com/algebra/images/matrix-multiply-a.svg">

$$
(1, 2, 3) \cdot (7, 9, 11)\ =\ 1\cdot7\ + 2\cdot9\ + 3\cdot11\ =\ 58
$$

	Al realizar la multiplicación entre dos matrices, es necesario que el 
	número de columnas de la 1ra matriz sea igual al número de filas de la 2da 
	matriz. La matriz resultante tendrá el mismo número de filas que la 1ra 
	matriz, y el mismo número de columnas que la 2da matriz.

$$
\begin{pmatrix}a & b & c\\d & e & f\end{pmatrix}_{2x3}\ \cdot \begin{pmatrix}g&h\\i&j\\k&l\end{pmatrix}_{3x2}\ =\ \begin{pmatrix}a\cdot g+b\cdot i+c\cdot k & a\cdot h+b\cdot j+c\cdot k\\d\cdot g+e\cdot i+f\cdot k & f\cdot h+e\cdot j+f\cdot l \end{pmatrix}_{2x2}$$

