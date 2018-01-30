[https://www.safaribooksonline.com/library/view/mastering-predictive-analytics/9781787121393/ch03s06.html](https://www.safaribooksonline.com/library/view/mastering-predictive-analytics/9781787121393/ch03s06.html)

One such method is **forward selection**, which is an example of **stepwise regression** that performs feature selection in a series of steps. With forward selection, the idea is to start out with an empty model that has no features selected. We then perform _k_ simple linear regressions \(one for every feature that we have\) and pick the best one. Here, we are comparing models that have the same number of features so that we can use the R2 statistic to guide our choice, although we can use metrics such as AIC as well. Once we have chosen our first feature to add, we then pick another feature to add from the remaining _k-1_ features. Therefore, we now run _k-1_ multiple regressions for every possible pair of features, where one of the features in the pair is the feature that we picked in the first step. We continue adding in features like this until we have evaluated the model with all the features included and stop. Note that, in every step, we make a hard choice about which feature to include for all future steps.

For example, models that have more than one feature in them and do not include the feature we chose in the first step of this process are never considered. Therefore, we do not exhaustively search our space. In fact, if we take into account that we also assess the null model, we can compute the total number of models we perform a linear regression on as follows:

![](/assets/forwardSel.png)

The order of magnitude of this computation is on the scale of _k2_, which for even small values of _k_ is already considerably less than _2k_. At the end of the forward selection process, we have to choose between _k+1_ models, corresponding to the subsets we obtained at the end of every step of the process. As the final part of the process involves comparing models with different numbers of features, we usually use a criterion such as the AIC or the adjusted R2 to make our final choice of model. We can demonstrate this process for our CPU dataset by running the following commands:

[https://www.safaribooksonline.com/library/view/statistics-for-machine/9781788295758/bdd4260c-5a10-4db7-b195-ca13d97b9d0a.xhtml](https://www.safaribooksonline.com/library/view/statistics-for-machine/9781788295758/bdd4260c-5a10-4db7-b195-ca13d97b9d0a.xhtml)

There are various methods to add or remove variables to determine the best possible model.

In the backward method, **iterations start with considering all the variables and we will remove variables one by one until all the prescribed statistics are met** \(such as no insignificance and multi-collinearity, and so on  [Assumptions of linear regression](/learning/supervised-learning/linear-regression/assumptions-of-linear-regression.md)\). **Finally, the overall statistic will be checked, such as if R-squared value is **_**&gt; 0.7**_** , it is considered a good model, else reject it. In industry, practitioners mainly prefer to work on backward methods.**



**In the case of forward, we will start with no variables and keep on adding significant variables until the overall model's fit improves.**

