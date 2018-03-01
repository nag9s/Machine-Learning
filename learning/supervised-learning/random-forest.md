![](/assets/rf1.png)

[https://www.safaribooksonline.com/library/view/internet-of-things/9781788470599/e3418e8b-ac43-424b-887a-7882f154af7f.xhtml](https://www.safaribooksonline.com/library/view/internet-of-things/9781788470599/e3418e8b-ac43-424b-887a-7882f154af7f.xhtml)

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

[https://www.safaribooksonline.com/library/view/practical-big-data/9781783554393/cb68c914-4bc1-4dbd-82fe-842c0db5b4fd.xhtml](https://www.safaribooksonline.com/library/view/practical-big-data/9781783554393/cb68c914-4bc1-4dbd-82fe-842c0db5b4fd.xhtml)



Random forest is an extension of the decision tree model that we just discussed. In practice, Decision Trees are simple to understand, simple to interpret, fast to create using available algorithms, and overall, intuitive. However, Decision Trees are sensitive to small changes in the data, permit splits only along an axis \(linear splits\) and can lead to overfitting. To mitigate some of the drawbacks of decision trees, whilst still getting the benefit of their elegance, algorithms such as Random Forest create multiple decision trees and sample random features to leverage and build an aggregate model.

Random forest works on the principle of bootstrap aggregating or bagging. Bootstrap is a statistical term indicating random sampling with replacement. **Bootstrapping a given set of records means taking a random number of records and possibly including the same record multiple times in a sample. Thereafter, the user would measure their metric of interest on the sample and then repeat the process.** In this manner, the distribution of the values of the metric calculated from random samples multiple times is expected to represent the distribution of the population, and so the entire dataset.



An example of Bagging a set of 3 numbers, such as \(1,2,3,4\), would be:

\(1,2,3\), \(1,1,3\), \(1,3,3\), \(2,2,1\), and others.

Bootstrap Aggregating, or _bagging_, implies leveraging a voting method using _multiple bootstrap samples_ at a time, building a model on each individual sample \(set of n records\) and then finally aggregating the results.

Random forests also implement another level of operation beyond simple bagging. It also randomly selects the variables to be included in the model building process at each split. For instance, if we were to create a random forest model using the PimaIndiansDiabetes dataset with the variables pregnant, glucose, pressure, triceps, insulin, mass, pedigree, age, and diabetes, in each bootstrap sample \(draw of n records\), we would select a random subset of features with which to build the model--for instance, glucose, pressure, and insulin; insulin, age, and pedigree; triceps, mass, and insulin; and others.

