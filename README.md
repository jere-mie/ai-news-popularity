# 3710-a2

Assignment 2 of COMP-3710

## Data Overview

The dataset under test consists of ~40,000 news articles, their number of shares, and a variety of statistics. Our objective is to analyze the data and make predictions about an article's popularity using these statistics and various algorithms. This has been made into a classification problem, where we determine if an article lands in the 0th percentile and above, 25th percentile and above, 75th percentile and above, or 75th percentile and above.

The data source can be found [here](https://archive.ics.uci.edu/ml/datasets/online+news+popularity).

## File Breakdown

### Preparation

The following notebooks are used for preparing the data:

- [data_prep.ipynb](code/data_prep.ipynb)
  - This notebook drops categorical features and other features that are unimportant to our algorithms. This should be the first notebook to be executed, and creates a classification problem out of this dataset. The expected input is [OnlineNewsPopularity.csv](code/data/OnlineNewsPopularity.csv). A cleaned csv ([OnlineNewsPopularityClean.csv](code/data/OnlineNewsPopularityClean.csv)) is the expected output.
- [tts.ipynb](tts.ipynb)
  - This notebook handles the train-test-split process, dividing the cleaned csv into four files ([train_features.csv](code/data/train_features.csv), [train_labels.csv](code/data/train_labels.csv), [test_features.csv](code/data/test_features.csv), [test_labels.csv](code/data/test_labels.csv)). The split ratio is 80/20, so 80% of the data goes to the training set, and 20% is left for testing.

### Algorithms

The following notebooks contain algorithms to be run on the train and test sets:

- [decision_tree.ipynb](code/decision_tree.ipynb)
  - This notebook runs a decision tree with the goal of classifying this data.
- [knn.ipynb](code/knn.ipynb)
  - This notebook runs the k-nearest-neighbours algorithm with the goal of classifying this data.
- [random_forest.ipynb](code/random_forest.ipynb)
  - This notebook runs the random forest algorithm with the goal of classifying this data.
- [gradient_boost.ipynb](code/gradient_boost.ipynb)
  - This notebook runs the gradient boost algorithm with the goal of classifying this data.
- [regression_comparison.ipynb](code/regression_comparison.ipynb)
  - Comparing algorithms in a regression context to see how they stack up.
