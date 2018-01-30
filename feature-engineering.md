[The importance of variables feature selection/attribute selection](/the-importance-of-variables-feature-selectionattribute-selection.md)

[https://www.safaribooksonline.com/library/view/spark-the-definitive/9781491912201/ch24.html](https://www.safaribooksonline.com/library/view/spark-the-definitive/9781491912201/ch24.html)

Now that you collected and claned your dataset, it’s time to convert it to a form suitable for machine learning, which generally means numerical features. The process of feature engineering includes a variety of tasks including: normalizing data, adding variables to represent the interactions of other variables, manipulating categorical variables, and converting them to the proper format to be input into our machine learning model.

**In MLlib, Spark’s machine learning library, all variables will usually have to be input as doubles \(regardless of what they actually represent\). This means you’re likely going to have to use something like One-Hot Encoding as well as leveraging other indexing style techniques.** We cover the process of feature engineering in great depth in [Chapter 25](https://www.safaribooksonline.com/library/view/spark-the-definitive/9781491912201/ch25.html#s6c2---preprocessing-and-feature-engineering). As you will see in that chapter, Spark provides the essentials you’ll need to manipulate your data using a variety of machine learning statistical techniques.

