In linear regression, only the **residual sum of squares** \(**RSS**\) is minimized, whereas in ridge and lasso regression, a penalty is applied \(also known as **shrinkage penalty**\) on coefficient values to regularize the coefficients with the tuning parameter _λ_.

When _λ=0_, the penalty has no impact, ridge/lasso produces the same result as linear regression, whereas _λ -&gt; ∞_ will bring coefficients to zero:

[Linear regression](/learning/supervised-learning/linear-regression.md)

