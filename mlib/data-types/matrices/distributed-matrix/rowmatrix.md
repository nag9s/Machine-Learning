**The basic type of distributed matrix is a **`RowMatrix`**, which is simply backed by an RDD of its rows.**

_Row-oriented distributed matrix without meaningful row indices _-RDD of sequence of vector without rows indices

Each row in turn is a local vector. This is suitable when the number of columns is very low. Remember, we need to pass RDDs to create distributed matrices, unlike the local ones. Let us look at an example:

![](/assets/distM.png)

