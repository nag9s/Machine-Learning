![](/assets/rf1.png)

A random forest is a subset of another machine learning model called the **decision tree**. A decision tree, as the diagram at the start of this section shows, is a group of learning algorithms that are part of the statistical set. A decision tree simply takes several variables into consideration and produces a single output that classifies the set. Each element evaluated is called the **set**. The decision tree produces a set of probabilities that a path has taken based on the input. One form of a decision tree is the **Classification and Regression Test** \(**CART**\), developed by Breiman in 1983. 

We now introduce the notion of bootstrap aggregating or _bagging_. When you have a single decision tree being trained, it is susceptible to noise injected into it and can form a bias. If, on the other hand, you have many decision trees being trained, we can lessen the chance of bias. Each tree will pick a random set of the training data or samples.

The output of the random forest training processes a decision tree based on a random selection of the training data, and a random selection of variables:  

