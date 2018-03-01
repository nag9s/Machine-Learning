![](/assets/rf1.png)

https://www.safaribooksonline.com/library/view/internet-of-things/9781788470599/e3418e8b-ac43-424b-887a-7882f154af7f.xhtml

A random forest is a subset of another machine learning model called the **decision tree**. A decision tree, as the diagram at the start of this section shows, is a group of learning algorithms that are part of the statistical set. A decision tree simply takes several variables into consideration and produces a single output that classifies the set. Each element evaluated is called the **set**. The decision tree produces a set of probabilities that a path has taken based on the input. One form of a decision tree is the **Classification and Regression Test** \(**CART**\), developed by Breiman in 1983.

We now introduce the notion of bootstrap aggregating or _bagging_. When you have a single decision tree being trained, it is susceptible to noise injected into it and can form a bias. If, on the other hand, you have many decision trees being trained, we can lessen the chance of bias. Each tree will pick a random set of the training data or samples.

The output of the random forest training processes a decision tree based on a random selection of the training data, and a random selection of variables:

![](/assets/rf2.png)

Random forest model. Here, two forests are constructed to pick a random, but not the whole set of variables.

Random forests extend bagging by not only selecting a random sample set, but also a subset of the number of features being qualified. This can be seen in the preceding image. This is counter-intuitive, since you want to train on as much data as possible. The rationale is that:

* Most trees are accurate, and provide correct predictions for most data
* Errors in the decision tree may happen at different places, in different trees

This is the rule of _group think_ and _majority decisions_. If the outcome of several trees agree with each other even though they arrived at that decision through different paths and a single tree is an outlier, one will naturally side with the majority. This creates a model with low variance, compared to a single decision tree model that can be extremely biased. We can see the following example with four trees in a random forest. Each has been trained on a different subset of data, and have chosen random variables. The result of the flow is that three of the trees produce a result of **9**, while the fourth tree produces a different result.

Regardless of what the fourth tree produced, the majority agreed by a different data set, different variable, and different tree structures that the result of the logic should be a **9**:

![](/assets/rf3.png)

Majority decision of a random forest. Here, several trees based on a random collection of variables, arrive at 9 as a decision. By arriving at a similar answer based on different input generally reinforces the model.

