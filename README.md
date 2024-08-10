Decision Tree
<br/>

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
1- Select the best attribute using Attribute Selection Measures(ASM) to split the records. <br/>
2- Make that attribute a decision node and breaks the dataset into smaller subsets. <br/>
3- Starts tree building by repeating this process recursively for each child until one of the condition will match:
 * All the tuples belong to the same attribute value.
 * There are no more remaining attributes.
 * There are no more instances.
