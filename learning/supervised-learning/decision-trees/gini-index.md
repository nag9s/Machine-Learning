[https://www.safaribooksonline.com/library/view/ensemble-machine-learning/9781788297752/ede44257-d3c9-4b34-8888-fe5d7b0ffb1d.xhtml](https://www.safaribooksonline.com/library/view/ensemble-machine-learning/9781788297752/ede44257-d3c9-4b34-8888-fe5d7b0ffb1d.xhtml)

# Gini index for impurity check

Gini index is the cost function used to evaluate splits \(nodes\) in the dataset. Whenever we use the word **split**, it belongs to the node, so each split has two important aspects; the first is attribute and the second is attribute value, which will divide our data into two groups.

Gini score can be used to know the impurity of our dataset just like the information gain of the attribute. But here, it works a bit differently; Gini score suggests how well the dataset can be separated. Let's understand this with an example.

Suppose we have a system that generates 0 at the output whenever the input is less than 0 and generates 1 at the output whenever the input is greater than or equal to 0. We want to write it in the form of an equation:

![](/assets/gini1.png)

If we test a series of input, we can get the result as follows:

![](/assets/gini2.png)

So, as you can see in the preceding table, whenever the input value is less than 0, the output is 0. And whenever the input is greater than 0, the output is 1. This leads us to creating a perfect separation of the preceding data into two groups.

There may be one more case when there is not necessarily a perfect separation \(or split\); for example, suppose we modify the preceding system as follows:

