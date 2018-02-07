[https://www.safaribooksonline.com/library/view/java-data-science/9781788475655/31238b56-8fa0-4105-9556-a7da2a41c7c2.xhtml](https://www.safaribooksonline.com/library/view/java-data-science/9781788475655/31238b56-8fa0-4105-9556-a7da2a41c7c2.xhtml)

**Mean Absolute Error** \(**MAE**\), is an alternative metric for evaluating performance. Instead of taking the squared error, it only takes the absolute value of the difference between the actual and predicted value. This is how we can compute it:

```
double sum = 0.0;
 for (int i = 0; i <  n; i++) 
 {     sum = sum + Math.abs(actual[i] - predicted[i]); 
 } 
 double mae = sum / n;
```

Sometimes we have outliers in the data--the values with quite irregular values. If we have a lot of outliers, we should prefer MAE to RMSE, since it is more robust to them. If we do not have many outliers, then RMSE should be the preferred choice.

