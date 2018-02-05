Apache Spark 2.x Machine Learning Cookbook

**Sparse and dense vectors and matrices**

Spark supports sparse and dense vectors and matrices. A vector or matrix is sparse if it contains mostly zeros. It’s more efficient to represent such data with pairs of indices and values at those indices. A sparse vector or matrix can be likened to a map \(or dictionary in Python\).

Conversely, a dense vector or matrix contains all the data—values at all index positions not storing the indices, similar to an array or a list.

![](/assets/MLlib.png)



**From Spark In Action**

 Matrices and vectors in Spark can be manipulated locally \(in the driver or executor processes\) or in a distributed manner. Implementations of distributed matrices in Spark enable you to perform linear algebra operations on huge amounts of data, spanning numerous machines. For local linear algebra operations, Spark uses the very fast Breeze and jblas libraries \(and NumPy in Python\), and it has its own implementations of distributed ones.

