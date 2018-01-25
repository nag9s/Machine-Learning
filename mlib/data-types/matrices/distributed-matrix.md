Distributed matrices are the most sophisticated ones and choosing the right type of distributed matrix is very important. A distributed matrix is backed by one or more RDDs. The row and column indices are of the type `long` to support very large matrices. The basic type of distributed matrix is a `RowMatrix`, which is simply backed by an RDD of its rows.

Each row in turn is a local vector. This is suitable when the number of columns is very low. Remember, we need to pass RDDs to create distributed matrices, unlike the local ones. Let us look at an example:



![](/assets/distM.png)

