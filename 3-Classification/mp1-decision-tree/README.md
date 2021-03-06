# Decision Tree Classifier

The [mp1-decision-tree.ipynb](./mp1-decision-tree.ipynb) notebook impelments a decision tree classifier for multi-class classification with continuous feature/attribute values. For the decision tree you are to implement, please always use binary split and a threshold to split data. That is, each decision node has the form:

```
if attribute X <= threshold theta:
    then left node
else:
    right node
```

where the best $X$ and $\theta$ are for you to determine. Please use information gain to construct the decision tree.

## Model Specifications

For the decision tree, let `max_depth=2` be the only stopping criterion. In other words, you should grow the tree as long as `max_depth=2` is not violated and not all training instances in the current node have the same label.

## Tie Breaking

We ensure each attribute is named by a non-negative integer, and each class label is named by a positive integer. Since we are to use HackerRank for grading, we have to eliminate additional randomness and generate deterministic results. We, therefore, enforce the following rule in this assignment: In the event of ties, always choose the attribute or label with the smallest value. Namely,

- When training a DT, if splitting on either attribute $X_1$ or $X_2$ gives us the best information gain, choose the smaller of $X_1$ and $X_2$.
- In prediction, if both labels $L_1$ and $L_2$ have the same number of training instances at a DT leaf node , predict the smaller of $L_1$ and $L_2$.

## Input format

Input testcases can be found in [dt_deug_testcases](./dt_debug_testcases/)

Each input dataset contains training instances followed by test instances. Each line has the following space-separated format:

```
[label] [attribute 1]:[value 1] [attribute 2]:[value 2]...
```

The name of each attribute, e.g., [attribute 2], is a non-negative integer. The value of an attribute, e.g., [value 2], is a float number. A line stands for a test instance if [label] is -1 and a training instance otherwise. The label of a training instance can be any positive integer.

Please do not assume the attribute names to start from $0$ or to be consecutive integers, and please do not assume the class labels to start from $1$ or to be consecutive integers.

## Output Format

The output is the prediction on the test instances made by the decision tree. In each line of the output, prediction for each test instance is printed in the notebook and follows the ordering of the test instances in the input file.
