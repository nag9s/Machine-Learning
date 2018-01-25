A `CoordinatedMatrix` stores data as tuples of row, column indexes, and element value. A `BlockMatrix` represents a distributed matrix in blocks of local matrices. Methods to convert matrices from one type to another are provided but these are expensive operations and should be used with caution.

elements values are explicit defined by using  IndexedRow\(row\_index, col\_index, value\).

