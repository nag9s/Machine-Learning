this question brings the usage of linear algebra

[https://www.quora.com/Why-are-matrices-vectors-used-in-machine-learning-data-analysis](https://www.quora.com/Why-are-matrices-vectors-used-in-machine-learning-data-analysis)

Another reason ... or maybe a practical example of the issue ... consider the neurons in a neural net and their corresponding weights. Many operations needed to train the network can be expressed through algebraic operations on the matrix of input feature values and the matrix of weights.

If one chooses an object oriented approach - just for example - instead of a matrix approach, in which the weights are instance variables inside an object, or instance variables inside a hierarchy of objects, then you may complicate the training of the network.

Highly optimized linear algebra libraries like BLAS and CUBLAS make the operations of Vector x Matrix or Matrix x Matrix operations extremely efficient versus piecewise operations on each element.

When I took Ng's ML class, I often first did the algorithms using standard nested for loops, then moved the solution to full matrix solutions. The performance differences on even these unoptimized solutions was dramatic. I recommend you try the equivalent in MatLab or Octave to see for yourself.

Add in the ability to move computations to GPUs via CUBLAS or the like and you have huge performance gains.

**EDIT:**

Here's a toy example which supposes inputting 5000 small images into the first layer of a neural net. The FOR loop implementation is very naive and does not implement any optimizations.

Computer are very adept at solving linear algebra problems efficiently, and writing algorithms in this framework \(turning the calculus into linear algebra\) allows for the exploitation of existing computational methods.

Because matrices/vectors  are convenient for computer processing.

matrix operation is much faster than circulation.

Phil Glau has given a very good example!



https://www.quora.com/How-is-linear-algebra-connected-with-machine-learning-and-big-data-analysis

A lot of ML algorithms rely heavily on linear algebra.

Linear regression, for example, is a linear algebra problem and can be solved purely by linear algebra.

Feed-forward neural networks: each layer has the form, whereis a matrix of weights. This not only allows for fast vectorized computation, but also makes backpropagation much easier.

Principal Component Analysis \(PCA\), probably the most popular dimensionality reduction technique, is pure linear algebra.

Collaborative filtering is a form of low-rank matrix factorization, a problem that comes up frequently in ML.

In fact, most ML models utilize a linear combination of features in some way. An understanding of linear algebra makes that much easier to deal with.

