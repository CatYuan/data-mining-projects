# Naive Bayes Classifier

The [mp2-naive-bayes.ipynb](./mp2-naive-bayes.ipynb) notebok implements a naive bayes classifer with Laplacian correction. 

## Data

For this project, we use the Zoo Animal Classification dataset from the UCI Machine Learning dataset. https://archive.ics.uci.edu/ml/datasets/Zoo

This dataset consists of 101 animals from a zoo. There are 16 variables with various traits to describe the animals. The 7 Class Types are: Mammal, Bird, Reptile, Fish, Amphibian, Bug and Invertebrate.

## Input Format

CSV file with the following fields: animal_name, hair, feathers, eggs, milk, airborne, aquatic, predator, toothed, backbone, breathes, venomous, fins, legs, tail, domestic, catsize, classtype. Do not use the animal_name and classtype for prediction.

The examples will be split into training and test set. For the training set, the classtype field will have an integer value from 1-7. For the test set, the classtype field will have the value -1.

- animal_name: Unique for each instance
- hair Boolean
- feathers Boolean
- eggs Boolean
- milk Boolean
- airborne Boolean
- aquatic Boolean
- predator Boolean
- toothed Boolean
- backbone Boolean
- breathes Boolean
- venomous Boolean
- fins Boolean
- legs Numeric (set of values: {0,2,4,5,6,8})
- tail Boolean
- domestic Boolean
- catsize Boolean
- class_type Numeric (integer values in range [1,7])

## Output Format

For each example in the test set, print the predicted classtype. Each example should be printed in a separate line.
