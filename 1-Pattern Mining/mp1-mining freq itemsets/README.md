# Frequent Itemset Mining Using Apriori

The [Apriori.ipynb](./Apriori.ipynb) notebook implements the Apriori algorithm and applies it to mine frequent itemsets from a dataset. 

## Input

The provided input file [categories.txt](./categories.txt) consists of the category lists of 77,185 places in the US. Each line corresponds to the category list of one place, where the list consists of a number of category instances (e.g., hotels, restaurants, etc.) that are separated by semicolons.

An example line is provided below:

```
Local Services;IT Services & Computer Repair
```

In the example above, the corresponding place has two category instances: "Local Services" and "IT Services & Computer Repair".

## Output

The algorithm mines category sets that are frequent in the input data and outputs the resulting frequent itemsets to the files `part1_patterns.txt` and `part2_patterns.txt`

### Part 1

`part1_patterns.txt` outputs all the length-1 frequent categories with their absolute supports into a text file named "patterns.txt". Every line corresponds to exactly one frequent category and should be in the following format:

```
support:category
```

For example, suppose a category (Fast Food) has an absolute support 3000, then the line corresponding to this frequent category set in "patterns.txt" should be:

```
3000:Fast Food
```

## Part 2

`part2_patterns.txt` writes all the frequent category sets along with their absolute supports into a text file named "patterns.txt". Every line corresponds to exactly one frequent category set and should be in the following format:

```
support:category_1;category_2;category_3;...
```

For example, suppose a category set (Fast Food; Restaurants) has an absolute support 2851, then the line corresponding to this frequent category set in "patterns.txt" should be:

```
2851:Fast Food;Restaurants
```
