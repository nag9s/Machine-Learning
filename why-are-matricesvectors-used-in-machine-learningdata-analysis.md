this question brings the usage of linear algebra



https://www.quora.com/Why-are-matrices-vectors-used-in-machine-learning-data-analysis

Another reason ... or maybe a practical example of the issue ... consider the neurons in a neural net and their corresponding weights. Many operations needed to train the network can be expressed through algebraic operations on the matrix of input feature values and the matrix of weights.

  


  


If one chooses an object oriented approach - just for example - instead of a matrix approach, in which the weights are instance variables inside an object, or instance variables inside a hierarchy of objects, then you may complicate the training of the network.

