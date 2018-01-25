Distributed matrices are the most sophisticated ones and choosing the right type of distributed matrix is very important. A distributed matrix is backed by one or more RDDs. The row and column indices are of the type `long` to support very large matrices.

![](/assets/distM.png)



 A distributed matrix is stored in one or more RDDs and hence is distributed in nature. Also the row and column indices of distributed matrix are of type long while the values are of double type. Conversion of a distributed matrix to any other type may require shuffling and hence is an expensive operation.

