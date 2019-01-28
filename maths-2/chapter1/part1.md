# MATRICES

### Transpose

1. (A + B)<sup>T</sup> = A<sup>T</sup> + B<sup>T</sup>
2. (A<sup>T</sup>)<sup>T</sup> = A
3. (AB)<sup>T</sup> = B<sup>T</sup>A<sup>T</sup>

### properties of inverse

1. If A is invertible, then inverse is unique 
2. (AB)<sup>-1</sup> = B<sup>-1</sup>A<sup>-1</sup>
3. (A<sup>T</sup>)<sup>-1</sup> = (A<sup>-1</sup>)<sup>T</sup>

#### symmetric matrix

\[a<sub>ij</sub>\] = \[a<sub>ji</sub>\] (A<sup>T</sup> = A)

- This condition forces A to be a square matrix

#### skew-symmetric matrix

A<sup>T</sup> = -A

\[a<sub>ij</sub>\] = -\[a<sub>ji</sub>\]

- This forces A to be a square matrix and diagonal elements zero

#### Nilpotent matrix

A<sup>k</sup> = O ; A<sup>m</sup> != O (m<k), k :point_right: order of nilpotency

- the fact that A can be multiplied with A itself tells that A is square matrix

> Note: If A is nilpotent, it is not invertible (assuming it exists)

A<sup>k</sup> = O ; A<sup>-1</sup>A<sup>k</sup> = O => A<sup>k-1</sup> = O
which is against the rule of nilpotent matrix.

#### Submatrix of matrix

Matrix obtained by deleting some of the rows and/or columns of a matrix is called submatrix of the given matrix.

#### Block Matrix

A<sub>mxn</sub> = \[B<sub>m\*r</sub>  C<sub>m\*(n-r)</sub>\]

A<sub>m\*n</sub> =  \[B<sub>r\*n</sub>\]
     
                    \[C<sub>(n-r)\*n</sub>\]



