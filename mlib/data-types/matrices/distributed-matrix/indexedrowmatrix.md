An `IndexedRowMatrix` stores a row index prefixed to the row entry. This is useful in executing joins. You need to pass `IndexedRow` objects to create an `IndexedRowMatrix`. An `IndexedRow` object is a wrapper with a long `Index` and a `Vector` of row elements.

like a row matrix, but with meaningful row indices.

Spark In Action

IndexedRowMatrix is an RDD of IndexedRow objects, each containing an index of the row and a Vector with row data. Although there is no built-in method for converting a RowMatrix to an IndexedRowMatrix, it’s fairly easy to do:

![](/assets/indexedRowMatrix.png)



![](/assets/indexedRow.png)

