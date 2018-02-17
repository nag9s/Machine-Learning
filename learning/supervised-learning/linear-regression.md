[https://www.safaribooksonline.com/library/view/hands-on-data-science/9781787280748/](https://www.safaribooksonline.com/library/view/hands-on-data-science/9781787280748/)

[https://www.safaribooksonline.com/library/view/statistics-for-machine/9781788295758/94fde0ee-fc9e-4cbc-aac4-d8dc1d9d94f4.xhtml](https://www.safaribooksonline.com/library/view/statistics-for-machine/9781788295758/94fde0ee-fc9e-4cbc-aac4-d8dc1d9d94f4.xhtml)

This is used for** the prediction of continuous variables such as customer income and so on.** It utilizes error minimization to fit the best possible line in statistical methodology. However, in machine learning methodology, squared loss will be minimized with respect to  _β _ coefficients. Linear regression also has a high bias and a low variance error.

[https://www.safaribooksonline.com/library/view/statistics-for-machine/9781788295758/a9a363b7-2535-46f5-b27b-0738aad3b260.xhtml](https://www.safaribooksonline.com/library/view/statistics-for-machine/9781788295758/a9a363b7-2535-46f5-b27b-0738aad3b260.xhtml)

In linear regression, only the **residual sum of squares** \(**RSS**\) is minimized, whereas in ridge and lasso regression, a penalty is applied \(also known as **shrinkage penalty**\) on coefficient values to regularize the coefficients with the tuning parameter _λ_.

When _λ=0_, the penalty has no impact, ridge/lasso produces the same result as linear regression, whereas _λ -&gt; ∞_ will bring coefficients to zero:

![](/assets/formula.png)

![](/assets/re1.png)

[https://www.safaribooksonline.com/library/view/scala-machine-learning/9781788479042/5355fd2b-8e0c-4bf8-a3f3-9e2ad9de7327.xhtml](https://www.safaribooksonline.com/library/view/scala-machine-learning/9781788479042/5355fd2b-8e0c-4bf8-a3f3-9e2ad9de7327.xhtml)

**Logistic regression** \(**LR**\) belongs to the family of regression algorithms. The goal of regression is to find relationships and dependencies between variables. It models the relationship between a continuous scalar dependent variable _y_ \(that is, label or target\) and one or more \(a D-dimensional vector\) explanatory variable \(also independent variables, input variables, features, observed data, observations, attributes, dimensions, and data points\) denoted as _x_ using a linear function:

![](/assets/lr2.png)

LR models the relationship between a dependent variable _y,_ which involves a linear combination of interdependent variables _xi_. The letters _A_ and _B_ represent constants that describe the _y_ axis intercept and the slope of the line respectively:

_y = A+Bx_

_Figure 9_, _Regression graph separates data points \(in red dots\) and the blue line is regression_ shows an example of simple LR with one independent variable—that is, a set of data points and a **best fit** line, which is the result of the regression analysis itself. It can be observed that the line does not actually pass through all of the points.

The distance between any data points \(measured\) and the line \(predicted\) is called the regression error. Smaller errors contribute to more accurate results in predicting unknown values. When the errors are reduced to their smallest levels possible, the line of best fit is created for the final regression error. Note that there are no single metrics in terms of regression errors; there are several as follows:

* **Mean Squared Error ** \(**MSE**\): It is a measure of how close a fitted line is to data points. The smaller the MSE, the closer the fit is to the data.
* **Root Mean Squared Error** \(**RMSE**\): It is the square root of the MSE but probably the most easily interpreted statistic, since it has the same units as the quantity plotted on the vertical axis.
* **R-squared**: R-squared is a statistical measure of how close the data is to the fitted regression line. R-squared is always between 0 and 100%. The higher the R-squared, the better the model fits your data.
* **Mean Absolute Error** \(**MAE**\): MAE measures the average magnitude of the errors in a set of predictions without considering their direction. It's the average over the test sample of the absolute differences between prediction and actual observation where all individual differences have equal weight.
* **Explained variance**:In statistics,**explained ** variation measures the proportion to which a mathematical model accounts for the variation of a given dataset.



