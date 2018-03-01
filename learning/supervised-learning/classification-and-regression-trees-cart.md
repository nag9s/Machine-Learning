[https://www.safaribooksonline.com/library/view/ensemble-machine-learning/9781788297752/f1165636-da31-4f86-837e-814a97160bab.xhtml](https://www.safaribooksonline.com/library/view/ensemble-machine-learning/9781788297752/f1165636-da31-4f86-837e-814a97160bab.xhtml)

CART was proposed by Leo Breiman to the machine learning community. Classically, this algorithm is known as **decision trees** only, but in the modern-day community, some programming languages refer to it as CART. This algorithm is the cornerstone of the ensemble machine learning system, like bagging and boosting.

The representation of CART is the binary tree only, and this is the same binary tree that we all have learned in data structures. Let's have a brief review of the binary tree algorithm.

Binary trees are different from other trees in the sense that in a normal tree structure, there may be any number of children for a parent node \(including root\); but in a binary tree, as its name suggests, any parent node can have a maximum of two branches \(or nodes\). This figure shows a representation of a simple binary tree:

![](/assets/CART1.png)

This tree is a subtree that we created in the previous chapter. Here, you can see that each node has a maximum of two children. One more thing to add in here—when we work with numerical values as attribute values, our binary tree will look like this:

![](/assets/CART2.png)



If you look closer at the preceding tree, you'll see that we have changed our attribute values from categorical to numerical. So, the criteria of node splitting is going to be based on numerical values only. There is an important property of binary trees: one branch will have values lesser than the parent node and the other will have them higher than the parent node. As you can see in the figure, all children on the left have values more than their parent nodes, while the children on the right have lower values than the parent nodes. This important criteria is used to divide data using an anchor point and create a subset out of it. Later on, we can check whether this subset can be divided further or not.

Now, let's try to create a simple binary tree out of a simple dataset to understand its concept.

Suppose we have the following array of values:

```
data = [0.7,0.65,0.83,0.54,0.9,0.11,0.44,0.35,0.75,0.3,0.78,0.15]
```

After executing the preceding line, we will have a list of numbers like this:

```
data = [0.7, 0.65, 0.83, 0.54, 0.9, 0.11, 0.44, 0.35, 0.75, 0.3, 0.78, 0.15]
```

Now, as we know that a binary tree may have a maximum of two branches \(left and right\), we can write it in the form of a Python dictionary with key values as left and right. There will be one more field called data, where we can store our data. Each node in our binary tree will have these three fields. Let's write a method to create a node with the aforementioned key values:

```
def getNewNode(data):


    node = {'data':[],'left':[],'right':[]}


    node['data'] = data   


return
 node
```

As you can see, our dictionary node has three fields where data will hold the node value at a particular node, and left and right will hold the next nodes.

Let's call the preceding method to create a root node for our tree; we will choose median of the preceding array as our root node. Let's create it:

```
med = np.median(data)


print
("Median of array is: %.2f"%med)


tree = getNewNode(med)




print
(tree)
```

After executing the preceding lines, we will get the following dictionary:

```
{'left': [], 'data': 0.59, 'right': []}
```

Now, as we have our root node, we can start building our tree out of it. We will take array values one by one using a for loop; we will put values less than the parent node in the left branch, while values greater than the parent node will go to the right branch. The following is the method to do this:

```
def 
createBinaryTree
(tree,data):




    #Check whether we have any node in the tree if not create one    


    if not
 tree:


        tree = getNewNode(data)




    #Now if current value is less than parent node put it in left     


    elif
 data
<
=tree['data']:


         tree['left'] = createBinaryTree(tree['left'],data)




    #else put it in right 


    else:


         tree['right'] = createBinaryTree(tree['right'],data)                         


    return tree
```

We will use recursion to create our tree. Recursion is the way to call the same function again and again to complete repetitive tasks, As you can see in the preceding method, we are calling createBinaryTree inside the same function to build a tree under a tree; each call to createBinaryTree will add a subtree to the respective node.

Now that we have sufficient code to create a binary tree for our small array, let's create tree out of it:

```
for  i in  range(len(data)):   


    value = data[i]   


    tree = createBinaryTree(tree,value)


import  pprint


pprint.pprint(tree)
```

As we have already created a root node of our tree, we will now start extracting values from the array and use them to create tree. After the execution of the preceding block, we will have a Python dictionary; it will have our entire tree structure, as follows:

```
{'data': 0.59,


 'left': {'data': 0.54,


          'left': {'data': 0.11,


                   'left': [],


                   'right': {'data': 0.44,


                             'left': {'data': 0.35,


                                      'left': {'data': 0.3,


                                               'left': {'data': 0.15,


                                                        'left': [],


                                                        'right': []},


                                               'right': []},


                                      'right': []},


                             'right': []}},


          'right': []},


 'right': {'data': 0.7,


           'left': {'data': 0.65, 'left': [], 'right': []},


           'right': {'data': 0.83,


                     'left': {'data': 0.75,


                              'left': [],


                              'right': {'data': 0.78, 'left': [], 'right': []}},


                     'right': {'data': 0.9, 'left': [], 'right': []}}}}
```

So, this is the tree we have built out of our array.

The first question that can come to your mind is, now what? What to do with this tree? Well, binary trees are extremely useful whenever you need to search for any element in them. However, binary search is out of our scope; we will see how a binary tree will help us make our decision tree.

**So, to make a decision tree out of a binary tree algorithm, what should be required to add to our code? Let's think about it:**

* **We should have some metric on the basis of which we can decide what should be the value of our node \(including the root node\)**
* **We must know where to split a tree branch**
* **We must know some stopping criteria of our tree growing process, or it may grow for infinite time**

**What do I mean by some metric? Well, we used information gain \(using the attribute entropy\) to select nodes in the previous chapter and that technique showed us some promising results. But that criteria to check the impurity of a subset is well defined for categorical data rather than numerical. So what should we use for our test case? Well, we will be using Gini index as our metric to quantify purity and choose the value of the node.**

