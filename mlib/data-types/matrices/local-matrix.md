Matrices may be local or distributed, dense or sparse. **A local matrix is stored on a single machine as a single dimensional array. A dense local matrix is stored in column major order \(column members are contiguous\) whereas a sparse local matrix values are stored in Compressed Sparse Column  \( CSC \) format in column major order.**

In this format, the matrix is stored in the form of three arrays. The first array contains row indices of non-zero values, the second array has the beginning value index for each column, and the third one is an array of all the non-zero values. Indices are of type integer starting from zero. The first array contains values from zero to the number of rows minus one. The third array has elements of type double. The second array requires some explanation. Every entry in this array corresponds to the index of the first non-zero element in each column. For example, assume that there is only one non-zero element in each column in a 3 by 3 matrix. Then the second array would contain 0,1,2 as its elements. The first array contains row positions and the third array contains three values. If none of the elements in a column are non-zero, you will note the same index repeating in the second array.

![](/assets/localMat.png)




