**Sparse and dense vectors and matrices**

Spark supports sparse and dense vectors and matrices. A vector or matrix is sparse if it contains mostly zeros. It’s more efficient to represent such data with pairs of indices and values at those indices. A sparse vector or matrix can be likened to a map \(or dictionary in Python\).

Conversely, a dense vector or matrix contains all the data—values at all index positions not storing the indices, similar to an array or a list.



![](/assets/MLlib.png)

