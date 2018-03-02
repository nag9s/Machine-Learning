Out-of-Bag is equivalent to validation or test data. In random forests, there is no need for a separate test set to validate result. It is estimated internally, during the run, as follows:

  


As the forest is built on training data , each tree is tested on the 1/3rd of the samples \(36.8%\) not used in building that tree

**\(similar to validation data set\)**

. This is the out of bag error estimate - an internal error estimate of a random forest as it is being constructed.



In bagging, an individual tree is built on a random sample of the dataset, roughly two-thirds of the total observations \(note that the remaining one-third is referred to as **out-of-bag** \(**oob**\)\). This is repeated dozens or hundreds of times and the results are averaged. Each of these trees is grown and not pruned based on any error measure, and this means that the variance of each of these individual trees is high. However, by averaging the results, you can reduce the variance without increasing the bias.

