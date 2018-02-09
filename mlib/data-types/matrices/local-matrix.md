> Matrices may be local or distributed, dense or sparse. **A local matrix is stored on a single machine as a single dimensional array. A dense local matrix is stored in column major order \(column members are contiguous\) whereas a sparse local matrix values are stored in Compressed Sparse Column  \( CSC \) format in column major order.**

In this format, the matrix is stored in the form of three arrays. The first array contains row indices of non-zero values\(colPtrs\), the second array has the beginning value index for each column\(rowIndices\), and the third one is an array of all the non-zero values. Indices are of type integer starting from zero. The first array contains values from zero to the number of rows minus one. The third array has elements of type double. The second array requires some explanation. Every entry in this array corresponds to the index of the first non-zero element in each column. For example, assume that there is only one non-zero element in each column in a 3 by 3 matrix. Then the second array would contain 0,1,2 as its elements. The first array contains row positions and the third array contains three values. If none of the elements in a column are non-zero, you will note the same index repeating in the second array.

![](/assets/localMat.png)

[https://medium.com/@rickynguyen/getting-started-with-spark-day-5-36b62a6d13bf](https://medium.com/@rickynguyen/getting-started-with-spark-day-5-36b62a6d13bf)

> A local matrix has integer-typed row and column indices and double-typed values, stored on a single machine

![](/assets/mat.png)

[http://blog.csdn.net/sinat\_29508201/article/details/54089771](http://blog.csdn.net/sinat_29508201/article/details/54089771)

![](/assets/mat5.png)

![](/assets/mat2.png)

![](/assets/matrix1.png)

CSC format is made of three arrays, containing column pointers, row indices, and the nonzero elements.

A row indices array contains the row index of each element in the elements array. The column pointers array contains ranges of indices of elements that belong to the same column.

