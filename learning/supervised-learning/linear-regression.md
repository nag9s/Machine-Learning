[https://www.safaribooksonline.com/library/view/hands-on-data-science/9781787280748/](https://www.safaribooksonline.com/library/view/hands-on-data-science/9781787280748/)

[https://www.safaribooksonline.com/library/view/statistics-for-machine/9781788295758/94fde0ee-fc9e-4cbc-aac4-d8dc1d9d94f4.xhtml](https://www.safaribooksonline.com/library/view/statistics-for-machine/9781788295758/94fde0ee-fc9e-4cbc-aac4-d8dc1d9d94f4.xhtml)

This is used for** the prediction of continuous variables such as customer income and so on.** It utilizes error minimization to fit the best possible line in statistical methodology. However, in machine learning methodology, squared loss will be minimized with respect to  _β _ coefficients. Linear regression also has a high bias and a low variance error.

In linear regression, only the **residual sum of squares** \(**RSS**\) is minimized, whereas in ridge and lasso regression, a penalty is applied \(also known as **shrinkage penalty**\) on coefficient values to regularize the coefficients with the tuning parameter _λ_.



When _λ=0_, the penalty has no impact, ridge/lasso produces the same result as linear regression, whereas _λ -&gt; ∞_ will bring coefficients to zero:



![](/assets/formula.png)

