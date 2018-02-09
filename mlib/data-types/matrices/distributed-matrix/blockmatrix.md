included set of  matrix block \(row\_index, col\_index, matrix\).

A `BlockMatrix` represents a distributed matrix in blocks of local matrices. Methods to convert matrices from one type to another are provided but these are expensive operations and should be used with caution.

It stores its values as RDDs of tuples \(\(i,j\), Matrix\). In other words, BlockMatrix contains local matrices \(blocks\) referenced by their position in the matrix. Sub-matrices take up blocks of the same sizes \(of rows-per-block and columns-per-block dimensions\), except for the last sub-matrices, which can be smaller \(to allow the total matrix to be of any dimensions\).

BlockMatrix

is the only distributed implementation with methods for adding and multiplying other distributed matrices.

