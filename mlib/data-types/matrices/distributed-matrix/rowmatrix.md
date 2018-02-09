**The basic type of distributed matrix is a **`RowMatrix`**, which is simply backed by an RDD of its rows.**

_Row-oriented distributed matrix without meaningful row indices _-RDD of sequence of vector without rows indices

Each row in turn is a local vector. This is suitable when the number of columns is very low. Remember, we need to pass RDDs to create distributed matrices, unlike the local ones. Let us look at an example:

![](/assets/distM.png)

#### Spark In Action

RowMatrixstores the rows of a matrix in an RDD ofVectorobjects. This RDD is accessible as the rows member field. The number of rows and columns can be obtained with numRows and numCols. RowMatrix can be multiplied by a local matrix \(producing another RowMatrix\) using the method multiply. RowMatrix also provides other useful methods, not available for other distributed implementations. We’ll describe those later.

Every other type of Spark distributed matrix can be converted to a RowMatrix using the built-in toRowMatrix methods, but there are no methods for converting a RowMatrix to other distributed implementations.



