[https://www.safaribooksonline.com/library/view/scala-machine-learning/9781788479042/2b2132b7-7abd-4ce3-ad7a-731a8e5cfe46.xhtml](https://www.safaribooksonline.com/library/view/scala-machine-learning/9781788479042/2b2132b7-7abd-4ce3-ad7a-731a8e5cfe46.xhtml)

Root Mean Squared Error \(RMSE\) is used to measure the difference between values predicted by a model and the values actually observed. By default, the smaller the calculated error, the better the model. In order to test the quality of the model, the test data is used.

[https://www.safaribooksonline.com/library/view/java-data-science/9781788475655/8c125d9e-14d9-46b9-a3ba-8c4bbe4492de.xhtml](https://www.safaribooksonline.com/library/view/java-data-science/9781788475655/8c125d9e-14d9-46b9-a3ba-8c4bbe4492de.xhtml)

**Mean Squared Error** \(**MSE**\) is the sum of squared differences between the actual and predicted values. It is quite easy to compute it in Java:

```
double[] actual, predicted;
```

```
int n = actual.length; 


double sum = 0.0; 


for (int i = 0; i 
<
 n; i++) { 


    diff = actual[i] - predicted[i]; 


    sum = sum + diff * diff; 


} 




double mse = sum / n;
```

Typically, the value of MSE is hard to interpret, which is why we often take a square root of MSE; this is called **Root Mean Squared Error** \(**RMSE**\). It is easier to interpret because it is in the same units as the target variable.

```
double rmse = Math.sqrt(mse);
```

```

```



