From [https://www.safaribooksonline.com/library/view/scala-for-machine](https://www.safaribooksonline.com/library/view/scala-for-machine)

MLlib is a scalable machine learning library built on top of Spark. The machine learning library is composed of two distinct packages, which are \[17:03\]:

1. `org.apache.spark.mllib`
   : RDD-based library of some common machine learning algorithms. This package** will be deprecated in future releases.**
2. `org.apache.spark.ml`
   : Library of machine learning algorithms that leverages datasets and data frames structures. The package supports tasks pipeline and stages that are described and illustrated in the next section.



https://www.safaribooksonline.com/library/view/spark-the-definitive/9781491912201/ch24.html

MLlib consists of two packages that leverage different core data structures. The package `org.apache.spark.ml` maintains an interface for use with Spark DataFrames. This package also maintains a high-level interface for building machine learning pipelines that help standardize the way in which you perform the above steps. The lower-level package, `org.apache.spark.mllib`, maintains interfaces for Spark’s low-level, RDD APIs. This book will focus exclusively on the DataFrame API. The RDD API is the lower-level interface, which is in maintenance mode \(meaning it will only receive bug fixes, not new features\) at this time. It has also been covered fairly extensively in other books on Spark and is therefore omitted here.



