# Clustering Validation Measures

The [mp3-validation.ipynb](./mp3-validation.ipynb) notebook implements two clustering validation measures: Normalized Mutual Information (NMI) and Jaccard similarity.

## Input Format

The input of each test case includes n lines. Each line i includes two numbers separated by a space. The first number is the ground-truth cluster label of the i-th instance, and the second number is the predicted cluster label of the i-th instance. Sample 0 is an example input of five instances, where instance 1 belongs to cluster 2 and is predicted to belong to cluster 3, instance 2 belongs to cluster 0 and is predicted to belong to cluster 0...

## Output Format

The validation measures should be printed in the notebook.

The project evaluates the clustering predictions with regard to the ground-truth by NMI and Jaccard measures. For each test case, your output is a single line, which includes two float numbers (rounded to exactly 3 decimal places) separated by a space.