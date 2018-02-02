[The importance of variables feature selection/attribute selection](/the-importance-of-variables-feature-selectionattribute-selection.md)

[https://www.safaribooksonline.com/library/view/spark-the-definitive/9781491912201/ch24.html](https://www.safaribooksonline.com/library/view/spark-the-definitive/9781491912201/ch24.html)

Now that you collected and claned your dataset, it’s time to convert it to a form suitable for machine learning, which generally means numerical features. The process of feature engineering includes a variety of tasks including: normalizing data, adding variables to represent the interactions of other variables, manipulating categorical variables, and converting them to the proper format to be input into our machine learning model.

**In MLlib, Spark’s machine learning library, all variables will usually have to be input as doubles \(regardless of what they actually represent\). This means you’re likely going to have to use something like One-Hot Encoding as well as leveraging other indexing style techniques.** We cover the process of feature engineering in great depth in [Chapter 25](https://www.safaribooksonline.com/library/view/spark-the-definitive/9781491912201/ch25.html#s6c2---preprocessing-and-feature-engineering). As you will see in that chapter, Spark provides the essentials you’ll need to manipulate your data using a variety of machine learning statistical techniques.



**Spark 24 Hours**

In machine learning, a feature is a measurable attribute or characteristic of an observation. Variables for developing models are sourced from a pool of features. Examples of simple features for building a retail or financial services propensity or risk model could be annual income, total amount spent in the last 12 months in a particular category, or a three-month moving average credit card cycle balance.

Often, features don’t present in the data itself. They are derived from the data, historical data, or other available data sources. Moreover, features could be aggregated or summarized from the underlying data. Creating the set of features used by an algorithm in a machine learning program is the process of feature extraction. Selecting and extracting an appropriate set of features is arguably as important \(if not more important\) as algorithm selection or tuning.

Features are often represented as numerical vectors \(recall the introduction to vectors in the previous chapter\). Sometimes it is necessary to represent textbased data as feature vectors. There are many established techniques for doing so including TF-IDF \(Term Frequency-Inverse Document Frequency\). TF-IDF measures the significance of an element relevant to other elements within a set. 

