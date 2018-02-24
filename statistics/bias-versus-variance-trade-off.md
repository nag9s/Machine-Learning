[https://www.safaribooksonline.com/library/view/hands-on-data-science/9781787280748/9f8cad93-99eb-4196-90b7-31054e9fc005.xhtml](https://www.safaribooksonline.com/library/view/hands-on-data-science/9781787280748/9f8cad93-99eb-4196-90b7-31054e9fc005.xhtml)

One of the basic challenges that we face when dealing with real-world data is overfitting versus underfitting your regressions to that data, or your models, or your predictions. When we talk about underfitting and overfitting, we can often talk about that in the context of bias and variance, and the bias-variance trade-off. So, let's talk about what that means.

So conceptually, bias and variance are pretty simple. **Bias is just how far off you are from the correct values, that is, how good are your predictions overall in predicting the right overall value. If you take the mean of all your predictions, are they more or less on the right spot? Or are your errors all consistently skewed in one direction or another? If so, then your predictions are biased in a certain direction.**

**Variance is just a measure of how spread out, how scattered your predictions are. So, if your predictions are all over the place, then that's high variance. But, if they're very tightly focused on what the correct values are, or even an incorrect value in the case of high bias, then your variance is small.**

Let's look at some examples. Let's imagine that the following dartboard represents a bunch of predictions we're making where the real value we're trying to predict is in the center of the bullseye:

![](/assets/bv1.png)

* Starting with the dartboard in the upper left-hand corner, you can see that our points are all scattered about the center. So overall, you know the mean error comes out to be pretty close to reality. **Our bias is actually very low, because our predictions are all around the same correct point. However, we have very high variance, because these points are scattered about all over the place.** So, this is an example of** low bias and high variance.**

* If we move on to the dartboard in the upper right corner, we see that our points are **all consistently skewed from where they should be, to the Northwest.** So this is an example of** high bias** in our predictions, where they're consistently off by a certain amount. We have l**ow variance because they're all clustered tightly around the wrong spot, but at least they're close together, so we're being consistent in our predictions**. That's low variance. But, the bias is high. So again, this is **high bias, low variance.**

* In the dartboard in the lower left corner, you can see that** our predictions are scattered around the wrong mean point.** So, we have** high bias;** everything is skewed to some place where it shouldn't be. But **our variance is also high.** So, this is kind of the worst of both worlds here; we have **high bias and high variance** in this example.

* Finally, **in a wonderful perfect world, you would have an example like the lower right dartboard, where we have low bias, **where everything is centered around where it should be, and **low variance, where things are all clustered pretty tightly around where they should be**. So, in a perfect world that's what you end up with.

This is bias-variance trade-off. You know the decision you have to make between how overall accurate your values are, and how spread out they are or how tightly clustered they are. That's the bias-variance trade-off and they both contribute to the overall error, which is the thing you really care about minimizing.

Decision trees is another example. We know that a single decision tree is prone to overfitting, so that might imply that it has a high variance. But, random forests seek to trade off some of that variance for bias reduction, and it does that by having multiple trees that are randomly variant and averages all their solutions together. It's like when we average things out by increasing K in KNN: we can average out the results of a decision tree by using more than one decision tree using random forests similar idea.

[https://www.safaribooksonline.com/library/view/statistics-for-machine/9781788295758/16bf3b8e-a897-45a8-8959-e3d2e1d0ec5b.xhtml](https://www.safaribooksonline.com/library/view/statistics-for-machine/9781788295758/16bf3b8e-a897-45a8-8959-e3d2e1d0ec5b.xhtml)

Every model has both bias and variance error components in addition to white noise. Bias and variance are inversely related to each other; while trying to reduce one component, the other component of the model will increase. The true art lies in creating a good fit by balancing both. The ideal model will have both low bias and low variance.



Errors from the bias component come from erroneous assumptions in the underlying learning algorithm. High bias can cause an algorithm to miss the relevant relations between features and target outputs; this phenomenon causes an underfitting problem.



An example of a high bias model is logistic or linear regression, in which the fit of the model is merely a straight line and may have a high error component due to the fact that a linear model could not approximate underlying data well.

An example of a high variance model is a decision tree, in which the model may create too much wiggly curve as a fit, in which even a small change in training data will cause a drastic change in the fit of the curve.

At the moment, state-of-the-art models are utilizing high variance models such as decision trees and performing ensemble on top of them to reduce the errors caused by high variance and at the same time not compromising on increases in errors due to the bias component. The best example of this category is random forest, in which many decision trees will be grown independently and ensemble in order to come up with the best fit;

