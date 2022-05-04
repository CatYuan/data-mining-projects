# Sequential Patterns in Text

The [mp2.ipynb](./mp2.ipynb) notebook implements a contiguous sequential pattern mining algorithm and apply it on text data to mine potential phrase candidates.

## Input

The provided input file [reviews_sample.txt](./reviews_sample.txt) consists of 10,000 online reviews from Yelp users.  The reviews have been stemmed (to remove the postfix of each word so words with similar semantics can have the same form), and most of the punctuation has been removed.  Therefore, each line is basically a list of strings separated by spaces.  

An example line is provided below:

```
cold cheap beer good bar food good service looking great pittsburgh style fish sandwich place breading light fish plentiful good side home cut fry good grilled chicken salad steak soup day homemade lot special great place lunch bar snack beer
```

## Output

The algorithm mines contiguous sequential patterns that are frequent in the input data and outputs the resulting frequent itemsets to the files `part1_patterns.txt` and `part2_patterns.txt`

 A contiguous sequential pattern is a sequence of items that frequently appears as a consecutive subsequence in a database of many sequences.  For example, if the database is 

 ```
A,B,A,C
A,C,A,B,A,B
B,A,A,C,D
 ```

and the minimum support is 2, then patterns like "A,B,A" or "A,C" are both frequent contiguous sequential patterns, while the pattern "A,A" is not a frequent contiguous sequential pattern because in the first two sequences the two A's are not consecutive to each other.  Notice that it is still a frequent sequential pattern though.  

Also, notice that multiple appearances of a subsequence in a single sequence record only counts once.  For example, the pattern "A,B" appears 1 time in the first sequence and 2 times in the second, but its support should be calculated as 2, as there are only 2 records containing subsequence "A,B".  

The relative minimum support is set to 0.01.  In other words, all the frequent contiguous sequential patterns that have an absolute support no smaller than 100.

Within the `part1_patterns.txt` and `part2_patterns.txt` files every line corresponds to exactly one pattern you found and should be in the following format:

```
support:item_1;item_2;item_3
```

For example, suppose the phrase "parking lot" has an absolute support 133, then the line corresponding to this frequent contiguous sequential pattern in "patterns.txt" should be:

```
133:parking;lot
```
