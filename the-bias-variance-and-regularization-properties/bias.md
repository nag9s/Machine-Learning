[https://www.safaribooksonline.com/library/view/statistics-for-machine/9781788295758/16bf3b8e-a897-45a8-8959-e3d2e1d0ec5b.xhtml](https://www.safaribooksonline.com/library/view/statistics-for-machine/9781788295758/16bf3b8e-a897-45a8-8959-e3d2e1d0ec5b.xhtml)

Every model has both bias and variance error components in addition to white noise. Bias and variance are inversely related to each other; while trying to reduce one component, the other component of the model will increase. The true art lies in creating a good fit by balancing both. The ideal model will have both low bias and low variance.

Errors from the bias component come from erroneous assumptions in the underlying learning algorithm. High bias can cause an algorithm to miss the relevant relations between features and target outputs; this phenomenon causes an underfitting problem.

On the other hand, errors from the variance component come from sensitivity to change in the fit of the model, even a small change in training data; high variance can cause an overfitting problem:

![](/assets/bv.png)

An example of a high bias model is logistic or linear regression, in which the fit of the model is merely a straight line and may have a high error component due to the fact that a linear model could not approximate underlying data well.

An example of a high variance model is a decision tree, in which the model may create too much wiggly curve as a fit, in which even a small change in training data will cause a drastic change in the fit of the curve.



![](/assets/bv2.png)

