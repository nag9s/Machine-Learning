A `CoordinatedMatrix` stores data as tuples of row, column indexes, and element value. A `BlockMatrix` represents a distributed matrix in blocks of local matrices. Methods to convert matrices from one type to another are provided but these are expensive operations and should be used with caution.

elements values are explicit defined by using  IndexedRow\(row\_index, col\_index, value\).



CoordinateMatrix stores its values as an RDD of MatrixEntry objects, which contain individual entries and their \(i,j\) positions in the matrix. This isn’t an efficient way of storing data, so you should use CoordinateMatrix only for storing sparse matrices. Otherwise, it could consume too much memory. 

