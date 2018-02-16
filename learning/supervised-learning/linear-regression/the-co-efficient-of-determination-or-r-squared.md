[https://www.safaribooksonline.com/library/view/machine-learning-with/9781785889936/53453938-8345-4d5f-8425-69b46485e3d3.xhtml](https://www.safaribooksonline.com/library/view/machine-learning-with/9781785889936/53453938-8345-4d5f-8425-69b46485e3d3.xhtml)

# The R-squared coefficient

The R-squared coefficient, also known as the coefficient of determination, is a measure of how well a model fits a dataset. It is commonly used in statistics. It measures the degree of variation in the target variable; this is explained by the variation in the input features. An R-squared coefficient generally takes a value between 0 and 1, where 1 equates to a perfect fit of the model.

[https://www.safaribooksonline.com/library/view/hands-on-data-science/9781787280748/94105517-242f-47cf-8cb8-ef52bd8dc2aa.xhtml](https://www.safaribooksonline.com/library/view/hands-on-data-science/9781787280748/94105517-242f-47cf-8cb8-ef52bd8dc2aa.xhtml)

how do I know how good my regression is? How well does my line fit my data? That's where r-squared comes in, and r-squared is also known as the coefficient of determination. Again, someone trying to sound smart might call it that, but usually it's called r-squared.

It is the fraction of the total variation in Y that is captured by your models. So how well does your line follow that variation that's happening? Are we getting an equal amount of variance on either side of your line or not? That's what r-squared is measuring.

# Interpreting r-squared

[https://www.safaribooksonline.com/library/view/hands-on-data-science/9781787280748/290c1421-7217-43b3-8276-466d2bfe70fb.xhtml](https://www.safaribooksonline.com/library/view/hands-on-data-science/9781787280748/290c1421-7217-43b3-8276-466d2bfe70fb.xhtml)

**For r-squared, you will get a value that ranges from 0 to 1. Now 0 means your fit is terrible. It doesn't capture any of the variance in your data. While 1 is a perfect fit, where all of the variance in your data gets captured by this line, and all of the variance you see on either side of your line should be the same in that case. So 0 is bad, and 1 is good. That's all you really need to know. Something in between is something in between. A low r-squared value means it's a poor fit, a high r-squared value means it's a good fit.**

As you'll see in the coming sections, there's more than one way to do regression. Linear regression is one of them. It's a very simple technique, but there are other techniques as well, and you can use r-squared as a quantitative measure of how good a given regression is to a set of data points, and then use that to choose the model that best fits your data.

