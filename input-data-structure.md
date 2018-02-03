the requirements for input data structure for each advanced analytics task in MLlib.

In the case of classification and regression, you want to get your data into a column of type `Double` to represent the label and a column of type `Vector` \(either dense or sparse\) to represent the features.

* In the case of recommendation, you want to get your data into a column of users, a column of targets \(say movies or books\), and a column of ratings.

* In the case of unsupervised learning, a column of type `Vector` \(either dense or sparse\) is needed to represent the features.

* In the case of graph analytics, you will want a DataFrame of vertices and a DataFrame of edges.

The best way to do this is through transformers.

