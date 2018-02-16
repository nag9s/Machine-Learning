[https://www.safaribooksonline.com/library/view/machine-learning-algorithms/9781785889622/b69ea832-19cd-48be-8a4d-08d6897d778a.xhtml](https://www.safaribooksonline.com/library/view/machine-learning-algorithms/9781785889622/b69ea832-19cd-48be-8a4d-08d6897d778a.xhtml)

A generic dataset \(we assume here that it is always numerical\) is made up of different values which can be drawn from different distributions, having different scales and, sometimes, there are also outliers. A machine learning algorithm isn't naturally able to distinguish among these various situations, and therefore, it's always preferable to standardize datasets before processing them. A very common problem derives from having a non-zero mean and a variance greater than one. In the following figure, there's a comparison between a raw dataset and the same dataset scaled and centered:

![](/assets/reg1.png)This result can be achieved using the StandardScaler class: \( SparkMLLib , Sci kit\)

