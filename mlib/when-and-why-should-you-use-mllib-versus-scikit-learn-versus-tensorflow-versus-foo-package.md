There are numerous tools for performing machine learning on a single-machine, and while there are several great options to choose from, these single machine tools do have their limits either in terms of the size of data you can train on or the processing time. This means single-machine tools \( Scikit , TensorFlow\) are  _complementary _ tools, not competitive ones. When you hit those scalability issues, take advantage of Spark’s abilities.



There are** two key use cases where you want to leverage Spark’s ability to scale.** **Firstly, you want to leverage Spark for preprocessing and feature generation to reduce the amount of time it might take to produce training and test sets from a large amount of data**. Then you might leverage single-machine learning algorithms to train on those given data sets. **Secondly, when your input data or model size become too difficult or inconvenient to put on one machine, use Spark to do the heavy lifting. Spark makes big data machine learning simple.**

