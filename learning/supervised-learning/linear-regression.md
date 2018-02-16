[https://www.safaribooksonline.com/library/view/hands-on-data-science/9781787280748/](https://www.safaribooksonline.com/library/view/hands-on-data-science/9781787280748/)

[https://www.safaribooksonline.com/library/view/statistics-for-machine/9781788295758/94fde0ee-fc9e-4cbc-aac4-d8dc1d9d94f4.xhtml](https://www.safaribooksonline.com/library/view/statistics-for-machine/9781788295758/94fde0ee-fc9e-4cbc-aac4-d8dc1d9d94f4.xhtml)

This is used for** the prediction of continuous variables such as customer income and so on.** It utilizes error minimization to fit the best possible line in statistical methodology. However, in machine learning methodology, squared loss will be minimized with respect to  _β _ coefficients. Linear regression also has a high bias and a low variance error.

[https://www.safaribooksonline.com/library/view/statistics-for-machine/9781788295758/a9a363b7-2535-46f5-b27b-0738aad3b260.xhtml](https://www.safaribooksonline.com/library/view/statistics-for-machine/9781788295758/a9a363b7-2535-46f5-b27b-0738aad3b260.xhtml)

In linear regression, only the **residual sum of squares** \(**RSS**\) is minimized, whereas in ridge and lasso regression, a penalty is applied \(also known as **shrinkage penalty**\) on coefficient values to regularize the coefficients with the tuning parameter _λ_.

When _λ=0_, the penalty has no impact, ridge/lasso produces the same result as linear regression, whereas _λ -&gt; ∞_ will bring coefficients to zero:

![](/assets/formula.png)

![](/assets/re1.png)

https://www.safaribooksonline.com/library/view/scala-machine-learning/9781788479042/5355fd2b-8e0c-4bf8-a3f3-9e2ad9de7327.xhtml



**Logistic regression** \(**LR**\) belongs to the family of regression algorithms. The goal of regression is to find relationships and dependencies between variables. It models the relationship between a continuous scalar dependent variable _y_ \(that is, label or target\) and one or more \(a D-dimensional vector\) explanatory variable \(also independent variables, input variables, features, observed data, observations, attributes, dimensions, and data points\) denoted as _x_ using a linear function:



![](/assets/lr2.png)

