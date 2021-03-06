From "statistics-for-machine book"

The development and deployment of machine learning models involves a series of steps that are almost similar to the statistical modeling process, in order to develop, validate, and implement machine learning models. The steps are as follows:

** Collection of data:** Data for machine learning is collected directly from structured source data, web scrapping, API, chat interaction, and so on, as machine learning can work on both structured and unstructured data \(voice, image, and text\).

**Data preparation and missing/outlier treatment:** Data is to be formatted as per the chosen machine learning algorithm; also, missing value treatment needs to be performed by replacing missing and outlier values with the mean/median, and so on.

** Data analysis and feature engineering: **Data needs to be analyzed in order to find any hidden patterns and relations between variables, and so on. Correct feature engineering with appropriate business knowledge will solve 70 percent of the problems. Also, in practice, 70 percent of the data scientist's time is spent on feature engineering tasks.

**Train algorithm on training and validation data:** Post feature engineering, data will be divided into three chunks \\(train, validation, and test data\\) rather than two \\(train and test\\) in statistical modeling. Machine learning are applied on training data and the hyperparameters of the model are tuned based on validation data to avoid overfitting.

**Test the algorithm on test data:** Once the model has shown a good enough performance on train and validation data, its performance will be checked against unseen test data. If the performance is still good enough, we can proceed to the next and final step.

** Deploy the algorithm:** Trained machine learning algorithms will be deployed on live streaming data to classify the outcomes. One example could be recommender systems implemented by e-commerce websites.



From https://www.safaribooksonline.com/library/view/**spark-the-definitive**/9781491912201/ch24.html



Gathering and collecting the relevant data for your task.

1. Cleaning and inspecting the data to better understand it.

2. Performing feature engineering to allow the algorithm to leverage more information.

3. Using a portion of this data as a training set to train one or more algorithms to generate some candidate models.

4. Evaluating and comparing models against your success criteria by objectively measuring results on a subset of the same data \(that was not used for training\). This allows you to better understand how your model may perform in the wild.

5. Leveraging the insights from the above process and/or using the model to make predictions, recommendations, detect anomalies, or solve more general business challenges.



