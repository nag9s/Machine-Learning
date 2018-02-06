# The vector data type

Remember when we were doing movie similarities and movie recommendations earlier in the book? An example of a vector might be a list of all the movies that a given user rated. There are two types of vector, sparse and dense. Let's look at an example of those. There are many, many movies in the world, and a dense vector would actually represent data for every single movie, whether or not a user actually watched it. So, for example, let's say I have a user who watched Toy Story, obviously I would store their rating for Toy Story, but if they didn't watch the movie Star Wars, I would actually store the fact that there is not a number for Star Wars. So, we end up taking up space for all these missing data points with a dense vector. A sparse vector only stores the data that exists, so it doesn't waste any memory space on missing data, OK. So, it's a more compact form of representing a vector internally, but obviously that introduces some complexity while processing. So, it's a good way to save memory if you know that your vectors are going to have a lot of missing data in them.

From [https://www.safaribooksonline.com/library/view/spark-for-data/9781785885655/ch06s02.html](https://www.safaribooksonline.com/library/view/spark-for-data/9781785885655/ch06s02.html)

Fundamental data types in this library are vectors and matrices. **Vectors are local, and may be dense or sparse. Dense vectors are stored as an array of values. Sparse vectors are stored as two arrays; the first array stores the non-zero value indices and the second array stores the actual values.** All element values are stored as doubles and indices are stored as integers starting from zero. Understanding the fundamental structures goes a long way in effective use of the libraries and it should help code up any new algorithm from scratch. Let us see some example code for a better understanding of these two vector representations:

I didnt see distributed Vector ? Need to find out why there is no distributed vector.

From [https://www.safaribooksonline.com/library/view/spark-for-data/9781785885655/ch06s02.html](https://www.safaribooksonline.com/library/view/spark-for-data/9781785885655/ch06s02.html)

![](/assets/vector1.png)

![](/assets/vector2.png)

**   Local vector:** Local vectors are stored on a single machine having values as double and indices of each such values are stored as an integer starting with zero. Local vectors can further be sub classified into dense and sparse vectors. A double array representing its values is called dense vector while sparse vector contains two arrays representing indices and values separately.

For example, a vector \( 2.0, 0.0, 5.0, 3.0 \) can be represented as a:

Dense vector as \[ 2.0, 0.0, 5.0, 3.0\]

Sparse vector as \[4, \(0,2,3\), \(2.0,5.0,3.0\) \]

From [https://medium.com/@rickynguyen/getting-started-with-spark-day-5-36b62a6d13bf](https://medium.com/@rickynguyen/getting-started-with-spark-day-5-36b62a6d13bf)

![](/assets/vect2.png)

##### From Spark In Action

**Local vectors in Spark are implemented with two classes—DenseVector and SparseVector**—implementing a common interface called Vector, making sure both implementations support exactly the same set of operations. **The main class for creating vectors is the Vectors class and its dense and sparse method. The dense method has two versions: it can take all elements as inline arguments or it can take an array of elements. For the sparse method, you need to specify a vector size, an array with indices, and an array with values. The following three vectors \(dv1, dv2, and sv\) contain the same elements and, hence, represent the same mathematical vectors:**

