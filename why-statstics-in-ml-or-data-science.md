It helps you to compare to classifiers, models .

[https://www.quora.com/How-important-it-is-to-learn-statistics-for-a-career-in-machine-learning](https://www.quora.com/How-important-it-is-to-learn-statistics-for-a-career-in-machine-learning)

[https://www.quora.com/How-Important-is-it-to-master-statistics-to-understand-machine-learning](https://www.quora.com/How-Important-is-it-to-master-statistics-to-understand-machine-learning)

you need statistics every time you report the performance of your model  - a number without confidence interval is no result

Machine learning is a branch of statistics, and blindly applying algorithms to data is disastrous for a company \(and can cause legal issues for that company down the road\). Applying the wrong algorithm, not understanding the biases or limitations of an algorithm, and not interpreting the output correctly. This is where statistics will be used to understand limitations, compare models etc ...

After you exactly understand how these ml algorithms work, You can look back to learn more statistic theories and study why these ml algorithms works.

**In one word, statistic helps you understand why these ml models work and how to improve them.**

optimization helps you to understand how it works.

[https://www.quora.com/What-are-the-roles-of-probability-and-statistics-in-machine-learning-How-important-are-they-What-are-their-applications-in-machine-learning](https://www.quora.com/What-are-the-roles-of-probability-and-statistics-in-machine-learning-How-important-are-they-What-are-their-applications-in-machine-learning)

There are several reasons probability and statistics are important in machine learning, but I think one of the most important reasons is because **they help justify the choices made by many models.**

[https://www.quora.com/What-is-the-best-way-to-compare-accuracy-of-multiple-classifiers-and-why/answer/Shehroz-Khan-2](https://www.quora.com/What-is-the-best-way-to-compare-accuracy-of-multiple-classifiers-and-why/answer/Shehroz-Khan-2)

Anyway, If you have a dataset, and

* If you want to compare the performance of two classifiers, you can try McNemar's Test, K-Fold Cross-Validated Paired t-Test, 5x2 cv Paired t-Test, or 5x2 cv Paired F-Test \(depending upon your case\).

* For comparing Multiple Algorithms, you should try Analysis of Variance

If there are multiple datasets, and

* If you want to compare two algorithms, you should try Wilcoxon signed rank test
* If there are multiple algorithms, you should try Kruskal-Wallis test.

[https://www.quora.com/How-important-it-is-to-learn-statistics-for-a-career-in-machine-learning](https://www.quora.com/How-important-it-is-to-learn-statistics-for-a-career-in-machine-learning)

In the simplest case, suppose you are comparing the performance of two classifiers A and B. A gives 90% accuracy and B gives 87% accuracy, which one is better? May be both A and B perform the **same **statistically, but you will never know this unless you know statistics. That is how much **statistics is important for understanding and interpreting results obtained from ML methods.**



You can implement everything without knowing any statistics, but you won’t be able to understand much \(why these things work\) without having a solid knowledge on statistics. I would say that statistics, linear algebra and optimization are the three most important prerequisites to do machine learning.

**Important to know from statistics**

probability - Bayes probability, conditional probability, is must-known knowledge

Analysis of Variance

Wilcoxon signed rank test

Kruskal-Wallis test.

