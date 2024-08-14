**Decision Tree**
<br/>

**Introduction** <br/>
A decision tree is a flowchart-like tree structure where an internal node represents feature(or attribute), the branch represents a decision rule, and each leaf node represents the outcome. The topmost node in a decision tree is known as the root node. It learns to partition on the basis of the attribute value. It partitions the tree in recursively manner call recursive partitioning. This flowchart-like structure helps you in decision making. It's visualization like a flowchart diagram which easily mimics the human level thinking. That is why decision trees are easy to understand and interpret. <br/>
<br/>

Decision Tree is a white box type of ML algorithm. It shares internal decision-making logic, which is not available in the black box type of algorithms such as Neural Network. Its training time is faster compared to the neural network algorithm. The time complexity of decision trees is a function of the number of records and number of attributes in the given data. The decision tree is a distribution-free or non-parametric method, which does not depend upon probability distribution assumptions. Decision trees can handle high dimensional data with good accuracy. <br/>
<br/>

**Classification and Regression Trees (CART)** <br/>
Nowadays, Decision Tree algorithm is known by its modern name CART which stands for Classification and Regression Trees. Classification and Regression Trees or CART is a term introduced by Leo Breiman to refer to Decision Tree algorithms that can be used for classification and regression modeling problems. <br/>
The CART algorithm provides a foundation for other important algorithms like bagged decision trees, random forest and boosted decision trees. In this kernel, I will solve a classification problem. So, I will refer the algorithm also as Decision Tree Classification problem. <br/>
<br/>

**Decision Tree algorithm terminology** <br/>
n a Decision Tree algorithm, there is a tree like structure in which each internal node represents a test on an attribute, each branch represents the outcome of the test, and each leaf node represents a class label. The paths from the root node to leaf node represent classification rules. <br/>
We can see that there is some terminology involved in Decision Tree algorithm. The terms involved in Decision Tree algorithm are as follows:
* **Root Node** - It represents the entire population or sample. This further gets divided into two or more homogeneous sets.
* **Splitting** - It is a process of dividing a node into two or more sub-nodes.
* **Decision Node** - When a sub-node splits into further sub-nodes, then it is called a decision node.
* **Leaf/Terminal Node** - Nodes that do not split are called Leaf or Terminal nodes.
* **Pruning** - When we remove sub-nodes of a decision node, this process is called pruning. It is the opposite process of splitting.
* **Branch/Sub-Tree** - A sub-section of an entire tree is called a branch or sub-tree.
* **Parent and Child Node** - A node, which is divided into sub-nodes is called the parent node of sub-nodes where sub-nodes are the children of a parent node. <br/>
<br/>

**How does the Decision Tree Algorithm Work?** <br/>
The basic idea behind any decision tree algorithm is as follows:
1. Select the best attribute using Attribute Selection Measures(ASM) to split the records. <br/>
2. Make that attribute a decision node and breaks the dataset into smaller subsets. <br/>
3. Starts tree building by repeating this process recursively for each child until one of the condition will match:
 * All the tuples belong to the same attribute value.
 * There are no more remaining attributes.
 * There are no more instances. <br/>
<br/>

**Attribute Selection Measures** <br/>
Attribute selection measure is a heuristic for selecting the splitting criterion that partition data into the best possible manner. It is also known as splitting rules because it helps us to determine breakpoints for tuples on a given node. ASM provides a rank to each feature(or attribute) by explaining the given dataset. Best score attribute will be selected as a splitting attribute (Source). In the case of a continuous-valued attribute, split points for branches also need to define. Most popular selection measures are:
1. Information Gain
2. Gain Ratio
3. Gini Index. <br/>

* **Information Gain** <br/>
Shannon invented the concept of entropy, which measures the impurity of the input set. In physics and mathematics, entropy referred as the randomness or the impurity in the system. In information theory, it refers to the impurity in a group of examples. Information gain is the decrease in entropy. Information gain computes the difference between entropy before split and average entropy after split of the dataset based on given attribute values. ID3 (Iterative Dichotomiser) decision tree algorithm uses information gain. <br/>

* **Gain Ratio** <br/>
Information gain is biased for the attribute with many outcomes. It means it prefers the attribute with a large number of distinct values. For instance, consider an attribute with a unique identifier such as customer_ID has zero info(D) because of pure partition. This maximizes the information gain and creates useless partitioning. <br/>
C4.5, an improvement of ID3, uses an extension to information gain known as the gain ratio. Gain ratio handles the issue of bias by normalizing the information gain using Split Info. Java implementation of the C4.5 algorithm is known as J48, which is available in WEKA data mining tool. <br/>

* **Gini Index** <br/>
Another decision tree algorithm CART (Classification and Regression Tree) uses the Gini method to create split points. <br/>
The Gini Index considers a binary split for each attribute. You can compute a weighted sum of the impurity of each partition. In case of a discrete-valued attribute, the subset that gives the minimum gini index for that chosen is selected as a splitting attribute. In the case of continuous-valued attributes, the strategy is to select each pair of adjacent values as a possible split-point and point with smaller gini index chosen as the splitting point. <br/>
<br/>

**Overfitting in Decision Tree algorithm** <br/>
Overfitting is a practical problem while building a Decision-Tree model. The problem of overfitting is considered when the algorithm continues to go deeper and deeper to reduce the training-set error but results with an increased test-set error. So, accuracy of prediction for our model goes down. It generally happens when we build many branches due to outliers and irregularities in data. <br/>
Two approaches which can be used to avoid overfitting are as follows: <br/>
* Pre-Pruning
* Post-Pruning <br/>

1. **Pre-Pruning** <br/>
In pre-pruning, we stop the tree construction a bit early. We prefer not to split a node if its goodness measure is below a threshold value. But it is difficult to choose an appropriate stopping point. <br/>
2. **Post-Pruning** <br/>
In post-pruning, we go deeper and deeper in the tree to build a complete tree. If the tree shows the overfitting problem then pruning is done as a post-pruning step. We use the cross-validation data to check the effect of our pruning. Using cross-validation data, we test whether expanding a node will result in improve or not. If it shows an improvement, then we can continue by expanding that node. But if it shows a reduction in accuracy then it should not be expanded. So, the node should be converted to a leaf node. <br/>
<br/>

**Pros VS. Cons** <br/>
1. **Pros** 
* Decision trees are easy to interpret and visualize.
* It can easily capture Non-linear patterns.
* It requires fewer data preprocessing from the user, for example, there is no need to normalize columns.
* It can be used for feature engineering such as predicting missing values, suitable for variable selection.
* The decision tree has no assumptions about distribution because of the non-parametric nature of the algorithm.
2. **Cons**
* Sensitive to noisy data. It can overfit noisy data.
* The small variation(or variance) in data can result in the different decision tree. This can be reduced by bagging and boosting algorithms.
* Decision trees are biased with imbalance dataset, so it is recommended that balance out the dataset before creating the decision tree.
