From Spark In Action

Linear algebra is a branch of mathematics focusing on vector spaces and linear operations and mappings between them expressed mainly by matrices.

Linear algebra is essential for understanding the math behind most machine-learning algorithms, so if you don’t know much about vectors and matrices.

**Matrices and vectors \(MLLib DataTypes\) in Spark can be manipulated locally \(in the driver or executor processes\) or in a distributed manner. Implementations of distributed matrices in Spark enable you to perform linear algebra operations on huge amounts of data, spanning numerous machines. **For local linear algebra operations, Spark uses the very fast Breeze and jblas libraries \(and NumPy in Python\), and it has its own implementations of distributed ones.

