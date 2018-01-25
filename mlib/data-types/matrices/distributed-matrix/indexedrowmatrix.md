An `IndexedRowMatrix` stores a row index prefixed to the row entry. This is useful in executing joins. You need to pass `IndexedRow` objects to create an `IndexedRowMatrix`. An `IndexedRow` object is a wrapper with a long `Index` and a `Vector` of row elements.

like a row matrix, but with meaningful row indices.

