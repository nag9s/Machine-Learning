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

**An example of Bagging a set of 3 numbers, such as \(1,2,3,4\), would be:**

**\(1,2,3\), \(1,1,3\), \(1,3,3\), \(2,2,1\), and others.**

Bootstrap Aggregating, or _bagging_, implies leveraging a voting method using _multiple bootstrap samples_ at a time, building a model on each individual sample \(set of n records\) and then finally aggregating the results.

Random forests also implement another level of operation beyond simple bagging. It also randomly selects the variables to be included in the model building process at each split. For instance, if we were to create a random forest model using the PimaIndiansDiabetes dataset with the variables pregnant, glucose, pressure, triceps, insulin, mass, pedigree, age, and diabetes, in each bootstrap sample \(draw of n records\), we would select a random subset of features with which to build the model--for instance, glucose, pressure, and insulin; insulin, age, and pedigree; triceps, mass, and insulin; and others.

[https://www.safaribooksonline.com/library/view/ensemble-machine-learning/9781788297752/10bf8a39-d15f-4bb3-8c39-9f2795865462.xhtml](https://www.safaribooksonline.com/library/view/ensemble-machine-learning/9781788297752/10bf8a39-d15f-4bb3-8c39-9f2795865462.xhtml)

the real world is not as easy as the conceptual world; you will not always get an ideal categorical dataset with only a few attribute values. Real-world data may be far bigger than you think. It may have millions of instances \(such as a dataset of a census analysis\) with many more attributes \(in hundreds\). In such cases, it is impossible to use a single decision tree to get predictions. So, what do you think is the solution? Yes! We have to **divide and conquer **; you get it, right? Increase the number of trees and divide the dataset into different trees.

Creating multiple trees out of a single dataset and then combining the predictions of all of them is known as **tree bagging**, which is a widely used method by the machine learning community. This group of multiple trees is known as a decision tree forest, and when we create this forest using randomly selected samples \(in combination with randomly selected features\) out of our dataset, this forest is known as a **random forest**.

This figure gives you an idea about bagged decision trees:

![](/assets/Rf4.png)



Let's try to understand it with the help of a problem. Do you remember we opened a fund adviser company in the last chapter and it can successfully choose its target customers using a decision tree? Now, after some months \(or years\) of effort, we are the topmost investment adviser group and want to expand our business throughout the country. So when we start expanding our business in different regions of our country, we will meet different kinds of customers. And there will be more parameters to add to our dataset, such as the financial status of a state, city, or village, educational status of the targeted region \(number of uneducated, graduate, and postgraduate investors, and so on\), and many more factors such as urban and rural lifestyle. So, there are many different parameters possible to create a strong dataset through which we can reach our target investors.

When we increase the number of parameters in our dataset, it becomes more complex, not only due to the more number of parameters, but also due to the need to include numerical values. So this dataset will not suit the decision tree algorithm learned in [Chapter 2](https://www.safaribooksonline.com/library/view/ensemble-machine-learning/9781788297752/d0e712f5-cbda-4311-91b0-69eecadff995.xhtml), _Decision Trees_. What! So, what we will do? One solution is to create a tree that can handle numerical values to create nodes and branches. How to do it? The answer is the **Classification and Regression Trees** \(**CART**\) algorithm, which is widely used to create decision trees. It is also the building block of our random forest algorithm.

