# mp2-AGNES

The [mp2-AGNES](./mp2-AGNES.ipynb) notebook implements an agglomerative hierarchical clustering algorithm with three different cluster similarity measures: single link, complete link, and average link.

It uses geographical data for this assignment. Each of the data points is a 2-D vector, with longitude and latitude as its dimensions.

Here is a brief review of the agglomerative clustering. During the clustering process, we iteratively aggregate the most similar two clusters, until there are $K$ clusters left. For initialization, each data point forms its own cluster.

The similarity of two clusters $C_i, C_j$ is determined by a distance measure. We use the following three measures in this assignment:

Single Link:

$$
D(C_i, C_j) = min\{d(v_p, v_1) | v_p \in C_i, v_q \in C_j\}
$$

Complete Link:

$$
D(C_i, C_j) = max\{d(v_p, v_q) | v_p \in C_i, v_q \in C_j\}
$$

Average Link: 

$$
D(C_i, C_j) = mean \{ d(v_p, v_q ) | v_p \in C_i, v_q \in C_j\}
$$

The smaller the distance is, the more similar the two clusters are.

$d(.,.)$ is a distance measure between two data points. We use Euclidean distance

## Input Format

The first line of the input will be three space separated integers $N K M$:

1. The number of data points (lines) following the first line $N$.
2. The number of output clusters $K$.
3. The cluster similarity measure $M$ to be used. $M=0$ for single link, $M=1$ for complete link, $M=2$ for average link.

Starting from the second line, each line will have exactly two floating point numbers, representing longitude and latitude of a location. Each line corresponds to a 2-D data point which will be fed into the clustering algorithm.

There will be $N+1$ lines in total.

Our objective is to use the similarity measure specified by $M$ to cluster $N$ data points into $K$ clusters.

## Output Format

Resulting clusters will be printed in the notebook.

There should be $N$ lines in the output, and one integer for each line, indicating the cluster label of the data point. The -th line in the output corresponds to the $i$-th data point in the input, i.e. the $(i+1)$-th line in the input.

The exact numbers used for cluster labels don't matter, but there should be exactly $K$ unique labels, and the data points in the same cluster should share the same label.
