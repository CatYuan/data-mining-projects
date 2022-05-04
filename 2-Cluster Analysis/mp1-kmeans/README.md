# mp1-kmeans

The [k-means.ipynb](./k-means.ipynb) notebook implements the k-means algorithm and applies it to a real-life data set.

## Input 

The provided input file [places.txt](./places.txt) consists of the locations of 300 places in the US. Each location is a two-dimensional point that represents the longitude and latitude of the place. For example, "-112.1,33.5" means the longitude of the place is -112.1, and the latitude is 33.5.

## Output 

The K-means algorithm is implemented with Euclidean distance and uses it to cluster the 300 locations into three clusters, such that the locations in the same cluster are geographically close to each other. 

After reading the 300 locations in "places.txt" and applying the k-means algorithm (with k = 3), we generate an output file named "clusters.txt". The output file should contain exactly 300 lines, where each line represents the cluster label of each location. Every line should be in the format: location_id cluster_label.

An example snippet of the output "clusters.txt" file is provided below:

```
0 1

1 0

2 1

3 2

4 0
```

In the above, the five lines denote the cluster ids of the first five locations in the input file, which means:

The first location belongs to cluster "1"

The second location belongs to cluster "0"

The third location belongs to cluster "1"

The fourth location belongs to cluster "2"

The fifth location belongs to cluster "0"
